---
layout: default
title: Team
permalink: /team/
css: /assets/css/team-member-card.css
order:       # Used to define an order of apparition
  - zappela
  - tournij
  - victorb
  - shaboua
  - erraywa
  - baupref
  - capronm
  - fromenl
  - jiangzh
  - laloums

share-title: DataLab Groupe - Team
share-description: Learn more about our team, at DataLab Groupe CASA.
# share-img: ""
---

# Team

<div class="team-container">
  {% for member in page.order %}
  {% for person in site.team_members %}
  {% if member == person.slug %}
    <div class="team-member-card">
      <img class="profile-picture" src="{{ person.image | absolute_url }}" alt="Photo de {{ person.name }}">
      <h3 class="team-member-card-name">
        {{ person.name }}
      </h3>
      <p class="team-member-card-designation">{{ person.designation }}</p>
      <div class="team-member-social-media">
        {% if person.github %}
          <a href="{{ person.github }}">
            <img class="team-member-card-social-media-img" src="{{ '/assets/img/github-logo.png' | absolute_url }}" alt="Logo GitHub" />
          </a>
        {% endif %}
        {% if person.linkedin %}
          <a href="{{ person.linkedin }}">
            <img class="team-member-card-social-media-img" src="{{ '/assets/img/linkedin-logo.png' | absolute_url }}" alt="Logo LinkedIn">
          </a>
        {% endif %}
      </div>
    </div>
  {% endif %}
  {% endfor %}
  {% endfor %}
  {% for person in site.team_members %}
  {% unless page.order contains person.slug %}
    <div class="team-member-card">
      <img class="profile-picture" src="{{ person.image | absolute_url }}" alt="Photo de {{ person.name }}">
      <h3 class="team-member-card-name">
        {{ person.name }}
      </h3>
      <p class="team-member-card-designation">{{ person.designation }}</p>
      <div class="team-member-social-media">
        {% if person.github %}
          <a href="{{ person.github }}">
            <img class="team-member-card-social-media-img" src="{{ '/assets/img/github-logo.png' | absolute_url }}" alt="Logo GitHub" />
          </a>
        {% endif %}
        {% if person.linkedin %}
          <a href="{{ person.linkedin }}">
            <img class="team-member-card-social-media-img" src="{{ '/assets/img/linkedin-logo.png' | absolute_url }}" alt="Logo LinkedIn">
          </a>
        {% endif %}
      </div>
    </div>
  {% endunless %}
  {% endfor %}
</div>