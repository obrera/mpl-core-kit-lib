# @obrera/mpl-core-kit-lib

Reusable MPL Core `@solana/kit` helper/plugin code extracted from [`beeman/mpl-core-kit`](https://github.com/beeman/mpl-core-kit).

## What this is

This repo packages the TypeScript library that currently lives under `/lib` in `beeman/mpl-core-kit` so it can be consumed independently while the upstream kit-plugin work is still in progress.

It is a library package only, not an app or CLI.

## Included surface area

- generated MPL Core client code
- helper utilities
- hooked account decoders
- plugin/helper types and converters

## Install

```bash
bun add @obrera/mpl-core-kit-lib
```

The package is intended to publish publicly to npm under the `@obrera` scope.

## Usage

```ts
import { MPL_CORE_PROGRAM_ADDRESS } from '@obrera/mpl-core-kit-lib'
import { createMplCoreProgram, fetchAssetV1 } from '@obrera/mpl-core-kit-lib/generated'
import { assetPluginsListFromAssetAccountData } from '@obrera/mpl-core-kit-lib/hooked'
import { pluginAuthorityFromBase } from '@obrera/mpl-core-kit-lib/plugins'
```

## Development

```bash
bun install
bun run build
bun run check-types
bun test
```

## Notes

- Source of truth for this extracted code is currently `beeman/mpl-core-kit/lib`.
- This package should be treated as temporary until the upstream reusable package shape settles.
- If the upstream code reorganizes its public API, this package should be rebased to match rather than growing a separate API story.
