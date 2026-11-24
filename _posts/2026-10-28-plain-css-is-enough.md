---
title: "Why I still write plain CSS"
description: "Why I still write plain CSS in 2026, and how custom properties, cascade layers and container queries cover most of what I need."
date: 2026-10-28 09:00:00 +0000
tags: [CSS, Front-end]
---

I still write plain CSS for almost every site I build. Clients sometimes expect a framework, and a few have asked me directly why I am not using one. The honest answer is that the browser has caught up with most of what frameworks were built to fix. Here is what I use, and when I reach for something else.

## Custom properties do the heavy lifting

Custom properties are the first thing I set up on every project. I put colours, spacing and type sizes on `:root`, and each component reads from them.

```css
:root {
  --color-ink: #1d1b18;
  --color-paper: #f7f4ef;
  --space-md: 1rem;
}

.card {
  color: var(--color-ink);
  background: var(--color-paper);
  padding: var(--space-md);
}
```

If the client changes the brand colour, I edit one line. Dark mode is a second block inside a media query, not a second stylesheet. Unlike Sass variables, custom properties exist at runtime, so a small script can change them too, for example when a visitor flips a theme switch.

## Cascade layers stop the specificity fights

Most big stylesheets do not go wrong because of the syntax. They go wrong because two rules fight over specificity, and somebody reaches for `!important`. Cascade layers fix that. I declare the order once at the top of the file, then put each part of the site into its own layer.

```css
@layer reset, base, components, utilities;
```

Anything in a later layer wins, however specific the selector is. My utilities layer sits last, so a one-off margin always works. I have not needed `!important` in a client project for a long time.

## Container queries fit components, not screens

Media queries ask about the window. A card in a narrow sidebar and the same card in a wide grid need different layouts, but the window width tells you nothing about either. Container queries ask about the space the component really has. I set `container-type: inline-size` on the wrapper, then write rules for the card inside it. The card now looks right wherever I drop it.

## When a framework is worth it

I am not against frameworks. A team of six working on a large app, or a design system shared across several products, can gain a lot from a component model and a build pipeline. A five-page site for a dentist does not need either.

My rule is simple. If I can describe the whole design in a page of custom properties and a few layers, I skip the tooling. Every dependency is something to update, debug and pay for later. A plain stylesheet has no build step to break and no generated file to read when something looks wrong. The browser does the work, and the page loads faster for it.

> Most CSS bugs I have seen came from a rule I forgot I wrote, not from the language itself. Keep the file small, and it stays easy to read.

I still reach for a framework now and then. Most of the time, though, plain CSS is the quickest route to a site that looks right and stays easy to change.
