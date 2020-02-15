---
author:
    name: "Hugo Authors"
title: "Emoji Support"
description: "Guide to emoji usage in Hugo"
tags: [
    "emoji",
    ]
date: 2019-12-08T00:00:00-00:00
buttonimage: "img/coolbutton.jpg"
images: ["img/cool01.jpg"]
imagealt: "Cool Page Image"
draft: false
weight: 4
---

Emoji can be enabled in a Hugo project in a number of ways. 
<!--more-->
The [`emojify`](https://gohugo.io/functions/emojify/) function can be called directly in templates or [Inline Shortcodes](https://gohugo.io/templates/shortcode-templates/#inline-shortcodes). 

To enable emoji globally, set `enableEmoji` to `true` in your site’s [configuration](https://gohugo.io/getting-started/configuration/) and then you can type emoji shorthand codes directly in content files; e.g.


:see_no_evil: :hear_no_evil: :speak_no_evil:

🙈 🙉 🙊

The [Emoji cheat sheet](http://www.emoji-cheat-sheet.com/) is a useful reference for emoji shorthand codes.

***

**N.B.** The above steps enable Unicode Standard emoji characters and sequences in Hugo, however the rendering of these glyphs depends on the browser and the platform. To style the emoji you can either use a third party emoji font or a font stack; e.g.

{{< highlight html >}}
.emoji {
font-family: Apple Color Emoji,Segoe UI Emoji,NotoColorEmoji,Segoe UI Symbol,Android Emoji,EmojiSymbols;
}
{{< /highlight >}}

{{< css.inline >}}
<style>
.emojify {
    font-family: Apple Color Emoji,Segoe UI Emoji,NotoColorEmoji,Segoe UI Symbol,Android Emoji,EmojiSymbols;
    font-size: 2rem;
    vertical-align: middle;
}
@media screen and (max-width:650px) {
    .nowrap {
    display: block;
    margin: 25px 0;
}
}
</style>
{{< /css.inline >}}

{{< dropdown summary="This demonstrates the dropdown shortcode.  Click this." >}}
* This stuff drops down because you clicked on the text.
* Markdown is supported in here.

```
# Code sections can go in here too
```
{{< /dropdown >}}
