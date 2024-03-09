---
title: 投稿サンプル
date: 2019-06-18
tags:
  - ブログ
  - 簡単な投稿
  - コード
---
コード投稿をデモする最良の方法は、実際の投稿を表示することです。そこで、[andy-bell.design](https://andy-bell.design/wrote/creating-a-full-bleed-css-utility/)からの、フルブリードCSSユーティリティに関する投稿をご覧ください。

- - -

時には、コンポーネントが置かれている制約から抜け出したいことがあります。このような状況がよく起こるのは、CMSのメインコンテンツエリアのように、コンポーネントが存在するコンテナをあまりコントロールできない場合です。

これは、[WordPress Gutenbergエディタ](https://wordpress.org/gutenberg/)のような編集ツールではさらに顕著です。理論的には、デザインシステムからコンポーネントを取り込んで、ウェブページのメインコンテンツで利用することができます。このような状況では、要素をビューポートの幅の100%にする小さなユーティリティがあると、とても便利です。

This is when I normally pull the `.full-bleed` utility class out of my back pocket.

## The `.full-bleed` utility

It’s small, but hella mighty:

```css
.full-bleed {
  width: 100vw;
  margin-left: 50%;
  transform: translateX(-50%);
}
```

Here it is in a context where it makes a fancy `<aside>` and a `<figure>` element bleed out of their parent container.

<iframe height="300" style="width: 100%;" scrolling="no" title="Piccalilli CSS Utility — Issue  #2 — Full bleed utility" src="//codepen.io/andybelldesign/embed/Nmxrwv/?height=300&theme-id=dark&default-tab=css,result" frameborder="no" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href='https://codepen.io/andybelldesign/pen/Nmxrwv/'>Piccalilli CSS Utility — Issue  #2 — Full bleed utility</a> by Andy Bell
  (<a href='https://codepen.io/andybelldesign'>@andybelldesign</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

The `.full-bleed` utility gives those elements prominence and *importantly* keeps their semantic place in the page. Just how I like it.

- - -

🔥 **Pro tip**: When working with a utility like `.full-bleed`, it’s a good idea to add an inner container that has a max-width and auto horizontal margin. For this, I normal create a shared `.wrapper` component like this:

```css
.wrapper {
  max-width: 50rem;
  margin-left: auto;
  margin-right: auto;
}
```

Having a container like `.wrapper` helps to create consistent, centred content.  

- - -

### How the `.full-bleed` utility works

We set the container to be `width: 100vw`, which equates to the full viewport width. We couldn’t set it to `width: 100%` because it would only fill the space of its parent element. The parent element’s width *is* useful though, because by setting `margin-left: 50%`, we are telling the component to align its **left edge** to the center of its parent element, because `50%` is half of the **parent element’s** width.

Finally, we use CSS transforms to `translateX(-50%)`. Because the transform works off the element’s dimensions and not the parent’s dimensions, it’ll pull the element back `50vw`, because it’s `100vw` wide, thus making it sit perfectly flush with the viewport’s edges.

## Wrapping up

Hopefully this short and sweet trick will help you out on your projects. If it does, [drop me a tweet](https://twitter.com/andybelldesign), because I’d love to see it!