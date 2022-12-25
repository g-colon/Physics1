---
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults
layout: default
title: Lesson Schedule
---

<!-- <div style="width:max-content; background-color: pink;"> -->
<!-- <div> -->
<!-- <h2 style="text-align:center;margin-top: 1rem; font-size:1.5rem; font-weight:bold; color: #828282">{{page.title}} </h2> -->

<div class="home-h2"> {{page.title}} </div>
<div>
<table class="syllabus">
  {% for row in site.data.syllabus %}
    {% if forloop.first %}
    <tr>
      {% for pair in row %}
        <th>{{ pair[0] }}</th>
      {% endfor %}
    </tr>
    {% endif %}

    {% tablerow pair in row %}
      {{ pair[1] }}
    {% endtablerow %}
  {% endfor %}
</table>
</div> 

<div>
<!-- <p><a href="lessons/l01_introduction.html"> Attempting link 1 </a></p> -->
<!-- <p><a href="_lessons/introduction.html"> Attempting link 2 </a></p> -->
</div>
