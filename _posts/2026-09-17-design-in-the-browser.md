---
title: "Designing in the browser"
description: "Why I design in the browser instead of a design tool, and the few cases where I still sketch on paper first."
date: 2026-09-17 09:00:00 +0000
tags: [Design, Process]
---

A few years ago I designed every project in a design tool. Each screen was a frame, each frame was a picture, and the picture never quite matched what the browser showed later. Now most of my design happens in the browser, in the same code that ships. Here is why I changed, and when I still start with a pencil.

## Why the browser won

A design file is a promise. It shows a button at one size, in one frame, with a heading that always fits on one line. The browser does not work like that. Text wraps, images change shape, and the menu breaks at 380 pixels. Finding those problems after the design is approved costs time and trust.

When I design in the browser, those problems show up on day one. I can see how a heading wraps at tablet width and fix it before the client sees anything. The design is the thing that gets built, so there is no handover where details get lost on the way.

## What I gain, and what I lose

The gains are real. I work with real content, not lorem ipsum. I test spacing with the actual fonts and colours, in light and dark mode. Change a colour token and every page updates at once. The client can open a preview link on their phone and comment on the real thing, not on a picture of it.

I do lose some things. Exploring is slower in code than on a canvas. Nobody wants to write twelve versions of a hero section just to see which one feels right. I also need to be comfortable with a bit of mess, because a browser draft looks rough until the last hour.

> A design file shows you one picture. A browser shows you every size a visitor might use.

## When I still sketch first

I still sketch first in three cases. The first is a brand-new concept, when the client does not yet know what they want. A few rough boards on paper keep the conversation about ideas rather than pixels. The second is a complex flow with many steps, such as a booking process. Drawing the path helps me see where people might get stuck before I write any markup. The third is a project where the client needs to approve a direction before any code exists.

Even then, the sketching is short. I spend an hour or two on paper, then move into the browser. I keep the sketches for reference, but the browser decides the final look.

## A simple way to start

My first session on a new project is always the same. I write the colour tokens, the type scale and one page filled with real content. Then I resize the window until something breaks, and fix it. By the end of the first day I have a rough site I can show. It is not pretty yet, but it is honest about how the design will behave on the screens people actually use.
