# maw-worktree agent contract

Keep this crate deterministic and side-effect-free. It owns worktree-to-window
matching policy only; filesystem, process, environment, time, network, and tmux
I/O belong in host adapters.

- Rust edition 2021; `unsafe_code` is forbidden.
- Clippy pedantic warnings are errors in CI.
- Preserve the maw-js JSON fixture contract.
- Keep fixture bytes behind the nondefault `fixtures` feature.
- Use exact full-SHA git dependencies.
- Run the README verification commands before opening a PR.
- Open changes through a branch and PR; do not push implementation changes
  directly to `main`.
- Never add or commit `ψ/`.
