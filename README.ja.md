# Japanese-Wikipedia Wikification Corpus

## このコーパスは何?
Wikification (テキスト中の語句をWikipediaのエンティティに対応づけること) の機械学習モデルを作ることに特化したWikipediaのタグ付きコーパスです。

## ダウンロード方法
サイズが大きいため、Dropboxにファイルをアップロードしています。

https://www.dropbox.com/sh/601gucye55nr1gq/AABekRrz4IYtp2n0_lTrKsGma

|File|Wikipedia dump date|md5|
| --- | --- | --- |
| [jawikicorpus.20180420.tar.xz](https://www.dropbox.com/s/x0ra2tjl874r42z/jawikicorpus.20180420.tar.xz) | 2018-04-20 | 3a81b9115463906e3a5dbfe99364a3ee |

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
