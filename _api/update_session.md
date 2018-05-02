---
title: Update Device Info
position: 140
type: post
description: PATH /session
parameters:
  - name: platform
    content: iOS
  - name: platform_version
    content: 11.0
  - name: app_version
    content: 0.2.4
  - name: notification_token
    content: "APNS OR FCM token"
content_markdown: |-
  User Login

left_code_blocks:
  - code_block: |-
      // ACCESS_TOKEN is Signed Authorization Token
      curl -X POST -H "Authorization: Bearer ACCESS_TOKEN" -H "Content-Type: application/json" https://api.mixin.one/session -D '{"platform": "iOS", "platform_version": "11.0", "app_version": "0.2.4", "notification_token": "token"}'
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
