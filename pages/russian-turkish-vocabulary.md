---
title: Russian
permalink: russian-turkish-vocabulary
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

        <table class="table table-bordered table-striped">
            <colgroup>
                <col class="col-xs-1">
                <col class="col-xs-2">
                <col class="col-xs-3">
                <col class="col-xs-1">
                <col class="col-xs-3">
                <col class="col-xs-1">
            </colgroup>

            <thead>
                <tr>
                    <th>No</th>
                    <th>English</th>
                    <th>Turkish</th>
                    <th>sound</th>
                    <th>Russian</th>
                    <th>sound</th>
                </tr>
            </thead>

            <tbody>
 {% assign satir = 10 %}
 {% assign sayfa = forloop.index0 | times: satir %}
            {% for word in site.data.russian-turkish-vocabulary.vocabulary limit:satir offset:sayfa %}
                <tr>
                <td> {{ sayfa | plus: forloop.index }} </td>
                <td> {{ word.en }} </td>
                <td> {{ word.tr }} </td>
                <td> <audio controls class="myaudio"> <source  src="{{ site.github.url }}/assets/sound/vocabulary/{{ word.tr-s }}.mp3" type="audio/mpeg"></audio> </td>
                <td> {{ word.ru }} </td>
                <td> <audio controls class="myaudio"> <source  src="{{ site.github.url }}/assets/sound/vocabulary/{{ word.ru }}.mp3" type="audio/mpeg"></audio> </td>
                </tr>
            {% endfor %}

            </tbody>
        </table>
        </div>
    
    </div>

{% endfor %}
</div>



