# TypeScript SDK examples

1. Install the SDK: `npm i @tirdad-ai/sdk`.
2. Copy `.env.sample` to `.env` and set **`TIRDAD_API_KEY`**. Optionally set **`TIRDAD_API_HOST`** to a full URL (default: `https://api.tirdad.ai/v1`).
3. Run: from the package root, `npx tsx examples/quick-start.ts`; or from `examples/`, `npx tsx quick-start.ts`.

**Integration tests:** Full API flows are in [api/tests/ts/test_sdk.ts](../../tests/ts/test_sdk.ts). Run `npm test` from `api/tests/ts`; see [api/tests/README.md](../../tests/README.md).
