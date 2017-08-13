---
title: Russian
permalink: russian-turkish-vocabulary
---

<div class="panel panel-default">

<table class="table table-bordered table-striped">
    <colgroup>
        <col class="col-xs-3">
        <col class="col-xs-3">
        <col class="col-xs-1">
        <col class="col-xs-3">
        <col class="col-xs-1">
    </colgroup>

    <thead>
        <tr>
            <th>English</th>
            <th>Turkish</th>
            <th>sound</th>
            <th>Russian</th>
            <th>sound</th>
        </tr>
    </thead>
    
    <tbody>
    
    {% for word in site.data.russian-turkish-vocabulary.vocabulary %}
        <tr>
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
