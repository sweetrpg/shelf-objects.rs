# AGENTS.md

This file provides guidance to Claude Code, Codex, GitHub Copilot, and other AI coding agents
working in this repository.

## About This Project

`shelf-objects.rs` defines the persistence models and API value objects for the Shelf
microservice's domain: library, wishlist, table, visibility. Pure data types - no business
logic, no I/O.

Currently a scaffold - no implementation yet, no Rust consumer exists today.

## Committing Code

Use [Conventional Commits](https://www.conventionalcommits.org/):

```
<type>(<scope>): <description>
```

## Branches and Workflow

* `develop` - integration branch, default branch, target for all PRs.
* `master` - latest released state, nothing committed directly.
* `feature/*`, `fix/*` branched from `develop`; `hotfix/*` branched from `master`.

See `CONTRIBUTING.md` for the full workflow.

## Running Checks Locally

```bash
cargo build --verbose
cargo clippy --verbose
cargo test --verbose
cargo doc --no-deps
cargo tarpaulin --engine llvm
```
