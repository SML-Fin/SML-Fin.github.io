---
layout: default
meta-description: "Seminar Series and Reading Group at Oxford"
---

# Seminar Series and Reading Group

Participants can join the [email list](https://groups.google.com/forum/#!forum/stanford-mlsys-seminars/join) to receive notifcations about events. 

Events have a hybrid format with participants onsite at the [Statistics Department](https://www.stats.ox.ac.uk/) and online throuh Zoom. 

Topics range from network analysis to portfolio selection to high-dimensional statistics and synthetic data generation. Please explore [projects](https://www.stats.ox.ac.uk/~cucuring/fin.htm) from our research group. 


{% for category in site.data.talks %}
# {{ category.type }}
<div class="talk-list">
  {% for talk in category.members %}
  <div class="talk list-group-item">
  <div class="talk-date">{{ talk.date }}</div>
  <div class="talk-presenter">{{ talk.speaker }}</div>
  {% if talk.title %}
  <div>
    {% if talk.recording %}
      <span><a class="talk-title-link" href="{{ talk.recording }}">{{ talk.title }} <i class="bi bi-box-arrow-up-right"></i></a></span>
    {% elsif talk.livestream %}
      <span><a class="talk-title-link" href="{{ talk.livestream }}">{{ talk.title }} <i class="bi bi-box-arrow-up-right"></i></a></span>
    {% else %}
      <span>{{ talk.title }}</span>
    {% endif %}
  </div>
  {% endif %}
  {% if talk.abstract %}
    <details>
    <summary>Abstract</summary>
    {{ talk.abstract }}
    
    {% if talk.bio %}
    <br><br>
    <strong>Bio: </strong> {{ talk.bio }}
    {% endif %}

    {% if talk.recording %}
      <br><br>
      <strong><a href="{{ talk.recording }}">Video Link</a></strong>
    {% elsif talk.livestream %}
      <br><br>
      <strong><a href="{{ talk.livestream }}">Livestream Link</a></strong>
    {% endif %}
    </details>
  {% endif %}
  </div>
  {% endfor %}
</div>
{% endfor %}

# About The Seminar

**Organizers:** Mihai Cucuringu 

You can reach us at mihai [dot] cucuringu [at] stats [dot] ox [dot] ac [dot] uk.

