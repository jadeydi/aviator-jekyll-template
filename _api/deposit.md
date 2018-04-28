---
title: Deposit
position: 7.0
type: get
description: PATH /assets/UUID
content_markdown: |-
  Get a user's deposit address (public_key).

left_code_blocks:
  - code_block: |-
      // ACCESS_TOKEN is Signed Authorization Token
      curl -H "Authorization: Bearer ACCESS_TOKEN" -H "Content-Type: application/json" https://api.mixin.one/assets/c6d0c728-2624-429b-8e0d-d9d19b6592fa

    title: Curl
    language: bash

right_code_blocks:
  - code_block: |-
      {
        type: "deposit",
        snapshot_id: "00c5a4ae-dcdc-48db-ab8e-a7eef69b442d",
        asset_id: "00c5a4ae-dcdc-48db-ab8e-a7eef69b442d",
        transaction_hash: "",
        ...
        sender: "0xAE9EA2D22E49B4c845Bbe57B57aB7172e548cE0B",
        amount: "10000",
        created_at: "2018-01-07T07:24:05.88098376Z"
      }
    title: Response
    language: json
---
