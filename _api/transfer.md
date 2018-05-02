---
title: Transfer
position: 162
type: post
description: PATH /transfers
parameters:
  - name: asset_id
    content: |
      Asset id you want to transfer to type: UUID
  - name: counter_user_id
    content: |
      User id you want to transfer to type: UUID
  - name: amount
    content: |
      Asset amount  you want to transfer type: string
  - name: pin
    content: |
      Encrypted Pin type: string
  - name: trace_id
    content: |
      You can trace all your transfer use the trace_id type: UUID
  - name: memo
    content: |
      memo type: string
content_markdown: |-
  Transfer coins to an user.

left_code_blocks:
  - code_block: |-
      // ACCESS_TOKEN is Signed Authorization Token
      curl -X POST -H "Authorization: Bearer ACCESS_TOKEN" -H "Content-Type: application/json" https://api.mixin.one/transfers
      {
        "asset_id": "00c5a4ae-dcdc-48db-ab8e-a7eef69b442d",
        "counter_user_id": "00c5a4ae-dcdc-48db-ab8e-a7eef69b442d",
        "amount": "0.01", 
        "pin": "encrypted_pin",
        "trace_id": "00c5a4ae-dcdc-48db-ab8e-a7eef69b442d",
        "memo": "Gong Xi Fa Cai", 
      }
    title: Curl
    language: bash

right_code_blocks:
  - code_block: |-
      {
        type: "transfer",
        snapshot_id: "00c5a4ae-dcdc-48db-ab8e-a7eef69b442d",
        counter_user_id: "00c5a4ae-dcdc-48db-ab8e-a7eef69b442d",
        asset_id: "00c5a4ae-dcdc-48db-ab8e-a7eef69b442d",
        ...
        trace_id: "00c5a4ae-dcdc-48db-ab8e-a7eef69b442d",
        amount: "0.01",
        created_at: "2018-01-07T07:24:05.88098376Z"
      }
    title: Response
    language: json
---
