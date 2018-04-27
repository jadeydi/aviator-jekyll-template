---
title: Encrypted Pin
position: 9
parameters:
  - name:
    content:
content_markdown: |-
  If you want to create a tranfer or change your pin etc. You must have an Encrypted PIN. Following is the explaination of params which are used by encrypting pin.

  ``` golang
    pin: PinCode
    pinToken: PinToken
    sessionId: SessionId
    key: PrivateKey
    iterator: Can be used only once and Auto Increasement, initial Internal is 0, and will be reset after sign out.
  ```

  Notice: if you want to change you old pin, you must encrypt old pin first, then new pin in order. Following is an example of Encrypted PIN.
  {: .warning }

  ```golang
    // Encrypted PIN
    Djx9Z9E7mSUnZikrhRrflrpQEEfy0BrZ+l0aBwARHhgVHmbQkkDAsczAu2pU/hnr
  ```


left_code_blocks:
  - code_block:
    title:
    language:
right_code_blocks:
  - code_block: |-
      func EncryptPIN(ctx context.Context, pin, pinToken, sessionId string, key *rsa.PrivateKey, iterator uint64) string {
        token, _ := base64.StdEncoding.DecodeString(pinToken)
        keyBytes, err := rsa.DecryptOAEP(sha256.New(), rand.Reader, key, token, []byte(sessionId))
        if err != nil {
          return ""
        }
        pinByte := []byte(pin)
        timeBytes := make([]byte, 8)
        binary.LittleEndian.PutUint64(timeBytes, uint64(time.Now().Unix()))
        pinByte = append(pinByte, timeBytes...)
        iteratorBytes := make([]byte, 8)
        binary.LittleEndian.PutUint64(iteratorBytes, iterator)
        pinByte = append(pinByte, iteratorBytes...)
        padding := aes.BlockSize - len(pinByte)%aes.BlockSize
        padtext := bytes.Repeat([]byte{byte(padding)}, padding)
        pinByte = append(pinByte, padtext...)
        block, _ := aes.NewCipher(keyBytes)
        ciphertext := make([]byte, aes.BlockSize+len(pinByte))
        iv := ciphertext[:aes.BlockSize]
        io.ReadFull(rand.Reader, iv)
        mode := cipher.NewCBCEncrypter(block, iv)
        mode.CryptBlocks(ciphertext[aes.BlockSize:], pinByte)
        return base64.StdEncoding.EncodeToString(ciphertext)
      }
    title: Golang
    language: golang
---
