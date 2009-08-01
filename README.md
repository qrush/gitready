# Git Ready

> There is only one way to *get ready* for immortality, and that is to love this life and live it as bravely and faithfully and cheerfully as we can.<br />
> ~ Henry Van Dyke

## Über

Dieses Repository beinhaltet HTML, CSS, Bilder und Beitrage für [gitready.com](http://gitready.com). Git Ready (war täglich, dann drei-wöchentlich, und jetzt) wöchentlich Tips für jene, die mehr über dieses verteilte Versionskontrollsystem lernen möchten oder gerade damit angefangen haben. Dieses Blog als Ganzes startete als Reise, um mehr über Git zu lernen und Anderen seine Nützlichkeit zu zeigen. Wenn du eine Frage zum Inhalt hast, schicke [qrush eine Nachricht auf GitHub](http://github.com/qrush) oder schreibe eine E-Mail an [nick@quaran.to](mailto://nick@quaran.to).

## Veröffentlichen

Das Blog wird mit der [Jekyll](http://github.com/mojombo/jekyll) Engine erzeugt. Die Formatierung orientiert sich an den Grundlagen, auch das statische HTML. Sorgen zur Skalierbarkeit existieren nicht.

## Mitmachen

Wenn du Ideen zu neuen Seiten, Layouts oder irgendetwas hast, spalte ab (fork)!<br /> Wenn du Tips einreichen möchtest, [mache das hier](http://gitready.com/submit.html).

## Übersetzung

Wenn du daran interessiert bist, Beiträge in deine Sprache zu übersetzen, großartig! Hier eine kurze Anleitung:

* Spalte das Projekt ab (fork).
* Erzeuge einen Zweig mit dem ISO Code für deine Sprache, für Englisch:

<pre>
git checkout -b en
</pre>

* Markiere alle Beiträge als unveröffentlicht und übergebe deine Änderungen:

<pre>
rake unpublish
git commit -am "Unpublishing all the posts"
</pre>

* Übersetze die Kopf- und Fußzeilen der Startseite. Schau dir die anderen übersetzen Seiten als Beispiele an, wie die [deutsche Seite](http://de.gitready.com).
* Übersetze so wenige oder so viele Beiträge, wie du möchtest.
* Lade deine Arbeit hoch (push) und vergiß nicht den richtigen Zweig zu verwenden!:
* Push your work back up (remember to use the right branch name!):

<pre>
git push origin en
</pre>

* Reiche alle Pull-Anfragen an qrushs Repository.

Sobald das erledigt ist, füge ich die Subdomain deiner Sprache hinzu und veröffentliche deine Arbeit.

## Lizensierung

Der tatsächliche Inhalt der Artikel ist unter der Creative Commons lizensiert. Der Quellcode, der dieses Projekt erzeugt, ist unter MIT lizensiert.

Grundsätzlich, wenn du die Blogbeiträge weiter verteilen möchtest, stelle die Rückverlinkung sicher. Wenn du den Inhalt veröffentlichen möchtest, ist das auch in Ordnung, behalte bitte die Lizenzinformationen bei.
