# dioxus-gp-deploy-action
An action to deploy static sites made with Dioxus to Github Pages

# Workflow file

This Provided you configured your Dioxus app and the repo settings correctly, creating `.github/workflows/deploy.yml` workflow will publish to Github Pages when pushing on branch `main`.

```yml
name: github pages

permissions:
  contents: write

on:
  push:
    branches:
      - main

jobs:
  build-deploy:
    runs-on: ubuntu-latest
    steps:
      - name: "Dioxus Deploy"
        uses: joej/dioxus-deploy-gp-action@0.1.0
```