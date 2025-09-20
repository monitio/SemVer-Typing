v2.0.0-rc.1.declaration | [6c8aa30](https://github.com/monitio/SemVer-Typing/commit/6c8aa30b9edfc56d2e4a6a45413ea18e3a1441a9)

Triggered by committer: [@james-beans](https://github.com/james-beans)

---

> [!WARNING]
> This file may not be always updated to the latest version as it is almost impossible without a bot to update this automatically every single time this is updated.

# What is [SemVer Typing](./VERSIONING.md)?
**SemVer Typing** is a set of conventions for using the pre-release tag feature of [Semantic Versioning (SemVer)](https://semver.org/). It provides a structured way to communicate a version's **development stage** and optional **build-specific metadata**.

This system ensures that versions are not only machine-readable by package managers but also easily understandable by developers at a glance.

---

# Format:
Use the following format for versions of your package/software using SemVer Typing. Note that a final, stable release will not have any pre-release tags (e.g., `1.0.0`).

```md
X.Y.Z-STAGE.N.METADATA
```

- `X.Y.Z`
  - The major, minor, and patch version numbers, following standard [Semantic Versioning rules](https://semver.org/#semantic-versioning-specification-semver). For projects before their first major release, it's common practice to start with `0.Y.Z`.
- `STAGE.N`
  - The **required** pre-release tag indicating the development stage.
  - `STAGE`: The maturity of the pre-release (e.g., `alpha`, `beta`).
  - `N`: A number that increments with each new build for that stage (e.g., `alpha.1`, `alpha.2`).
- `METADATA`
  - **Optional**, dot-separated identifiers describing the build. This is where you can specify the platform, build format, or status. You can chain multiple metadata tags.

---

## Tag Components
### Stage (**Required** for pre-releases, pick one)
This component describes the stability and completeness of a pre-release version.
  - `alpha` - **Early Development**: Features may be incomplete, unstable or buggy. Used for initial testing.
  - `beta` - **Feature Complete**: All major features are implemented, but the build is undergoing public testing to find and fix bugs.
  - `rc` - **Release Candidate**: The version is considered stable and ready for release. This is a final testing phase to catch critical last-minute issues.

### Metadata (**Optional**)
These are descriptive tags that provide context about a specific build artifact. You can use any of the identifiers below and chain them together. Custom options are supported.

- `build-format`:
  - `asm` - Assembly build
  - `wasm` - Web Assembly build
  - `js` - JavaScript build
  - `ts` - TypeScript build
  - `src` - Plain source-code
  - `bin`/`binary` - Binary executable build
  - `dts` - TypeScript declarations (`*.d.ts` files)
- `platform`:
  - `windows` - Any Windows OS
  - `linux` - Any Linux distro
  - `darwin` - Any macOS version
  - `multiplatform` - Builds for multiple platforms
- `status`:
  - `working` - Functional / passing tests
  - `broken` - Failing / non-functional
  - `error` - Build failed due to an error

---

## Examples & Workflow
Here’s how a version might progress from early development to a final release.

1. First alpha build for upcoming `0.1.0` release:
  - `0.1.0-alpha.1`
2. A new alpha build, creating a specific binary for Windows:
  - `0.1.0-alpha.2.windows.bin`
3. After alpha testing, the first beta is released:
  - `0.2.0-beta.1` (Minor version bumped for new features added during alpha)
4. The code is now considered stable and ready for the `1.0.0` release:
  - `1.0.0-rc.1`
5. The final, stable public release:
  - `1.0.0`

