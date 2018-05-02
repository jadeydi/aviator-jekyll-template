---
title: Create Contacts
position: 194
type: post
description: PATH /contacts
parameters:
  - name: phone
    content: |
      String: "+8613800013800"
  - name: full_name
    content: |
      String: "Jason"
content_markdown: |-
  Create user's contacts

left_code_blocks:
  - code_block: |-
      // ACCESS_TOKEN is Signed Authorization Token
      curl -X POST -H "Authorization: Bearer ACCESS_TOKEN" -H "Content-Type: application/json" https://api.mixin.one/contacts -D '{"phone": "+8613800013800", "full_name": "Jason"}'
    title: Curl
    language: bash

right_code_blocks:
  - code_block: |-
      {}
    title: Response
    language: json
---
