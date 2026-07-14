# Public batch commitments

> EXPERIMENTAL — TEST NETWORK ONLY — NOT A FINANCIAL PRODUCT OR SERVICE — NO REAL FUNDS — AS IS, NO WARRANTY, NO LIABILITY — USE AT YOUR OWN RISK

This directory is mirrored in the public commitments repository (https://github.com/Degrudv/caravan-commitments) as the public-branch publication channel for T-M4.4. Each live artifact is named
`<batchId>.json`, validates against `schema.json`, and contains only the batch hash, Base Sepolia transaction
hash, chain ID, batch ID, and integer close time. The private canonical matcher snapshot is never committed.

A file alone never unlocks reveal. The API also verifies that its exact batch hash is the complete calldata of
a successful Base Sepolia self-transaction from the explicitly configured Caravan publisher. See
`docs/specs/batch-commitment.md` for the canonical serialization and fail-closed rules.

## Live testnet evidence

The live artifact [`batch-2026-07-13-00.json`](batch-2026-07-13-00.json) commits batch hash
`0x32c2eed4031d8283ce95eb912cbfe55897f2975fe4fb16157a3d353912c6fff8`. Its matching successful
[Base Sepolia transaction](https://sepolia.basescan.org/tx/0x705068ff05604ba16b3c11d7f170f9c6e5689b1bc58ac9ea3fe2ff82e42fffd3)
is the authorized publisher self-transaction whose complete calldata is that hash.

Only this strict metadata artifact and the 32-byte commitment are public. The canonical matcher snapshot,
participants, offers, prices, quantities, regions, endpoints, signing material, and credentials remain private.
