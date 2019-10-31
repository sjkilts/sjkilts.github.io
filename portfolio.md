---
layout: sidebar
title: work
permalink: /work/
sidebar: A selection of personal and client work. Filter using the buttons below
---

<ul>
    {% for project in site.portfolio reversed %}
        {% if project.index == true %}
        {% else %}
        <li class="grid">
            {% if project.redirect %}
                {% include project-redirect.html %}
            {% else %}
                {% include project-thumbnail.html %}
            {% endif %}
        </li>
        {% endif %}
    {% endfor %}
</ul>