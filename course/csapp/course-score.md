---
title: csapp course
layout: defaultCourse
---

<h1>course scores</h1>

<ul>
    <li>
      
        {{ "学号" }} 
        &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;
        {{ "考勤" }}
      
    </li>
  {% for student in site.data.csapp-mark %}
    <li>
         {{ student.stuid }}
        &emsp; &emsp;
       
        {{ student.mark_question}}
    </li>
  {% endfor %}
</ul>

<style>
 .menu { text-align: center; }
 .menu ul { display:inline-table; }
 .menu li { display:inline; }
</style>