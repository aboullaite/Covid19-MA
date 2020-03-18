---
layout: main
css: ../
title: Data per city
---

{% assign csvData=site.data.times_series %}

<table>
    <caption>Time series of COVID-19 data in Morocco / التسلسل الزمني لبيانات فيروس كورونا في المغرب</caption>
    <thead>
    {% for column in csvData[0] %}
        <th>{{ column[0] }}</th>
    {% endfor %}
    </thead>
    <tbody>
    {% for row in csvData %}
        <tr>
        {% for cell in row %}
            <td>{{ cell[1] }}</td>
        {% endfor %}
        </tr>
    {% endfor %}
    </tbody>
</table>