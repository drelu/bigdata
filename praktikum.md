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
* Python 2.7.3
* Hostname: `cloud.luckow-hm.de`
* [Netzmafia Einführung Linux](http://netzmafia.de/skripten/unix/index.html)
* User werden beim ersten Praktikum vergeben!

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

<br/>

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
		

