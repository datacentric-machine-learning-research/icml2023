---
layout: page
title: Organizers
permalink: /organizers/
description: The people who donate their time to make the workshop happen. Each time the site is recompiled the order is reshuffled &#35;perpetualrevolution 😉.
nav: false
nav-order: 5
---

<div class="projects grid">

  {% assign sorted_contributors = site.contributors | sample:100 %}
  {% for contributor in sorted_contributors %}
  <div class="grid-item">
    {% if contributor.redirect %}
    <a href="{{ contributor.redirect }}" target="_blank">
    {% else %}
    <a href="{{ contributor.url | relative_url }}">
    {% endif %}
      <div class="card hoverable">
        {% if contributor.img %}
        <img src="{{ contributor.img | relative_url }}" alt="contributor thumbnail">
        {% endif %}
        <div class="card-body">
          <h3 class="card-title">{{ contributor.name }}</h3>
          <p class="card-title">{{ contributor.affiliation }}</p>
          <p class="card-text">{{ contributor.minibio }}</p>
          <br/>
          <div class="row ml-1 mr-1 p-0">
            {% if contributor.mail %}
            <div class="col-sm-2">
              <div class="icon" data-toggle="tooltip" title="Email">
                <a href="mailto:{{ contributor.mail | encode_email }}"><i class="fas fa-envelope"></i></a>
              </div>
            </div>
            {% endif %}
            {% if contributor.website %}
            <div class="col-sm-2">
              <div class="icon" data-toggle="tooltip" title="Website">
                <a href="{{ contributor.website }}" target="_blank"><i class="fas fa-globe"></i></a>
              </div>
            </div>
            {% endif %}
            {% if contributor.twitter %}
            <div class="col-sm-2">
              <div class="icon" data-toggle="tooltip" title="Twitter">
                <a href="{{ contributor.twitter }}" target="_blank"><i class="fab fa-twitter"></i></a>
              </div>
            </div>
            {% endif %}
            {% if contributor.linkedin %}
            <div class="col-sm-2">
              <div class="icon" data-toggle="tooltip" title="LinkedIn">
                <a href="{{ contributor.linkedin }}" target="_blank" title="LinkedIn"><i class="fab fa-linkedin"></i></a>
              </div>
            </div>
            {% endif %}
            {% if contributor.googlescholar %}
            <div class="col-sm-2">
              <div class="icon" data-toggle="tooltip" title="Google Scholar">
                <a href="{{ contributor.googlescholar }}" target="_blank" title="Google Scholar"><i class="ai ai-google-scholar"></i></a>
              </div>
            </div>
            {% endif %}
            {% if contributor.github %}
            <div class="col-sm-2">
              <div class="icon" data-toggle="tooltip" title="Code Repository">
                <a href="{{ contributor.github }}" target="_blank"><i class="fab fa-github gh-icon"></i></a>
              </div>
              {% if contributor.github_stars %}
              <span class="stars" data-toggle="tooltip" title="GitHub Stars">
                <i class="fas fa-star"></i>
                <span id="{{ contributor.github_stars }}-stars"></span>
              </span>
              {% endif %}
            </div>
            {% endif %}
          </div>
        </div>
      </div>
    </a>
  </div>
{% endfor %}

</div>
