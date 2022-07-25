---
layout: default
img: hacker.png
caption: You will act as a web3 hacker in this assignment
title: Homework 2 - Vulnerability Exploitation
active_tab: homework
release_date: 2022-09-19
due_date: 2022-10-04 23:59:00EDT
materials:
submission_link: 
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




Homework 2: Exploiting Vulnerabilities [100 points]
=============================================================

In this assignment you will act as a hacker to exploit vulnerabilities in smart contracts. 

#### Learning Goals:
In this assignment you will learn..
1. Classes of vulnerabilities and how to exploit them
2. Refine your skills for spotting vulnerabilities in the wild
3. Increased familiarity with interacting with deployed smart contracts

<br>

## Instructions
For each of the following deployed course smart contracts, there is a `winner` mapping. 
To get points for that contract: 
1. Study the contract manually
2. Find the vulnerability
3. Exploit the vulnerability and add yourself to the `winner` data structure. 
4. Check that you are indeed a winner by inspecting the `winner` data structure.
5. Record the series of calls you made for the exploit.

Adding yourself to the winner mapping simulates an escalation of privileges or transfer of funds in a real world smart contract.

**Contracts to exploit:**
TBD

<br>
### What to submit
For this assignment, submit a text file or pdf with the calls you made to exploit each vulnerability. 
Grading will also be based on who is in the winner mapping at the time this assignment is due. 


