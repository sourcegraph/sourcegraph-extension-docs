---
description: How to set up your development environment for creating and publishing Sourcegraph extensions.
---

# Set up your Development environment

Sourcegraph extensions are written in TypeScript and are distributed as bundled JavaScript files that run on the client. Let's install the software required.

## Node.js

Install [Node.js](https://nodejs.org) for building and packaging your extension.

## Sourcegraph CLI

To publish your extension, you need a [Sourcegraph.com account](https://sourcegraph.com/sign-up). Sourcegraph Enterprise supports a [private extension registry](https://docs.sourcegraph.com/extensions).

Then install the [Sourcegraph CLI (`src`)](https://github.com/sourcegraph/src-cli#installation), making sure you [configure `src` with an access token](https://github.com/sourcegraph/src-cli#authentication).

## Using your extension

Sourcegraph extensions allow you to extend code hosts like GitHub in the same way that editor extensions allow you to extend editors. This is possible because of the [Sourcegraph browser extension](https://docs.sourcegraph.com/integration/browser_extension).

Install [Sourcegraph for Chrome](https://chrome.google.com/webstore/detail/sourcegraph/dgjhfomjieaadpoljlnidmbgkdffpack) or [Sourcegraph for Firefox](https://addons.mozilla.org/en-US/firefox/addon/sourcegraph/).
