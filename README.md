# learn-rust

Rust の学習用リポジトリ。

## 構成

| ディレクトリ | 内容 |
| --- | --- |
| `book/` | [The Rust Programming Language](https://doc.rust-lang.org/book/)（[日本語版](https://doc.rust-jp.rs/book-ja/)）の写経・演習。章ごとに crate を作る |
| `exercises/` | 自分で書く小さな練習 |
| `projects/` | CLI や Web サーバなどの小さなアプリ |
| `notes/` | 詰まった点・学んだことのメモ |

全体を 1 つの Cargo workspace にしている。

```sh
cargo new book/ch02-guessing-game
cargo run -p ch02-guessing-game
cargo clippy --workspace
```
