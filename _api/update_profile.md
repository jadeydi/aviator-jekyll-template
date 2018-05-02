---
title: Update Profile
position: 111
type: get
description: PATH /me
parameters:
  - name: full_name
    content: |
      "Mixin Develeper"
  - name: avatar_base64
    content: |
      Base64 of image
content_markdown: |-
  Update user informations

left_code_blocks:
  - code_block: |-
      // ACCESS_TOKEN is Signed Authorization Token
      curl -X POST -H "Authorization: Bearer eyJhbGciOiJ...yrSxTHwzYjjueAxKJt4hmj0pY" -H "Content-Type: application/json" https://api.mixin.one/me -D '{"name": "World Around", "avatar_base64": "base64 of image"}'
    title: Curl
    language: bash

right_code_blocks:
  - code_block: |-
      {
        type: "user",
        user_id: "00c5a4ae-dcdc-48db-ab8e-a7eef69b442d",
        identity_number: "3650126",
        full_name: "World Around",
        ...
        session_id: "00c5a4ae-dcdc-48db-ab8e-a7eef69b442d",
        code_id: "00c5a4ae-dcdc-48db-ab8e-a7eef69b442d",
        pin_token: "GSusC2myf/meJJnqorrcg2EWnHE...h9fTFJfR4=",
      }
    title: Response
    language: json
---
