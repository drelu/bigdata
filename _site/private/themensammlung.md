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
    1. Welche Seiten werden am meisten genutzt?
 	1. Wie viele HTTP Fehler gab es?
 	1. Nutzen Sie die Data tools um folgende Auswertungen zu erzeugen:
		* Histogram der angeforderten Paths

Lösung:

    wc -l
    head 
    cat access_log.txt | head -n 5 | awk '{print $4}' | sort | uniq -c | sort -rn 

	cat /data/NASA_access_log_Jul95 | awk  '{print $(NF-1)}'| sort | uniq -c
	
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

1. Starten Sie einen 1 Knoten Hadoop Cluster mit Elastic MapReduce!


1. Loggen Sie sich auf den Master-Knoten ein! Machen Sie sich mit Hadoop vertraut (`hadoop help`)!


1. Testen Sie das HDFS! Wie viel Speicher ist im HDFS verfügbar? Laden Sie das Buch "The Outline of Science" ins HDFS!


1. Führen Sie den HDFS TestIO Test auf dem Cluster durch!


1. Lassen Sie das Word Count Beispiel aus der vorangegangen Übung auf dem Cluster laufen!
    * <http://hadoop.apache.org/docs/r1.0.3/streaming.html>


Lösung:
    elastic-mapreduce --create --name "WS2012" --hive-interactive --alive
    elastic-mapreduce --ssh --jobflow j-36V79ZKX2EE00

    hadoop jar /home/hadoop/contrib/streaming/hadoop-streaming-1.0.3.jar -input /user/luckow/ -output /user/luckow/output/ -mapper map.py -reducer reduce.py  -file `pwd`/map_reduce.py -file `pwd`/map.py -file `pwd`/reduce.py
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