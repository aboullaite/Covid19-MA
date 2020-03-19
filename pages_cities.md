---
layout: main
css: ../../
title: Data per city
---

{% assign csvData=site.data.cities %}

<table>
    <caption>COVID-19 Data in Morocco by city / بيانات فيروس كورونا في المغرب حسب المدينة</caption>
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