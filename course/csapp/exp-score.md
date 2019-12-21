---
title: csapp course
layout: defaultCourse
---

<h1>course scores</h1>

<ul>
    <li>
      
        {{ "学号" }} 
        &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;
        {{ "exp1" }}
        &emsp;&emsp;&emsp;&emsp;&emsp;
        {{ "exp2" }}
        &emsp;&emsp;&emsp;&emsp;&emsp;
        {{ "exp3" }}
      
    </li>
  {% for student in site.data.csapp-exp %}
    <li>
         {{ student.id }}
        &emsp; &emsp;&emsp; &emsp;
       
        {{ student.exp1}}
        &emsp; &emsp;&emsp; &emsp;
       
        {{ student.exp2}}
        &emsp; &emsp;&emsp; &emsp;
       
        {{ student.exp3}}
    </li>
  {% endfor %}
</ul>

<style>
 .menu { text-align: center; }
 .menu ul { display:inline-table; }
 .menu li { display:inline; }
</style>