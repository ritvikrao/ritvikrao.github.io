---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

{% if site.coming_soon.cv %}

Coming soon!

{% else %}

[Download CV (PDF)]({{ base_path }}/files/cv.pdf) · [Download one-page resume (PDF)]({{ base_path }}/files/resume.pdf)

<object data="{{ base_path }}/files/cv.pdf" type="application/pdf" width="100%" height="1000px">
  <p>Your browser can't display the PDF here. <a href="{{ base_path }}/files/cv.pdf">Open my CV</a> instead.</p>
</object>

{% endif %}
