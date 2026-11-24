---
title: "A hundred on PageSpeed, without tricks"
description: "How I reach a 100 PageSpeed score on client sites with inline critical CSS, one web font, responsive WebP and deferred scripts."
date: 2026-10-09 09:00:00 +0000
tags: [Performance, Front-end]
---

A 100 on PageSpeed is not magic. Most of the time it comes from a short list of decisions made early, before the design is even finished. Here is the list I work through on every client site, and the reason behind each step.

## Send the first screen in the first response

A browser cannot paint the page until it has the CSS for it. If that CSS sits in a file the browser has to fetch first, the screen stays blank for longer. I inline the small amount of CSS needed for the top of the page, the critical CSS, straight into the head. The rest of the styles load as a normal stylesheet after that.

```html
<head>
  <style>
    body { margin: 0; font-family: "Inter", sans-serif; }
    .hero { min-height: 70vh; display: grid; place-items: center; }
  </style>
  <link rel="stylesheet" href="/css/site.css" media="print" onload="this.media='all'">
</head>
```

The inline block only covers what the visitor sees first. Everything else can wait a few milliseconds.

## Use one web font, and only the weights you need

Web fonts are a common cause of slow text. Each family and weight is another request, and the text can stay invisible while the file loads. I use one family, usually a variable font, in two weights at most. I preload the file that holds the body text, and I set `font-display: swap` so visitors can read something straight away.

I also check the fallback font. If its sizes are close to the web font's, the text barely moves when the real font arrives. That keeps the layout stable, which matters for the score as much as the speed does.

## Images as WebP, with srcset and fixed sizes

Most of the page weight on a portfolio or a shop is images. I export everything as WebP at a few widths, then let the browser pick the one that fits the screen. A phone should never download the desktop hero. I give every image a width and height, so the browser can reserve the space before the file arrives. Lazy loading goes on anything below the fold, and never on the hero image, because that one is needed straight away.

## Hold back third-party scripts until someone asks

Chat widgets, video embeds, social feeds and tag managers are where most scores go to die. They load a lot of code, often before the visitor has done anything at all. My default is a plain placeholder. For a chat widget, that means a button that says "Chat with us". The real script loads when the visitor clicks, so the first paint is not held up by code they may never use.

Analytics is the one thing I keep running from the start. I use a small, privacy-friendly script, load it after the page has finished, and check its cost in the trace.

## Measure on a phone, not only on my laptop

I run PageSpeed on the mobile test, because it is the harder one. My laptop is quick, so local scores can look fine while the real visitor on a cheap phone waits. Where the client already has traffic, I also check the field data. I change one thing at a time, so I know which change actually helped.

A hundred is a nice number, but the real goal is a page that opens fast for the person who needs it. The score is just the proof that the basics are in place.
