# Sourcegraph extension authoring documentation

Sourcegraph extensions allow you to extend code hosts like GitHub in the same way that editor extensions allow you to extend editors. Once you write an extension, it runs anywhere you see code (e.g. GitHub).

For example, the [Codecov extension](https://github.com/sourcegraph/sourcegraph-codecov) shows coverage information from Codecov on GitHub and Sourcegraph.

![Codecov Sourcegraph extension which shows coverage information from Codecov on GitHub and Sourcegraph.com](https://images.ctfassets.net/le3mxztn6yoo/3WZ3oy1haU4YeYWywuS0Qe/a25491260dd59fb4028e6bcea6c4c88a/CodeCovExtension.gif)

When you publish your extension to the [Sourcegraph extension registry](https://sourcegraph.com/extensions), anyone can install and instantly start using it. (Sourcegraph Enterprise supports a [private extension registry](https://docs.sourcegraph.com/extensions)).

Sourcegraph extensions are considered alpha and these docs are a work in progress.

 - [Set up your development environment](docs/development_environment.md)
 - [Creating an extension](docs/creating_an_extension.md)
 - [Sample extensions](https://github.com/sourcegraph/sourcegraph-extension-samples)
 - [Sourcegraph extension API](https://github.com/sourcegraph/sourcegraph-extension-api), the [Sourcegraph.com extension registry](https://sourcegraph.com/extensions)
 - [Extensions cookbook](docs/cookbook.md)
 - [Sourcegraph extension early adopters](docs/early_adopters.md)
 - [Extension publishing](docs/extension_publishing.md)

## Help and feedback

Noticed an error or have a suggestion for improving these docs? [Submit an issue](https://github.com/sourcegraph/sourcegraph-extension-docs/issues) or a pull request.
