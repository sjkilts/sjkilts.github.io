---
layout: sidebar
title: portfolio
permalink: /portfolio/
sidebar: <!--this copy is basically taken straight from jessica hische's site. probably aught to change it up a little-->
    As a designer, I strive to create beautiful legible work with loads of personality and a high level of technical precision. To inquire about a new project or to license existing artwork, hmu
---
<ul>
    {% for project in site.portfolio %}
    <li>
        {% if project.redirect %}
            {% include project-redirect.html %}
        {% else %}
            {% include project-thumbnail.html %}
        {% endif %}
    </li>
    {% endfor %}
</ul>