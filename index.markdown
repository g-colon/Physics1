---
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults
layout: default
title: Lesson Schedule
---

<!-- <div style="width:max-content; background-color: pink;"> -->
<!-- <div> -->
<!-- <h2 style="text-align:center;margin-top: 1rem; font-size:1.5rem; font-weight:bold; color: #828282">{{page.title}} </h2> -->

<p style="padding-top:1em;"> <b> Course Description:</b> </p>
<p style="margin-left:2%; "> An introduction to the fundamental principles of physics with an emphasis in rigid-body mechanics.  This course focusses on the classical theory of motion as understood using Newton’s laws and the conservation principles of energy and momentum.
</p>
<hr class="cdes">


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

<div style="margin-bottom: 1rem">
&bull; Note: Some documents require that you sign in with your MMA account.
</div>
<div>
<!-- <p><a href="lessons/l01_introduction.html"> Attempting link 1 </a></p> -->
<!-- <p><a href="_lessons/introduction.html"> Attempting link 2 </a></p> -->
</div>
