---
layout: page
title: portfolio
permalink: /portfolio/
---
<div class="wrapper">
<b>Client Work</b>
    <div class="client-work">
        {% for project in site.portfolio %}

        {% if project.redirect %}
            <div class="project">
                <div class="thumbnail">
                    <a href="{{ project.redirect }}" target="_blank">
                        {% if project.img %}
                            <img class="thumbnail" src="{{ project.img }}"/>
                        {% else %}
                            <div class="thumbnail blankbox"></div>
                        {% endif %}    
                    <span>
                        <h1>{{ project.title }}</h1>
                        <br/>
                        <p>{{ project.description }}</p>
                    </span>
                    </a>
                </div>
            </div>
        
        {% elsif project.client %}

            <div class="project">
                <div class="thumbnail">
                    <a href="{{ site.baseurl }}{{ project.url }}">
                        {% if project.img %}
                            <img class="thumbnail" src="{{ project.img }}"/>
                        {% else %}
                            <div class="thumbnail blankbox"></div>
                        {% endif %}    
                    <span>
                        <h1>{{ project.title }}</h1>
                        <br/>
                        <p>{{ project.description }}</p>
                    </span>
                    </a>
                </div>
            </div>

        {% endif %}
        {% endfor %}
    </div> <!--/.client-work-->
</div> <!--/.wrapper-->

<div class="wrapper">

<b>Personal Projects</b>

    <div class="personal-work">

        {% for project in site.portfolio %}
        {% if project.client %}
        {% elsif project.redirect %}

            <div class="project">

                <div class="thumbnail">

                    <a href="{{ project.redirect }}" target="_blank">
                        {% if project.img %}
                            <img class="thumbnail" src="{{ project.img }}"/>
                        {% else %}
                            <div class="thumbnail blankbox"></div>
                        {% endif %}    
                    <span>
                        <h1>{{ project.title }}</h1>
                        <br/>
                        <p>{{ project.description }}</p>
                    </span>
                    </a>
                </div>
            </div>
        {% elsif project.projectName %}

            <div class="project">
                <div class="thumbnail">
                    <a href="{{ site.baseurl }}{{ project.url }}">
                        {% if project.img %}
                            <img class="thumbnail" src="{{ project.img }}"/>
                        {% else %}
                            <div class="thumbnail blankbox"></div>
                        {% endif %}    
                    <span>
                        <h1>{{ project.title }}</h1>
                        <br/>
                        <p>{{ project.description }}</p>
                    </span>
                    </a>
                </div>
            </div>

        {% endif %}
        {% endfor %}
    </div> <!--/.personal-work-->
</div> <!--/.wrapper-->

<div class="wrapper">
<b>Artwork</b>
<div class="art-work">

{% for project in site.portfolio %}


{% if project.client %}
{% elsif project.projectName %}
{% elsif project.redirect %}
<div class="project">
    <div class="thumbnail">
        <a href="{{ project.redirect }}" target="_blank">
        {% if project.img %}
        <img class="thumbnail" src="{{ project.img }}"/>
        {% else %}
        <div class="thumbnail blankbox"></div>
        {% endif %}    
        <span>
            <h1>{{ project.title }}</h1>
            <br/>
            <p>{{ project.description }}</p>
        </span>
        </a>
    </div>
</div>
{% else %}

<div class="project ">
    <div class="thumbnail">
        <a href="{{ site.baseurl }}{{ project.url }}">
        {% if project.img %}
        <img class="thumbnail" src="{{ project.img }}"/>
        {% else %}
        <div class="thumbnail blankbox"></div>
        {% endif %}    
        <span>
            <h1>{{ project.title }}</h1>
            <br/>
            <p>{{ project.description }}</p>
        </span>
        </a>
    </div>
</div>

{% endif %}

{% endfor %}
</div><!--/.art-work-->
</div><!--/.wrapper-->

<!-- {% for project in site.portfolio %}

{% if project.redirect %}
<div class="project">
    <div class="thumbnail">
        <a href="{{ project.redirect }}" target="_blank">
        {% if project.img %}
        <img class="thumbnail" src="{{ project.img }}"/>
        {% else %}
        <div class="thumbnail blankbox"></div>
        {% endif %}    
        <span>
            <h1>{{ project.title }}</h1>
            <br/>
            <p>{{ project.description }}</p>
        </span>
        </a>
    </div>
</div>
{% else %}

<div class="project ">
    <div class="thumbnail">
        <a href="{{ site.baseurl }}{{ project.url }}">
        {% if project.img %}
        <img class="thumbnail" src="{{ project.img }}"/>
        {% else %}
        <div class="thumbnail blankbox"></div>
        {% endif %}    
        <span>
            <h1>{{ project.title }}</h1>
            <br/>
            <p>{{ project.description }}</p>
        </span>
        </a>
    </div>
</div>

{% endif %}

{% endfor %} -->
