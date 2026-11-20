# Contributing

Thanks for looking. QBIT is one Node.js program with no dependencies.

## Getting set up

```bash
git clone https://github.com/QBITL1/qbit
cd qbit
npm start            # http://localhost:8310
npm test             # end-to-end: real ML-DSA-44 signatures against an in-process node
```

Node 24 or newer.

## Where things live

- `server/index.js` is the chain: state, block production, attestations, the HTTP API and the JSON-RPC.
- `server/launchpad.js` is the token launchpad: bonding curve, fees, GitHub verification for tech tokens.
- `client/` is the site: one HTML file per page, a shared `qbit.css` and `common.js`.
- `client/qbit.js` is the SDK and `client/qbit-node.js` is the single-file validator.
- `test/` holds the end-to-end suite.

## Making a change

1. Branch from `dev`.
2. Keep the change small and add a test that fails without it.
3. Run the tests.
4. Open a pull request against `dev`, and say which tests you ran.

Security issues go through [private reporting](https://github.com/QBITL1/qbit/security/advisories/new), not pull requests.
