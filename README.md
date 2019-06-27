# ejs-create-json
複数のjsonファイルをひとつにまとめて、`ejs-cli`で使用するサンプル

## 概要
`ejs-cli`は、オプションにjsonファイルを指定できますが、どうやら複数ファイルには対応できないっぽい。。

複数のjsonファイルを指定したい場合（ファイルが肥大化して管理しにくい等）、あらかじめjsonを1ファイルにまとめてから使用したらいいんじゃないか？と考えたサンプルです。

1. `./src/ejs/data/source/`配下に、ソースとなるjsonファイルを配置。
2. `create-json.js`でjsonファイルをまとめ、`./src/ejs/data/data.json`として吐き出す。
3. `package.json`のscripts内、ejs-cliのオプションには、2で作成した`data.json`を指定する。
4. create-json.jsは、`npm run create-json`で実行。
5. `npm run dev`で、開発