---
layout: page
title: "Praktikum"
description: ""
published: false

---
{% include JB/setup %}

# Infrastruktur

* Linux Cluster hosted at Amazon EC2
* Ubuntu 12.04
* Python 2.7.3, Python Dokumentation: <http://docs.python.org/>
* Hostname: `cloud.luckow-hm.de`
<!--* Amazon Console: <https://bigdata.signin.aws.amazon.com/console>-->

* [Netzmafia Einführung Linux](http://netzmafia.de/skripten/unix/index.html)
* User werden beim ersten Praktikum am 12.10.2012 vergeben!

<br/>

# 1. Umgang mit SSH und Linux

1. Loggen Sie sich mit SSH auf der Linux VM ein! Ändern Sie ihr Passwort!

1. Beantworten Sie folgende Fragen:
    * Wie viele User sind aktuell auf dem Server angelegt? Wie viele sind derzeit angemeldet?
    * Wie viel Plattenspeicher ist verfügbar?
    * Wann wurde der Rechner das letzte Mal gestartet?
    * Welcher Prozess hat aktuell den höchsten CPU/Speicher Verbrauch?

1. Gehen Sie durch das Python Tutorial:
    * http://docs.python.org/tutorial/introduction.html

<br/>

# 2. RESTful Cloud APIs am Beispiel von Twitter

1. Erstellen Sie in einer Programmiersprache ihre Wahl einen Twitter Client. Der Client soll:
	* die aktuelle Public Timeline und 
	* in der Nähe gepostet Tweets 

	anzeigen können.

1. Zusatzaufgabe: Nutzen Sie eine OAuth Bibliothek, um User gegenüber Twitter authentisieren und autorisieren.

	Material:
	* Twitter Developer Site, <http://dev.twitter.com/>
	* Twitter Streaming API Präsentation, <http://www.slideshare.net/jkalucki/thinking-in-streaming-twitter-streaming-api>
	* Tweetstream Package: <http://pypi.python.org/pypi/tweetstream>

<br/>

# 3. Datenanalyse mit Kommando-Zeile und Python
<br/>  

Notwendige Daten/Tools
* <http://ita.ee.lbl.gov/html/contrib/NASA-HTTP.html>
* Commandline data tools <https://github.com/bitly/data_hacks>
* Daten: `cloud.luckow-hm.de:/data/NASA_access_log_Jul95`

<br/> 

1. Nutzen die Kommandos `head`, `cat`, `uniq`, `wc`, `sort`, `find`, `xargs`, `awk` um die NASA Access Logs auszuwerten:
    1. Welche Seiten wurden am meisten angesurft?
 	1. Welcher Fehler trat am Meisten auf?
	1. Wie viele HTTP Fehler gab es insgesamt? Wieviel Prozent der Requests wurden mit einem Fehler beendet.

<br/> 
	
# 4. MapReduce-basierte Log-Dateien Auswertung

Informationen:
* Hadoop Dokumentation: <http://hadoop.apache.org/docs/r1.0.3/>
* Hadoop Help Pages:

    hadoop fs -help 
    hadoop jar $HADOOP_HOME/contrib/streaming/hadoop-streaming-2.0.0-mr1-cdh4.1.1.jar -info

* Hadoop Web Schnittstellen:
    * Namenode: lynx http://localhost:50070
    * Jobtracker: lynx http://localhost:50030
* Hadoop Home: `/usr/lib/hadoop-0.20-mapreduce/`
* Hadoop Streaming Bibliothek: 
`/usr/lib/hadoop-0.20-mapreduce/contrib/streaming/hadoop-streaming-2.0.0-mr1-cdh4.1.1.jar`
* Input Daten: `cloud.luckow-hm.de:/data/NASA_access_log_Jul95`

1. Nutzen Sie das MapReduce Programmiermodell, um die Statistiken auf Aufgabe 3 
zu erfolgen. Nutzen Sie das folgende [Python-Skript](src/map_reduce.py) als 
Template! Testen Sie das Skript:

        cat <input file> | python map_reduce.py map | sort | python map_reduce.py reduce

1. Machen Sie sich mit dem Hadoop Dateisystem vertraut! Laden Sie die Eingabedateien für den 
MapReduce Job in das Hadoop Filesystem (auf `cloud.luckow-hm.de`). Kopieren Sie die Eingabedateien 
in ein Verzeichnis `input` in ihrem HDFS Home Verzeichnis!
	
1. Lassen Sie ihr erstelltes Auswertungsskript mit Hadoop laufen. Beobachten Sie die Ausführungen: Wie viele Map Tasks werden generiert? Wie viel Map Slots belegt die Applikation?

1. Vergleichen Sie die Laufzeiten der lokalen Ausführung mit der Hadoop Variante. Erlären Sie den Unterschied!



