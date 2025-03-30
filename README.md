# `opencloudtool` GitHub Action

This GitHub Action allows you to run [opencloudtool](https://github.com/opencloudtool/opencloudtool) commands directly in your GitHub Actions workflows.

## Usage

### Basic Example

```yaml
name: opencloudtool Workflow

on:
  push:
    branches: [main]

jobs:
  oct-job:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout code
        uses: actions/checkout@v4

      - name: Run opencloudtool Command
        uses: opencloudtool/oct-action@v1
        with:
          command: "deploy"
          working-directory: "."
```

### Input Parameters

| Parameter           | Description                                  | Required | Default |
| ------------------- | -------------------------------------------- | -------- | ------- |
| `command`           | The opencloudtool command to run             | Yes      | N/A     |
| `working-directory` | Directory where the command will be executed | Yes      | `.`     |

## License

This project is licensed under the MIT License - see the LICENSE file for details.
