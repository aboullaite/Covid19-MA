---
layout: main
css: ../../
title: Data per region
---

{% assign csvData=site.data.regions %}

<table>
    <caption>COVID-19 Data n Morocco by region / بيانات فيروس كورونا في المغرب حسب الجهة</caption>
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