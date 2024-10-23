# action-release-checksums

Background information: https://github.com/orgs/community/discussions/23512#discussioncomment-6602360

```yaml
name: Release

permissions:
  contents: write

on:
  push:
    tags:
      - "v*.*.*"

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout
        uses: actions/checkout@v3
      - name: Release
        uses: softprops/action-gh-release@v1
      - name: Checksums
        uses: wangzuo/action-release-checksums@v1
```
