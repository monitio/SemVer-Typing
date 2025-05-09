# What is [SemVer Typing](./src/VERSIONING.md)?
**SemVer Typing** is a versioning scheme that extends [Semantic Versioning](https://semver.org) or [SemVer](https://semver.org) for short. It allows meaningful tags to be used at the end of each version to describe types and context.

## Declaration
The format itself is declared in the [VERSIONING.md](./src/VERSIONING.md) file. That file will contain all concepts and the types of the values themselves.

## Compatibility
[SemVer Typing](./src/VERSIONING.md) has been checked to work on these by default with the correct formatting:
- [Github Packages](https://docs.github.com/en/packages/learn-github-packages/introduction-to-github-packages) ([NPM-style packages only](https://docs.github.com/packages/working-with-a-github-packages-registry/working-with-the-npm-registry))
- [NPM](https://www.npmjs.com/) registry

> [!WARNING]
> [NPM](https://www.npmjs.com/) will not work if you leave the dash at the end. Always remove the dash if your not using the next parameter. Example: `1.0.0-release-` will not work. But `1.0.0-release` will work.
