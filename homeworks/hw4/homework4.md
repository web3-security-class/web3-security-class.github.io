---
layout: default
img: manticore.png
img_link: https://github.com/trailofbits/manticore
caption: The Manticore Logo
title: HW4 - Symbolic Execution with Manticore
active_tab: homework
release_date: 2022-10-12
due_date: 2022-10-18 23:59:00EDT

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




Homework 4: Symbolic Execution with Manticore [100 points]
=============================================================

#### Learning Goals:
Gain an...
1. Ability to run and configurate a real symbolic execution engine to find bugs in smart contracts.
2. Understanding of the limitations of Manticore and an understanding of the limitations of symbolic execution.
3. Understanding of the benefits and utility of a symbolic execution tool.
<br>

#### Suggested Readings
1. [Manticore: A User-Friendly Symbolic Execution Framework for Binaries and Smart Contracts](https://arxiv.org/pdf/1907.03890.pdf)
2. [Automated Whitebox Fuzz Testing](https://patricegodefroid.github.io/public_psfiles/ndss2008.pdf)

<br>
<br>

## Instructions
For each of the deployed course smart contracts, attempt to find the vulnerability by running Manticore. 
Use your knowledge of the vulnerabilities from the previous homeworks.
If Manticore can't find the bug out of the box, don't give up! Attempt to modify the configuration, or even transform the source of the smart contract.

For each of the contracts, report the following:
1. Did Manticore find the bug? Y/N
    - If Yes:
        -  what was the time taken?
        -  list the transaction trace Manticore found to hit the bug. Was this the same way you manually exploited the bug in HW2? Was this the same trace Echidna found in HW3?
    - If No, why not? Is this a limitation of the Manticore tool or a fundamental limitation of randomized testing? 

2. List any modifications you made to the config file or source, and report the effect.

<br>
### What to Submit 
1. PDF or text file with the report detailed above.
2. Answer the following short answer questions:  (Only 2-3 sentence response for each)
    - What are the advantages of symbolic execution compared to manual auditing and fuzzing?
    - What are the limitations of symbolic execution?
