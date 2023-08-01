# action-release-checksums

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
