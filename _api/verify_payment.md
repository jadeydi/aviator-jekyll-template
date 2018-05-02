---
title: Verify Payment
position: 163
type: post
description: PATH /payments
parameters:
  - name: asset_id
    content: |
      UUID, Asset id you want to transfer to. 
  - name: counter_user_id
    content: |
      UUID, User id you want to transfer to.
  - name: amount
    content: |
      String, asset amount  you want to transfer
  - name: trace_id
    content: |
      UUID, you can trace all your transfer use the trace_id
content_markdown: |-
  Verify a transfer is valid or not.

left_code_blocks:
  - code_block: |-
      // ACCESS_TOKEN is Signed Authorization Token
      curl -X POST -H "Authorization: Bearer ACCESS_TOKEN" -H "Content-Type: application/json" https://api.mixin.one/payments
      {
        "asset_id": "00c5a4ae-dcdc-48db-ab8e-a7eef69b442d",
        "counter_user_id": "00c5a4ae-dcdc-48db-ab8e-a7eef69b442d",
        "amount": "0.01", 
        "trace_id": "00c5a4ae-dcdc-48db-ab8e-a7eef69b442d",
      }
    title: Curl
    language: bash

right_code_blocks:
  - code_block: |-
      {
        recipient: {
          type: "user",
          user_id: "00c5a4ae-dcdc-48db-ab8e-a7eef69b442d",
        },
        asset: {
          type: "asset",
          asset_id: "00c5a4ae-dcdc-48db-ab8e-a7eef69b442d"
        },
        amount: "0.01",
        status: "paid",
      }
    title: Response
    language: json
---
