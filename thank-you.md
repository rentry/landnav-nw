---
layout: page
title: Thank you
permalink: /thank-you/
description: Your message has been sent.
sitemap: false
noindex: true
sections:
  - type: page-header
    heading: Thanks, your message is on its way.
    text: I'll reply within two working days.
---
{% if site.izar.form.provider != 'web3forms' and site.izar.form.provider != 'formspree' %}{{ site.data.strings.demo_notice | default: 'This is the theme demo, so nothing was sent. Thanks for trying the form!' }}
{% endif %}
<a class="cmd" href="{{ '/' | relative_url }}">{{ site.data.strings.back_home | default: 'Back to the home page' }}</a>
