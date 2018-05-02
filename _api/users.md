---
title: Read Users
position: 121
type: get
description: PATH /users/fetch
parameters:
  - content: |
      ["UUID", "UUID", "UUID" ...]
content_markdown: |-
  Read users' informations

left_code_blocks:
  - code_block: |-
      // ACCESS_TOKEN is Signed Authorization Token
      curl -X POST -H "Authorization: Bearer eyJhbGciOiJ...yrSxTHwzYjjueAxKJt4hmj0pY" -H "Content-Type: application/json" https://api.mixin.one/users
    title: Curl
    language: bash

right_code_blocks:
  - code_block: |-
      [{
        type: "user",
        user_id: "00c5a4ae-dcdc-48db-ab8e-a7eef69b442d",
        identity_number: "3650126",
        full_name: "World Around",
        ...
        created_at: "2018-01-07T07:24:05.88098376Z"
      },
      ...
      ]
    title: Response
    language: json
---
