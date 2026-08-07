<!-- i18n: language-switcher -->
[English](README.md) | [日本語](README.ja.md)

# irodori-sql

Irodori Tableやその他のRustホストで使用されるSQLヘルパー。

## 提供内容

- 方言メタデータ
- 識別子の引用
- プレースホルダーおよびページングヘルパー
- クエリパラメータ検出
- スキーマ／メタモデルクエリビルダー
- スキーマ差分ヘルパー
- マイグレーションSQLおよび検証SQLビルダー

このクレートはデータベースに接続しません。

## 使用方法

```toml
[dependencies]
irodori-sql = { git = "https://github.com/irodori-table/irodori-sql", tag = "v0.3.0" }
```

```rust
use irodori_sql::dialect::{quote_identifier, DbEngine};

let name = quote_identifier(DbEngine::Postgres, "order");
assert_eq!(name, "\"order\"");
```

## 開発

```sh
cargo test
```

ライセンス: `MIT OR 0BSD`。

## ライセンス

0BSD。このプロジェクトはほぼあらゆる目的で使用、コピー、改変、配布が可能です。