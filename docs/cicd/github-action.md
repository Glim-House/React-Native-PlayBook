---
sidebar_position: 1
---

# Github Action

Github actions are the service provided by the github to automate process. In react native we can use the github actions to automate release and run automation tests.

## Setup

for creating a new action, just create a file named `{action_name}.yml` in the `.github/workflows`. Then just write some actions on the file.

```yml
name: Deploy to GitHub Pages

on:
  push:
    branches:
      - main

jobs:
  deploy:
    name: Deploy to GitHub Pages
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - uses: actions/setup-node@v3
        with:
          node-version: 18
          cache: yarn

      - name: Install dependencies
        run: yarn install --frozen-lockfile
      - name: Build website
        run: yarn build

      # Popular action to deploy to GitHub Pages:
      # Docs: https://github.com/peaceiris/actions-gh-pages#%EF%B8%8F-docusaurus
      - name: Deploy to GitHub Pages
        uses: peaceiris/actions-gh-pages@v3
        with:
          github_token: ${{ secrets.GITHUB_TOKEN }}
          # Build output to publish to the `gh-pages` branch:
          publish_dir: ./build
          # The following lines assign commit authorship to the official
          # GH-Actions bot for deploys to `gh-pages` branch:
          # https://github.com/actions/checkout/issues/13#issuecomment-724415212
          # The GH actions bot is used by default if you didn't specify the two fields.
          # You can swap them out with your own user credentials.
          user_name: github-actions[bot]
          user_email: 41898282+github-actions[bot]@users.noreply.github.com
```

This is a small action file to deploy to `gh-pages`. Like this we can also deploy the react native app to the stores.

## Some explanations

```yml
on:
  push:
    branches:
      - main
```

The following actions will execiute on when a push happenes to the main branch

```yml
with:
  github_token: ${{ secrets.GITHUB_TOKEN }}
```

Its the action secrets should be stored in the github to perform actions. you have to store the token in `https://github.com/{account_name}/{repo_name}/settings/secrets/actions`

## References

- [https://docs.github.com/en/actions](https://docs.github.com/en/actions)
