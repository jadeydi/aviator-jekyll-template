---
title: Delete Address
position: 172
type: post
description: PATH /addresses/:id/delete
content_markdown: |-
  Delete user's address

left_code_blocks:
  - code_block: |-
      // ACCESS_TOKEN is Signed Authorization Token
      curl -X POST -H "Authorization: Bearer ACCESS_TOKEN" -H "Content-Type: application/json" https://api.mixin.one/addresses/:id/delete
    title: Curl
    language: bash

right_code_blocks:
  - code_block: |-
      {}
    title: Response
    language: json
---
