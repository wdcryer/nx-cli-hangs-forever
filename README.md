This demonstrates an issue in which Nx CLI commands hang forever. To reproduce the issue:

1. Use Node 20. Version managers like NVM or FNM can be used to install the correct version.
2. Run `corepack enable` to install the correct `pnpm` version.
3. Run `pnpm install`.
4. Run `pnpm nx report` or `pnpm build`.
5. Observe that the command hangs indefinitely.
6. Delete the code in `apps/docs/src/__tests__/some.test.mjs`.
7. Run `pnpm nx report` or `pnpm build`.
8. Observe that the command works as expected.
