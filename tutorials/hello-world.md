# Building a "Hello, world!" Sourcegraph extension

[Sourcegraph extensions](https://github.com/sourcegraph/sourcegraph-extension-api) let you add  features and show new kinds of information alongside your code on Sourcegraph.com, GitHub, and other code hosts.

This guide shows you how to create a simple Sourcegraph extension that:

- Shows a friendly "Hello, world! 🎉🎉🎉" message when you hover over code.
- Works on all code on GitHub (requires the Sourcegraph extension for [Chrome](https://chrome.google.com/webstore/detail/sourcegraph/dgjhfomjieaadpoljlnidmbgkdffpack) or [Firefox](https://addons.mozilla.org/en-US/firefox/addon/sourcegraph/)).
- Works on all code on Sourcegraph.com.
- Runs entirely client-side in the browser (your code remains local and is not sent to any server).

## Prerequisites

Follow the instructions for [setting up your development environment](../docs/development_environment.md).

## Create the extension

We'll use the [Sourcegraph extension generator](https://github.com/sourcegraph/create-extension) to get started.

```shell
mkdir my-extension
cd my-extension
npm init @sourcegraph/extension
```

The code for the extension is in the `src` directory. That's all it takes to create a simple extension! 

Now let's publish it so you (and other people) can use it.

## Publishing the extension

Publishing an extension requires an [account on Sourcegraph.com](https://sourcegraph.com/sign-up) and configuring [`src`](https://github.com/sourcegraph/src-cli) with an [access token](https://github.com/sourcegraph/src-cli#authentication) which is covered in [setting up your development environment](../docs/development_environment.md).

Now publish the extension by running:

```shell
src ext publish
```

Now that the extension is published, let's use it.

## Use the extension

After publishing the extension, visit the URL output in the terminal. This is the extension's listing page on the [Sourcegraph.com extension registry](https://sourcegraph.com/extensions). Anyone can visit this page to see more information about the extension and to start using it.

Toggle the slider to enable the extension for your account to start using it.

Now you can:

- Visit any code file on Sourcegraph (such as [this file](https://sourcegraph.com/github.com/ReactiveX/rxjs/-/blob/src/internal/observable/SubscribeOnObservable.ts)) and hover over code to see the "Hello, world! 🎉🎉🎉" message.
- Visit any code file on GitHub (such as [this file](https://github.com/ReactiveX/rxjs/blob/HEAD/src/internal/observable/SubscribeOnObservable.ts)) and hover over code to see it say the same.

## Next steps

You've created your first Sourcegraph extension!

Now check out the [Sourcegraph extensions documentation](../README.md) to see how to build more powerful extensions.
