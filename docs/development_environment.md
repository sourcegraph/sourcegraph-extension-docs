---
description: How to set up your development environment for creating and publishing Sourcegraph extensions.
---

# Set up your Development environment

Sourcegraph extensions are written in TypeScript and are distributed as bundled JavaScript files that run on the client. Let's install the software required.

## Node.js and npm

Install [Node.js](https://nodejs.org) for building and packaging your extension.

## Sourcegraph CLI

Install the [Sourcegraph CLI (`src`)](https://github.com/sourcegraph/src-cli#installation) for communicating with a Sourcegraph instance.

To publish your extension, you will need a [Sourcegraph.com account](https://sourcegraph.com/sign-up). Only [Enterprise customers](https://about.sourcegraph.com/pricing) can publish to a private Sourcegraph instance.  

## Using your extension

Sourcegraph extensions require the [Sourcegraph for Chrome](https://chrome.google.com/webstore/detail/sourcegraph/dgjhfomjieaadpoljlnidmbgkdffpack) or [Sourcegraph for Firefox](https://addons.mozilla.org/en-US/firefox/addon/sourcegraph/).
