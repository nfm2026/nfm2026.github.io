---
layout: default
title: Committees
---



## Organization
---

{% for group in site.data.committees %}
<h3 class="role-title">{{ group.role }}</h3>

<div class="committee-group">
  {% for member in group.members %}
    <div class="committee-member">
      {% if member.image %}
        <img src="{{ member.image }}" alt="{{ member.name }}" class="committee-photo">
      {% endif %}
      <p>
        {% if member.homepage %}
          <a href="{{ member.homepage }}"><strong>{{ member.name }}</strong></a>
        {% else %}
          <strong>{{ member.name }}</strong>
        {% endif %}
        <br>
        <span class="affiliation">{{ member.affiliation }}</span>
      </p>
    </div>
  {% endfor %}
</div>
{% endfor %}




<!-- ### Local Arrangements
- TBA

## Program Committee
- TBA -->
