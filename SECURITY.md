# Security

QBIT is a public testnet. The code that matters most is the signature path: every transaction (ML-DSA-44) and every block and attestation (ML-DSA-65) is verified in `server/index.js` with the Node.js runtime's native ML-DSA before it changes state.

## Reporting a vulnerability

Use GitHub's private vulnerability reporting on this repository: [report a vulnerability](https://github.com/QBITL1/qbit/security/advisories/new). Include the steps to reproduce and what you observed. Please do not open a public issue for anything in the list below.

You will get an acknowledgement within 72 hours and a fix or a written assessment within 14 days.

## In scope

- Accepting a transaction, block or attestation whose signature does not verify
- Spending or minting balance without a valid signature from the owner
- Replaying a signed transaction or a signed app operation (nonce handling)
- Anything in the launchpad, DEX, vaults or lifeboat that moves funds without the signer's intent
- Halting block production or corrupting chain state from the public API

## Supported versions

The `main` branch and the latest release.
