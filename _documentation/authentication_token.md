---
title: Authentication Token
position: 7
parameters:
  - name:
    content:
content_markdown: |-
  If you want to access API, you should prepare a signed authentication token, which contains all of your informations.

  ``` golang
    uid: ClientId
    sid: SessionId
    privateKey: PrivateKey
    method: HTTP Request method, e.g.: GET, POST
    url: URL path without hostname, e.g.: /transfers
    body: HTTP Request body, e.g.: {"pin": "encrypted pin token"}
  ```
  This will generate a JWT token, which will be used for all API as a Bearer Authorization HTTP header. An example of Signed Authentication Token:

  ```golang
    // Signed Authentication Token
    eyJhbGciOiJSUzUxMiIsInR5cCI6IkpXVCJ9.eyJhaWQiOiJjYmRlMzE3MC0yYTkxLTQxYTItYTU1MS0zNWI1OTQwNzFiMGUiLCJleHAiOjE1NTMwNTkwMjQsImlhdCI6MTUyMTUyMzAyNCwiaXNzIjoiZmI0NThlMDYtMDE3Ni00ZmRlLWFhZmYtNmUwZThiOWMyYzY3In0.CuFSwf31DXvRgupnaTCTmGx3U-7Qrplbt_wEqOh9jdRCmchbzrF0NHtNgDwakb8WQDGdR6LasQxDc07UvLHuw1yoN7J6ptA4AEqJs7eaT5_4M57Egcf2aCjWyY28rIRV2hKM02wkZHJdfZ7f-1yrSxTHwzYjjueAxKJt4hmj0pY
  ```

left_code_blocks:
  - code_block:
    title:
    language:
right_code_blocks:
  - code_block: |-
      func SignAuthenticationToken(uid, sid, privateKey, method, uri, body string) (string, error) {
        expire := time.Now().UTC().Add(time.Hour * 24 * 30 * 3)
        sum := sha256.Sum256([]byte(method + uri + body))
        token := jwt.NewWithClaims(jwt.SigningMethodRS512, jwt.MapClaims{
          "uid": uid,
          "sid": sid,
          "iat": time.Now().UTC().Unix(),
          "exp": expire.Unix(),
          "jti": uuid.NewV4().String(),
          "sig": hex.EncodeToString(sum[:]),
        })

        block, _ := pem.Decode([]byte(privateKey))
        key, err := x509.ParsePKCS1PrivateKey(block.Bytes)
        if err != nil {
          return "", err
        }
        return token.SignedString(key)
      }
    title: Golang
    language: golang
---
