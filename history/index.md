---
layout: page
title: "History"
permalink: /history/
---

The NASA Formal Methods Symposium is an annual event organized by the NASA Formal Methods (NFM) Research Group, comprised of researchers spanning six NASA centers. The symposium originated from the earlier Langley Formal Methods Workshop series.

## NASA Formal Methods Symposia (NFM)

<ul>
{% for conf in site.data.history %}
  {% if conf.label contains "NASA Formal Methods Symposium" %}
    <li>
      <strong>
        {% if conf.homepage %}
          <a href="{{ conf.homepage }}">{{ conf.label }}</a>
        {% else %}
          {{ conf.label }}
        {% endif %}
      </strong><br>

      {{ conf.date }}, {{ conf.location }}
      {% if conf.organizer %} – organized by {{ conf.organizer }}{% endif %}<br>

      {% if conf.url %}
        Proceedings: <a href="{{ conf.url }}">{{ conf.proceedings }}</a>
      {% else %}
        Proceedings: {{ conf.proceedings }}
      {% endif %}

      {% if conf.notes %}
        <br><em>{{ conf.notes }}</em>
      {% endif %}
    </li>
  {% endif %}
{% endfor %}
</ul>

---

## NASA Langley Formal Methods Workshops (LFM)

<ul>
{% for conf in site.data.history %}
  {% if conf.label contains "NASA Langley Formal Methods Workshop" %}
    <li>
      <strong>{{ conf.label }}</strong><br>

      {{ conf.date }}, {{ conf.location }}<br>

      {% if conf.url %}
        Proceedings: <a href="{{ conf.url }}">{{ conf.proceedings }}</a>
      {% else %}
        Proceedings: {{ conf.proceedings }}
      {% endif %}
    </li>
  {% endif %}
{% endfor %}
</ul>
