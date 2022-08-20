# nuxt3-leaflet-example

## Overview

Nuxt.js v3 で Leaflet を使用するサンプルプログラムです。
以下の記事を解説するために作成したリポジトリです。

An example program that uses Leaflet in Nuxt.js v3.
This is a repository created to explain the following article.

- [Nuxt3 で GoogleMap の代替である Leaflet を使う方法](https://std9.jp/articles/01GAWCQH4ANGP4A9ABHZB32DXH)

## Requirement

- Node.js (v16.14.2)

## Setup

```shell
# 依存関係のパッケージをインストール
$ npm i

# 開発環境で実行 (http://localhost:3000/)
$ npm run dev
```

## Author

[twitter](https://twitter.com/hikaru_firecamp)


## ビルド時の警告について

現状の leafletjs:1.8.0 を使用するとビルド時に `[vite:css] Replace color-adjust to print-color-adjust. The color-adjust shorthand is currently deprecated.` 警告が表示されます。現状、無視しても特に問題はありません。

[issue](https://github.com/Leaflet/Leaflet/issues/8210) によると 2022/05/03 にリポジトリ的には修正済みのようだがリリースがいまだにされていない。
次期バージョンである [v1.9.0](https://github.com/Leaflet/Leaflet/milestone/38) に組み込まれる予定とのこと。
