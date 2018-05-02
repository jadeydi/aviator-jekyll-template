---
title: Read Assets
position: 180
type: get
description: PATH /assets
content_markdown: |-
  Get user's assets

left_code_blocks:
  - code_block: |-
      // ACCESS_TOKEN is Signed Authorization Token
      curl -H "Authorization: Bearer ACCESS_TOKEN" -H "Content-Type: application/json" https://api.mixin.one/assets
    title: Curl
    language: bash

right_code_blocks:
  - code_block: |-
      [{
        type: "asset",
        asset_id: "00c5a4ae-dcdc-48db-ab8e-a7eef69b442d",
        symbol: "XIN",
        name: "Mixin",
      },
      ...]
    title: Response
    language: json
---
