---
layout: default
meta-description: "Seminar Series and Reading Group"
---

# Seminar Series and Reading Group

Participants can join the [email list](https://groups.google.com/forum/#!forum/stanford-mlsys-seminars/join) to receive notifcations. Events have a hybrid format where participants at the [Statistics Department](https://www.stats.ox.ac.uk/) connect to Zoom. 

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
    {% if talk.link %}
      <span><a class="talk-title-link" href="{{ talk.link }}">{{ talk.title }} <i class="bi bi-box-arrow-up-right"></i></a></span>
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
    <strong>Biography: </strong> {{ talk.bio }}
    {% endif %}

    {% if talk.recording %}
      <br><br>
      <strong><a href="{{ talk.recording}}">Recording</a></strong>
    {% endif %}
    </details>
  {% endif %}
  </div>
  {% endfor %}
</div>
{% endfor %}

# About The Seminar

**Organizers:** Mihai Cucuringu (mihai [dot] cucuringu [at] stats [dot] ox [dot] ac [dot] uk)

Website template from the [Stanford MLSys Seminar Series](https://mlsys.stanford.edu)