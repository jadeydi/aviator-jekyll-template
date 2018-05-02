---
title: Change Phone Number
position: 12
type: post
description: PATH /verifications/:id
parameters:
  - name: code
    content: "1234"
  - name: pin
    content: Encrypted user pin
content_markdown: |-
  Update user pin

left_code_blocks:
  - code_block: |-
      // ACCESS_TOKEN is Signed Authorization Token
      curl -H "Authorization: Bearer eyJhbGciOiJ...yrSxTHwzYjjueAxKJt4hmj0pY" -H "Content-Type: application/json" https://api.mixin.one/verifications/00c5a4ae-dcdc-48db-ab8e-a7eef69b442d -D '{"code": "1234", "pin": "GSusC2myf/meJJnqorrcg2EWnHE...h9fTFJfR4="}'
    title: Curl
    language: bash

right_code_blocks:
  - code_block: |-
      {}
    title: Response
    language: json
---
