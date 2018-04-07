# Japanese-Wikipedia Wikification Corpus

## What is this corpus?
A Wikipedia tagged corpus specific to creating a machine learning model for Wikification which stands for the process of linking terms in a plain text to corresponding Wikipedia entities.

## Download
Due to the large file size, files are uploaded to Google Drive.

https://drive.google.com/drive/folders/1H6-LYqhtMqtO8Sd30fE5Y-dd6Ih-Y5Ag

|File|Wikipedia dump date|md5|
| --- | --- | --- |
| jawikicorpus.20180320.tar.gz | 2018-03-20 | 6fa89642eb520c5c241c00f2112dbccd |

## Files
By decompressing an archive with a tar command, the following 3 files are created.

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

Note that the markdowns for article links are formatted as '[[Wikipedia entity|displayed text]]'.
In addition, the article links are limited to those suitable for Wikification tagging.
The selection rules are the same as those shown in the entities.tsv section.

### LICENSE.md
Document regarding licensing.
