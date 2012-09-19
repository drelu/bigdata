---
layout: page
title: Überblick
tagline: 
---
{% include JB/setup %}


## Inhalte

Dieses Modul hat das Ziel dem Studierenden einen Überblick über das Themengebiet daten-intensive Anwendungen 
zu vermitteln. Ziel ist es sowohl  betriebswirtschaftliches Verständnis von daten-basierten Business-
Modellen und Produkten, als auch technisches Verständnis von large-scale Systemen und Infrastruktur für Big 
Data, zu vermitteln. Die Studierenden vertiefen ihre betriebswirtschaftlichen und Informatik-Kenntnisse 
praxisorientiert im Umfeld Big Data. Sie werden vertraut gemacht mit Methoden, Techniken, Verfahren, 
Werkzeugen und Infrastrukturen für die Verarbeitung von großen Datenmengen.

Im Rahmen dieses Kurses werden Sie im Rahmen einer Studienarbeit ein Thema 
vertieft bearbeiten. Des Weiteren werden mehrere praktische Übungen unter 
Nutzung der Cloud Dienste von [Amazon Web Services](http://aws.amazon.com) durchgeführt. Vielen Dank gilt dabei
der Firma Amazon, welche diesen Kurs im Rahmen ihres Education Programmes
unterstützt.


## Aktuelle Informationen


<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>


## Themen

1. Einführung: Big Data und seine Anwendungen 
1. Daten-intensive Anwendungen in der Wissenschaft
1. Cloud-Technologie: Amazon Web Services (EC2, EBS, S3) 
1. Cloud-Technologie: Windows Azure 
1. Cloud-Technologie: Google Compute und App Engine 
1. Data-Intensive Computing mit MapReduce und Hadoop 
1. Verteilte Datenbanken und Key-Value Stores: Datenmodelle, Konsistenzmodelle, Performance, Skalierbarkeit, Technologien 
1. Amazon und Big Data: Elastic Map Reduce, DynamoDB
1. Google Infrastruktur: Dremel and Spanner
1. Google & Big Data: Google App Engine Map Reduce, Big Query, Prediction API
1. Fehlertoleranz in Verteilten Systemen: Quorum Protokolle, Apache Zookeeper
1. Sicherheit: Risiken, Datenschutz, Sicherheitsmaßnahmen, Protokolle (OpenID, OAuth)
1. Practical Machine Learning (Apache Mahout, Scikit-Learn)
1. Natural Language Processing
1. Datenvisualisierungen


## Literatur

Bitte die folgenden Literaturempfehlungen als Startpunkt für eigene Recherchen 
wählen.


### 1. Einführung und Motivation

1. Tony Hey, Stewart Tansley, Kristin Tolle (Editors), The Fourth Paradigm, <http://research.microsoft.com/en-us/collaboration/fourthparadigm/>, 2009
1. Stephen Wolfram: A New Kind of Science, <http://www.wolframscience.com/>, 2002
1. DJ Patil, Data Jujitsu, O'Reilly, <http://oreillynet.com/oreilly/data/radarreports/data-jujitsu.csp>, 2012
1. Mike Loukides, What is data science, <http://radar.oreilly.com/2010/06/what-is-data-science.html> O'Reilly, 2010
1. Alon Halevy, Peter Norvig, and Fernando Pereira, The Unreasonable Effectiveness of Data, <http://googleresearch.blogspot.de/2009/03/unreasonable-effectiveness-of-data.html>, 2009
1. IDC/EMC Digital Universe Study, <http://www.emc.com/leadership/programs/digital-universe.htm>, 2011
1. McKinsey Global Institute, Big data: The next frontier for innovation, competition, and productivity, <http://www.mckinsey.com/insights/mgi/research/technology_and_innovation/big_data_the_next_frontier_for_innovation>, 2011

### 2. Cloud Computing und Large Scale Infrastrukturen
1. Peter Mell and Tim Grance. The NIST Definition of Cloud Computing, <http://csrc.nist.gov/groups/SNS/cloud-computing/>
1. Michael Armbrust, Armando Fox, Rean Griffith, Anthony D. Joseph, Randy H. Katz, Andrew Konwinski, Gunho Lee, David A. Patterson, Ariel Rabkin, Ion Stoica, and Matei Zaharia. Above the clouds: A Berkeley View of Cloud Computing. Technical Report University of Berkley, 2009, <http://www.eecs.berkeley.edu/Pubs/TechRpts/2009/EECS-2009-28.pdf>
1. S. Jha, D. Katz, A. Luckow, A. Merzky, K. Stamou, Understanding Scientific Applications for Cloud Environments, submitted to book on Cloud Computing, <http://www.cct.lsu.edu/~sjha/select_publications/cloud_book_chapter.pdf>
1. R. Buyya, Chee Shin Yeo, Srikumar Venugopal. Market-Oriented Cloud Computing: Vision, Hype, and Reality for Delivering IT Services as Computing Utilities, HPCC 2008, <http://www.buyya.com/papers/hpcc2008_keynote_cloudcomputing.pdf>
1. W3C HTTP Protocol, <http://www.w3.org/Protocols/>
1. W3C Consortium. Web Services Architecture, <http://www.w3.org/TR/ws-arch/>
1. R. Fielding. Architectural Styles and the Design of Network-based Software Architectures. PhD thesis, University of California, Irvine, 2000, <http://www.ics.uci.edu/~fielding/pubs/dissertation/top.htm>
1. Amazon Web Services, <http://aws.amazon.com>
1. Amazon Web Services Whitepaper, 2009, <http://awsmedia.s3.amazonaws.com/AWS_Overview_Whitepaper_120809.pdf>
1. Google App Engine. <http://code.google.com/appengine/>
1. Windows Azure. <http://www.microsoft.com/windowsazure/>
1. Eucalyptus. <http://open.eucalyptus.com/>
1. Eucalyptus Walrus. <http://open.eucalyptus.com/wiki/EucalyptusStorage_v1.4> 
1. K. Keahey, I. Foster, T. Freeman, and X. Zhang. Virtual Workspaces: Achieving Quality of Service and Quality of Life in the Grid. Scientific Programming, 13(4):265–275, 2005.
1. Cloud Standards Wiki, <http://cloud-standards.org>
1. Giuseppe DeCandia, Deniz Hastorun, Madan Jampani, Gunavardhan Kakulapati, Avinash Lakshman, Alex Pilchin, Swaminathan Sivasubramanian, Peter Vosshall and Werner Vogels. Dynamo: Amazon’s Highly Available Key-value Store, 2007, <http://s3.amazonaws.com/AllThingsDistributed/sosp/amazon-dynamo-sosp2007.pdf>
1. Amazon Security Whitepaper,  <http://awsmedia.s3.amazonaws.com/pdf/AWS_Security_Whitepaper.pdf>, 2009
1. Amazon Security Best Practices, 2010, <http://awsmedia.s3.amazonaws.com/Whitepaper_Security_Best_Practices_2010.pdf>
1. OAuth, <http://oauth.net/>
1. Cloud Computing Tutorial. <https://research.microsoft.com/en-us/projects/azure/sc09cc.ppsx>
1. Sriram Krishnan, Programming Windows Azure, O'Reilly, 2010.
1. Leslie Lamport, The Part-Time Parliament, <http://research.microsoft.com/en-us/um/people/lamport/pubs/lamport-paxos.pdf>
1. Thorsten Claus, Daniel Kellmereit, Yasmin Narielvala, The Future of Cloud,
<http://thefutureofcloud.com/>
1. Jeffrey Dean et. al., Spanner: Google's Globally-Distributed Database, OSDI, 2012, <Spanner: Google's Globally-Distributed Database>
1. Sergey Melnik, Andrey Gubarev, Jing Jing Long, Geoffrey Romer, Shiva Shivakumar, Matt Tolton, Theo Vassilakis, Dremel: Interactive Analysis of Web-Scale Datasets, <http://research.google.com/pubs/pub36632.html>



### 3. Big Data und MapReduce

1. Jeffrey Dean and Sanjay Ghemawat. MapReduce: Simplified Data Processing on Large Clusters. In OSDI’04: Proceedings of the 6th conference on Symposium on Operating Systems Design & Implementation, pages 137–150, Berkeley, CA, USA, 2004. USENIX  Association.
1. Sanjay Ghemawat, Howard Gobioff, and Shun-Tak Leung. The Google File System. SIGOPS Oper. Syst. Rev., 37(5):29–43, 2003.
1. Fay Chang, Jeffrey Dean, Sanjay Ghemawat, Wilson C. Hsieh, Deborah A. Wallach, Mike Burrows, Tushar Chandra, Andrew Fikes, and Robert E. Gruber. Bigtable: a distributed storage system for structured data. In OSDI ’06: Proceedings of the 7th USENIX Symposium on Operating Systems Design and Implementation, pages 15–15, Berkeley, CA, USA, 2006. USENIX Association
1. Tom White, Hadoop: The Definitive Guide, 3rd Edition, <http://shop.oreilly.com/product/0636920021773.do>
1. Hadoop: Open Source Implementation of MapReduce. <http://hadoop.apache.org/>
1. Hadoop File System. <http://hadoop.apache.org/common/docs/current/hdfs_design.html>
1. Amazon Elastic MapReduce. <http://aws.amazon.com/elasticmapreduce/>
1. Hadoop on Azure. <https://www.hadooponazure.com/>
1. MapReduce: Patterns, Algorithms and Use Cases,  <http://highlyscalable.wordpress.com/2012/02/01/mapreduce-patterns/>
1. Apache HBase, <http://hadoop.apache.org/hbase/>
1. Apache Cassandra, <http://cassandra.apache.org/>
1. Amazon SimpleDB, <http://aws.amazon.com/simpledb/>


### 4. Machine Learning
1. Scikit Learn, <http://scikit-learn.org/>
1. Scikit Learn Tutorial, <http://www.youtube.com/watch?v=Zd5dfooZWG4&feature=player_embedded#!>
1. Jacob Perkins, Python Text Processing with NTLK 2.0 Cookbook, Packt Publishing, 2010
1. Greg Linden, Brent Smith, and Jeremy York, Amazon.com
Recommendations Item-to-Item Collaborative Filtering, IEEE Computer Society, 
2003

### 5. Visualisierungen
1. Robert Kabacoff, R in Action, Manning, 2011
1. Hadley Wickham, ggplot2 - Elegant Graphics for Data Analysis, 2009
1. D3: Data-driven Documents, <http://d3js.org/>
1. Jeff Hammerbach, Toby Segaran, Beautiful Data, O'Reilly, 2009
1. Julie Steele, Noah Iliinsky, Beautiful Visualizations, O'Reilly, 2010



# Acknowledgements

![Amazon Web Services](http://upload.wikimedia.org/wikipedia/de/thumb/1/1d/AmazonWebservices_Logo.svg/220px-AmazonWebservices_Logo.svg.png)