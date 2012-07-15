---
layout: page
title: FWP Fach im Studiengang Wirtschaftsinformatik
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

    
## Aktuelle Informationen


<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>


## Themen

1. Einführung: Cloud Computing und seine Anwendungen (1, 2, 3, 4, 39, 53)
2. Grundlagen: Web- und Service-orientierte Architekturen (HTTP, Service-orientierte Architekturen, Web Services) (5, 6, 7)
3. Grundlagen: Virtualisierung (KVM, XEN) (8, 9, 10)
4. Cloud-Technologie: Amazon Web Services (EC2, EBS, S3) (11, 12)
5. On-Premise Cloud-Technologien: Eucalyptus, Nimbus und OpenNebula (16, 17, 18, 19)
6. Cloud-Technologie: Google App Engine (13, 40)
7. Cloud-Technologie: Windows Azure (14)
8. Cloud-Technologie: Salesforce: force.com (15)
9. Google Infrastructure: Chubby (51)
10. Google Infrastructure: Paxos (52)
11. Cloud Standards: OCCI, SNIA Cloud Data Management, OVF (20, 21, 22, 23)
12. Data-Intensive Computing mit MapReduce (Hadoop) (24, 25, 26, 27, 28)
13. Cloud Datenbanken (Datenmodelle, Konsistenzmodelle, Performance, Skalierbarkeit, Technologien (BigTable, HBase, Cassandra, SimpleDB)) (29, 30, 31, 32, 33)
14. Sicherheit (Risiken, Sicherheitsmaßnahmen, Protokolle (OpenID, OAuth), Technologien (Amazon VPC, Google Secure Data Connector)) (34, 35, 36, 37, 38)


## Literatur

1. Peter Mell and Tim Grance. The NIST Definition of Cloud Computing, <http://csrc.nist.gov/groups/SNS/cloud-computing/>
1. Michael Armbrust, Armando Fox, Rean Griffith, Anthony D. Joseph, Randy H. Katz, Andrew Konwinski, Gunho Lee, David A. Patterson, Ariel Rabkin, Ion Stoica, and Matei Zaharia. Above the clouds: A Berkeley View of Cloud Computing. Technical Report University of Berkley, 2009, <http://www.eecs.berkeley.edu/Pubs/TechRpts/2009/EECS-2009-28.pdf>
1. S. Jha, D. Katz, A. Luckow, A. Merzky, K. Stamou, Understanding Scientific Applications for Cloud Environments, submitted to book on Cloud Computing, <http://www.cct.lsu.edu/~sjha/select_publications/cloud_book_chapter.pdf>
1. R. Buyya, Chee Shin Yeo, Srikumar Venugopal. Market-Oriented Cloud Computing: Vision, Hype, and Reality for Delivering IT Services as Computing Utilities, HPCC 2008, <http://www.buyya.com/papers/hpcc2008_keynote_cloudcomputing.pdf>
1. W3C HTTP Protocol, <http://www.w3.org/Protocols/>
1. W3C Consortium. Web Services Architecture, <http://www.w3.org/TR/ws-arch/>
1. R. Fielding. Architectural Styles and the Design of Network-based Software Architectures. PhD thesis, University of California, Irvine, 2000, <http://www.ics.uci.edu/~fielding/pubs/dissertation/top.htm>
1. Amit Singh, An Introduction to Virtualization, <http://www.kernelthread.com/publications/virtualization/>
1. Linux KVM, http://www.linux-kvm.org/
1. Paul Barham et al. Xen and the Art of Virtualization, <http://www.cl.cam.ac.uk/research/srg/netos/papers/2003-xensosp.pdf>
1. Amazon Web Services, <http://aws.amazon.com>
1. Amazon Web Services Whitepaper, 2009, <http://awsmedia.s3.amazonaws.com/AWS_Overview_Whitepaper_120809.pdf>
1. Google App Engine. <http://code.google.com/appengine/>
1. Windows Azure. <http://www.microsoft.com/windowsazure/>
1. Salesforce: Force.com Developer Resources, <http://developer.force.com/>
1. Eucalyptus. <http://open.eucalyptus.com/>
1. Eucalyptus Walrus. <http://open.eucalyptus.com/wiki/EucalyptusStorage_v1.4> 
1. K. Keahey, I. Foster, T. Freeman, and X. Zhang. Virtual Workspaces: Achieving Quality of Service and Quality of Life in the Grid. Scientific Programming, 13(4):265–275, 2005.
1. OpenNebula - The Open Source Toolkit for Cloud Computing, <http://www.opennebula.org/>
1. Cloud Standards Wiki, <http://cloud-standards.org>
1. Open Cloud Computing Interface, <http://www.occi-wg.org/doku.php>
1. SNIA, Cloud Data Management Interface, <http://www.snia.org/tech_activities/publicreview/Cloud_Data_Management_Interface_Draft1.0.pdf>
1. Open Virtual Machine Format White Paper, <http://www.dmtf.org/standards/published_documents/DSP2017_1.0.0.pdf>
1. Jeffrey Dean and Sanjay Ghemawat. MapReduce: Simplified Data Processing on Large Clusters. In OSDI’04: Proceedings of the 6th conference on Symposium on Operating Systems Design & Implementation, pages 137–150, Berkeley, CA, USA, 2004. USENIX  Association.
1. Sanjay Ghemawat, Howard Gobioff, and Shun-Tak Leung. The Google File System. SIGOPS Oper. Syst. Rev., 37(5):29–43, 2003.
1. Hadoop: Open Source Implementation of MapReduce. <http://hadoop.apache.org/>
1. Hadoop File System. <http://hadoop.apache.org/common/docs/current/hdfs_design.html>
1. Amazon Elastic MapReduce. <http://aws.amazon.com/elasticmapreduce/>
1. Fay Chang, Jeffrey Dean, Sanjay Ghemawat, Wilson C. Hsieh, Deborah A. Wallach, Mike Burrows, Tushar Chandra, Andrew Fikes, and Robert E. Gruber. Bigtable: a distributed storage system for structured data. In OSDI ’06: Proceedings of the 7th USENIX Symposium on Operating Systems Design and Implementation, pages 15–15, Berkeley, CA, USA, 2006. USENIX Association
1. Giuseppe DeCandia, Deniz Hastorun, Madan Jampani, Gunavardhan Kakulapati, Avinash Lakshman, Alex Pilchin, Swaminathan Sivasubramanian, Peter Vosshall and Werner Vogels. Dynamo: Amazon’s Highly Available Key-value Store, 2007, <http://s3.amazonaws.com/AllThingsDistributed/sosp/amazon-dynamo-sosp2007.pdf>
1. Apache HBase, <http://hadoop.apache.org/hbase/>
1. Apache Cassandra, <http://cassandra.apache.org/>
1. Amazon SimpleDB, <http://aws.amazon.com/simpledb/>
1. Amazon Security Whitepaper, 2009, <http://awsmedia.s3.amazonaws.com/pdf/AWS_Security_Whitepaper.pdf>
1. Amazon Security Best Practices, 2010, <http://awsmedia.s3.amazonaws.com/Whitepaper_Security_Best_Practices_2010.pdf>
1. Google Secure Data Connector, <http://code.google.com/intl/de-DE/securedataconnector/docs/1.0/overview.html>
1. Amazon VPC, <http://aws.amazon.com/vpc/>
1. OAuth, <http://oauth.net/>
1. Cloud Computing Tutorial. <https://research.microsoft.com/en-us/projects/azure/sc09cc.ppsx>
1. VMWare/Google Collaboration. <http://www.vmware.com/company/news/releases/vmware-google.html>
1. Sriram Krishnan, Programming Windows Azure, O'Reilly, 2010.
1. How to Develop a Rich, Native-quality User Experience for Mobile Using Web Standards: <http://slidesha.re/csGs3u>
1. Jonathan Stark, Building iPhone Apps with HTML, CSS and Javascript, O'Reilly, 2010, <http://slidesha.re/9JyrWu>
1. Mike Burrows, The Chubby Lock Service for Loosely-Coupled Distributed Systems, <http://labs.google.com/papers/chubby.html>
1. Leslie Lamport, The Part-Time Parliament, <http://research.microsoft.com/en-us/um/people/lamport/pubs/lamport-paxos.pdf>
1. Thorsten Claus, Daniel Kellmereit, Yasmin Narielvala, The Future of Cloud, <http://thefutureofcloud.com/>