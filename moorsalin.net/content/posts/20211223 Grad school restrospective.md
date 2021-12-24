---
title: "Grad school in review"
date: 2021-12-23T12:00:00-05:00
type: posts
tags: ['grad school']
---

Finally, after four long years I have completed my Masters program in computer science. What have I learned? Let us have a look:

## Courses I completed

* [CS 6262 Network Security](http://www.omscs.gatech.edu/cs-6262-network-security)
* [CS 6035 Introduction to Information Security](http://www.omscs.gatech.edu/cs-6035-introduction-to-information-security)
* [CS 6300 Software Development Process](http://www.omscs.gatech.edu/cs-6300-software-development-process)
* [CS 6250 Computer Networks](http://www.omscs.gatech.edu/cs-6250-computer-networks)
* [CS 7646 Machine Learning for Trading](http://www.omscs.gatech.edu/cs-7646-machine-learning-trading)
* [CS 6340 Software Analysis](http://www.omscs.gatech.edu/cs-6340-software-analysis)
* [CS 6601 Artificial Intelligence](http://www.omscs.gatech.edu/cs-6601-artificial-intelligence)
* [CS 6400 Database Systems Concepts and Design](http://omscs.gatech.edu/cs-6400-database-systems-concepts-and-design)
* [CS 6238 Secure Computer Systems](http://omscs.gatech.edu/cs-6238-secure-computer-systems)
* [CS 6515 Intro to Graduate Algorithms](http://www.omscs.gatech.edu/cs-8803-ga-graduate-algorithms)

I suppose I should give summaries of the above courses. More details will follow, here is what I can remember off the top of my head:

## CS 6262 Network Security

* Network traffic can be monitored for unfriendly communications
* Firewalls and packet filtering are major mitigations against malware profliferation
* Enforcing the most basic security measures can mitigate the majority of security risks, save state actors with considerable backing

## CS 6035 Introduction to Information Security

* Confidentiality, Integrity, Assurance
* Cryptography basics
* Web app exploits in how inputs are processed

## CS 6300 Software Development Process

* Developing software in groups takes a lot of planning
* In fact, most of software development is spent on planning, not so much coding
* It is important to make sure the plan delivers what the stakeholders want
* Version control is important

## CS 6250 Computer Networks

* Routers run the internet
* ISPs and similiar large organizations route to each other using BGP
* Networks need to find paths to each other in order to peer
* Router software runs at the kernel level or hardware level

## CS 7646 Machine Learning for Trading

* Most machine learning models are crap for trading stocks
* Stick to simple measures like linear regression, decision trees, and mean reversions for high volume equities in stocks
* Complex ML models may work on other equities like futures, swaps, or other products not widely available to the public

## CS 6340 Software Analysis

* Programs are parsed into abstract syntax **trees**
* Trees allow for all sorts of analysis from finding dead ends to redundant branches to comparison with other trees for similiarity
* Finding edge cases can be automated with tools such as randoop

## CS 6601 Artificial Intelligence

* Robots are whack
* Simple probabalistic machines can still go a long way (see bayes network)
* General AI is still a long way off
* Computers can beat players in video games but cannot write good poems.
* GPT-3 is more akin to a super fancy markov chain model

## CS 6400 Database Systems Concepts and Design

* 99% of business applications are a database application in one way or another
* Most web apps are database applications
* Everyone needs data and ways to store it

## CS 6238 Secure Computer Systems

* Intel and AMD chips run complex security systems outside the CPU to manage access to the hardware
* Intel management engine and TPM attempt to provide hardware security for the OS, but ae more of a hinderance for hobbyists
* There are techniques for detecting covert channels in networks

## CS 6515 Intro to Graduate Algorithms

* Dynamic programming is a very powerful technique to solve almost any problem
* Divide and conquer is a very powerful technique to solve almost any problem
* Expressing a problem in terms of graphs can be a good way of arriving at a solution to a problem
* NP problems can be extremely hard to solve
