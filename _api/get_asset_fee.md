---
title: Read Asset Fee
position: 183
type: get
description: PATH /assets/:id/fee
content_markdown: |-
  Get user's asset fee

left_code_blocks:
  - code_block: |-
      // ACCESS_TOKEN is Signed Authorization Token
      curl -H "Authorization: Bearer ACCESS_TOKEN" -H "Content-Type: application/json" https://api.mixin.one/assets/00c5a4ae-dcdc-48db-ab8e-a7eef69b442d/fee
    title: Curl
    language: bash

right_code_blocks:
  - code_block: |-
      {
        type: "fee",
        asset_id: "00c5a4ae-dcdc-48db-ab8e-a7eef69b442d",
        amount: "0.01",
      }
    title: Response
    language: json
---
