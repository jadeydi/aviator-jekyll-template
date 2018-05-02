---
title: Create Address
position: 170
type: post
description: PATH /addresses
parameters:
  - name: asset_id
    content: UUID
  - name: public_key
    content: |
      String e.g.: 0x86fa049857e0209aa7d9e616f7eb3b3b78ecfdb0
  - name: label
    content: 
      String e.g.: "Jason's ETH Address"
  - name: pin
    content:
      String, Encrypted PIN
content_markdown: |-
  Create an addresses, which is the target address when you make a withdrawal.

left_code_blocks:
  - code_block: |-
      // ACCESS_TOKEN is Signed Authorization Token
      curl -X POST -H "Authorization: Bearer ACCESS_TOKEN" -H "Content-Type: application/json" https://api.mixin.one/addresses -D
      {
        "address_id": "00c5a4ae-dcdc-48db-ab8e-a7eef69b442d",
        "public_key": "Djx9Z9E7mSUnZikrhRrflrpQEEfy0BrZ+l0aBwARHhgVHmbQkkDAsczAu2pU/hnr",
        "label": "Jason's ETH Address",
        "trace_id": "00c5a4ae-dcdc-48db-ab8e-a7eef69b442d",
        "pin": "Djx9Z9E7mSUnZikrhRrflrpQEEfy0BrZ+l0aBwARHhgVHmbQkkDAsczAu2pU/hnr", 
      }
    title: Curl
    language: bash

right_code_blocks:
  - code_block: |-
      {
        type: "address",
        address_id: "00c5a4ae-dcdc-48db-ab8e-a7eef69b442d",
        asset_id: "00c5a4ae-dcdc-48db-ab8e-a7eef69b442d",
        public_key: "0xAE9EA2D22E49B4c845Bbe57B57aB7172e548cE0B",
        label: "Jason's ETH Address",
        updated_at: "2018-01-07T07:24:05.88098376Z"
      }
    title: Response
    language: json
---
