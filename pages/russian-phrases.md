---
title: Russian
permalink: russian-phrases
---

<p class="text-right"><a class="btn btn-primary" href="{{ site.github.url }}/russian-phrases-test.html" role="button">Test</a></p>


<ul class="nav nav-pills" role="tablist">
{% for i in (1..5) %}
    <li role="presentation" class="{% if forloop.index0 == 0 %}active {% endif %}"><a href="#s{{ i }}" aria-controls="s{{ i }}" role="tab" data-toggle="tab">{{ i }}</a></li>
{% endfor %}
</ul>

<div style="margin-top:20px"></div>

<div class="tab-content">

{% for i in (1..25) %}

    <div role="tabpanel" class="tab-pane {% if forloop.index0 == 0 %}active {% endif %}" id="s{{ i }}">

        <div class="panel panel-default">

        <table class="table table-bordered table-striped">
            <colgroup>
                <col class="col-xs-1">
                <col class="col-xs-6">
                <col class="col-xs-5">
            </colgroup>

            <thead>
                <tr>
                    <th>No</th>
                    <th>English</th>
                    <th>Russian</th>
                </tr>
            </thead>

            <tbody>
 {% assign satir = 20 %}
 {% assign sayfa = forloop.index0 | times: satir %}
            {% for phrase in site.data.russian-turkish-phrases.phrases limit:satir offset:sayfa %}
            
            {% assign phrases = phrase.phrase | split: ';' %}
            
                <tr>
                <td> {{ sayfa | plus: forloop.index }} </td>
                <td> {{ phrases[0] }} </td>
                <td> {{ phrases[1] }} </td>
                </tr>
            {% endfor %}

            </tbody>
        </table>
        </div>
    
    </div>

{% endfor %}
</div>
