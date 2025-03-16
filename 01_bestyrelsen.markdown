---
layout: page
title: Bestyrelsen
permalink: /bestyrelsen/
---

<div class="card-container">
  {% for person in site.data.persons %}
    {% include person_card.html name=person.name address=person.address role=person.role image=person.image %}
  {% endfor %}
</div>

<style>
.card-container {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
}

.card {
  box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);
  transition: 0.3s;
  width: 40%;
  margin: 10px;
}

.card:hover {
  box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2);
}

.container {
  padding: 2px 16px;
}

/* Add this media query */
@media (max-width: 600px) {
  .card {
    width: 100%;
  }
}
</style>