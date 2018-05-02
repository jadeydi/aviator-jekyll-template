---
title: Update Preferences
position: 112
type: post
description: PATH /me/preferences
parameters:
  - name: |-
      receive_mess
      age_source
    content: |
      "EVERYBODY" or "CONTACTS"
content_markdown: |-
  Update user's preferences

left_code_blocks:
  - code_block: |-
      // ACCESS_TOKEN is Signed Authorization Token
      curl -H "Authorization: Bearer eyJhbGciOiJ...yrSxTHwzYjjueAxKJt4hmj0pY" -H "Content-Type: application/json" https://api.mixin.one/me/preferences -D '{"receive_message_source": "CONTACTS"}'
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
