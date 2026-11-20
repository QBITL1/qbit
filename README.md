# QBIT

[![license](https://img.shields.io/badge/license-MIT-c8ccd2)](LICENSE) [![node](https://img.shields.io/badge/node-%E2%89%A5%2024-c8ccd2)](.node-version) [![dependencies](https://img.shields.io/badge/dependencies-0-c8ccd2)](package.json)

**[qbitl1.org](https://qbitl1.org)** · [Docs](https://qbitl1.org/docs) · [X](https://x.com/QBITL1) · [Changelog](CHANGELOG.md) · [Security](SECURITY.md)

[Changelog](CHANGELOG.md) · [Security](SECURITY.md)

A quantum-resistant layer 1, running as a public testnet. Every block, attestation and transaction is signed with ML-DSA (FIPS 204) and hashed with SHA3-256. There are no elliptic curves anywhere in the chain.

One Node.js process serves the chain, the explorer, the wallet and the apps. No dependencies.

```bash
npm start      # http://localhost:8310   (Node 24 or newer: the chain uses the runtime's native ML-DSA)
npm test       # launchpad end-to-end: real ML-DSA-44 signatures against an in-process node
```

- Blocks and attestations: ML-DSA-65. Transactions: ML-DSA-44, signed in the browser. Addresses: `qbt1` + SHA3-256(public key)[0..20].
- Pages: `/` `/explorer` `/wallet` `/launchpad` `/dex` `/vault` `/node` `/rpc` `/lifeboat` `/scan` `/forge` `/validators` `/points` `/docs` `/whitepaper`.
- Public JSON-RPC at `POST /rpc` (`qbit_*` methods) and a one-file SDK at `/qbit.js`.

| Variable | Default | Purpose |
|---|---|---|
| `PORT` | `8310` | HTTP port |
| `DATA_PATH` | `./data.json` | Chain state. Put it on a persistent disk |
| `SITE_URL` | request origin | The site's public address, written into the docs, SDK and node script as they are served |
| `X_URL`, `GH_URL` | the project's X and GitHub | Links shown in the nav and footer |
| `QBIT_MINT` | empty | The $QBIT token address, shown on the front page once it exists |
| `ADMIN_KEY`, `GH_TOKEN`, `FORGE_QBIT` | empty | Points grants, GitHub API quota for tech launches, Forge bounty text |

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md). Report vulnerabilities through [SECURITY.md](SECURITY.md).

## License

[MIT](LICENSE)
