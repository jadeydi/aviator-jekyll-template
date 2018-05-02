---
title: Register User
position: 11
type: post
description: PATH /verifications/:id
parameters:
  - name: code
    content: "1234"
  - name: session_secret
    content: base64 of isa public_key
  - name: platform
    content: |
      "iOS" or "Andoird"
  - name: platform_version
    content: "11.0"
  - name: app_version
    content: "0.2.11"
  - name: notification_token
    content: "APNS or FCM token"
  - name: registration_id
    content: "Clients should only do this once, at install time."
content_markdown: |-
  User sign in or sign up

left_code_blocks:
  - code_block: |-
      curl -X POST -H "Content-Type: application/json" https://api.mixin.one//verifications/00c5a4ae-dcdc-48db-ab8e-a7eef69b442d -D '{"code": "1234", "session_secret": "GSusC2myf/meJJnqorrcg2EWnHE...h9fTFJfR4=", platform: "iOS", "platform_version": "11.0", "app_version": "0.2.11", "notification_token": "GSusC2myf/meJJnqorrcg2EWnHE...h9fTFJfR4="}'
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
