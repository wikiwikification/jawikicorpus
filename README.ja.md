# Japanese-Wikipedia Wikification Corpus

## 概要
Wikification (テキスト中の語句をWikipediaのエンティティに対応づけること) の機械学習モデルを作ることに特化したWikipediaタグ付きコーパスです。

## ダウンロード方法
サイズが大きいため、Dropboxにファイルをアップロードしています。

https://www.dropbox.com/sh/601gucye55nr1gq/AABekRrz4IYtp2n0_lTrKsGma

|File|Wikipedia dump date|md5|
| --- | --- | --- |
| [jawikicorpus.20180920.tar.xz](https://www.dropbox.com/s/4rcuw3385cz4t64/jawikicorpus.20180920.tar.xz) | 2018-09-20 | fb4c33ab28d0a81b68e049a29b166e53 |
| [jawikicorpus.20180901.tar.xz](https://www.dropbox.com/s/jsi40gqfqbhm4z0/jawikicorpus.20180901.tar.xz) | 2018-09-01 | 4317ec92d9958c38cbb362cd15894a83 |
| [jawikicorpus.20180820.tar.xz](https://www.dropbox.com/s/dq5ku6smcagzubb/jawikicorpus.20180820.tar.xz) | 2018-08-20 | aa448cae5c641acc6afca0e0edeb37a8 |
| [jawikicorpus.20180720.tar.xz](https://www.dropbox.com/s/annralia8gihpno/jawikicorpus.20180720.tar.xz) | 2018-07-20 | 18c3838931d03d8e0459c0bb7ba22a7f |
| [jawikicorpus.20180701.tar.xz](https://www.dropbox.com/s/xlbf1tuveg4ps9j/jawikicorpus.20180701.tar.xz) | 2018-07-01 | cfa9eb391ee09cb3c6f803d28529be84 |
| [jawikicorpus.20180620.tar.xz](https://www.dropbox.com/s/o870ax9ut9pgjbh/jawikicorpus.20180620.tar.xz) | 2018-06-20 | 1c7593696fbc300c3dd72eb533e69ab5 |
| [jawikicorpus.20180601.tar.xz](https://www.dropbox.com/s/022mo7gomlom3mi/jawikicorpus.20180601.tar.xz) | 2018-06-01 | f89f7966d5f5a8ac6e6eaf7a6201e051 |
| [jawikicorpus.20180520.tar.xz](https://www.dropbox.com/s/5lxe9rpv06bifzz/jawikicorpus.20180520.tar.xz) | 2018-05-20 | 218a2b3a61e786054dc85c8e477bcabb |
| [jawikicorpus.20180501.tar.xz](https://www.dropbox.com/s/lt1ndxjw2hlb5cs/jawikicorpus.20180501.tar.xz) | 2018-05-01 | 1a2fa10d2b9376d85cfa6f7989836a36 |

## ファイル構成
以下のtarコマンドでファイルを解凍すると3つのファイルが作られます。

```bash
tar xvJf jawikicorpus.yyyyMMdd.tar.xz
```

### entities.tsv
テキスト中の語句とそれに対応するWikipediaエンティティが記載されたtsvファイルです。テキスト中の語句については、Wikipediaのエンティティ一覧、および、記事リダイレクト情報を元に作成しています。またWikipediaエンティティについてはWikificationとしてタグ付けするにふさわしいもののみ選定しています。現時点での条件は以下のとおりです。
* 曖昧さ回避のページではないもの。
* 対応するWikipedia記事が存在するもの。
    * ※ リダイレクトを挟むものについてはリダイレクト先のWikipediaエンティティを採用しています。

### articles.txt
記事リンク以外のMarkdownを取り除いたWikipediaの記事本文です。
1行1記事になっています。元のmarkdownでの改行はタブ文字に対応しています。記事のWikipediaエンティティ名は行頭に記載しています。

なお記事リンクのMarkdownは `[[Wikipediaエンティティ|表示上のテキスト]]` の形式になっています。また記事リンクはWikificationとしてタグ付けするにふさわしいWikipediaエンティティに関してのみ付与しています。選定条件についてはentities.tsvにセクションで示したものと同じです。

### LICENSE.md
ライセンスについての文書です。
