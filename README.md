# rust-vps-deploy

GitHub Action for deploying Rust to a VPS

## Example Usage

```yml
on:
  push:
    branches:
      - main
  workflow_dispatch:

jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: will-lynas/rust-vps-deploy@v0.11.0
        with:
          host: ${{ secrets.VPS_HOST }}
          username: ${{ secrets.VPS_USER }}
          ssh-private-key: ${{ secrets.SSH_PRIVATE_KEY }}
```
