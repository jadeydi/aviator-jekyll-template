---
title: Withdrawal
position: 7.0
type: post
description: PATH /withdrawals
parameters:
  - name: address_id
    content: UUID
  - name: amount
    content: "100000"
  - name: pin
    content: "Encrypted Pin"
  - name: trace_id
    content: UUID
  - name: memo
    content: memo
content_markdown: |-
  Withdrawal to a blockchain address

left_code_blocks:
  - code_block: |-
      // ACCESS_TOKEN is Signed Authorization Token
      curl -X POST -H "Authorization: Bearer ACCESS_TOKEN" -H "Content-Type: application/json" https://api.mixin.one/withdrawals -D
      {
        "address_id": "00c5a4ae-dcdc-48db-ab8e-a7eef69b442d",
        "amount": "10000",
        "pin": "Djx9Z9E7mSUnZikrhRrflrpQEEfy0BrZ+l0aBwARHhgVHmbQkkDAsczAu2pU/hnr",
        "trace_id": "00c5a4ae-dcdc-48db-ab8e-a7eef69b442d",
        "memo": "You got it", 
      }
    title: Curl
    language: bash

right_code_blocks:
  - code_block: |-
      {
        type: "withdrawal",
        snapshot_id: "00c5a4ae-dcdc-48db-ab8e-a7eef69b442d",
        receiver: "0xAE9EA2D22E49B4c845Bbe57B57aB7172e548cE0B",
        amount: "10000",
        ...
        trace_id: "00c5a4ae-dcdc-48db-ab8e-a7eef69b442d",
        memo: "You got it",
        created_at: "2018-01-07T07:24:05.88098376Z"
      }
    title: Response
    language: json
---
