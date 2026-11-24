# Izar: a dark developer-portfolio theme for Jekyll

A fast, dark, monospace portfolio for front-end developers and designers. Every page is a list of ready-made sections you edit in plain text, and every page is built to score 100 on PageSpeed: one font file, no framework, no jQuery, and only a few lines of JavaScript.

**Documentation:** https://tortoizthemes.com/docs/izar/
**Live demo:** https://izar.tortoizthemes.com · **Section catalogue:** https://izar.tortoizthemes.com/blocks/

## Features

- **Pages built from sections.** Hero, services, client logos, works, testimonials, awards, notes, contact and a page header: 15 variants in all. Copy a section's snippet from `/blocks/`, paste it into a page, change the words.
- **Works.** One Markdown file per project, each with its own page: details, a large screenshot, the write-up, an optional gallery and a "Next project" link.
- **Notes**, a blog with reading time, topics, previous and next links, code blocks styled for the dark theme, and an RSS feed.
- **Contact form** with no JavaScript, sent through Web3Forms or Formspree, with a spam trap and a thank-you page.
- **Dark by default**, with light mode and "follow the system" one setting away, and an optional light/dark switch in the header that remembers each visitor's choice.
- **Sections fade in as you scroll.** The effect is built to keep PageSpeed at 100, and it's switched off for visitors who ask their device for less motion.
- **Accessible:** WCAG AA contrast in both modes, keyboard-friendly tabs and menu, and one clear heading outline per page.
- **SEO:** titles, descriptions, canonical URLs, share images, structured data (Person, BlogPosting, CreativeWork), a sitemap and a feed.
- **Works on GitHub Pages** as it is: it uses only the plugins GitHub Pages allows, and plain CSS (no Sass).
- **One words file** (`_data/strings.yml`) for every word the theme prints, so you can reword or translate it in one place.

## Getting started

You need Ruby 3 and Bundler.

```bash
bundle install
bundle exec jekyll serve     # http://localhost:4000
bundle exec jekyll build     # the finished site is in _site/
```

Then open `_config.yml` and put in your name, email, links and form settings. Everything there has a comment saying what it does.

## What's where

```text
_config.yml          Your name, links, footer, contact form, colours and switches
index.md             The home page: a list of sections
works.md             The Works page
notes.md             The Notes page (notes-tags.md lists posts by topic)
contact.md           The Contact page (thank-you.md follows a sent message)
_projects/           One file per project (Works)
_posts/              One file per note, named YYYY-MM-DD-title.md
_data/strings.yml    Every word the theme prints
_data/examples/      The snippets shown on /blocks/
_includes/sections/  One file per section type, with its fields listed at the top
_includes/css/       Colours, type, spacing and one CSS file per section
assets/img/          Your pictures
```

## Building a page

A page is a list of sections in its front matter. Copy any snippet from `/blocks/` under `sections:`:

```yaml
---
layout: page
title: About
description: One sentence for search engines.
sections:
  - type: page-header
    badge: About
    heading: Hi, I'm Daniel
    text: I design and code beautifully simple things.
  - type: services
    variant: grid
    tone: band
    heading: What I do
    items:
      - title: Design
        text: Create digital products with unique ideas
        icon: pen
        count: 20 projects
---
```

- Add `tone: band` to every other section for the alternating background.
- Add `hidden: true` to switch a section off without deleting it.
- Anything written below the front matter appears after the sections.

## Adding a project or a note

- **A project:** copy `_projects/kiko.md`, rename it (the file name becomes the address, `/works/<name>/`) and change the details. Set `featured: true` to show it in the home page's Latest Works, and use `order` to sort.
- **A note:** add a file to `_posts/` named like `2026-12-01-my-first-note.md`, with `title`, `description`, `date` and `tags`.

## Pictures

- Put pictures in `assets/img/` and give each one its real `width` and `height`, so the page doesn't jump while it loads.
- WebP is the best format. For a sharp picture on every screen, save a few widths named `name-360.webp`, `name-540.webp` and `name-710.webp`. Then write `src: /assets/img/work/name` and `widths: [360, 540, 710]`, and the browser picks the right one.
- The demo's portrait, three of its project screenshots and the testimonial photos aren't included. Your download has neutral stand-ins with the same file names, so you can replace them one by one.
- The hero portrait works best as a cut-out (transparent background) about 750 pixels wide.

## Contact form

1. Get a free access key from web3forms.com, or a form endpoint from formspree.io.
2. In `_config.yml`, set `izar.form.provider` to `web3forms` or `formspree`, and fill in `access_key` or `endpoint`.

On `demo`, the form sends nothing and goes straight to the thank-you page.

## Deploying

- **GitHub Pages:** push the site to a repository, then turn on Pages in the repository settings (deploy from the main branch). Set `url` in `_config.yml`, and `baseurl` if the site lives at `username.github.io/repository`.
- **Cloudflare Pages or Netlify:** use build command `bundle exec jekyll build` and output folder `_site`.

## Credits

- JetBrains Mono, SIL Open Font License 1.1 (`assets/fonts/OFL.txt`).
- Icons drawn for Izar.

## Licence

See `LICENSE`. Theme by [Tortoiz Themes](https://tortoizthemes.com).
