---
layout: default
title: Publicaciones
permalink: /publicaciones/
---

<h1>Mis Publicaciones</h1>

<ul>
  {% for paper in site.data.papers %}
    <li style="margin-bottom: 25px;">
      <strong style="font-size: 1.1em;">{{ paper.title }}</strong><br>
      
      <em>{{ paper.authors }}</em><br>
      
      <span style="color: #666;">{{ paper.venue }} - {{ paper.year }}</span><br>
      
      <div style="margin-top: 5px;">
        {% if paper.link %}
          <a href="{{ paper.link }}" target="_blank" style="text-decoration: none; border: 1px solid #ccc; padding: 2px 8px; border-radius: 4px; font-size: 0.9em; margin-right: 5px;">
            📄 Ver en Web
          </a>
        {% endif %}

        {% if paper.pdf %}
          <a href="{{ paper.pdf | relative_url }}" target="_blank" style="text-decoration: none; border: 1px solid #ccc; padding: 2px 8px; border-radius: 4px; font-size: 0.9em;">
            ⬇️ Descargar PDF
          </a>
        {% endif %}
      </div>
    </li>
  {% endfor %}
</ul>
