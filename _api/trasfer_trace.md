---
title: Read Transfer
position: 164
type: get
description: PATH /transfers/trace/:id
content_markdown: |-
  Get transfer from trace_id

left_code_blocks:
  - code_block: |-
      // ACCESS_TOKEN is Signed Authorization Token
      curl -X POST -H "Authorization: Bearer ACCESS_TOKEN" -H "Content-Type: application/json" https://api.mixin.one/transfers/trace/00c5a4ae-dcdc-48db-ab8e-a7eef69b442d
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
