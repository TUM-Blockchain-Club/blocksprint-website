# AGENTS.md

## Project Overview

This is the BlockSprint website, built with SvelteKit, Svelte 5, Vite, and Tailwind CSS. The app routes live in `src/routes`, shared Svelte components live in `src/lib/components`, static files live in `static`, and image assets live in `src/lib/img`.

## Tooling

- Use `pnpm` for Node.js dependency installation and scripts.
- The local pnpm version currently in use is pnpm 11.
- Use `pnpm run dev` for local development.
- Use `pnpm run build` to verify production builds.
- Use `pnpm run lint` for formatting and lint checks.

## Dependency Setup

pnpm build script approvals are stored in `pnpm-workspace.yaml`. `esbuild` is approved because Vite and related build tooling require its postinstall script to prepare the platform-specific binary.

If pnpm reports ignored build scripts, approve only the required dependency scripts intentionally instead of disabling the safety mechanism globally.

## Conventions

- Keep Svelte route pages under `src/routes`.
- Keep reusable UI primitives under `src/lib/components/ui`.
- Keep project-specific reusable components under `src/lib/components`.
- Prefer small, focused changes that match the existing SvelteKit and Tailwind structure.
- Document notable setup or architecture changes in Markdown under `docs/`.
