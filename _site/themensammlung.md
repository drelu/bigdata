# RESTful Cloud APIs am Beispiel von Twitter

1. Erstellen Sie in einer Programmiersprache ihre Wahl einen Twitter Client. Der Client soll:
	* die aktuelle Public Timeline und 
	* in der Nähe gepostet Tweets 

	anzeigen können.

1. Zusatzaufgabe: Nutzen Sie eine OAuth Bibliothek, um User gegenüber Twitter authentisieren und autorisieren.

	Material:
	* Twitter Developer Site, <http://dev.twitter.com/>
	* Twitter Streaming API Präsentation, <http://www.slideshare.net/jkalucki/thinking-in-streaming-twitter-streaming-api>
	* Tweetstream Package: <http://pypi.python.org/pypi/tweetstream>

Beispiel Kommandozeile:

    curl -d 'locations=11.0,48.1,11.5,48.3'  https://stream.twitter.com/1.1/statuses/filter.json -uCCMobileHM:mucmuc


Beispiel Python:

    #!/bin/bash
    import tweetstream
    
    words = ["muc"]
    locations = ["11.0,48", "12, 49"]
    stream = tweetstream.FilterStream("CCMobileHM", "mucmuc", track=words,
                                  locations=locations) 
    for tweet in stream:
    	print "Got interesting tweet:", tweet

# Datenanalyse mit Kommando-Zeile und Python
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
 	

Lösung:

    wc -l
    head 
    cat access_log.txt | head -n 5 | awk '{print $4}' | sort | uniq -c | sort -rn 

	cat /data/NASA_access_log_Jul95 | awk  '{print $(NF-1)}'| sort | uniq -c
	
# Hadoop Streaming

1. Nutzen Sie das MapReduce Programmiermodell, um die Statistiken auf Aufgabe 3 
zu erfolgen. Nutzen Sie das folgende [Python-Skript](src/map_reduce.py) als 
Template!

1. Testen Sie das Skript:
        * Lokal:
            cat input | python map_reduce.py map | sort | python map_reduce.py reduce
        * Hadoop Local Runner

Hadoop Test:

/usr/bin/hadoop jar /usr/lib/hadoop-0.20-mapreduce/hadoop-examples.jar grep input output 404

Hadoop Streaming:
/usr/bin/hadoop jar /usr/lib/hadoop-0.20-mapreduce/contrib/streaming/hadoop-streaming-2.0.0-mr1-cdh4.1.1.jar -file nasa.py -input /user/ubuntu/input -output /user/ubuntu/output -mapper "nasa.py map" -reducer "nasa.py reduce"	
	
# Open Data

1. Nutzen die Daten der [Stadt München](http://www.muenchen.de/opendata), um folgende Fragen zu beantworten:
    * In welchem Stadtviertel sind die meisten Fahrzeuge zugelassen?
    * In welchem Stadtviertel gibt es die meisten Kinder (im Verhältnis zu den dort lebenden Einwohnern)?

1. Berlin Open Data:
    * http://daten.berlin.de/datensaetze/einwohner-2011-zum-stichtag


1. Visualisieren Sie die Daten auf einer Karte (z.B. Google Maps oder Google Fusion Tables)!

# Getting Started mit Amazon EC2 und S3

S3 Dokumentation: <http://aws.amazon.com/documentation/s3/>
EC2 Dokumentation: <http://aws.amazon.com/documentation/ec2/>

1. Konfigurieren Sie die EC2 und S3 Tools mit ihrem Amazon Access und Secret Access Schlüssel!

1. Nutzen Sie `s3cmd`, um eine Datei ihrer Wahl auf S3 hochzuladen! Machen Sie die Datei Public! Prüfen Sie ob Sie die Datei über den Web-Browser erreichen können!

1. Erstellen Sie ein Python Programm unter Nutzung von [Boto](http://docs.pythonboto.org/en/latest/index.html), das `/data` Verzeichnis auf Amazon S3 zu kopieren. Messen Sie die notwendige Zeit und berechnen Sie die Bandbreite!

1. Erstellen Sie EC2 Instanz (Typ: `t1.micro`). Folgen Sie dazu allen notwendigen Schritten (z.B. Erstellung eines Keys). Loggen Sie sich auf dieser mit SSH ein!



# Map Reduce Hello World

1. Machen Sie sich mit der gegebenen MapReduce [Implementierung](src/map_reduce.py) eines Word Counts vertraut!

1. Führen Sie das Wordcount auf der dem Buch "The Outline of Science" aus ([Download](http://www.gutenberg.org/cache/epub/20417/pg20417.txt) von Projekt Gutenberg Web Seite)



# Amazon's Elastic MapReduce

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

TestDFSIO: <http://answers.oreilly.com/topic/460-how-to-benchmark-a-hadoop-cluster/>

1. Starten Sie einen 1 Knoten Hadoop Cluster mit Elastic MapReduce! Nutzen Sie dabei die Optionen `--hive-interactive` und `--alive`! 

1. Loggen Sie sich auf den Master-Knoten ein! Machen Sie sich mit Hadoop vertraut (`hadoop help`)!

1. Testen Sie das HDFS! Wie viel Speicher ist im HDFS verfügbar? 


1. Lassen Sie das Log-File Beispiel aus der vorherigen Übung auf dem Cluster laufen! 

1. Generieren Sie durch kopieren der Daten im HDFS ein Input Datensatz von 10 GB! Messen Sie die Laufzeit auf 1 Knoten!

1. Stoppen Sie den JobFlow und starten Sie einen weiteren Jobflow mit 3 Knoten (d.h. 2 Data Nodes)! Wiederholen Sie das Experiment und messen Sie die Laufzeit! 

1. Legen Sie die gleichen Input Daten auf Amazon S3 ab und wiederholen Sie das Experiment. Erklären Sie das Ergebnis!

1. Führen Sie den HDFS TestDFSIO Test auf dem Cluster durch (`hadoop jar hadoop-test-1.0.3.jar`)!

1. Lassen Sie den TeraSort auf einen 8 Knoten Cluster laufen!



Lösung:
    elastic-mapreduce --create --name "WS2012" --hive-interactive --alive
    elastic-mapreduce --ssh --jobflow j-36V79ZKX2EE00


EC2
/usr/bin/hadoop jar /usr/lib/hadoop-0.20-mapreduce/contrib/streaming/hadoop-streaming-2.0.0-mr1-cdh4.1.2.jar -file nasa.py -input /user/ubuntu/input -output /user/ubuntu/output -mapper "nasa.py map" -reducer "nasa.py reduce"


EMR
elastic-mapreduce --put nasa.py -j j-DNAIWYDJC5WS 

hadoop jar /home/hadoop/contrib/streaming/hadoop-streaming-1.0.3.jar -file nasa.py -input s3://nasa-ws2012 -output s3n://nasa-ws2012/output -mapper "nasa.py map" -reducer "nasa.py reduce"

hadoop jar /home/hadoop/contrib/streaming/hadoop-streaming-1.0.3.jar -file nasa.py -input /user/hadoop/input -output /user/hadoop/output -mapper "nasa.py map" -reducer "nasa.py reduce"

<br/><br/>
# Hive
<br/>
Hive Dokumentation: <http://hive.apache.org/>
<br/>

1. Starten Sie 1 EMR Jobflow mit 1 Knoten unter Nutzung des Kommandozeilentools `elastic-mapreduce` (Optionen: `--hive-interactive` und `--alive`)!

1. Machen Sie sich mit Hive vertraut in dem Sie sich auf der Kommandozeile auf den Master-Knoten des EMR-Clusters einloggen.!

1. Erstellen Sie für das National Climate Data Center Datensample eine Hive Tabelle. Laden Sie die Sample-Daten `cloud.luckow-hm.de:/data/ncdc/sample.txt` in diese Tabelle!

1. Erstellen Sie eine SQL Query die die Maximaltemperatur pro Jahr ausgibt! Lassen Sie diese laufen!

elastic-mapreduce --create --name "WS2012" --hive-interactive --alive
elastic-mapreduce -j j-25US0QEGKJI0F --put /data/ncdc/sample.txt 
elastic-mapreduce --ssh --jobflow j-36V79ZKX2EE00

$ mkdir ncdc

$ hive
>CREATE TABLE records (year STRING, temperature INT, quality INT) ROW FORMAT DELIMITED FIELDS TERMINATED BY '\t' LOCATION '/home/hadoop/ncdc';

>LOAD DATA LOCAL INPATH '/home/hadoop/sample.txt' OVERWRITE INTO TABLE records;

>SELECT year, MAX(temperature) FROM records WHERE temperature != 9999 AND (quality = 0 OR quality = 1 OR quality = 4 OR quality = 5 OR quality = 9) GROUP BY year;



# Google AppEngine

	1. Installieren Sie das Google Plugin in Eclipse! Folgen Sie dazu der folgenden Anleitung: http://code.google.com/intl/de-DE/appengine/docs/java/tools/eclipse.html

	2. Erstellen Sie eine Web-Anwendung (in Java oder Python), welche eine Liste von allen Teilnehmer ausgibt. Testen Sie die Anwendung im Simulator und auf Google!

	3. Installieren Sie ein Beispiel ihrer Wahl auf GAE!


# Zookeeper

http://zookeeper.apache.org/doc/trunk/recipes.html

# Scikit-Learn

1. Classification using a decision tree

1. Clustering using kmeans

http://thingiverse.com