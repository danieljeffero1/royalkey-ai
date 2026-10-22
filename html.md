name: Generate API Key
on:
  workflow_dispatch:
jobs:
  generate:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - name: Generate API Key
        uses: your_github_handle/generate-api-key@v1.0
        with:
          KEY_LENGTH: 32
      - name: Output Key
        run: echo "Your API Key: ${{ steps.generate.outputs.key }}"
