# Japanese-Wikipedia Wikification Corpus

## Summary
A Wikipedia tagged corpus specific to creating a machine learning model for Wikification which stands for the process of linking terms in a plain text to corresponding Wikipedia entities.

## Download
Due to the large file size, files are uploaded to Dropbox.

https://www.dropbox.com/sh/601gucye55nr1gq/AABekRrz4IYtp2n0_lTrKsGma

|File|Wikipedia dump date|md5|
| --- | --- | --- |
| [jawikicorpus.20180820.tar.xz](https://www.dropbox.com/s/6mhk3u389o9uerk/jawikicorpus.20180820.tar.xz) | 2018-08-20 | 046713f75a0e2eef4ed8d3b1c8ede9ae |
| [jawikicorpus.20180720.tar.xz](https://www.dropbox.com/s/annralia8gihpno/jawikicorpus.20180720.tar.xz) | 2018-07-20 | 18c3838931d03d8e0459c0bb7ba22a7f |
| [jawikicorpus.20180701.tar.xz](https://www.dropbox.com/s/xlbf1tuveg4ps9j/jawikicorpus.20180701.tar.xz) | 2018-07-01 | cfa9eb391ee09cb3c6f803d28529be84 |
| [jawikicorpus.20180620.tar.xz](https://www.dropbox.com/s/o870ax9ut9pgjbh/jawikicorpus.20180620.tar.xz) | 2018-06-20 | 1c7593696fbc300c3dd72eb533e69ab5 |
| [jawikicorpus.20180601.tar.xz](https://www.dropbox.com/s/022mo7gomlom3mi/jawikicorpus.20180601.tar.xz) | 2018-06-01 | f89f7966d5f5a8ac6e6eaf7a6201e051 |
| [jawikicorpus.20180520.tar.xz](https://www.dropbox.com/s/5lxe9rpv06bifzz/jawikicorpus.20180520.tar.xz) | 2018-05-20 | 218a2b3a61e786054dc85c8e477bcabb |
| [jawikicorpus.20180501.tar.xz](https://www.dropbox.com/s/lt1ndxjw2hlb5cs/jawikicorpus.20180501.tar.xz) | 2018-05-01 | 1a2fa10d2b9376d85cfa6f7989836a36 |

## Files
By decompressing an archive with the following tar command, 3 files are created.

```bash
tar xvJf jawikicorpus.yyyyMMdd.tar.xz
```

### entities.tsv
A tsv file containing terms appeared in a plain text and corresponding Wikipedia entities.
The terms are made from a list of Wikipedia entites and a list of redirect pages.
The Wikipedia entities are limited to those suitable for Wikification tagging.
At present, the selection rules are as follows:
* Entities assigned "Disambiguation pages" category are omitted.
* Entities with no corresponding Wikipedia articles are omitted.
   * Note that if an entity redirects inside, the redirected entity is adopted.

### articles.txt
A body of Wikipedia articles removed any markdowns except article links.
Each line of the plain text corresponds to a Wikipedia article.
Line breaks in its original markdowns are replaced with tab characters.
Each entity of the article is listed at the beginning of each line.

Note that the markdowns for article links are formatted as `[[Wikipedia entity|displayed text]]`.
In addition, the article links are limited to those suitable for Wikification tagging.
The selection rules are the same as those shown in the entities.tsv section.

### LICENSE.md
Document regarding licensing.
