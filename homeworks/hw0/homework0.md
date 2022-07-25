---
layout: default
img: wallet.png
caption: Managing your precious ETH
title: Homework 0 - Mint a Course NFT
active_tab: homework
release_date: 2022-08-31
due_date: 2022-09-06 23:59:00EDT
materials:
submission_link: https://www.gradescope.com/
---

<!-- Check whether the assignment is ready to release -->
{% capture today %}{{'now' | date: '%s'}}{% endcapture %}
{% capture release_date %}{{page.release_date | date: '%s'}}{% endcapture %}
{% if release_date > today %} 
<div class="alert alert-danger">
Warning: this assignment is under construction. Check with your instructor before you start working on this assignment.
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


Homework 0: Mint a Course NFT [100 points]
=============================================================


In this assignment, you will learn to interact with a smart contract deployed on Ethereum's Rinkeby test network. 

<br>
#### Resources

1. [Ethereum Account Documentation](https://ethereum.org/en/developers/docs/accounts/)
2. [Ethereum Transaction Documentation](https://ethereum.org/en/developers/docs/transactions/)
3. [Ethereum Whitepaper](https://ethereum.org/669c9e2e2027310b6b3cdce6e1c52962/Ethereum_Whitepaper_-_Buterin_2014.pdf)

<br>
#### Background: Ethereum Accounts

Accounts are the portion of the EVM state which hold ether.

> "An Ethereum account is an entity with an ether (ETH) balance that can send transactions on Ethereum."

There are two types of accounts:
1. Externally Owned Accounts (EOAs) - This is the type of account you will create in this assignment. They only have the ability to send and receive transactions. 
2. Smart Contracts - Smart contracts are executable programs that run on the Ethereum blockchain. They are an account in that they hold a balance and can send and receive transactions. Smart contracts can define more complex functionality for transactions. For example, a smart contract can define an auction, but an EOA can only send transactions to interact with that auction.

Both externally owned accounts and smart contracts have the ability to interact with other smart contracts.

<br>
<br>

## Instructions


### 1. Setting up your Ethereum wallet

A wallet is a interface that allows you to interact with your Ethereum account.
More instructions upcoming..

{% comment %}

MORE INFO HERE ON HOT AND COLD ACCOUNTS and the TEST NETWORK

For this course, we suggest using MetaMask....

[More instructions here]

https://ethereum.org/en/wallets/find-wallet/

{% endcomment %}

<br>
<br>

### 2. Get some Test ETH!
{% comment %}

[instructions here]

{% endcomment %}

<br>
<br>


### 3. Send a transaction to mint a course NFT
Now that you have an account with some test ETH, and a wallet to manage your account, you are ready to "buy" a course enrollment NFT.
<br>
<br>


#### Background: Transactions
> "An Ethereum transaction refers to an action initiated by an externally-owned account"

Transactions change the state of the EVM. 
More on lifecycle of a transaction upcoming...




