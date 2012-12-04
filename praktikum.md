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
* Amazon Console: <https://bigdata.signin.aws.amazon.com/console>

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

*Lösung*

    cat /data/NASA_access_log_Jul95 | awk  '{print $(NF-1)}'| sort | uniq -c

<br/> 
	
# 4. MapReduce-basierte Log-Dateien Auswertung
<br/> 

*Informationen:*

* Hadoop Dokumentation: <http://hadoop.apache.org/docs/r1.0.3/>
* Hadoop Help Pages:

        hadoop fs -help 
        hadoop jar $HADOOP_HOME/contrib/streaming/hadoop-streaming-2.0.0-mr1-cdh4.1.2.jar -info

* Hadoop Web Schnittstellen:

    * Namenode: `lynx http://localhost:50070`

    * Jobtracker: `lynx http://localhost:50030`

* Hadoop Home: `/usr/lib/hadoop-0.20-mapreduce/`
* Hadoop Streaming Bibliothek: 
`/usr/lib/hadoop-0.20-mapreduce/contrib/streaming/hadoop-streaming-2.0.0-mr1-cdh4.1.1.jar`
* Input Daten: `cloud.luckow-hm.de:/data/NASA_access_log_Jul95`
* [Introduction to Hadoop](http://cdn.oreillystatic.com/en/assets/1/event/85/An%20Introduction%20to%20Hadoop%20Presentation.pdf)

<br/>
<br/>

1. Nutzen Sie das MapReduce Programmiermodell, um die Statistiken auf Aufgabe 3 
zu erfolgen. Nutzen Sie das folgende [Python-Skript](src/map_reduce.py) als 
Template! Testen Sie das Skript:

        cat <input file> | python map_reduce.py map | sort | python map_reduce.py reduce



1. Machen Sie sich mit dem Hadoop Dateisystem vertraut! Laden Sie die Eingabedateien für den 
MapReduce Job in das Hadoop Filesystem (auf `cloud.luckow-hm.de`). Legen Sie dazu 
ein neues Verzeichnis `input` in ihrem HDFS Home Verzeichnis an!
	
1. Lassen Sie ihr erstelltes Auswertungsskript mit Hadoop laufen. Beobachten Sie die Ausführungen: Wie viele Map Tasks werden generiert? Wie viel Map Slots belegt die Applikation?

1. Vergleichen Sie die Laufzeiten der lokalen Ausführung mit der Hadoop Variante. Erlären Sie den Unterschied!

<br/> 
*Lösung*<br/>

[Python-Skript](src/nasa.py)

<br/>
<br/> 
# 5. Getting Started mit Amazon EC2 und S3
<br/> 
S3 Dokumentation: <http://aws.amazon.com/documentation/s3/>
EC2 Dokumentation: <http://aws.amazon.com/documentation/ec2/>

*Bitte stellen Sie sicher, dass Sie alle Instanzen am Ende der Vorlesung beenden!*

1. Konfigurieren Sie die EC2 und S3 Tools mit ihrem Amazon Access und Secret Access Schlüssel!

1. Nutzen Sie `s3cmd`, um eine Datei ihrer Wahl auf S3 hochzuladen! Machen Sie die Datei Public! Prüfen Sie ob Sie die Datei über den Web-Browser erreichen können!

1. Erstellen Sie ein Python Programm unter Nutzung von [Boto](http://docs.pythonboto.org/en/latest/index.html), das `/data` Verzeichnis auf Amazon S3 zu kopieren. Messen Sie die notwendige Zeit und berechnen Sie die Bandbreite!

1. Erstellen Sie EC2 Instanz (Typ: `t1.micro`). Folgen Sie dazu allen notwendigen Schritten (z.B. Erstellung eines Keys). Loggen Sie sich auf dieser mit SSH ein!

<br/>
<br/>
# 6. Amazon's Elastic MapReduce
<br/>
Elastic MapReduce Dokumentation: <http://docs.amazonwebservices.com/ElasticMapReduce/latest/GettingStartedGuide/Welcome.html>

    Bitte legen Sie eine Datei `credentials.json`
    {
        "access_id": "",
        "private_key": "",
        "keypair": "MyKey",
        "key-pair-file": "<HOME>/.ssh/id_rsa",
        "log_uri": "s3://emr-drelu-log",
        "region": "us-east-1"
    }

<!--TestDFSIO: <http://answers.oreilly.com/topic/460-how-to-benchmark-a-hadoop-cluster/>-->

1. Starten Sie einen 1 Knoten Hadoop Cluster mit Elastic MapReduce! Nutzen Sie dabei das Kommandozeilentool `elastic-mapreduce` und die Optionen `--hive-interactive` und `--alive`! 

1. Loggen Sie sich auf den Master-Knoten ein! Machen Sie sich mit Hadoop vertraut (`hadoop help`)!

1. Testen Sie das HDFS! Wie viel Speicher ist im HDFS verfügbar? 

1. Lassen Sie das Log-File Beispiel aus der vorherigen Übung auf dem Cluster laufen! 

1. Generieren Sie durch kopieren der Daten im HDFS ein Input Datensatz von 10 GB! Messen Sie die Laufzeit auf 1 Knoten!

1. Stoppen Sie den JobFlow und starten Sie einen weiteren Jobflow mit 3 Knoten (d.h. 2 Data Nodes)! Wiederholen Sie das Experiment und messen Sie die Laufzeit! 

1. Legen Sie die gleichen Input Daten auf Amazon S3 ab und wiederholen Sie das Experiment. Erklären Sie das Ergebnis!

# 7. Hive

<br/>
Hive Dokumentation: <http://hive.apache.org/>
<br/>

1. Starten Sie 1 EMR Jobflow mit 1 Knoten unter Nutzung des Kommandozeilentools `elastic-mapreduce` (Optionen: `--hive-interactive` und `--alive`)!

1. Machen Sie sich mit Hive vertraut in dem Sie sich auf der Kommandozeile auf den Master-Knoten des EMR-Clusters einloggen.!

1. Erstellen Sie für das National Climate Data Center Datensample eine Hive Tabelle. Laden Sie die Sample-Daten `cloud.luckow-hm.de:/data/ncdc/sample.txt` in diese Tabelle!

1. Erstellen Sie eine SQL Query die die Maximaltemperatur pro Jahr ausgibt! Lassen Sie diese laufen!