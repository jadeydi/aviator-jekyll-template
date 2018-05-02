---
title: Send SMS
position: 10
type: post
description: PATH /verifications
parameters:
  - name: phone
    content: |
      "+8613800013800"
  - name: purpose
    content: |
      "SESSION"  or "PHONE"
content_markdown: |-
  Send Message to user's phone

left_code_blocks:
  - code_block: |-
      curl -X POST -H "Content-Type: application/json" https://api.mixin.one/verifications -D '{"phone": "+8613800013800", "purpose": "SESSION"}'
    title: Curl
    language: bash

right_code_blocks:
  - code_block: |-
      {
        type: "phone_verification",
        id: "00c5a4ae-dcdc-48db-ab8e-a7eef69b442d",
      }
    title: Response
    language: json
---
