---
title: Read Contacts
position: 191
type: get
description: PATH /contacts
content_markdown: |-
  Get user's contacts

left_code_blocks:
  - code_block: |-
      // ACCESS_TOKEN is Signed Authorization Token
      curl -H "Authorization: Bearer ACCESS_TOKEN" -H "Content-Type: application/json" https://api.mixin.one/contacts
    title: Curl
    language: bash

right_code_blocks:
  - code_block: |-
      [{
        type: "contact",
        phone: "+8613800013800",
        full_name: "Jason"
      },
      ...
      ]
    title: Response
    language: json
---
