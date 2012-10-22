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

# Umgang mit SSH und Linux

1. Loggen Sie sich mit SSH auf der Linux VM ein! Ändern Sie ihr Passwort!

1. Beantworten Sie folgende Fragen:
    * Wie viele User sind aktuell auf dem Server angelegt? Wie viele sind derzeit angemeldet?
    * Wie viel Plattenspeicher ist verfügbar?
    * Wann wurde der Rechner das letzte Mal gestartet?
    * Welcher Prozess hat aktuell den höchsten CPU/Speicher Verbrauch?

1. Gehen Sie durch das Python Tutorial:
    * http://docs.python.org/tutorial/introduction.html

<br/>

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

<br/>

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