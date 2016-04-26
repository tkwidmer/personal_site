---
layout: page
title: Speaking
permalink: '/pages/speaking.html'
---
<h1> Speaking </h1>

<div class="row">
  <div class="col-sm-8">
    <h3> Past Engagements </h3>

    <div class="panel-group" id="accordian" role="tablist" aria-multiselectable="true">
      {% for date in site.data.speaking.past %}
      <div class="panel panel-default">
        <div class="panel-heading" role="tab" id="heading{{ date[0] }}">
          <div class="panel-title">
            <a role="button" data-toggle="collapse" data-parent="#accordion" href="#collapse{{ date[0] }}" aria-expanded="true" aria-controls="collapse{{ date[0] }}">
              {{ date[0] }}
            </a>
          </div>
        </div>
        {% if forloop.first == true %}
          {% assign panelClass = 'in'%}
        {% else %}
          {% assign panelClass = '' %}
        {% endif %}
        <div id="collapse{{ date[0] }}" class="panel-collapse collapse {{panelClass}}" role="tabpanel" aria-labelledby="heading{{ date[0] }}">
          <div class="panel-body">
          <ul>
            {% for speaking in date[1] %}
              <li>
                <b>{{speaking.role}}.
                {% if speaking.link %}
                  <a href="{{speaking.link}}"> "{{speaking.title}}."</a>
                {% else %}
                  "{{speaking.title}}."
                {% endif %}
                </b>
                <br>
                {{speaking.location}}.
                {{speaking.date}}
                <br>
              </li>
            {% endfor %}
          </ul>
          </div>
        </div>
      </div>
      {% endfor %}
    </div>


  </div>
  <div class="col-sm-4">
    <img src="/images/teagan_speaking.jpg"/>
  </div>
</div>
