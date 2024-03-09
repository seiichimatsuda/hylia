---
title: 画像とビデオの投稿
socialImage: /images/p1150608.jpg
date: 2019-06-18
tags:
  - ブログ
  - 簡単な投稿
  - メディア
---
ブログ記事がHylia上でどのように見えるかを示すための投稿。コンテンツはすべてマークダウンとして "Body "フィールドに設定され、Eleventyが適切なHTML投稿に変換する。CMSを使いたくない場合は、マークダウンファイルを直接編集することもできる。

画像をブリードアウトさせたい場合は、その画像にtitle属性を追加すれば、フロントエンドが自動的に<figure>タグで囲んでくれます。

![青空を背景にした灰色のコンクリート・ビルの屋上](/images/p1150608.jpg "最高のブルータリズム。Photo by Artificial Photography on Unsplash.")

また、YouTubeやVimeo（または、本当にどこでも）から投稿にビデオを追加することもでき、フロントエンドは、あなたのためにそれらをブリードアウトすることもできます。

<iframe width="560" height="315" src="https://www.youtube.com/embed/_38JDGnr0vA" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></iframe

Finally, how about a `<blockquote>`?

> Quotes will take a slightly different style to normal body text and look fancy.

![同じ川を背景にした川辺と建物の写真を掲げる人物](/images/demo-image-2.jpg "図とキャプションが必要な場合は、bodyフィールドの画像に'title'属性を追加することを忘れないでください - Photo by Kharytonova Antonina on Unsplash.")

これで、Hyliaを使って見栄えの良いブログを作るのがいかに簡単かがお分かりいただけたと思う。