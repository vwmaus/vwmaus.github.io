---
layout: page
permalink: /publications/
title: Publications
#description: Publications by categories in reversed chronological order
years_articles: [2022, 2021, 2020, 2019, 2018, 2017, 2016, 2015, 2009]
years_proceedings: [2017, 2016, 2015, 2011]
years_software: [2022, 2020, 2019, 2018]
years_other: [2021, 2016, 2014, 2013, 2011, 2009]
years_outreach: [2020, 2019, 2018, 2017]
nav: true
---

<div class="panel panel-default">

<ul class="nav nav-tabs" id="myTab" role="tablist">
  <li class="nav-item">
    <a class="nav-link active" id="home-tab" data-toggle="tab" href="#home" role="tab" aria-controls="home" aria-selected="true">Journal articles</a>
  </li>
  <li class="nav-item">
    <a class="nav-link" id="profile-tab" data-toggle="tab" href="#profile" role="tab" aria-controls="profile" aria-selected="false">Proceedings</a>
  </li>
  <li class="nav-item">
    <a class="nav-link" id="contact-tab" data-toggle="tab" href="#contact" role="tab" aria-controls="contact" aria-selected="false">Software and data</a>
  </li>
  <li class="nav-item">
    <a class="nav-link" id="other-tab" data-toggle="tab" href="#other" role="tab" aria-controls="other" aria-selected="false">Other publications</a>
  </li>
  <li class="nav-item">
    <a class="nav-link" id="outreach-tab" data-toggle="tab" href="#outreach" role="tab" aria-controls="outreach" aria-selected="false">Science outreach</a>
  </li>
</ul>

<div class="tab-content" id="myTabContent">
  <div class="tab-pane fade show active" id="home" role="tabpanel" aria-labelledby="home-tab">
    <div class="publications">
      {% for y in page.years_articles %}
        <!-- <h5 class="year">{{y}}</h5> -->
        {% bibliography -f papers -q @Article[year={{y}}]* %}
      {% endfor %}
    </div>
  </div>
  <div class="tab-pane fade" id="profile" role="tabpanel" aria-labelledby="profile-tab">
    <div class="publications">
      {% for y in page.years_proceedings %}
        <!-- <h5 class="year">{{y}}</h5> -->
        {% bibliography -f papers -q @InProceedings[year={{y}}]* %}
      {% endfor %}
    </div>
  </div>
  <div class="tab-pane fade" id="contact" role="tabpanel" aria-labelledby="contact-tab">
    <div class="publications">
      {% for y in page.years_software %}
        <!-- <h5 class="year">{{y}}</h5> -->
        {% bibliography -f papers -q @Software[year={{y}}]* %}
      {% endfor %}
    </div>
  </div>
  <div class="tab-pane fade" id="other" role="tabpanel" aria-labelledby="contact-tab">
    <div class="publications">
      {% for y in page.years_other %}
        <!-- <h5 class="year">{{y}}</h5> -->
        {% bibliography -f papers -q @PhdThesis[year={{y}}]* %}
        {% bibliography -f papers -q @Thesis[year={{y}}]* %}
        {% bibliography -f papers -q @TechReport[year={{y}}]* %}
        {% bibliography -f papers -q @Manual[year={{y}}]* %}
      {% endfor %}
    </div>
  </div>
  <div class="tab-pane fade" id="outreach" role="tabpanel" aria-labelledby="contact-tab">
    <div class="publications">
      {% for y in page.years_outreach %}
        <!-- <h5 class="year">{{y}}</h5> -->
        {% bibliography -f papers -q @Misc[year={{y}}]* %}
      {% endfor %}
    </div>
  </div>
</div>


