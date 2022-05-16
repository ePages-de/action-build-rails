# action-build-rails

GitHub Action for setting up a Rails environment installing Ruby and Yarn dependencies. It caches dependencies for reduced execution times.

## Inputs

| Name                 | Description                  | Default | Required |
|----------------------|------------------------------|---------|----------|
| `ruby_version`       | The ruby version to be used. | `3.1.2` | `true`   |
| `node_version`       | The node version to be used. | `18`    | `true`   |
| `bundle_github__com` | The GitHub access token.     | `nil`   | `false`  |

## Usage

```yml
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - name: Build Rails
        uses: ePages-de/action-build-rails@v1
        with:
          node_version: 18
          ruby_version: 3.1.2
          bundle_github__com: ${{ secrets.GITHUB_TOKEN }}
```
