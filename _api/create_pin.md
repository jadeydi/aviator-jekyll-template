---
title: Create Pin
position: 130
type: post
description: PATH /pin/update
parameters:
  - name: old_pin
    content: |
      "" for Create or "ENCRYPTED_PIN" for update
  - name: pin
    content: Encrypted New PIN
content_markdown: |-
  Create or Update user's Pin, use `pin_token` to get an Encrypted PIN.

left_code_blocks:
  - code_block: |-
      // ACCESS_TOKEN is Signed Authorization Token
      curl -X POST -H "Authorization: Bearer ACCESS_TOKEN" -H "Content-Type: application/json" https://api.mixin.one/pin/update -D '{"old_pin": "Encrypted PIN or Null", "pin": "Encrypted PIN"}'
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
        pin_token: "GSusC2myf/meJJnqorrcg2EWnHE...h9fTFJfR4=",
      }
    title: Response
    language: json
---
