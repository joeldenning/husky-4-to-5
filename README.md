# husky-4-to-6

> Easily migrate your husky 4 config to husky 5

While it should cover most basic migrations, it's **recommended** to have a look at husky 5 [documentation](https://typicode.github.io/husky).

If your `package.json` is not at the same level as `.git`, please update manually.

## Usage

### npm

```shell
npm install husky@5 --save-dev \
  && npx --no-install husky init \
  && npm exec -- github:typicode/husky-4-to-6 --remove-v4-config
```

### yarn

```shell
yarn add husky@5 --dev \
  && yarn husky init \
  && npm exec -- github:typicode/husky-4-to-6 --remove-v4-config
```

## What each command does

`husky init` sets up Git hooks and updates your `package.json` scripts (you may want to commit your changes to `package.json` before running `husky init`).

`husky-4-to-6` creates hooks based on your husky v4 config. If `--remove-v4-config` is passed, previous config will be deleted (recommended).

## Revert

If there's an error during the process, you can clean things up by running:

```sh
rm -rf .husky && git config --unset core.hooksPath
```
