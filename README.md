<p align="center">
  <a href="https://commonworld.one/">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/commonworld-one/commonworld/main/docs/assets/banner-commonworld-dark.svg">
      <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/commonworld-one/commonworld/main/docs/assets/banner-commonworld-light.svg">
      <img alt="Commonworld. A shared world for humans and agents." src="https://raw.githubusercontent.com/commonworld-one/commonworld/main/docs/assets/banner-commonworld-light.svg" width="880">
    </picture>
  </a>
</p>

<p align="center">
  <a href="https://commonworld.one/">Commonworld</a> ·
  <a href="https://commonworld.one/atlas/">Atlas</a> ·
  <a href="https://raise.commonworld.one/">RAISE</a> ·
  <a href="https://github.com/commonworld-one/commonworld-testnet">Commonworld Testnet</a> ·
  <a href="https://explorer-testnet.commonworld.one/">Testnet Explorer</a> ·
  <a href="https://rpc-testnet.commonworld.one/">Testnet RPC</a>
</p>

# Commonworld Besu

Commonworld's source fork of [Besu](https://github.com/besu-eth/besu), the Apache-2.0 Ethereum execution client. Network configuration and genesis are maintained separately in [Commonworld Testnet](https://github.com/commonworld-one/commonworld-testnet).

> Status: experimental Commonworld Testnet client source. The deployment facts below are copied from the network passport and are dated evidence, not a fresh server check.

## Current Commonworld Testnet client

| Field | Recorded value |
|---|---|
| Besu version | `26.11.0` |
| Upstream source | Tag [`26.11.0`](https://github.com/besu-eth/besu/tree/26.11.0), commit `0e595f9eaf4b760ee7069fcdf8d901685f1641eb` |
| Image | `hyperledger/besu@sha256:3d6ac0368d449c13c4ba075acac90d6b96afa5b3113295385d88c4d5122c8808` (`linux/amd64`) |
| Network profile | [Commonworld Testnet execution and storage record](https://github.com/commonworld-one/commonworld-testnet/blob/main/docs/NETWORK.md) |

The network passport records this upstream image and source version as verified on 21 November 2026. This repository does not build or deploy the image. Its `main` branch preserves the source baseline; the chain's genesis, runtime settings, and deployment record stay in the network repository.

Upstream Besu `26.11.1` was released on 18 November 2026. It is not recorded as deployed on Commonworld Testnet; review and testing are separate from updating this source fork. See the [upstream release notes](https://github.com/besu-eth/besu/releases/tag/26.11.1).

## Branches

- `main` is the Besu source baseline recorded for the current Commonworld Testnet deployment.
- `commonworld-testnet` is the working branch for candidate client changes. Promote a commit to `main` only after it has been reviewed, tested, and deployed.
- `upstream-main` preserves the upstream `main` tip captured when this fork was created. Refresh it deliberately when comparing upstream changes.

## Plugins

Besu plugins are separate Java extensions built against a specific Besu Plugin API version. Any Commonworld plugin will be versioned and checksummed separately; it will not be silently bundled into this client source. Start with the [Besu plugin guide](https://docs.besu-eth.org/plugins) and its [quickstart](https://docs.besu-eth.org/plugins/get-started/quickstart).

## Upstream and attribution

This is a GitHub fork of [`besu-eth/besu`](https://github.com/besu-eth/besu). Upstream history and the Apache-2.0 [license](LICENSE) are retained. The upstream documentation and project links below remain useful for Besu operation and development; upstream badges refer to upstream checks, not a Commonworld build.

---

## Upstream Besu documentation

The following project documentation is retained from upstream.

 [![CodeQL](https://github.com/besu-eth/besu/actions/workflows/codeql.yml/badge.svg)](https://github.com/besu-eth/besu/actions/workflows/codeql.yml)
 [![OpenSSF Best Practices](https://www.bestpractices.dev/projects/3174/badge)](https://www.bestpractices.dev/en/projects/3174)
 [![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://github.com/besu-eth/besu/blob/main/LICENSE)
 [![Discord](https://img.shields.io/discord/905194001349627914?logo=Hyperledger&style=plastic)](https://discord.com/invite/hyperledger)
 [![X Follow](https://img.shields.io/twitter/follow/Besu_eth)](https://x.com/Besu_eth)

[Download](https://github.com/besu-eth/besu/releases)

Besu is an Apache 2.0 licensed, Mainnet compatible, Ethereum client written in Java.

## Useful Links

* [Besu User Documentation]
* [Besu Issues]
* [Besu Wiki](https://github.com/besu-eth/besu/wiki)
* [How to Contribute to Besu][Contributing Guidelines]

## Community and support

If you have a question, need help, or want to engage with the Besu community, the following resources are available.

### Documentation

The [Besu documentation](https://docs.besu-eth.org/) answers many common questions. Some useful starting points:

* [System requirements](https://docs.besu-eth.org/public-networks/get-started/system-requirements)
* [Troubleshoot peering](https://docs.besu-eth.org/public-networks/how-to/troubleshoot/peering)
* [Troubleshoot performance](https://docs.besu-eth.org/public-networks/how-to/troubleshoot/performance)
* [Configure ports](https://docs.besu-eth.org/public-networks/how-to/connect/configure-ports)
* [Understand metrics](https://docs.besu-eth.org/public-networks/how-to/monitor/understand-metrics)
* [Configure the JVM](https://docs.besu-eth.org/public-networks/how-to/configure-java/pass-jvm-options)

### Chat

* Join the [Besu Discord](https://discord.com/invite/hyperledger): `#besu` to interact with the dev team and get support, and `#besu-contributors` if you are interested in contributing to the client.
* Besu is an execution client and must be paired with a consensus client. If you are also running the [Teku](https://github.com/Consensys/teku) consensus client, the [Teku Discord](https://discord.com/invite/teku) is useful too.

### GitHub

The [Besu GitHub repository](https://github.com/besu-eth/besu) tracks recent releases, patch notes, and known issues with up-to-date status on fixes and mitigations. If Discord can't resolve your problem, [search the existing issues](https://github.com/besu-eth/besu/issues) and, if needed, [open a new issue](https://github.com/besu-eth/besu/issues/new/choose) with relevant logs and context.

### Announcements

Version announcements are posted in the Discord announcements channel. Occasionally, the team also posts emergency alerts and support information on Discord and [X](https://x.com/Besu_eth).

## Issues 

Besu issues are tracked [in the github issues tab][Besu Issues].
See our [contributing guidelines][Contributing Guidelines] for more details on searching and creating issues.

If you have any questions, queries or comments, [Besu channel on Discord] is the place to find us.


## Besu Users

To install the Besu binary, follow [these instructions](https://docs.besu-eth.org/public-networks/get-started/install/binary-distribution).    

## Besu Developers

* [Contributing Guidelines]
* [Coding Conventions](https://github.com/besu-eth/besu/wiki/Developing-and-Conventions)
* [Command Line Interface (CLI) Style Guide](https://github.com/besu-eth/besu/wiki/Developing-and-Conventions-Besu-CLI-Style-Guide)
* [Besu User Documentation] for running and using Besu


### Development

Instructions for how to get started with developing on the Besu codebase. Please also read the
[contributing guidelines][Contributing Guidelines] for more details on how to submit a pull request (PR).  

* [Checking Out and Building](https://github.com/besu-eth/besu/wiki/Developing-and-Conventions-Building-from-Source)
* [Logging](https://github.com/besu-eth/besu/wiki/Developing-and-Conventions-Logging) or the [Documentation's Logging section](https://docs.besu-eth.org/public-networks/how-to/monitor/logging)

#### Dependency Verification

This project uses [Gradle dependency verification](https://docs.gradle.org/current/userguide/dependency_verification.html). Whenever you add or update a dependency or a Gradle plugin (including the `apiBaselineVersion` bump), regenerate `gradle/verification-metadata.xml` with:

```shell
./gradlew --write-verification-metadata sha256 --refresh-dependencies --rerun-tasks --no-parallel updateVerificationMetadata
```

and commit the updated file. The `updateVerificationMetadata` task resolves everything the build and the IDE need, so that their checksums get recorded:

* the binary and source JARs of every project's dependencies; the source JARs are required for IDE sync, since IntelliJ automatically downloads sources and fails the sync on missing checksums;
* the `.pom` of every dependency, resolved via `generateLicenseReport`; normal resolution prefers Gradle Module Metadata (`.module`) over the `.pom`, so without the license report those POM checksums are never recorded and `checkLicense` fails verification on a fresh clone;
* the binary and source JARs of every project's Gradle plugins, including the ones declared in subproject `plugins {}` blocks;
* the released Plugin API baseline and the tooling used by `:plugin-api:checkAPICompatibility`.

All four flags are required, and the task fails fast if any of them is missing. `--refresh-dependencies` and `--rerun-tasks` make the regeneration behave like a clean checkout: without them, cached dependency metadata and cached task results can produce a silently incomplete file that passes locally but fails on a fresh clone. `--no-parallel` is required because `generateLicenseReport` resolves cross-project configurations under an exclusive lock that only serial execution provides.

To check that the metadata is complete without modifying it (this is what CI runs), use:

```shell
./gradlew verifySourceArtifacts
```

### Profiling Besu

Besu supports performance profiling using [Async Profiler](https://github.com/async-profiler/async-profiler), a low-overhead sampling profiler.  
You can find setup and usage instructions in the [Profiling Guide](docs/PROFILING.md).

Profiling can help identify performance bottlenecks in block processing, transaction validation, and EVM execution.  
Please ensure the profiler is run as the same user that started the Besu process.

## Release Notes

[Release Notes](CHANGELOG.md)

## Reference Tests and JSON Tracing

Besu includes support for running Ethereum reference tests and generating detailed EVM execution traces.

To learn how to run the tests and enable opcode-level JSON tracing for debugging and correctness verification, see the [Reference Test Execution and Tracing Guide](REFERENCE_TESTS.md).

[Besu Issues]: https://github.com/besu-eth/besu/issues
[Besu User Documentation]: https://docs.besu-eth.org
[Besu channel on Discord]: https://discord.com/invite/hyperledger
[Contributing Guidelines]: CONTRIBUTING.md
