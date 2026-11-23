---
layout: default
title: Contact
description: "Contact João Paulo Almeida de Mendonça: emails, SIMaP postal address in Grenoble, and social/academic profiles."
---

<div class="grid-2">
  <div class="card">
    <h2>Email</h2>
    <ul>
      {% for e in site.data.contact.emails %}
      <li>{{ e.label }}: <a class="mail-link" href="mailto:{{ e.address }}">{{ e.address }}</a></li>
      {% endfor %}
    </ul>
    <p style="color: var(--color-muted); font-size: 0.9rem;">Please identify yourself in your first message.</p>
  </div>
  <div class="card">
    <h2>Postal address (work)</h2>
    <address>
      <strong>{{ site.data.contact.postal.name }}</strong><br>
      {% for line in site.data.contact.postal.lines %}
      {{ line }}<br>
      {% endfor %}
      {{ site.data.contact.postal.phone_label }}: {{ site.data.contact.postal.phone }}<br>
      <a href="{{ site.data.contact.postal.access_page }}">How to reach the lab (tram, access map)</a>
    </address>
  </div>
</div>

<h2>Profiles &amp; socials</h2>
<ul class="social-list">
  {% for s in site.data.socials %}
  <li>
    <a href="{{ s.url }}" target="_blank" rel="noopener">
      <svg viewBox="0 0 24 24" width="26" height="26" aria-hidden="true"><path fill="currentColor" d="{{ s.path }}"/></svg>
      <span><span class="s-name">{{ s.name }}</span><span class="s-blurb">{{ s.blurb }}</span></span>
    </a>
  </li>
  {% endfor %}
</ul>

<p style="margin-top: 24px; color: var(--color-muted); font-size: 0.9rem;">
  Out of work hours, you can also find me as <em>Alastus</em> on Steam and Roll20.
</p>
