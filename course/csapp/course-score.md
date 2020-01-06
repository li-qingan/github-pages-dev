---
title: csapp course
layout: defaultCourse
---

<h1>csapp 问答及作业</h1>

<ul>
    <li>
      
        {{ "学号" }} 
        &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;
        {{ "问答" }}
        &emsp;&emsp;&emsp;
        {{ "作业1" }}
        &emsp;&emsp;&emsp;
        {{ "作业2" }}
        &emsp;&emsp;&emsp;
        {{ "作业3" }}
        &emsp;&emsp;&emsp;
        {{ "作业4" }}

      
    </li>
  {% for student in site.data.csapp-mark %}
    <li>
        {{ student.stuid }}
        &emsp;&emsp;&emsp;&emsp;
       
        {{ student.question }}
        &emsp; &emsp;&emsp;&emsp;&emsp;
       
        {{ student.assignment1 }}
        &emsp;&emsp;&emsp;&emsp;&emsp;

        {{ student.assignment2 }}
        &emsp;&emsp;&emsp;&emsp;&emsp;

        {{ student.assignment3 }}
        &emsp;&emsp;&emsp;&emsp;&emsp;

        {{ student.assignment4 }}

    </li>
  {% endfor %}
</ul>

<style>
 .menu { text-align: center; }
 .menu ul { display:inline-table; }
 .menu li { display:inline; }
</style>