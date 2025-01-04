<span style="font-size: 200%">CPSC 416: Distributed Systems &nbsp;&nbsp;&nbsp;</span><span style="font-weight: 1">Syllabus - 2024/25 W 2</span>

- [Course Description](#course-description)
  - [Learning Goals](#learning-goals)
- [Logistics](#logistics)
  - [Staff](#staff)
  - [Office Hours](#office-hours)
  - [Communication](#communication)
  - [Textbook](#textbook)
  - [Go Resources](#go-resources)
  - [GitHub Submission Instructions](#github-submission-instructions)
- [Schedule](#schedule)
  - [Topics](#topics)
  - [Calendar   (Subject to Change Throughout the Term)](#calendar-subject-to-change-throughout-the-term)
  - [Labs](#labs)
  - [Quizzes](#quizzes)
  - [Grades](#grades)
- [UBC Values and Policies](#ubc-values-and-policies)
- [Academic Integrity](#academic-integrity)


# Course Description

[Leslie Lamport](https://en.wikipedia.org/wiki/Leslie_Lamport), a computer scientist who won the 2013 ACM Turing Award, gave the following definition of a distributed system.

> A distributed system is one in which the failure of a computer you didn't even know existed can render your own computer unusable.

Yet, distribution provides numerous benefits. A system becomes more fault tolerant if there are fewer points of failure and it has no centralized components. By extending the system with more physical nodes the system gains performance and becomes more scalable, capable of handling more load. Distribution can also improve latency, by improving geographic diversity, by placing resources closer to clients who use the system.

Achieving these benefits is not easy. As the quote above illustrates, distributed systems can fail in complex ways and these systems are more difficult to build, test, and understand than centralized systems.

This course will introduce you to a broad range of topics in distributed systems. The tentative topics are listed in the schedule below. For the most part this will be a lecture-style course. However, distributed system concepts are notoriously challenging to internalize without first-hand experience. The emphasis of this course, therefore, will be on building distributed system prototypes, small and large.

Course pre-requisites: CPSC 317 (networks) and CPSC 313 (computer hardware and operating systems).

## Learning Goals
The course will provide an opportunity for students to:
- understand key principles in designing and implementing distributed systems;
- reason about problems that involve distributed components;
- become familiar with important techniques for solving problems that arise in distributed contexts; and
- build distributed system prototypes using the Go programming language.

# Logistics

## Staff

|Name|Role|Contact Info|Office|
----|---|---|---
Mike Feeley | Instructor | feeley@cs.ubc.ca | ICCS 393
Arun Balamurali | TA
Mishaal Kazmi | TA
Junxuan Li | TA
Praveen Gupta | TA
Ryan Wang | TA

## Office Hours

Who|When|Where
---|----|----
Mike|Tu 2:30-3:30 & We 10:30-11:30|ICCS 393 (feeley@cs.ubc.ca)

> [!NOTE]
> Mike's office hours cancelled for Jan 15.

## Communication

[Piazza](https://piazza.com/class/m502jr8kaui37v) is the main place for formal, academic Q&A and discussion with each other and with the teaching staff.

Discord is a good place for informal, non-academic discussions with each other (without us there).

## Textbook
[*Distributed Systems*. Van Steen, Maarten, and Andrew S. Tanenbaum.  4th edition, distributed-systems.net, 2023.](https://www.distributed-systems.net/index.php/books/ds4/ds4-ebook/)

## Go Resources

In this course we will exclusively use the [Go programming language](http://golang.org/) for all course work. Learning a new programming language is an important skill. You will practice it in this course. For the most part I will expect that you learn this language on your own. We will be using Go version 1.23.4 (available at /cs/local/bin/go on ugrad servers). If you use a personal machine, make sure to [install this exact version](https://go.dev/dl/). Though, please note that all homework solutions will be tested on the ugrad server machines.

Go is a systems language originally introduced by Google. It is especially well suited to building distributed systems. Like with any language, the fastest way to become proficient at Go is to put in the time writing programs in Go. Here are some resources to get you started:

- [Go tutorial (start here)](https://tour.golang.org/welcome/1)
- [How to Write Go Code](https://golang.org/doc/code.html)
- [Effective Go](https://golang.org/doc/effective_go.html)
- [Go by Example](https://gobyexample.com/)
- The Go Programming Language [(Online)](https://go.dev/doc/) [(Book)](https://www.amazon.ca/Go-Programming-Language-Alan-Donovan/dp/0134190440/ref=sr_1_1?crid=KHUPD50TD9NM&dib=eyJ2IjoiMSJ9.hRBKL3GK8sS1T4rm8utVtmQ9jf6-jOdBvYBMIza19qJL9MzAKfW4s9UcPosjH_LxZEsG2X-4uafywnBNvR_wl4K5TCk7MAq_GsP0eeEEAIyfgtvO-BZ8WLC0d_DAwfZmy0dMFolKJzMAuWA_X4bm-hGIbL5LQ69sunti1SgjqzItPOmayGWkPaE5tCWFGGVqhOO5ceMjINxgdAr-eKuL7JU9O1PVMwqQ6FG4kGk83vCu5KPjjQ8bT8-0wBiooQ-rpj_7UDdq3vMyRjCBqxxif9V79ieGsl3ldOWz_gbnX34.YIo2Yf1eCuHjNLezTR9zMOlM9bzUpiyvpTzeYfI2dVY&dib_tag=se&keywords=the+go+programming+language&qid=1732748001&sprefix=the+go+programming+language%2Caps%2C137&sr=8-1)
- [Programming in Go](https://www.amazon.ca/Programming-Go-Creating-Applications-Developers-ebook/dp/B007Y6KDTG?ref_=ast_author_dp&dib=eyJ2IjoiMSJ9.G3m9RY9JoMavdJ9607FHj26b4fdS-vIju_T4ULV74_WB1jGQdnLvp28NJP1THx4jBqFgO0b_pu6jW3s6eLmC2MBs7A2LS-ed2PXAqUsLtpAa8yjlE2KiTOcjjSDwJ7BmrCOGhan02DvHq5d3ywHniCu_jOY-8NYcp_z4eyUBy9WV8PrV9JggDMNl_Zojblwf-2R1Ehz07RkolkQthVpREQ.Es5Yzyum1brqZ7YFEAYPOCPoF1XxD2_v-sp1eN0OSIM&dib_tag=AUTHOR)
- [More Go resources](https://go.dev/wiki/Learn)

Amanda Carbonan and Stewart Grant led an in-class Go tutorial in the 2017. Here is the recorded version: [Part 1](https://www.youtube.com/watch?v=L04p8SSmW-c&t=1s), and [Part 2](https://www.youtube.com/watch?v=xAU1_chlGBA&t=1786s).

After you install the correct version of Go, you can now install an IDE of your choice. For example, *VS Code* provides good support for Go.  Another popular option is *JetBrain's GoLand* (free to students; [register here](https://www.jetbrains.com/student/) with your UBC email).

## GitHub Submission Instructions

We will use an enterprise version of GitHub at UBC for all assignment/project code and writeup submissions.

Log into [github.students.cs.ubc.ca](https://github.students.cs.ubc.ca) and connect to the CPSC416-2024W-T2 organization, which contains two repositories: **shared** and **students**.  The **shared** repo contains lecture slides, sample code, and other similar information.  The **students** is a private repository where you and your lab partner will find lab starter code and where you will submit your solutions.  

Work inside your **students** lab repo as you would usually. 

> [!IMPORTANT] 
> **Push Commits Frequently.**
> 
> You are required to show incremental changes to your code to demonstrate your evolving work product.  
> 
> We will mark the commit that immediately precedes the deadline, but we will also examine this history to see how your work evolved.  
> 
> A single commit that contains a fully-formed solution will be flagged as suspicious and may result in a mark of zero for the lab and trigger an academic-integrity investigation.

# Schedule

## Topics
Unit | Topic / Slides ‡ | Textbook | Papers
-----|-------|---------|-------
0 | [Introduction](lectures/0_intro/0_intro.pdf)
1 | [RPC](lectures/1_rpc/1_rpc.pdf) | § 4.2, 8.3.2 | [Implementing RPC](lectures/1_rpc/papers/rpc.pdf)
|||| [Grapevine](lectures/1_rpc/papers/grapevine.pdf)
2 |  [Consistency](lectures/2_consistency/2_consistency.pdf) | § 7.1, 7.2.1, 7.2.3, 7.3 | [Linearizability](lectures/2_consistency/papers/linearizability.pdf)
|||| [Release Consistency](lectures/2_consistency/papers/release_consistency.pdf)
3 | [Time](lectures/3_time/3_time.pdf) | § 5.2, 5.3.1-5.3.3 | [Time, Clocks, and the Ordering of Events in a Distributed System](lectures/3_time/papers/time.pdf)
|||| [Why Logical Clocks are Easy](lectures/3_time/papers/clocks_easy.pdf)
4 | [Replication](lectures/4_replication/4_replication.pdf) | § 7.5.1, 7.5.5, 8.4 | [A Simple and Reliable Broadcast Protocol](lectures/4_replication/papers/kaashoek.pdf)
|||| [Lightweight Causal and Atomic Group Multicast](lectures/4_replication/papers/isis.pdf)
5 | Consensus | § 5.44, 8.1, 8.2| PAXOS: The Partime Parliament
|||| PAXOS Made Simple
|||| Raft
|||| FLP
|||| CAP
6 | Transactions | § 8.5
7 | Naming | § 6.1-6.3 | AFS
|||| Chord
8 | Example Systems | | ZooKeeper
|||| Google File System
|||| DynamoDB
9 | Byzantine Failure | § 8.2.5 | Byzantine Generals
|||| PBFT

*‡ Slides can change up to day of lecture; check git for the latest version.*

## Calendar &nbsp;&nbsp;<span style="font-size: medium; font-weight: 1; font-style: italic">(Subject to Change Throughout the Term)</span>

Date|Topic |Lab Released|Lab Due|Quiz
----|-----|------------|-------|----
J07 | Intro | Lab 0 
J09 | RPC
||
J14 | RPC 
J16 | RPC | Lab 1
||
J21 | Consistency
J23 | Consistency
||
J28 | Time
J30 | Time  | Lab 2 | Lab 1
||
F04 | Replication 
F06 | Replication ||| Quiz 1
||
F11 | Consensus | Lab 3 | Lab 2
F13 | Consensus 
||
*BREAK*
||
F25 | Consensus
F27 | Consensus | Lab 4a | Lab 3
||
M04 | Consensus 
M06 | Transactions 
||
M11 | Transactions | Lab 4b | Lab 4a
M13 | Naming ||| Quiz 2
||
M18 | Naming | Lab 4c | Lab 4b
M20 | Naming 
||
M25 | DynamoDB | Lab 5 | Lab 4c
M27 | Zookeeper 
||
A01 | Google File System
A03 | Byzantine Failure || Lab 5
||
A08 | Bysantine Failure 

## Labs

Lab | Topic | Released | Due | Weight
----|-------|----------|-----|-------
0 | [Go...](labs/00_go/README.md) | J07 | | 0%
1 | RPC | J16 | J30 | 16%
2 | Time | J30 | F11 | 14%
3 | Replication | F11 | F27 | 14%
4a | Raft: Leader Election | F27 | M11 | 14%
4b | Raft: Logging | M11 | M18 | 14%
4c | Raft: Persistence | M18 | M25 | 14%
5  | Relaiable Key-Value Store (Using Raft) | M25 | A03| 14%

## Quizzes

Quiz | Date | Topics
-----|------|-------
1    | F06-08  | RPC &ndash; Time
2    | M13-15  | Replication &ndash; Consensus

FaQuizzes are closed-book and 50-minutes in duration.  They are administered online through *Prairie Learn* in the Computer-Based Testing Facility (CBTF) at a self-scheduled time between the Thursday and Saturday dates listed above for each Quiz.

## Grades

Component | Percentage
----------|-----------
Labs | 30%
Quizzes | 40%
Final | 30%


# UBC Values and Policies

UBC provides resources to support student learning and to maintain healthy lifestyles but recognizes that sometimes crises arise and so
there are additional resources to access including those for survivors of sexual violence. UBC values respect for the person and ideas of
all members of the academic community. Harassment and discrimination are not tolerated nor is suppression of academic
freedom. UBC provides appropriate accommodation for students with disabilities and for religious and cultural observances. UBC
values academic honesty and students are expected to acknowledge the ideas generated by others and to uphold the highest academic
standards in all of their actions. Details of the policies and how to access support are available at [https://senate.ubc.ca/policies-
resources-support-student-success](https://senate.ubc.ca/policies-resources-support-student-success).

# Academic Integrity

Labs can be completed in pairs.  You must not share any portion of your assignent with anyone other than your lab parter.  If you change parters part way through a lab, you must contact course staff for permission to share any part of your previous work with your new partner.

You must not consult online or
other resources that include any portion of a solution to a lab.  You must not use a tutor for help with a lab. You must not use large language model, generative AI tools (e.g., ChatGPT or GitHub Copilot) to write lab code.  All work that you submit must be entirely original to you and/or your partner unless you explicitly 
indicate otherwise and must not, for example, contain any generated code.

Course material is provided for registered students only. You must not provide this material to
anyone else in any form.

Violation of these course rules constitutes academic misconduct. Other examples of misconduct
and a more detailed description can be found on the [department page on collaboration](https://my.cs.ubc.ca/docs/collaboration-plagiarism) and on the
[University Academic Integrity page](https://academicintegrity.ubc.ca/about-academic-integrity).
