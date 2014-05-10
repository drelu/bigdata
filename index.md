---
layout: page
title: Überblick
tagline: 
---
{% include JB/setup %}


## Inhalte

Die Menge an Daten, die Unternehmen anfallen und verarbeitet werden müssen steigen ständig ([McKinsey Big Data
Report](http://www.mckinsey.com/insights/mgi/research/technology_and_innovation/big_data_the_next_frontier_for_innovation)). Mit Big Data bezeichnet man
üblicherweise Daten, die mit herkömmlichen Mittel nicht oder nur schwer verarbeitet sind. Beispiele dafür sind: (i) klassische Unternehmensdaten (z.B.
Kundendaten, Transaktionen), (ii) machinen-generierte Daten, wie z.B. Sensodaten, Web Service/Maschinen Logdateien,  und (iii) Social Media Daten.

Dieses Modul hat das Ziel dem Studierenden einen Überblick über das Themengebiet daten-intensive Anwendungen 
zu vermitteln. Ziel ist es sowohl  betriebswirtschaftliches Verständnis von daten-basierten Business-
Modellen und Produkten, als auch technisches Verständnis von large-scale Systemen und Infrastrukturfür Big 
Data, aufzubauen. Die Studierenden vertiefen ihre Informatik-Kenntnisse praxisorientiert und wird vertraut 
gemacht mit Methoden, Techniken, Verfahren, Werkzeugen und Infrastrukturen für die Verarbeitung und Analyzse von (großen) Daten.

Im Rahmen dieses Kurses wird von jedem studierenden ein Thema als Studienarbeit vertieft bearbeiten. Des Weiteren werden 
mehrere praktische Übungen unter Nutzung der Cloud Dienste von [Amazon Web Services](http://aws.amazon.com) durchgeführt. 
Vielen Dank gilt dabei der Firma Amazon, welche diesen Kurs im Rahmen ihres Education Programmes unterstützt.


## Aktuelle Informationen


<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>


## Themen

1. Einführung: Big Data und seine Anwendungen in der Wirtschaft und Wissenschaft (1.1-1.7)
1. Open Data and Government (1.8-1.12)
1. MapReduce und Hadoop: HDFS und Hadoop MapReduce Framework (3.1-3.6)
1. MapReduce Patterns und Applikationen (3.41-3.43)
1. Big Table und HBase (3.3, 3.4, 3.39, 3.40)
1. Hive, Pig und HCatalog (3.7-3.10)
1. Hadoop Ecosystem: Distributionen und Tools (3.36, 3.37, 3.38)
1. Hadoop 2.0: Yarn (3.4, 3.5)
1. In-Memory Databases (3.20)
1. Analytical Databases: Greenplum (3.31, 3.35)
1. Stream Processing (Twitter Storm, Infosphere Streams) (3.24-3.26, 3.45)
1. CAP Theorem and Eventual Consistency (3.21-3.23)
1. Fehlertoleranz in Verteilten Systemen: Quorum Protokolle, Apache Zookeeper (3.19, 3.27)
1. Amazon und Big Data: Elastic Map Reduce, SimpleDB, DynamoDB (3.11, 3.16, 3.21)
1. Google Infrastruktur: Pregel und Dremel (3.18, 3.30, 3.44)
1. Google Filesystem Evolution: GFS, Megastore und Spanner (3.2, 3.17, 3.29)
1. Google & Big Data: Google App Engine Map Reduce, Big Query, Prediction API (3.6, 3.18, 3.32, 3.33, 3.34)
1. Einführung Machine Learning (4.9, 4.10)
1. Machine Learning mit Apache Mahout (4.1,4.2)
1. Natural Language Processing (4.6, 4.7)
1. Datenvisualisierungen (5.1-5.5, 1.12)


## Material

Weiterführende Materialien zur Veranstaltung finden Sie hier:

* [Vorlesung](http://fara.cs.uni-potsdam.de/~luckow/ws2012/)

* [Praktikum](./praktikum.html)



## Literatur

Bitte die folgenden Literaturempfehlungen als Startpunkt für eigene Recherchen wählen.


### 1. Einführung, Motivation und Open Daten

1. Tony Hey, Stewart Tansley, Kristin Tolle (Editors), The Fourth Paradigm, <http://research.microsoft.com/en-us/collaboration/fourthparadigm/>, 2009
1. Stephen Wolfram: A New Kind of Science, <http://www.wolframscience.com/>, 2002
1. DJ Patil, Data Jujitsu, O'Reilly, <http://oreillynet.com/oreilly/data/radarreports/data-jujitsu.csp>, 2012
1. Mike Loukides, What is data science, <http://radar.oreilly.com/2010/06/what-is-data-science.html> O'Reilly, 2010
1. Alon Halevy, Peter Norvig, and Fernando Pereira, The Unreasonable Effectiveness of Data, <http://googleresearch.blogspot.de/2009/03/unreasonable-effectiveness-of-data.html>, 2009
1. IDC/EMC Digital Universe Study, <http://www.emc.com/leadership/programs/digital-universe.htm>, 2011
1. McKinsey Global Institute, Big data: The next frontier for innovation, competition, and productivity, <http://www.mckinsey.com/insights/mgi/research/technology_and_innovation/big_data_the_next_frontier_for_innovation>, 2011
1. München Open Data, <http://www.muenchen.de/opendata>
1. Berlin Open Data, <http://daten.berlin.de/>
1. New York Open Data, <http://www.nyc.gov/html/data/about.html>
1. Alex Howard, Data for Public Good, <http://strata.oreilly.com/2012/02/data-public-good.html>, O'Reilly, 2012
1. Jonathan Gray, Liliana Bounegru, Lucy Chambers (editors), The Data Journalism Handbook,  <http://datajournalismhandbook.org/>, 2012

### 2. Cloud Computing
1. Peter Mell and Tim Grance. The NIST Definition of Cloud Computing, <http://csrc.nist.gov/groups/SNS/cloud-computing/>
1. Michael Armbrust, Armando Fox, Rean Griffith, Anthony D. Joseph, Randy H. Katz, Andrew Konwinski, Gunho Lee, David A. Patterson, Ariel Rabkin, Ion Stoica, and Matei Zaharia. Above the clouds: A Berkeley View of Cloud Computing. Technical Report University of Berkley, 2009, <http://www.eecs.berkeley.edu/Pubs/TechRpts/2009/EECS-2009-28.pdf>
1. S. Jha, D. Katz, A. Luckow, A. Merzky, K. Stamou, Understanding Scientific Applications for Cloud Environments, submitted to book on Cloud Computing, <http://www.cct.lsu.edu/~sjha/select_publications/cloud_book_chapter.pdf>
1. Amazon Web Services, <http://aws.amazon.com>
1. Amazon Web Services Whitepaper, 2009, <http://awsmedia.s3.amazonaws.com/AWS_Overview_Whitepaper_120809.pdf>
1. Google App Engine. <http://code.google.com/appengine/>
1. Windows Azure. <http://www.microsoft.com/windowsazure/>
1. K. Keahey, I. Foster, T. Freeman, and X. Zhang. Virtual Workspaces: Achieving Quality of Service and Quality of Life in the Grid. Scientific Programming, 13(4):265–275, 2005.
1. Cloud Standards Wiki, <http://cloud-standards.org>
1. Amazon Security Whitepaper,  <http://awsmedia.s3.amazonaws.com/pdf/AWS_Security_Whitepaper.pdf>, 2009
1. Amazon Security Best Practices, 2010, <http://awsmedia.s3.amazonaws.com/Whitepaper_Security_Best_Practices_2010.pdf>
1. OAuth, <http://oauth.net/>
1. Cloud Computing Tutorial. <https://research.microsoft.com/en-us/projects/azure/sc09cc.ppsx>
1. Sriram Krishnan, Programming Windows Azure, O'Reilly, 2010.
1. Thorsten Claus, Daniel Kellmereit, Yasmin Narielvala, The Future of Cloud,
<http://thefutureofcloud.com/>


### 3. Big Data

1. Jeffrey Dean and Sanjay Ghemawat. MapReduce: Simplified Data Processing on Large Clusters. In OSDI’04: Proceedings of the 6th conference on Symposium on Operating Systems Design & Implementation, pages 137–150, Berkeley, CA, USA, 2004. USENIX  Association.
1. Sanjay Ghemawat, Howard Gobioff, and Shun-Tak Leung. The Google File System. SIGOPS Oper. Syst. Rev., 37(5):29–43, 2003.
1. Fay Chang, Jeffrey Dean, Sanjay Ghemawat, Wilson C. Hsieh, Deborah A. Wallach, Mike Burrows, Tushar Chandra, Andrew Fikes, and Robert E. Gruber. Bigtable: a distributed storage system for structured data. In OSDI ’06: Proceedings of the 7th USENIX Symposium on Operating Systems Design and Implementation, pages 15–15, Berkeley, CA, USA, 2006. USENIX Association
1. Tom White, Hadoop: The Definitive Guide, 3rd Edition, <http://shop.oreilly.com/product/0636920021773.do>
1. Hadoop: Open Source Implementation of MapReduce. <http://hadoop.apache.org/>
1. Hadoop File System. <http://hadoop.apache.org/common/docs/current/hdfs_design.html>
1. Hive Project: <http://hive.apache.org/>
1. Edward Capriolo, Dean Wampler and Jason Rutherglen, Programming Hive, O'Reilly Media, 2012
1. Pig Project, <http://pig.apache.org/>
1. Alan Gates, Programming Pig, 2011
1. Amazon Elastic MapReduce. <http://aws.amazon.com/elasticmapreduce/>
1. Hadoop on Azure. <https://www.hadooponazure.com/>
1. MapReduce: Patterns, Algorithms and Use Cases,  <http://highlyscalable.wordpress.com/2012/02/01/mapreduce-patterns/>
1. Apache HBase, <http://hadoop.apache.org/hbase/>
1. Apache Cassandra, <http://cassandra.apache.org/>
1. Amazon SimpleDB, <http://aws.amazon.com/simpledb/>
1. Jeffrey Dean et. al., Spanner: Google's Globally-Distributed Database, OSDI, 2012, <Spanner: Google's Globally-Distributed Database>
1. Sergey Melnik, Andrey Gubarev, Jing Jing Long, Geoffrey Romer, Shiva Shivakumar, Matt Tolton, Theo Vassilakis, Dremel: Interactive Analysis of Web-Scale Datasets, <http://research.google.com/pubs/pub36632.html>
1. Leslie Lamport, The Part-Time Parliament, <http://research.microsoft.com/en-us/um/people/lamport/pubs/lamport-paxos.pdf>
1. Hasso Plattner, Alexander Zeiler, In-Memory Data Management, Springer, 2011
1. Giuseppe DeCandia, Deniz Hastorun, Madan Jampani, Gunavardhan Kakulapati, Avinash Lakshman, Alex Pilchin, Swaminathan Sivasubramanian, Peter Vosshall and Werner Vogels. Dynamo: Amazon’s Highly Available Key-value Store, 2007, <http://s3.amazonaws.com/AllThingsDistributed/sosp/amazon-dynamo-sosp2007.pdf>
1. E. A. Brewer,  Towards robust distributed systems. <http://www.cs.berkeley.edu/~brewer/cs262b-2004/PODC-keynote.pdf> In Proceedings of the 19th Annual ACM Symposium on Principles of Distributed Computing (July 16-19, Portland, Oregon), 2000
1. Werner Vogels, Eventually Consistent - Revisited, <http://www.allthingsdistributed.com/2008/12/eventually_consistent.html>, 2008
1. Gedik, Bugra and Andrade, Henrique and Wu, Kun-Lung and Yu, Philip S. and Doo, Myungcheol, SPADE: The System S Declarative Stream Processing Engine, Proceedings of the 2008 ACM SIGMOD international conference on Management of data, 2008
1. IBM Infosphere Streams, <http://www-01.ibm.com/software/data/infosphere/streams/>
1. Twitter Storm, <http://storm-project.net/>
1. Apache Zookeeper, <http://zookeeper.apache.org/>
1. Cloudera, BranchReduce: Distributed Branch-and-Bound on YARN, <http://www.cloudera.com/resource/hadoop-summit-2012-branchreduce-distributed-branch-and-bound-on-yarn-presentation-slides/>
1. Jason Baker, Chris Bond, James C. Corbett, JJ Furman, Andrey Khorlin, James Larson,
Jean-Michel Leon, Yawei Li, Alexander Lloyd, Vadim Yushprakh, Megastore: Providing Scalable, Highly Available Storage for Interactive Services, 2011
1. Grzegorz Malewicz et.al., Pregel: a system for large-scale graph processing, <http://googleresearch.blogspot.de/2009/06/large-scale-graph-computing-at-google.html>, 2009
1. Joseph M. Hellerstein, Christopher Ré, Florian Schoppmann, Zhe Daisy Wang, Eugene Fratkin, Aleksander Gorajek, Kee Siong Ng, Caleb Welton, Xixuan Feng, Kun Li, Arun Kumar, The MADlib Analytics Library or MAD Skills, the SQL, Technical Report University of Berkley, <http://www.greenplum.com/sites/default/files/Madlib_Whitepaper.pdf>, 2012
1. Google App Engine Map Reduce, <http://code.google.com/p/appengine-mapreduce/>
1. Google Big Query, <https://developers.google.com/bigquery/>
1. Prediction API, <https://developers.google.com/prediction/>
1. Greenplum Database, <http://www.greenplum.com/products/greenplum-database>
1. Hortonworks, <http://www.hortonworks.com>
1. Cloudera, <http://www.cloudera.com>
1. MapR, <http://www.mapr.com>
1. Lars George, HBase: The Definitive Guide, O'Reilly, 2011
1. Lars George, HBase vs. BigTable Comparison, <http://www.larsgeorge.com/2009/11/hbase-vs-bigtable-comparison.html>, 2009
1. MapReduce Patterns, <http://highlyscalable.wordpress.com/2012/02/01/mapreduce-patterns/>
1. Lawrence Page and Sergey Brin and Rajeev Motwani and Terry Winograd, The PageRank Citation Ranking: Bringing Order to the Web, Stanford Technical Report, <http://ilpubs.stanford.edu:8090/422/>, 1999
1. M. Schatz, CloudBurst: Highly Sensitive Short Read Mapping with MapReduce, <http://sourceforge.net/apps/mediawiki/cloudburst-bio/index.php?title=CloudBurst>, 2009 
1. Apache Drill, <http://www.slideshare.net/jasonfrantz/drill-bay-area-hug-20120919/13>
1. Apache Flume, <http://flume.apache.org/>

### 4. Machine Learning
1. Apache Mahout, <http://mahout.apache.org>
1. Sean Owen, Robin Anil, Ted Dunning, and Ellen Friedman, Mahout in Action, Manning, 2011
1. Cloudera, Mahout, CDH3 and Recommendations, <http://www.cloudera.com/resource/hadoop-summit-2012-branchreduce-distributed-branch-and-bound-on-yarn-presentation-slides/>
1. Scikit Learn, <http://scikit-learn.org/>
1. Scikit Learn Tutorial, <http://www.youtube.com/watch?v=Zd5dfooZWG4&feature=player_embedded#!>
1. Jacob Perkins, Python Text Processing with NTLK 2.0 Cookbook, Packt Publishing, 2010
1. Steven Bird, Ewan Klein, and Edward Loper, Natural Language Processing with Python, O'Reilly, 2009
1. Greg Linden, Brent Smith, and Jeremy York, Amazon.com
Recommendations Item-to-Item Collaborative Filtering, IEEE Computer Society, 
2003
1. Toby Segaran, Programming Collective Intelligence, O'Reilly, 2007
1. Drew Conway, John Myles White, Machine Learning for Hackers, O'Reilly, 2012 
1. Test, Learn, Adapt: Developing Public Policy with Randomised Controlled Trials: <http://www.pacts.org.uk/docs/pdf-bank/TLA-1906126.pdf>
1. Jimmy Lin and Chris Dyer, Data-Intensive Text Processing with MapReduce, Morgan & Claypool Publishers, 2010, <http://mapreduce.cc/>

### 5. Visualisierungen
1. Robert Kabacoff, R in Action, Manning, 2011
1. Hadley Wickham, ggplot2 - Elegant Graphics for Data Analysis, 2009
1. D3: Data-driven Documents, <http://d3js.org/>
1. Jeff Hammerbach, Toby Segaran, Beautiful Data, O'Reilly, 2009
1. Julie Steele, Noah Iliinsky, Beautiful Visualizations, O'Reilly, 2010



# Acknowledgements

![Amazon Web Services](http://awsmedia.s3.amazonaws.com/AWS_Logo_PoweredBy_127px.png)