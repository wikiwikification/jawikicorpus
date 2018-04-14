# Japanese-Wikipedia Wikification Corpus

## このコーパスは何?
Wikification (テキスト中の語句をWikipediaのエンティティに対応づけること) の機械学習モデルを作ることに特化したWikpediaのタグ付きコーパスです。

## ダウンロード方法
サイズが大きいため、Google Driveにファイルをアップロードしています。

https://drive.google.com/drive/folders/1H6-LYqhtMqtO8Sd30fE5Y-dd6Ih-Y5Ag

|ファイル名|Wikipediaのダンプ日付|md5|
| --- | --- | --- |
| jawikicorpus.20180401.tar.gz | 2018-04-01 | a838ece1b8ead3d3eb0d8444a883c3ee |
| jawikicorpus.20180320.tar.gz | 2018-03-20 | 6fa89642eb520c5c241c00f2112dbccd |

## ファイル構成
tarコマンドでファイルを解凍すると以下の3つのファイルが作られます。

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
