---
description: Creating an extension using the Sourcegraph extension creator.
---

# Creating an extension

Creating an extension is easy thanks to the [Sourcegraph extension creator](https://github.com/sourcegraph/create-extension). It will ask you a series of questions about your extension, then create the file structure so you can start developing your extension immediately.

Once you have [set up your development environment](development_environment.md), you're ready to go: 

```shell
mkdir my-extension
cd my-extension
npm init @sourcegraph/extension
```

## Created files

Your extension folder now contains the following.

```shell
├── README.md
├── node_modules
├── package-lock.json
├── package.json
├── src
│   └── {extension-name}.ts
├── tsconfig.json
└── tslint.json
```

The `README.md` explains how to set up and use your extension.

The entry point for your extension code is `src/{extension-name}.ts`.

The `package.json` defines important commands used during development and publishing. To run them, prefix the command key with `npm run`. For example, to lint and type check your code:

```shell
npm run lint
npm run typecheck
```

Other files such as `tsconfig.json` and `tslint.json` configure how your code is linted and compiled. They are fine as is but feel free to change them.

## Issues or improvements

Noticed a bug? Any ideas for improving the extension creation process? [File an issue](https://github.com/sourcegraph/create-extension/issues).
