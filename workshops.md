---
layout: default
title:  "Workshops"
stuff:
   -
    date: 2017-07-24
    title: No workshops in week 1 
    show: 1
   -
    date: 2017-07-31
    title: Review of fundamentals (KNN, evaluation); getting started in python/numpy
    worksheet:
      - 2a_classification-KNN.ipynb
      - 2b_performance_evaluation.ipynb
      - 2a_classification-KNN_answers.ipynb
      - 2b_performance_evaluation_answers.ipynb
      - spambase.data
    show: 1
   -
    date: 2017-08-7
    title: Linear and Polynomial Regression; Regularization
    worksheet:
      - 3a_linear_regression.ipynb
      - 3b_polynomial_regression.ipynb
    show: 1
---
## Workshops

Workshop exercises are shown below, and will be updated to contain the materials for each week's classes. Note that workshops begin in week 2.  
<p>

<table class="display">
<colgroup>
<col width="15%" />
<col width="30%" />
<col width="55%" />
</colgroup>
<thead>
<tr>
    <td><b>Week beg.</b></td>
    <td><b>Topic</b></td>
    <td><b>Materials</b></td>
</tr>
</thead>
<tbody>
{% for lect in page.stuff %}
<tr>
  <td>
       {{ lect.date  | date: "%a %-d/%-m" }}
  </td>
  <td><i>{{ lect.title }}</i>
    {% for matter in lect.materials %}
    <br> {{ matter }}
    {% endfor %}
  </td>
  <td>
    {% if lect.show == 1 %}
        {% if lect.slides %}
            <b>Slides: </b>
            {% assign first = 1 %}
            {% for matter in lect.slides %}
                {% if first == 1 %}
                    {% assign first = 0 %}
                {% else %}
                    <br> &nbsp;
                {% endif %}
                <a href="slides/{{ matter }}">{{ matter }}</a>
            {% endfor %}
            <br>
        {% endif %}
        {% if lect.worksheet %}
            <b>Worksheet: </b>
            {% assign first = 1 %}
            {% for matter in lect.worksheet %}
                {% if first == 1 %}
                    {% assign first = 0 %}
                {% else %}
                    <br> &nbsp;
                {% endif %}
                <a href="worksheets/{{ matter }}">{{ matter }}</a>
            {% endfor %}
            <br>
        {% endif %}
        {% if lect.reading %}
            <b>Reading: </b>
            {% assign first = 1 %}
            {% for matter in lect.reading %}
                {% if first == 1 %}
                    {% assign first = 0 %}
                {% else %}
                    <br> &nbsp;
                {% endif %}
                {{ matter }}
            {% endfor %}
            <br>
        {% endif %}
        {% if lect.notebook %}
            <b>Notebook: </b>
            {% assign first = 1 %}
            {% for matter in lect.notebook %}
                {% if first == 1 %}
                    {% assign first = 0 %}
                {% else %}
                    <br> &nbsp;
                {% endif %}
                <a href="notebooks/{{ matter }}">{{ matter }}</a>
            {% endfor %}
            <br>
        {% endif %}
    {% endif %}

     {% if lect.show == 2 %}
        {% if lect.reading %}
            <b>Reading: </b>
            {% assign first = 1 %}
            {% for matter in lect.reading %}
                {% if first == 1 %}
                    {% assign first = 0 %}
                {% else %}
                    <br> &nbsp;
                {% endif %}
                {{ matter }}
            {% endfor %}
            <br>
        {% endif %}
       {% endif %}

  </td>
</tr>
{% endfor %}
</tbody>
</table>

All materials Copyright 2017, The University of Melbourne, and should not be reproduced or distributed without permission.
