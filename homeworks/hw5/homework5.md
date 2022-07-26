---
layout: default
img: scribble.png
img_link: https://github.com/ConsenSys/scribble
caption: The Scribble Logo
title: HW5 - Annotations and Instrumentation with Scribble
active_tab: homework
release_date: 2022-10-19
due_date: 2022-10-25 23:59:00EDT

---

<!-- Check whether the assignment is ready to release -->
{% capture today %}{{'now' | date: '%s'}}{% endcapture %}
{% capture release_date %}{{page.release_date | date: '%s'}}{% endcapture %}
{% if release_date > today %} 
<div class="alert alert-danger">
Warning: this assignment is under construction.  Check with your instructor before you start working on this assignment.
</div>
{% endif %}
<!-- End of check whether the assignment is up to date -->


<!-- Check whether the assignment is up to date -->
{% capture this_year %}{{'now' | date: '%Y'}}{% endcapture %}
{% capture due_year %}{{page.due_date | date: '%Y'}}{% endcapture %}
{% if this_year != due_year %} 
<div class="alert alert-danger">
Warning: this assignment is out of date.  It may still need to be updated for this year's class.  Check with your instructor before you start working on this assignment.
</div>
{% endif %}
<!-- End of check whether the assignment is up to date -->


<div class="alert alert-info">
This assignment is due on {{ page.due_date | date: "%A, %B %-d, %Y" }} before {{ page.due_date | date: "%I:%M%p" }}. 
</div>


{% if page.materials %}
<div class="alert alert-info">
You can download the materials for this assignment here:
<ul>
{% for item in page.materials %}
<li><a href="{{item.url}}">{{ item.name }}</a></li>
{% endfor %}
</ul>
</div>
{% endif %}




Homework 5: Annotations and Instrumentation with Scribble [100 points]
=============================================================

#### Learning Goals:
Gain a...
1. Ability to run and configurate a real symbolic execution engine to find bugs in smart contracts.
2. Hands on experience with program instrumentation 
3. Understanding of the Scribble annotation language
4. Ability to create program transformations using the `solc-typed-ast` library
<br>

#### Suggested Readings
1. [Scribble Specification Language](https://docs.scribble.codes/language/introduction)
2. [Automated Whitebox Fuzz Testing](https://patricegodefroid.github.io/public_psfiles/ndss2008.pdf)

#### Useful Links
1. [solc-typed-ast Documentation](https://consensys.github.io/solc-typed-ast/modules.html)

## Instructions
TBD..
