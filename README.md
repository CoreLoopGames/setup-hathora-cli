# Setup Hathora CLI Action

The Setup Hathora CLI Action is a [GitHub action](https://github.com/features/actions) designed to set up the [Hathora](https://hathora.dev/) CLI Tools.

## Available Inputs

Here are the available input parameters for the Setup Yarn Berry Action:

| Name    | Type    | Description                                |
|---------| ------- |--------------------------------------------|
| `appId` | String  | The Hathora App-ID to use for CLI commands |
| `token` | Boolean | The Hathora token to use for CLI commands  |

## Example Usage

Here's a basic example demonstrating how to utilize the Setup Hathora CLI Action in the GitHub workflow:

```yaml
name: Node.js CI
on:
  push:
jobs:
  build:
    name: Build Project
    runs-on: ubuntu-24.04
    steps:
      - name: Checkout
        uses: actions/checkout@v4.2.2

      - name: Setup Hathora CLI
        uses: CoreLoopGames/setup-hathora-cli@main
        with:
          appId: ${{ secrets.HATHORA_APP_ID }}
          token: ${{ secrets.HATHORA }}

      # Add more steps as needed for your workflow
```

## License

This project is licensed under the terms of the [MIT License](./LICENSE).

Copyright © 2025 [CoreLoopGames](https://github.com/CoreLoopGames/)