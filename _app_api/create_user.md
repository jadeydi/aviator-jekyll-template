---
title: Create User
position: 100
type: post
description: PATH /users
parameters:
  - name: session_secret
    content: Base64 of RSA PUBLIC KEY
  - name: full_name
    content: Name of An New User
content_markdown: |-
  Create a new none-phone user.

left_code_blocks:
  - code_block: |-
      // ACCESS_TOKEN is Signed Authorization Token
      curl -X POST -H "Authorization: Bearer ACCESS_TOKEN" -H "Content-Type: application/json" https://api.mixin.one/users
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
