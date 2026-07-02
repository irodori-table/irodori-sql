# Contributing

`irodori-sql` contains SQL dialect, parameter, metamodel, and schema helpers used
by Irodori Table and sibling Rust hosts.

## Clean-Room Rules

Follow the Irodori clean-room policy before using reference products, source
code, snippets, generated assets, or database-client behavior notes:

<https://hjosugi.github.io/irodori-docs/clean-room.html>

Project-authored code uses `MIT OR 0BSD` unless a file states otherwise.

## Local Checks

```sh
cargo fmt --all -- --check
cargo test
```

Integration tests that need external database services should document the
required service and environment variables in the test or PR.
