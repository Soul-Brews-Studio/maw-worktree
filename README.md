# maw-worktree

Portable worktree-to-window matching policy for the maw fleet.

This crate is extracted from
[`Soul-Brews-Studio/maw-rs`](https://github.com/Soul-Brews-Studio/maw-rs)
and mirrors the maw-js `worktree-window-match` behavior through a committed JSON
fixture corpus.

## Use

Consumers use this unpublished crate as a Cargo git dependency pinned to an
immutable full commit SHA.

The production dependency has no fixture payload. Differential consumers can
enable the nondefault `fixtures` feature to access
`WORKTREE_WINDOW_MATCH_FIXTURES_JSON` in tests.

## Verify

```bash
cargo fmt --all -- --check
cargo test --locked --no-fail-fast
cargo test --locked --features fixtures --no-fail-fast
cargo clippy --locked --all-targets -- -D warnings
cargo clippy --locked --all-targets --features fixtures -- -D warnings
```

## Provenance

The initial crate source, tests, and fixture were copied from `maw-rs` alpha at
`2a83db7104e54a1dcc41b911a528279c96fe1c8a`.
