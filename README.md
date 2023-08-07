<div align="right">

[![GitHub License](https://img.shields.io/github/license/block-foundation/blocktxt?style=flat-square&logo=readthedocs&logoColor=FFFFFF&label=&labelColor=%23041B26&color=%23041B26&link=LICENSE)](https://github.com/block-foundation/docker-polkadot-node/blob/main/LICENSE)
[![devContainer](https://img.shields.io/badge/Container-Remote?style=flat-square&logo=visualstudiocode&logoColor=%23FFFFFF&label=Remote&labelColor=%23041B26&color=%23041B26)](https://vscode.dev/redirect?url=vscode://ms-vscode-remote.remote-containers/cloneInVolume?url=https://github.com/block-foundation/docker-polkadot-node)

</div>

---

<div>
    <img align="right" src="https://raw.githubusercontent.com/block-foundation/brand/master/src/logo/logo_gray.png" width="96" alt="Block Foundation Logo">
    <h1 align="left">Polkadot Node</h1>
    <h3 align="left">Block Foundation Docker Containers</h3>
</div>

---

<img align="right" width="75%" src="https://raw.githubusercontent.com/block-foundation/brand/master/src/image/repository_cover/block_foundation-containers.jpg"  alt="Block Foundation Containers">

### Contents

- [Introduction](#introduction)
- [Colophon](#colophon)

<br clear="both"/>

---

<div align="right">

[![Report a Bug](https://img.shields.io/badge/Report%20a%20Bug-GitHub?style=flat-square&&logoColor=%23FFFFFF&color=%23E1E4E5)](https://github.com/block-foundation/docker-polkadot-node/issues/new?assignees=&labels=Needs%3A+Triage+%3Amag%3A%2Ctype%3Abug-suspected&projects=&template=bug_report.yml)
[![Request a Feature](https://img.shields.io/badge/Request%20a%20Feature-GitHub?style=flat-square&&logoColor=%23FFFFFF&color=%23E1E4E5)](https://github.com/block-foundation/docker-polkadot-node/issues/new?assignees=&labels=Needs%3A+Triage+%3Amag%3A%2Ctype%3Abug-suspected&projects=&template=feature_request.yml)
[![Ask a Question](https://img.shields.io/badge/Ask%20a%20Question-GitHub?style=flat-square&&logoColor=%23FFFFFF&color=%23E1E4E5)](https://github.com/block-foundation/docker-polkadot-node/issues/new?assignees=&labels=Needs%3A+Triage+%3Amag%3A%2Ctype%3Abug-suspected&projects=&template=question.yml)
[![Make a Suggestion](https://img.shields.io/badge/Make%20a%20Suggestion-GitHub?style=flat-square&&logoColor=%23FFFFFF&color=%23E1E4E5)](https://github.com/block-foundation/docker-polkadot-node/issues/new?assignees=&labels=Needs%3A+Triage+%3Amag%3A%2Ctype%3Abug-suspected&projects=&template=suggestion.yml)
[![Start a Discussion](https://img.shields.io/badge/Start%20a%20Discussion-GitHub?style=flat-square&&logoColor=%23FFFFFF&color=%23E1E4E5)](https://github.com/block-foundation/docker-polkadot-node/issues/new?assignees=&labels=Needs%3A+Triage+%3Amag%3A%2Ctype%3Abug-suspected&projects=&template=discussion.yml)

</div>

## Introduction

Welcome to the Block Foundation's Polkadot Node Docker Image Repository! This repository embodies our dedication to open-source development and our commitment to making blockchain technology accessible and straightforward for everyone.

Polkadot, for those unfamiliar, is a sharded, scalable, interoperable, and secure network protocol for the next web generation. It provides an environment for connecting multiple chains together in a single network, enabling them to process transactions in parallel and exchange data efficiently. Docker, on the other hand, is a leading platform used for automating the deployment, scaling, and management of applications within containers.

This repository houses a Docker image that has been specifically designed for the effortless operation of a Polkadot Node. By leveraging the advantages of Docker, this image simplifies the process of setting up and running a Polkadot Node, thereby making the power of the Polkadot network accessible to a broader audience.

Within this repository, you'll find the Dockerfile used to build the image and step-by-step instructions on how to deploy and run the Docker image. We wholeheartedly encourage everyone to use this image, contribute towards its development, and share their insights to help improve it.

By providing this tool, we hope to reduce barriers to participation in the world of blockchain technology and align it with our broader mission of revolutionizing the architectural and real estate sectors. Every contribution, no matter its size, brings us closer to our shared goal of a more inclusive, sustainable, and technologically advanced future.

We are thrilled to have you here and look forward to your valuable contributions to the Block Foundation community. Thank you for being a part of this exciting journey towards a more decentralized future!

## Setup

### Environment Variables

You can pass a number environment variables to configure the node

#### Flags

| Environment Variable            | Flag                    | Description |
| ------------------------------- | ----------------------- | ----------- |
| `POLKADOT_ENABLE_DEV`           | `--dev`                 | Run in development mode; implies `--chain=dev --validator --key Alice` |
| `POLKADOT_ENABLE_LIGHTCLIENT`   | `--light`               | Run in light client mode |
| `POLKADOT_NO_TELEMETRY`         | `--no-telelmetry`       | Should not connect to the Polkadot telemetry server (telemetry is on by default on global chains) |
| `POLKADOT_TELEMETRY`            | `-t` `--telemetry`      | Listen to all RPC interfaces (default is local) |
| `POLKADOT_VALIDATOR`            | `--validator`           | Enablevalidator mode |
| `POLKADOT_RPC_EXTERNAL`         | `--rcp-external`        | Listen to all RPC interfaces (default is local) |
| `POLKADOT_WS_EXTERNAL`          | `--ws-external`         | Listen to all Websocket interfaces (default is local) |

#### Options

| Environment Variable            | Flag                    | Description |
| ------------------------------- | ----------------------- | ----------- |
| `POLKADOT_BASE_PATH`            | `-d` `--base-path`      | Specify custom base path |
| `POLKADOT_BOOTNODES`            | `--bootnodes`           | Specify a list of bootnodes |
| `POLKADOT_CHAIN`                | `--chain`               | Specify the chain specification (one of krummelanke, dev, local or staging) |
| `POLKADOT_DB_CACHE`             | `--db-cache`            | Limit the memory the database cache can use |
| `POLKADOT_EXECUTION`            | `--execution`           | The means of execution used when calling into the runtime. Can be either wasm, native or both. |
| `POLKADOT_IN_PEERS`             | `--in-peers`            | Specify the maximum number of incoming connections we're accepting |
| `POLKADOT_KEY`                  | `--key`                 | Specify additional key seed |
| `POLKADOT_KEYSTORE_PATH`        | `--keystore-path`       | Specify custom keystore path |
| `POLKADOT_LISTEN_ADDR`          | `--listen-addr`         | Listen on this multiaddress |
| `POLKADOT_LOG`                  | `-l` `--log`            | Sets a custom logging filter |
| `POLKADOT_MAX_HEAP_PAGES`       | `--max-heap-pages`      | The maximum number of 64KB pages to ever allocate for Wasm execution. Don't |
| `POLKADOT_MIN_HEAP_PAGES`       | `--min-heap-pages`      | The number of 64KB pages to allocate for Wasm execution initially. |
| `POLKADOT_NAME`                 | `--name`                | The human-readable name for this node, as reported to the telemetry server, if enabled |
| `POLKADOT_NODE_KEY`             | `--node-key`            | Specify node secret key (64-character hex string) |
| `POLKADOT_PORT`                 | `--port`                | Specify p2p protocol TCP port |
| `POLKADOT_PRUNING`              | `--pruning`             | Specify the pruning mode, a number of blocks to keep or "archive". Default is 256. |
| `POLKADOT_RESERVED_NODES`       | `--reserved-nodes`      | Specify a list of reserved node addresses |
| `POLKADOT_RPC_PORT`             | `--rpc-port`            | Specify HTTP RPC server TCP port |
| `POLKADOT_WS_PORT`              | `--ws-port`             | Specify WebSockets RPC server TCP port |
| `POLKADOT_TELEMETRY_URL`        | `--telemetry-url`       | The URL of the telemetry server. Implies `--telemetry` |

## Resources

- https://hub.docker.com/r/parity/polkadot/
- https://hub.docker.com/r/ajcrowe/polkadot
- https://github.com/paritytech/polkadot/blob/master/doc/docker.md
- https://wiki.polkadot.network/docs/maintain-sync
- https://albertocevallos.medium.com/setting-up-a-polkadot-node-the-easy-way-3a885283091f

---

## Colophon

### Authors

This is an open-source project by the **[Block Foundation](https://www.blockfoundation.io "Block Foundation website")**.

The Block Foundation mission is enabling architects to take back initiative and contribute in solving the mismatch in housing through blockchain technology. Therefore the Block Foundation seeks to unschackle the traditional constraints and construct middle ground between rent and the rigidity of traditional mortgages.

website: [www.blockfoundation.io](https://www.blockfoundation.io "Block Foundation website")

### Development Resources

#### Contributing

We'd love for you to contribute and to make this project even better than it is today!
Please refer to the [contribution guidelines](.github/CONTRIBUTING.md) for information.

### Legal Information

#### Copyright

Copyright &copy; 2023 [Stichting Block Foundation](https://www.blockfoundation.io/ "Block Foundation website"). All Rights Reserved.

#### License

Except as otherwise noted, the content in this repository is licensed under the
[Creative Commons Attribution 4.0 International (CC BY 4.0) License](https://creativecommons.org/licenses/by/4.0/), and
code samples are licensed under the [Apache 2.0 License](http://www.apache.org/licenses/LICENSE-2.0).

Also see [LICENSE](https://github.com/block-foundation/community/blob/master/src/LICENSE) and [LICENSE-CODE](https://github.com/block-foundation/community/blob/master/src/LICENSE-CODE).

#### Disclaimer

**THIS SOFTWARE IS PROVIDED AS IS WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESS OR IMPLIED, INCLUDING ANY IMPLIED WARRANTIES OF FITNESS FOR A PARTICULAR PURPOSE, MERCHANTABILITY, OR NON-INFRINGEMENT.**
