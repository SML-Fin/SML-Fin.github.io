---
layout: default
meta-description: "Seminar Series and Reading Group"
---

# Seminar Series 

Participants can join our <a href=mailto:smlfin-subscribe@maillist.ox.ac.uk?subject="smlfin mailing list">mailing list</a> to receive notifcations about the seminar series. 

Organizers plan events in a hybrid format allowing participants on-site at the [Oxford Statistics Department](https://www.stats.ox.ac.uk/) to connect with participants off-site through Zoom. 

The seminar series covers a wide range of topics at the intersection of machine learning and finance. Topics range from network analysis to portfolio selection to high-dimensional statistics and synthetic data generation. 

Please explore [projects](https://www.stats.ox.ac.uk/~cucuring/fin.htm) from our research group. 

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
    {% elsif talk.recording %}
      <span><a class="talk-title-link" href="{{ talk.recording }}">{{ talk.title }} <i class="bi bi-box-arrow-up-right"></i></a></span>
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
      <strong><a href="{{ talk.recording }}">Recording</a></strong>
    {% endif %}
    </details>
  {% endif %}
  </div>
  {% endfor %}
</div>
{% endfor %}

# About The Seminar

**Organizers:** [Mihai Cucuringu](https://www.stats.ox.ac.uk/~cucuring/) 

**Acknowledgements:**  Website template from the [Stanford MLSys Seminar Series](https://mlsys.stanford.edu)