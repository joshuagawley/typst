# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Build Commands
- Build: `cargo build --release`
- Run tests: `cargo test --workspace`
- Run specific test: `cargo test --workspace --test tests -- --exact test-name`
- Run tests matching pattern: `cargo test --workspace --test tests -- "pattern"`
- Run tests in path: `cargo test --workspace --test tests -- -p tests/suite/path`
- Update test references: `cargo test --workspace --test tests -- --exact test-name --update`
- Lint: `cargo clippy --workspace`

## Code Style
- Use Rust 2021 edition
- Follow rustfmt settings (max_width: 90, use_small_heuristics: "Max")
- Maintain existing code patterns and module organization
- Document all new Rust types with doc comments
- Write concise examples for Typst definitions (5-10 lines with <38 columns)
- Add tests for new features (prefer assertions over reference images when possible)
- Follow incremental compilation design for all language features
- Design with composability in mind, avoid overly specific knobs
- Use consistent naming conventions in existing modules