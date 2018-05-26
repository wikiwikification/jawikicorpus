# Japanese-Wikipedia Wikification Corpus

## このコーパスは何?
Wikification (テキスト中の語句をWikipediaのエンティティに対応づけること) の機械学習モデルを作ることに特化したWikipediaタグ付きコーパスです。

## ダウンロード方法
サイズが大きいため、Dropboxにファイルをアップロードしています。

https://www.dropbox.com/sh/601gucye55nr1gq/AABekRrz4IYtp2n0_lTrKsGma

|File|Wikipedia dump date|md5|
| --- | --- | --- |
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
