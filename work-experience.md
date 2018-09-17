---
layout: default
title:  "Work Experience"
date:   2017-08-18 23:00:22 -0700

permalink: /work-experience
---

<div class="container" style="padding-left:0">
	<div class="row align-items-center">
		<div class="col-6">
			<h1>Work Experience</h1>
		</div>
		<div class="col-6">
			<img src="/assets/images/programmer.png" height="200" width="200" style="float:right"/>
		</div>
	</div>
</div>

### [Internships](#internships) and [teaching positions](#teaching):

I've been incredibly lucky to intern at some great companies as well as course assist for some of the core computer science courses at Stanford.

#### <a name="internships"></a> Internships


##### <a name="intuit"></a> [Intuit][intuit-url] - Summer 2018
This most recent summer I interned with Intuit's cybersecurity team in San Diego.  I learned a great deal
about offensive security, how a large company works to secure its products, and good practices in
writing safe code, among other things.

My project involved researching the use of [property graphs][propgraph-url] in static code analysis.
While most static code analyzers only detect vulnerabilities based on code syntax, property graphs
allow for the modeling of control and data flow as well, which enables a security auditer to ask
questions like "Are there any calls to `memcpy` where the `len` argument is *attacker controlled*
(data flow) and isn't *properly sanitized* (control flow)?"

To be a little more specific, I used [Joern][joern-url], which is an implementation of this
property-graph-for-vulnerability-finding idea written by [Dr. Fabian Yamaguchi][fabian-url].
Joern parses C/C++ codebases and outputs a Neo4j graph database to run Gremlin/Cypher queries on.
Using Joern, I was able to discover 5 new buffer overflow vulnerabilities in the OpenJPEG library
that I reported on GitHub. These aren't complicated or Spectre/Meltdown-level vulns, but finding
them using this new technology was a great proof of concept for my team to move forward with my
project after I left.

[intuit-url]: https://www.intuit.com
{:target="_blank"}


[propgraph-url]: https://neo4j.com/developer/graph-database/#property-graph
{:target="_blank"}


[joern-url]: http://mlsec.org/joern/
{:target="_blank"}


[fabian-url]: https://fabs.codeminers.org/
{:target="_blank"}
##### <a name="oracle"></a> [Oracle][oracle-url] - Summer 2017
This was my first "big tech company" experience, and I really enjoyed it!  I worked with the NLP group
on the [Intelligent Bots Cloud Service (IBCS)][ibcs-url], which is Oracle's venture into the chatbot space
for enterprises.  My teammates were brilliant, and I was exposed to some of the most pressing
problems in language processing, such as entity extraction, intent recognition, and multiword expression
identification. Some of my contributions to the Bots platform included:

* implementing trie-based matching for entity extraction
* building prototypes for automated dialogue based on past customer conversations
* constructing knowledge graphs that the bot can query for question-answering

Oracle Bots is a product that continues to grow and improve, so make sure to keep up
with its progress!

[oracle-url]: https://www.oracle.com/index.html
{:target="_blank"}

[ibcs-url]: https://www.oracle.com/solutions/mobile/bots.html
{:target="_blank"}

##### <a name="netquarry"></a> [NetQuarry][netquarry-url] - Summer 2016

[netquarry-url]: https://netquarry.com/
{:target="_blank"}

NetQuarry helps enterprises build and maintain web applications to run their businesses.  As
a software development intern, I got my hands wet in multiple areas of web development,
including

* using jQuery libraries such as Google's [libphonenumber][libphone-url] to make webpages reponsive
* building SQLServer tables to store customer data which could be mapped to C# objects
* styling webpages using the Bootstrap framework


Working at a smaller company, I really felt like I was contributing important pieces
to the product we were working on.  I learned a lot about working on a team, getting feedback
on ideas, and working at a fast pace to meet customer deadlines!

[libphone-url]: https://github.com/googlei18n/libphonenumber

##### <a name="csuf"></a> [Cal State Fullerton Computer Science Department][csuf-url] - Summer 2014
This was my first experience programming "in the real world".  I worked
in Cal State Fullerton's computer science department under the supervision of [Dr. Yun Tian][yun-url],
whose research interests include distributed computing and cloud security. At the time, Dr. Tian was interested in geospatial databases, so my role involved finding geospatial datasets (such as that of [Yelp's dataset challenge][yelp-url]), creating MySQL database schemas, and writing scripts to import the datasets into MySQL for
further analysis.

[yelp-url]: https://www.yelp.com/dataset/challenge
{:target="_blank"}

[yun-url]: http://tianyun.ecs.fullerton.edu/
{:target="_blank"}

[csuf-url]: https://www.fullerton.edu/ecs/cs/
{:target="_blank"}
<hr style="border-top: 3px double #8c8b8b">

#### <a name="teaching"></a> Teaching Experience 


##### <a name="cs106A"></a> [CS 106A][cs106A-url] - Programming Methodology (Winter 2018)
[cs106A-url]: http://cs106a.stanford.edu
{:target="_blank"}

Many of those who are familiar with Stanford's computer science department have at least
heard of the section leading program. In a nutshell, section leaders are undergraduates who serve as
teaching assistants for Stanford's introductory computer science courses (any class
prefixed by CS106). For those who are curious, you can find out more at [this link][sl-url]!

In particular, CS 106A is the very first computer science class for many Stanford students.  Taught
in Java, it details the basics of programming syntax and organization, data types and structures,
and object oriented programming.  One of our main responsibilities as section leaders is to
teach students good programming practices, including decomposition, clear commenting and 
variable names, and iterative testing.  Despite being an introductory course, I found myself
learning a lot as I section led this course, and I strongly urge any undergraduates to get
involved in the section leading program ASAP!

[sl-url]: https://cs198.stanford.edu/cs198/
{:target="_blank"}

##### <a name="cs106B"></a> [CS 106B][cs106B-url] - Programming Abstractions (Fall 2018)
[cs106B-url]: http://cs106b.stanford.edu
{:target="_blank"}

To be completed this coming fall!

##### <a name="cs110"></a> [CS 110][cs110-url] - Principles of Computer Systems (Fall 2017, Spring 2018)
[cs110-url]: http://cs110.stanford.edu
{:target="_blank"}

CS 110 doesn't fall under the umbrella of CS 106, so I wasn't technically a section
leader when I TA'd this class. That being said, a lot of my responsibilities paralleled
those of being a section leader: I held weekly office hours, ran a section every Friday
to go over practice problems or dive deeper into concepts, and graded exams and
assignments.  The main difference is that there are no interactive grading sessions
(for more on those see [here][ig-url]) after the 106 series.

Despite the similar responsibilities, TAing a higher level class feels a lot different
than section leading, but it's still a lot of fun!  The concepts in 110 are 
incredibly important (filesystems, multiprocessing/threading, and networking to name
a few), and I enjoy teaching and motivating these ideas for students to learn.

[ig-url]: https://cs198.stanford.edu/cs198/ProgramStructure.aspx
{:target="_blank"}












[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
