---
title: 공동체IT사회적협동조합 정관
layout: default
---

{% assign constitution = site.docs | where: "category", "constitution" %}
{% assign constitution = constitution | first %}

<h1>공동체IT사회적협동조합 문서</h1>

<section id="constitution">
  <h2>정관 <small>constitution 헌법</small></h2>
  <div class="card border-primary col-sm-6">
    <div class="card-body text-center">
      <h3 class="card-title">
        <a href="{{ constitution.url | relative_url }}">{{ constitution.title }}</a>
      </h3>
    </div>
  </div>
</section>

<section id="codes">
  <h2>규약 <small>codes 법률</small></h2>
  <div class="row">
    {% assign codes = site.docs | where: "category", "code" %}
    {% for code in codes  %}
    <div class="col-sm-4">
      <div class="card my-2 border-success">
        <div class="card-body text-center py-3">
          <h4 class="card-title">
            <a{% if forloop.first %} class="small"{% endif %} href="{{ code.url | relative_url }}">{{ code.title }}</a>
          </h4>
        </div>
      </div>
    </div>
    {% endfor %}
  </div>
</section>

<section id="plans">
  <h2>사업 계획 <small>plans</small></h2>
  <div class="row">
    {% assign plans = site.docs | where: "category", "plan" %}
    {% for plan in plans  %}
    <div class="col-sm-4">
      <div class="card my-2 border-warning">
        <div class="card-body text-center py-3">
          <h4 class="card-title"><a href="{{ plan.url | relative_url }}">{{ plan.title }}</a></h4>
        </div>
      </div>
    </div>
    {% endfor %}
  </div>
</section>

<section id="references">
  <h2>참고 자료 <small>references</small></h2>
  <div class="row">
    {% for reference in site.data.references %}
    <div class="col-sm-4">
      <div class="card my-2 border-info">
        <div class="card-body text-center py-3">
          <h4 class="card-title"><a href="{{ reference.url }}" target="_blank">{{ reference.title | newline_to_br }}</a></h4>
          {% if reference.source %}<p class="text-muted"><a href="{{ reference.source }}" target="_blank">출처</a></p>{% endif %}
        </div>
      </div>
    </div>
    {% endfor %}
  </div>
</section>
