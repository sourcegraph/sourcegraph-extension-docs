# Extension publishing

Publishing is a two step process:

- Packaging: Transpiling and bundling your extension into a single file (name does not matter)
- Publishing: Pushing your JavaScript file to the Sourcegraph extension registry

## Packaging

We recommend using [Parcel](https://parceljs.org/) for a nice, zero configuration transpiler and bundler and [this is what our extension generator uses](creating_an_extension.md).

Parcel takes your code and creates a single JavaScript file ("parcel") that is uploaded to the extension registry. Nothing is stopping you using webpack or Babel but Parcel works for us.

The name of the file uploaded doesn't matter. We recommend it match your extension name so you can easily identify it when using your browser developer tools.

## Pre-publishing

### Check you have the latest sourcegraph package

Sourcegraph extensions depends on the [Sourcegraph extension API](https://www.npmjs.com/package/sourcegraph) package and we recommend checking for a newer version on a regular basis.

```shell
npm outdated --save-dev
```

### Type check and lint

The extension generator includes `npm` commands for type checking and linting your code. You don't have to, but we recommend running them before publishing.

```shell
npm run typecheck
npm run tslint
```

## Publishing

This guide presumes you will be publishing to [Sourcegraph.com](https://sourcegraph.com/).

Ensure you [installed and configured the `src` CLI](development_environment.md#sourcegraph-cli).

Now you can publish with a single command.

```shell
src ext publish
```

This is the command you'll run when releasing a new version.

However doing this as part of your development workflow would be slow and tedious. See the [workflow for extension reloading without publishing](#Extension-reloading-without-re-publishing).

## Current publishing limitations

Currently, publishing is limited to [Sourcegraph.com](https://sourcegraph.com/extensions) and a Sourcegraph Enterprise [private extension registry](https://docs.sourcegraph.com/extensions).

We know [you need a way to develop locally before publishing](https://github.com/sourcegraph/sourcegraph/issues/489), as well as having a way to [mark an extension as a WIP/preview](https://github.com/sourcegraph/sourcegraph/issues/480).

We recommend you subsribe to these issues so you can track our progress.

## Extension reloading without re-publishing

We can use parcel to serve and re-package the extension on file change and set the `url` of the extension to our local development environment.

Presuming you used the [extension generator](creating_an_extension.md), you can run:

```shell
npm run serve
```

In a new terminal window, now re-publish your extension, overriding the `url` to point to your bundled JavaScript file.

```shell
src ext publish --url=http://localhost:1234/my-extension-name.js
```
