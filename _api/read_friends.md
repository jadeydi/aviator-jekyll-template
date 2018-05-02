---
title: Read Friends
position: 190
type: get
description: PATH /friends
content_markdown: |-
  Get user's friends

left_code_blocks:
  - code_block: |-
      // ACCESS_TOKEN is Signed Authorization Token
      curl -H "Authorization: Bearer ACCESS_TOKEN" -H "Content-Type: application/json" https://api.mixin.one/friends
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
