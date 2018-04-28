---
title: Read User
position: 1.01
type: get
description: PATH /users/:id
content_markdown: |-
  Read user informations

left_code_blocks:
  - code_block: |-
      // ACCESS_TOKEN is Signed Authorization Token
      curl -H "Authorization: Bearer eyJhbGciOiJ...yrSxTHwzYjjueAxKJt4hmj0pY" -H "Content-Type: application/json" https://api.mixin.one/users/00c5a4ae-dcdc-48db-ab8e-a7eef69b442d
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
        created_at: "2018-01-07T07:24:05.88098376Z"
      }
    title: Response
    language: json
---
