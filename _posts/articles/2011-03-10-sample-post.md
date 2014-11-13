---
layout: post
title: Intro zu CasperJS
excerpt: "Einführung und Installation von CasperJS zum Frontend Testing."
modified: 2013-05-31
categories: articles
tags: [intro-post]
image:
  feature: tumblr_msyxzmyZtE1rihds2o1_1280.jpg
  credit: Max Stottrop
  creditlink: http://photogenicseeing.tumblr.com/
comments: true
share: true
---

### Vorraussetzungen

Ihr habt eine laufende Ubuntu Installation und mindestens eine Stunde Zeit.

### Los geht's

Jeder, dessen Aufgabe es ist das Frontend einer Software zu testen, kann nachvollziehen wie unschön es ist, alles händisch zu machen. Dauernd müssen Buttons gedrückt, Texte verglichen und ein und dieselbe Aufgabe immer wieder ausgeführt werden. Schnell bekommt man das Gefühl, Teil einer Beschäftigungstherapie zu sein. Doch gottseidank gibt es auch andere Wege, Fehler im der Software ausfindig zu machen. Das Zauberwort heißt "headless browser".

Was genau kann man sich darunter vorstellen? Nun, im Grunde liegt die Magie von einer Headless Browser Engine darin, dass die Arbeitsschritte (drücken, klicken, warten...) nicht mehr im Browser, sondern in der Kommandozeile ausgeführt werden können. Dabei fühlt man sich nicht nur wie ein cooler Hollywood Hacker, sondern spart Zeit und arbeitet effektiver.

### Installation

Wie arbeitet man nun mit einer Headless Browser Engine? In dieses Beispiel werden wir mit CasperJS arbeiten, das auf PhantomJS aufbaut. Im Gegensatz zu Alternativen wie Selenium oder ist hier nicht nur die API einfacher, sondern es gibt auch noch die Möglichkeit Test mit Hilfe von Travis oder Cronjobs zu automatisieren. Aber dazu später mehr.

Bevor wir aber anfangen können, müssen wir CasperJS erst einmal auf unserem System installieren. Dazu benötigen wir eine bestehende Internetverbindung und Zugriff auf das Terminal.

**Zuerst, einige Vorbereitungen:**

{% highlight css %}

sudo apt-get update
sudo apt-get install build-essential
sudo apt-get install libreadline-gplv2-dev libncursesw5-dev libssl-dev libsqlite3-dev tk-dev libgdbm-dev libc6-dev libbz2-dev
sudo apt-get install nodejs
sudo apt-get install npm

{% endhighlight %}

**Funktioniert alles reibungslos, installieren wir nun PhantomJS:**

{% highlight css %}

cd /usr/local/share
sudo wget https://bitbucket.org/ariya/phantomjs/downloads/phantomjs-1.9.8-linux-x86_64.tar.bz2
sudo tar xjf phantomjs-1.9.7-linux-x86_64.tar.bz2
sudo ln -s /usr/local/share/phantomjs-1.9.8-linux-x86_64/bin/phantomjs /usr/local/share/phantomjs
sudo ln -s /usr/local/share/phantomjs-1.9.8-linux-x86_64/bin/phantomjs /usr/local/bin/phantomjs
sudo ln -s /usr/local/share/phantomjs-1.9.8-linux-x86_64/bin/phantomjs /usr/bin/phantomjs

{% endhighlight %}

**Und schlussendlich CasperJS:**

{% highlight css %}

sudo npm install casperjs

{% endhighlight %}

Nachdem alles fertig installiert wurde, einmal neustarten und folgende Zeilen ins Terminal eingeben:

{% highlight css %}

phantomjs --version
casperjs

{% endhighlight %}

Sieht die Ausgabe ungefähr so aus, sind wir für heute fertig:

{% highlight css %}

phantomjs --version
1.9.2
casperjs
CasperJS version 1.1.0-DEV at /Users/xyz/Desktop/casperjs, using phantomjs version 1.9.8

{% endhighlight %}


Es gibt jetzt zwei Möglichkeiten wie ihr euch die Zeit bis zum nächsten Post vertreiben könnt. Entweder lest ihr euch die Dokumentationen von [PhantomJS](http://phantomjs.org/documentation/) und [CasperJS](casperjs.readthedocs.org) durch, welche sehr schön und simple gehalten sind. Habt ihr aber noch keine Ahnung, wie JavaScript funktioniert, was Programmieren ist empfehle ich am JavaScript Kurs auf [Codeacademy](http://www.codecademy.com/en/tracks/javascript) teilzunehmen.

Nächstes Mal werden wir dann unseren ersten Tests mit CasperJS schreiben.