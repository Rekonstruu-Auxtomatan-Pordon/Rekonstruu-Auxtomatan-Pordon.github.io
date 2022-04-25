# ここについて

このリポジトリは後付け自動ドア開発チームのドキュメントリポジトリです

## セットアップ方法

- [Rust](https://www.rust-lang.org/ja/tools/install)からインストーラーをダウンロードします。
- インストーラーを実行すると、標準ではパスが通ります。

- コマンドプロンプトからmdbookをインストールします。

```shell
cargo install mdbook
```

- リポジトリのルートディレクトリで、mdbookを起動します。

```shell
mdbook serve
```

- 標準だと、

```url
http://localhost:3000
```

で立ち上がります。

## 使用したものについて

- [mdBook](https://github.com/rust-lang/mdBook)はrustで作られた文章管理ツールです。
- peaceiris様が作られた、[actions-mdbook](https://github.com/peaceiris/actions-mdbook)を使用しています。
