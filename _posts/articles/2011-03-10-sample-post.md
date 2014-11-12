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

## Code Snippets

Syntax highlighting via Pygments

{% highlight css %}
#container {
  float: left;
  margin: 0 -240px 0 0;
  width: 100%;
}
{% endhighlight %}