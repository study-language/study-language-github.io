---
title: Russian
permalink: russian-turkish-vocabulary-anki
---

<ul class="nav nav-pills" role="tablist">
{% for i in (1..2) %}
    <li role="presentation" class="{% if forloop.index0 == 0 %}active {% endif %}"><a href="#s{{ i }}" aria-controls="s{{ i }}" role="tab" data-toggle="tab">{{ i }}</a></li>
{% endfor %}
</ul>

<div style="margin-top:20px"></div>

<div class="tab-content">

{% for i in (1..2) %}

    <div role="tabpanel" class="tab-pane {% if forloop.index0 == 0 %}active {% endif %}" id="s{{ i }}">

        <div class="panel panel-default">

        
            {% assign satir = 20 %}
            {% assign sayfa = forloop.index0 | times: satir %}
            {% for word in site.data.russian-turkish-vocabulary.vocabulary limit:satir offset:sayfa %}
            
            {% assign words = word.word | split: ';' %}
            {{ words[0] }};{{ words[1] }};{{ words[2] }};{{ words[3] }};[sound:{{ words[4] }}.mp3];[sound:{{ words[5] }}.mp3];{{ words[6] }};{{ words[7] }} <br>
                
            {% endfor %}


        </div>
    
    </div>

{% endfor %}
</div>
