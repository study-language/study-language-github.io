---
title: Russian
permalink: russian-turkish-vocabulary
---

<ul class="nav nav-pills" role="tablist">
    <li role="presentation" class="active"><a href="#s1" aria-controls="s1" role="tab" data-toggle="tab">1</a></li>
    <li role="presentation" class="active"><a href="#s2" aria-controls="s2" role="tab" data-toggle="tab">2</a></li>
</ul>

<div style="margin-top:20px"></div>

{% for i in (1..2) %}



<div class="tab-content">

    <div role="tabpanel" class="tab-pane active" id="s{{ i }}">

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
 {% assign sayfa = forloop.index0 | times: 10 %}
            {% for word in site.data.russian-turkish-vocabulary.vocabulary limit:10 offset:sayfa %}
                <tr>
                <td> {{ forloop.index }} </td>
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


</div>


{% endfor %}
