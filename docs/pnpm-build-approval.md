# pnpm Build Approval

## Context

Running `pnpm run dev` triggered pnpm's dependency status check, which attempted an install and failed with `ERR_PNPM_IGNORED_BUILDS`.

pnpm reported ignored build scripts for `esbuild@0.21.5` and `esbuild@0.25.12`. These postinstall scripts are required by Vite/SvelteKit build tooling so that the correct platform-specific esbuild binary is available.

## Fix

`esbuild` was approved with:

```sh
pnpm approve-builds esbuild
```

This updated `pnpm-workspace.yaml` to allow esbuild build scripts:

```yaml
allowBuilds:
  esbuild: true
```

After approval, `pnpm install` completed successfully.
