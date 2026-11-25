---
# Your home page. Each item under `sections:` is one section, in order.
# Copy more from /blocks/, delete what you don't need, or add `hidden: true` to switch one off.
layout: home
title: LandNav NW
description: A land navigation school designed to empower people to rediscover the joy and freedom of self-reliant wayfinding.
sections:
  - type: hero
    variant: portrait
    badge: Land Navigation Instructor
    heading: |
      Find your way home
      with LandNav NW.
    text: I help individuals and groups rediscover the freedom and independence of self-reliant wilderness navigation.
    action:
      label: Let's explore!
      url: /contact/
    stats:
      - value: "18"
        label: Years map & compass instructor
      - value: "4"
        label: Years search & rescue volunteer
    image:
      src: /assets/img/hero/developer
      widths: [380, 560, 754]
      width: 754
      height: 764
      alt: Daniel in a grey hoodie, hood up
    chips:
      - image: /assets/img/hero/logo-angular.webp
        alt: Angular
        at: left
        size: m
      - image: /assets/img/hero/logo-python.webp
        alt: Python
        at: top
        size: s
      - image: /assets/img/hero/logo-node.webp
        alt: Node.js
        at: right
        size: l
  - type: services
    variant: intro
    tone: band
    eyebrow: Introduce
    heading: Hello! I'm Daniel Stephan
    lead: Every great design begins with an even better story
    text: |
      Since beginning my journey as a freelance designer nearly 8 years ago, I've done remote work for agencies, consulted for startups, and collaborated with talented people to create digital products for both business and consumer use. I'm quietly confident, naturally curious, and perpetually working on improving my chopstick dexterity.
    items:
      - title: Design
        text: Create digital products and unique ideas
        icon: pen
        count: 20 projects
        highlight: true
      - title: Front-End
        text: Bring them to life with super smooth code
        icon: code
        count: 40 projects
      - title: SEO
        text: Boost your business with SEO optimized sites
        icon: target
        count: 10 projects
  - type: logos
    variant: grid
    tone: band
    heading: Clients I have worked with
    hide_heading: true
    items:
      - { name: Northwind Labs, image: /assets/img/clients/northwind.svg, width: 133, height: 48 }
      - { name: Kiko, image: /assets/img/clients/kiko.svg, width: 100, height: 44 }
      - { name: Atlas Travel, image: /assets/img/clients/atlas.svg, width: 120, height: 48 }
      - { name: "Quill & Co", image: /assets/img/clients/quill.svg, width: 104, height: 48 }
      - { name: Orbit, image: /assets/img/clients/orbit.svg, width: 121, height: 48 }
      - { name: Pinecone Coffee, image: /assets/img/clients/pinecone.svg, width: 123, height: 48 }
      - { name: Halo Studio, image: /assets/img/clients/halo.svg, width: 95, height: 48 }
  - type: works
    variant: staggered
    tone: default
    heading: Latest Works
    note: Perfect solutions for digital experience
    limit: 3
    link:
      label: All projects
      url: /works/
    footnote: '\* Some projects aren''t public because of NDAs. If you''d like to see more, [contact me](/contact/).'
  - type: testimonials
    variant: tabs
    tone: band
    heading: Testimonials
    note: What clients say about me
    items:
      - quote: Daniel was a real pleasure to work with and we look forward to working with him again. He's definitely the kind of designer you can trust with a project from start to finish.
        name: Benjamin Bryant
        role: VP & Co-Founder
        company: Wiser
        company_url: https://wiser.example
        rating: 5
        avatar: { src: /assets/img/people/benjamin-73.webp, width: 73, height: 73 }
      - quote: He took a rough brief and turned it into a clear, fast site that our team can edit without calling anyone. Every deadline was met, and every question got a straight answer.
        name: Rasid Hossain
        role: Project Management
        company: Pensalab
        company_url: https://pensalab.example
        rating: 5
        avatar: { src: /assets/img/people/rasid-73.webp, width: 73, height: 73 }
      - quote: Daniel cares about the small details most people skip. Our pages load in a blink now, and customers keep telling us how easy the new site is to use.
        name: Logan Cee
        role: UI/UX Designer
        company: LoganCee
        company_url: https://logancee.example
        rating: 5
        avatar: { src: /assets/img/people/logan-73.webp, width: 73, height: 73 }
  - type: awards
    variant: list
    heading: Awards
    note: How to make my projects become valuable
    years:
      - year: "2017"
        items:
          - org: Awwwards
            award: Site of the Year
            project: Lewis
          - org: CSS Design Awards
            award: Honorable Mention
            project: Bauhaus
            url: https://bauhaus.example
          - org: Product Hunt Maker
            award: Gold in Digital Craft
            project: Biforde
      - year: "2016"
        items:
          - org: FWA
            award: Corporate Social Responsibility
            project: Arquito
          - org: Semplice
            award: Best Showcase
            project: Focus
---
