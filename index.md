---
layout: index
---

#### Overview

The goal of this class is two-fold. First, to introduce you to core database concepts (e.g., data modeling, logical design, SQL) so that you too can build a billion dollar application. Second, to teach enough about database engine internals (e.g., physical database design, query optimization, transaction processing) so you have a good sense of why queries may be running slowly/incorrectly.  We will also discuss their relevance to systems used in industry.

<!--**Advanced Assignments**  There will several [optional extra-credit assignments](https://github.com/w4111/advanced) that will dive deeper into concepts introduced in class.   Some of them will involve extending a simple Python-based database engine with additional functionality!  They are labeled `AA#` in the schedule.  There is no obligation to do these, but they are available if you want to do then in addition to, or in lieu of the normal assignments.-->

<!--
<center><span style="padding: 2em; font-size: 20pt">Please do not ask me about the waitlist</span></center>
-->


<!--
#### Automated Exercises/resources

Developed for W4111

* [Transaction scheduling](https://w4111.github.io/concurrency.html)
* [Join optimization problem generator](https://w4111.github.io/join.html)
* Want more functional dependencies?  How about 100!  [Functional Dependency Problem Generator](./fd)

Developed by others:

* An [external Relation Algebra calculator](http://dbis-uibk.github.io/relax/calc.htm#) that might help you write and understand relational algebra.
* Here is a [link to another DB course's database recovery simulator](https://mwhittaker.github.io/aries/) (ARIES protocol).  It is more in depth than what we discussed in class, but is nice if you are interested in the details.
-->

#### Announcements

* 4/24
  * Added [extra credit assignment](https://github.com/w4111/w4111.github.io/wiki)
  * added extra credit assignment on Gradescope.  Named "Extra Credit Drawing"
* 4/22: links to practice problems for...
  * [Join ordering and access methods](./join.html)
  * [FDs](./fd.html)
  * [Schedules](./concurrency.html)
* 4/2
  * Updated lecture 7 to clarify conditions when checking BCNF, as well as additional examples
    of BCNF decomposition.
* 3/4
  * Updated lecture 5 with group-by examples and midterm logistics.
* 3/2
  * HW2 won't accept late submission after 3/5 10:00 AM EST because we will release solution.  

* 2/28
  * Updated lecture 4 to include full example of "Students that reserved all books"
  * Updated lecture 5 with full example of INTERSECT
* 2/25
  * Updated lecture 3 slide 82 so it say "Alternatively combine Courses and Instructs" rather than "Courses and Users"
  * [Practice exams](https://github.com/w4111/w4111.github.io/tree/main/files/reading)
  * [Link to class SQL demo notebook](https://github.com/w4111/w4111.github.io/tree/main/src/notebooks)
* [Sign up for Project 1 Part 1 staff meetings!](https://calendar.google.com/calendar/u/0/selfsched?sstoken=UUpOU05mUUpZYXk2fGRlZmF1bHR8YmE0YmE0M2MzNzkyYWZjOTcxYjRkMTBmNDNmNjA1NDc)  One meeting per team.
* Updated lecture 2 slides to clarify constraints over N-way relationships.
* [HW0](https://github.com/w4111/hw0) released.  

#### Schedule

<table class="table table-striped schedule">
  <thead>
  <tr>
    <!--<th class="idx"></th>-->
    <th class="date" style="width: 5em; max-width: 5em;"> <p> <span>Date </span> </p> </th>
    <th style="min-width: 20%;"> <p> <span>Topic </span> </p> </th>
    <!--<th style="width: 15%"> <p> <span>Readings </span> </p> </th>-->
    <th style="width: 25%;"> <p> <span>Assigned</span> </p> </th>
    <th style="width: 25%;"> <p> <span>Due</span> </p> </th>
  </tr>
  </thead>
{% assign idx = 0 %}

{% for r in site.data.schedule %}
  {% assign idx = idx | plus: 1  %}
  <tr style="background-color: {{r.color}}; ">
    <!--<td class="idx">L{{idx}}</td>-->
    <td class="date">{{r.date}}</td>
    <td class="slug">
      {% if r.lshow == "1" %} <a href="{{r.link}}"> {% endif %}
        <b>{{r.slug}}</b>
      {% if r.lshow == "1" %} </a> {% endif %}
      {%if r.title %}: {{r.title}}{% endif %}
      {% if r.optional %}<br/>{{r.optional | safe}}{% endif%}
      
      {% if r.readings %}
        <br/>optional: Textbook {{r.readings | safe}}
      {% endif %}
      </td>
    <!--<td class="readings">{{r.readings | safe}}</td>-->
    <td>{% if 1 or r.ashow == "1" %} {{r.assigned | safe}} {% endif %}</td>
    <td>{% if 1 or r.dshow == "1" %} {{r.due | safe}} {% endif %}</td>
  </tr>
{% endfor %}
</table>


