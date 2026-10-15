# Kapitel 3: Bedrohungen und Schadenszenarien einordnen

![Kapitelbild](bilder/03_kapitelbild.png)

In diesem Kapitel werden Sie ...

---

## Handlungssituation

Die ChangeIT GmbH führt bei der RECPLAST GmbH eine Kundenschulung zur Informationssicherheit durch. Frau Weber hat Beschäftigte aus Produktion, Labor, Einkauf, Personalabteilung und Instandhaltung eingeladen. Sie begleiten die Schulung als Auszubildende/Auszubildender der ChangeIT GmbH mit dem Ziel den letzten Termin der Fortbildungsreihe selbst zu gestalten.

---

## Kompetenz 3.0: Sicherheitsvorfälle mit Grundbegriffen der IT-Sicherheit beschreiben

Zum Einstieg in die Fortbildung zeigt ein Mitarbeiter der ChangeIT einen Fernsehbeitrag über die White-Hat-Hacker eines Partnerunternehmens, die im Auftrag einer Bäckerei einen Penetrationstest durchgeführt haben. Frau Weber fragt in die Runde: 

"Hätte uns das auch passieren können?"

---

###  A|3.0: Einen Penetrationstest auswerten und Angriffsszenarien sammeln

#### Aufgabe 1
Sehen Sie sich den M|3.0.0: Fernsehbeitrag an und notieren Sie, auf welchen Wegen die Pentester in die Bäckerei gelangt sind und was sie dort erreicht haben bzw. hätten erreichen können.

#### Aufgabe 2
Der Beitrag nennt drei Phasen eines Penetrationstests:

* Informationsbeschaffung
* Angriffsvektoren finden
* Eindringen (Exploiting)

Ordnen Sie Ihre Notizen aus Aufgabe 1 diesen Phasen zu.

#### Aufgabe 3
Führen Sie ein Brainstorming durch: Welche Angriffsszenarien kennen Sie oder haben Sie schon einmal gehört? Halten Sie die Nennungen fest.

#### Aufgabe 4
Informieren Sie sich in M|3.0.1: Schwachstelle, Bedrohung, Angriff, Schaden und M|3.0.2: Penetrationstest und erklären Sie die Begriffe in eigenen Worten.

---

### M|3.0.1: Schwachstelle, Bedrohung, Angriff, Schaden

Schwachstelle, Bedrohung, Angriff und Schaden

Oft werfen wir Begriffe wie „Sicherheitslücke“, „Gefahr“, „Hackerangriff“ und „Schaden“ durcheinander. In der IT-Sicherheit haben sie dagegen genaue Bedeutungen, und erst mit ihnen lässt sich sauber beschreiben, was bei einem Vorfall passiert ist. Wer nur sagt „Die Firma wurde gehackt“, weiß noch nicht, wo er ansetzen muss. Wer dagegen sagt „Über eine Schwachstelle im Prozess hat ein Angreifer einen Schaden an der Verfügbarkeit verursacht“, kann gezielt Gegenmaßnahmen planen.

Vier Begriffe bilden eine Kette. Die Schwachstelle ist die Lücke im System. Die Bedrohung ist die Möglichkeit, dass jemand oder etwas diese Lücke ausnutzt. Der Angriff ist das tatsächliche Ausnutzen. Der Schaden ist die Folge. Fehlt ein Glied, bricht die Kette ab: Eine Schwachstelle ohne Bedrohung bleibt folgenlos, und eine Bedrohung ohne Schwachstelle läuft ins Leere.

Die vier Bausteine

**Schwachstelle (Vulnerability)**

Eine Schwachstelle ist ein Mangel in einem System, einem Prozess oder im Verhalten, der es ermöglicht, ein Schutzziel zu verletzen. Sie ist zunächst nur ein Zustand und richtet für sich allein keinen Schaden an. Schwachstellen gibt es nicht nur in Software, sondern in allen Bereichen eines Unternehmens.

- **Technisch:** Veraltete Software ohne Updates, ungesicherte Schnittstellen, fehlende Redundanz.
- **Organisatorisch:** Fehlende Regeln, unklare Zuständigkeiten, Schlüssel ohne Verwaltung, kein Change Management.
- **Menschlich:** Fehlendes Bewusstsein, Gutgläubigkeit, Bequemlichkeit, etwa das Passwort auf dem Notizzettel.
- **Physisch:** Offene Türen und Fenster, unbeaufsichtigte Räume, fehlende Zutrittskontrolle.

*💻 Beispiel aus der IT-Praxis: Auf einem Dateiserver läuft ein Betriebssystem, für das seit Monaten Sicherheitsupdates vorliegen, die aber nicht eingespielt wurden. Die Lücke ist in öffentlichen Datenbanken (CVE) dokumentiert. Das System ist verwundbar, obwohl noch niemand etwas ausgenutzt hat.*

**Bedrohung (Threat)**

Eine Bedrohung ist ein mögliches Ereignis oder ein möglicher Akteur, der eine Schwachstelle ausnutzen und damit ein Schutzziel verletzen könnte. Sie beschreibt, was passieren kann, und nicht, was bereits passiert ist. Das BSI fasst typische Bedrohungen im IT-Grundschutz-Kompendium als Elementare Gefährdungen zusammen (G 0.1 bis G 0.47). Sie reichen von Feuer und Stromausfall über Schadprogramme bis zu Social Engineering und Fehlbedienung.

- **Vorsätzlich:** Kriminelle, Innentäter, Spione, Aktivisten, Konkurrenz.
- **Fahrlässig:** Bedienfehler, Unachtsamkeit, Missverständnisse, fehlende Schulung.
- **Technisch:** Hardwaredefekt, Softwarefehler, Ausfall von Dienstleistern.
- **Höhere Gewalt:** Brand, Wasser, Blitzschlag, Unwetter.

Eine Bedrohung wird erst dann gefährlich, wenn sie auf eine passende Schwachstelle trifft. Ein Hochwasser ist für einen Serverraum im Keller eine große Bedrohung, für einen Serverraum im dritten Stock kaum.

*💻 Beispiel aus der IT-Praxis: Ein Admin liest im Newsletter des BSI, dass eine Ransomware-Gruppe aktuell Schwachstellen in Fernwartungszugängen ausnutzt. Die Bedrohung ist damit für alle relevant, die einen solchen Zugang betreiben. Er prüft als Erstes, ob die eigene Firewall diese Schwachstelle hat.*

**Angriff (Attack)**

Ein Angriff ist das tatsächliche, zielgerichtete Ausnutzen einer Schwachstelle durch einen Angreifer. Der Weg, auf dem der Angreifer in das System gelangt, heißt Angriffsvektor, das Programm oder Vorgehen, das die Schwachstelle ausnutzt, heißt Exploit. Angriffe laufen meist in mehreren Schritten ab: Informationen sammeln, Schwachstellen suchen, eindringen, Ziel erreichen, Spuren verwischen.

- **Angriffsvektor:** E-Mail-Anhang, USB-Stick, offenes Fenster, Anruf beim Schichtleiter, ungesichertes WLAN.
- **Exploit:** Schadcode oder Trick, der die Lücke nutzt, etwa ein präpariertes Word-Dokument oder eine erfundene Geschichte.
- **Angriffsfläche:** Summe aller möglichen Einstiegspunkte. Je mehr Systeme, Zugänge und Personen, desto größer.
- **Zufall oder Absicht:** Ein Angriff ist zielgerichtet. Ein Bedienfehler ist ein Vorfall, aber kein Angriff.

*💻 Beispiel aus der IT-Praxis: Eine Mitarbeiterin im Personalwesen erhält eine Initiativbewerbung als Word-Datei. Das Dokument enthält ein Makro, das beim Öffnen Schadcode nachlädt. Angriffsvektor ist die E-Mail, Exploit das Makro, die Schwachstelle die Gewohnheit, Anhänge von Fremden ohne Prüfung zu öffnen.*

**Schaden (Damage)**

Ein Schaden ist die nachteilige Folge eines erfolgreichen Angriffs oder eines anderen Ereignisses. Er lässt sich immer einem oder mehreren Schutzzielen zuordnen: Vertraulichkeit (Daten sind abgeflossen), Integrität (Daten oder Steuerungen wurden verändert) oder Verfügbarkeit (Systeme stehen still). Manche Schäden sind sofort messbar, etwa der Produktionsausfall pro Stunde, andere zeigen sich erst später, etwa ein Vertrauensverlust bei Kunden. Welche Schadenskategorien es gibt und wie man sie einordnet, erarbeiten Sie in A|3.2.

- **Direkt:** Ausfallkosten, Wiederherstellung, Ausschuss, Lösegeld.
- **Indirekt:** Imageverlust, Vertragsstrafen, verlorene Aufträge.
- **Materiell:** Geld, Maschinen, Daten, Material.
- **Immateriell:** Vertrauen, Ruf, Gesundheit, Persönlichkeitsrechte.

Die Kette im Überblick und der Ausblick auf das Risiko

Die vier Begriffe lassen sich auf einen Satz bringen: Eine Bedrohung nutzt durch einen Angriff eine Schwachstelle aus und verursacht einen Schaden. Wie wahrscheinlich das ist und wie hoch der Schaden ausfällt, beschreibt das Risiko (Eintrittswahrscheinlichkeit und Schadenshöhe). Es ist nicht Gegenstand dieses Kapitels, sondern wird in der Schutzbedarfsanalyse in Kapitel 4 bewertet.

Begriff | Frage | Beispiel RECPLAST
Schwachstelle | Was ist die Lücke? | Passwort auf dem Notizzettel am Leitstand
Bedrohung | Wer oder was könnte sie nutzen? | Unbefugte Personen mit Zutritt zur Halle
Angriff | Wie wird sie genutzt? | Anmeldung mit dem Gruppenkonto und Änderung der Rezeptur
Schaden | Was ist die Folge? | 8 Tonnen unbrauchbares Granulat (Integrität)

Praxisbeispiel: Einen Vorfall in die Kette einordnen

Ein Lieferant ruft an und meldet, seine Systeme seien durch Ransomware verschlüsselt, er könne vorerst nicht liefern. Das Beispiel zeigt, wie Sie einen Vorfall in drei Schritten zerlegen:

+--------------------------------------------------------+
| Schritt 1 - Schaden beschreiben                        |
| Was ist eingetreten, welches Schutzziel ist betroffen? |
| Lieferung fällt aus -> Verfügbarkeit (Lieferkette)     |
+--------------------------------------------------------+
                           |
                           v
+--------------------------------------------------------+
| Schritt 2 - Angriff und Bedrohung benennen             |
| Wie kam es dazu, wer oder was steckt dahinter?         |
| Ransomware-Angriff, Bedrohung: Schadprogramme          |
+--------------------------------------------------------+
                           |
                           v
+--------------------------------------------------------+
| Schritt 3 - Schwachstelle suchen                       |
| Warum hat es geklappt, was war die Lücke?              |
| Hier unbekannt, mögliche Kandidaten: fehlende Updates, |
| Phishing-Mail, ungesicherter Fernzugang                |
+--------------------------------------------------------+

Beachten Sie die Reihenfolge: Bei einem echten Vorfall kennen Sie meist zuerst den Schaden und müssen die Ursache rückwärts ermitteln. Ob die Schwachstelle beim Lieferanten lag, bleibt oft offen. Für die RECPLAST GmbH bleibt der Schaden dennoch real, auch wenn die eigene IT nicht angegriffen wurde.

--- 

### M|3.0.2: Penetrationstest

Penetrationstest

Ein Penetrationstest, kurz Pentest, ist ein vereinbarter, kontrollierter Angriff auf ein Unternehmen mit dem Ziel, Schwachstellen zu finden, bevor es echte Angreifer tun. Die Testenden gehen dabei so vor wie Kriminelle, haben aber einen Auftrag, einen festen Rahmen und die Pflicht, ihre Ergebnisse offenzulegen. Weil sie im Auftrag der Geschäftsführung und mit guter Absicht handeln, spricht man auch von White-Hat-Hackern oder ethischen Hackern. Ein Angreifer ohne Erlaubnis und mit eigennützigen Zielen wird dagegen Black-Hat-Hacker genannt.

Damit ein Pentest nützlich und rechtmäßig ist, greifen drei Dinge ineinander. Ein fester Ablauf sorgt dafür, dass systematisch statt zufällig getestet wird. Die Wahl der Testart bestimmt, wie viel die Testenden vorab wissen und wo sie ansetzen. Der Rechtsrahmen legt fest, was erlaubt ist, und trennt den Pentest von einer Straftat. Fehlt der Rahmen, wird aus dem Test ein Rechtsverstoß, und fehlt die Auswertung, bleibt der Test ohne Nutzen.

Die drei Bausteine

**Ablauf eines Penetrationstests**

Ein Pentest folgt in der Regel denselben Phasen, die auch echte Angreifer durchlaufen. Der Unterschied liegt am Ende: Die Testenden dokumentieren ihre Ergebnisse und übergeben sie mit Handlungsempfehlungen an das Unternehmen.

- **1. Informationsbeschaffung:** Öffentlich verfügbare Informationen sammeln, etwa über die Firma, ihre Mitarbeitenden, Standorte, Ausweise auf Social-Media-Fotos oder Stellenanzeigen mit Hinweisen auf eingesetzte Technik (OSINT, Open Source Intelligence).
- **2. Angriffsvektoren finden:** Aus den Informationen ableiten, an welchen Stellen ein Eindringen möglich sein könnte: Türen, Fenster, Netzwerkzugänge, Personen, Fremdfirmen, veraltete Systeme.
- **3. Eindringen (Exploiting):** Die gefundenen Schwachstellen kontrolliert ausnutzen, um zu belegen, dass der Zugang wirklich möglich ist. Meist wird nur der Nachweis erbracht und kein echter Schaden angerichtet.
- **4. Dokumentation und Bericht:** Alle Schritte, Funde und Belege festhalten, die Risiken bewerten und konkrete Empfehlungen geben. Dieser Schritt macht den Pentest erst wertvoll.

*💻 Beispiel aus der IT-Praxis: Ein Pentester findet auf einem Karriereportal Fotos von Mitarbeitenden mit sichtbarem Firmenausweis. Er druckt eine ähnliche Karte, tritt in Warnweste am Hintereingang auf und wird von der Mitarbeiterin hereingelassen, die ihm die Tür aufhält. Im Bericht steht der Fund mit Foto und Uhrzeit, dazu die Empfehlung, Ausweise zu schulen und Hintereingänge zu sichern.*

**Testarten und Angriffsflächen**

Pentests unterscheiden sich darin, wie viel Wissen die Testenden vorab haben und von wo aus sie angreifen. Je weniger Vorwissen, desto realistischer ist die Simulation eines fremden Angreifers, je mehr Vorwissen, desto gründlicher lässt sich in kurzer Zeit prüfen. Außerdem kann an verschiedenen Stellen getestet werden, denn Angriffe erfolgen nicht nur über das Netzwerk.

- **Black Box:** Die Testenden erhalten keine Informationen über das Ziel und gehen wie ein Außenstehender vor.
- **Grey Box:** Die Testenden erhalten begrenzte Informationen, etwa ein normales Benutzerkonto.
- **White Box:** Die Testenden kennen Aufbau, Konfiguration und Dokumentation und prüfen sehr gründlich.
- **Angriffsfläche:** Technisch (Netzwerk, Server, Webanwendungen), physisch (Gebäude, Räume, Schlüssel), organisatorisch (Prozesse, Fremdfirmen) und menschlich (Social Engineering).

*💻 Beispiel aus der IT-Praxis: Eine Geschäftsführung beauftragt zuerst einen Black-Box-Test von außen, um zu sehen, was ein Fremder erreicht. Nach der Behebung der gefundenen Lücken folgt ein Grey-Box-Test mit dem Konto eines normalen Mitarbeiters, um zu prüfen, wie weit sich ein Täter im Inneren bewegen kann.*

**Rechtsrahmen: Was Pentest und Straftat trennt**

Ein Pentest ist nur legal, wenn der Auftraggeber ihn ausdrücklich erlaubt hat. Ohne Erlaubnis können dieselben Handlungen Straftaten sein, zum Beispiel Ausspähen von Daten (§ 202a StGB), das Vorbereiten solcher Taten durch bestimmte Hackerwerkzeuge (§ 202c StGB) oder Hausfriedensbruch (§ 123 StGB). Deshalb wird der Auftrag schriftlich festgehalten, und es wird genau bestimmt, was getestet werden darf und was nicht.

- **Auftrag und Einwilligung:** Schriftliche Erlaubnis einer befugten Person, in der Regel der Geschäftsführung.
- **Scope (Geltungsbereich):** Welche Gebäude, Systeme und Personen getestet werden dürfen und welche nicht.
- **Regeln und Grenzen:** Zeitraum, erlaubte Methoden, Umgang mit gefundenen Daten, keine Beschädigung, Abbruch bei Gefahr.
- **Dritte:** Systeme von Dienstleistern oder Cloud-Anbietern dürfen nur mit deren Zustimmung getestet werden.
- **Notfallkontakt:** Eine Ansprechperson, die bei Rückfragen oder Alarm den Test bestätigen kann.

*💻 Beispiel aus der IT-Praxis: Ein Pentester wird in einer Halle von einem Mitarbeiter gestellt, der die Polizei rufen will. Er zeigt sein Schreiben mit der Unterschrift der Geschäftsführung und nennt die Notfallnummer, die im Vorfeld vereinbart wurde. Der Mitarbeiter ruft dort an, die Situation klärt sich. Ohne dieses Schreiben wäre es Hausfriedensbruch.*

Praxisbeispiel: Ein Pentest für eine Spedition

Eine mittelständische Spedition beauftragt einen Pentest von Lager, Büro und Netzwerk. Der Ablauf von der Beauftragung bis zur Umsetzung läuft in drei Schritten ab:

+--------------------------------------------------------+
| Schritt 1 - Auftrag und Rahmen klären                  |
| Schriftlicher Auftrag der Geschäftsführung, Scope:     |
| Lager, Büro, internes Netz. Nicht: Kundensysteme.      |
| Zeitraum und Notfallkontakt festgelegt.                |
+--------------------------------------------------------+
                           |
                           v
+--------------------------------------------------------+
| Schritt 2 - Testen und belegen                         |
| Informationen sammeln, Angriffswege finden, Zutritt    |
| und Netzzugang nachweisen. Fotos und Protokolle als    |
| Beleg, keine Daten kopieren oder verändern.            |
+--------------------------------------------------------+
                           |
                           v
+--------------------------------------------------------+
| Schritt 3 - Auswerten und umsetzen                     |
| Bericht mit Funden und Risikobewertung, Empfehlungen   |
| priorisieren, Schulungen und technische Maßnahmen      |
| planen, später mit einem Nachtest prüfen.              |
+--------------------------------------------------------+

Der Pentest endet nicht mit dem Eindringen, sondern mit der Verbesserung. Die Erkenntnisse münden häufig in Schulungen für die Belegschaft, weil sich zeigt, dass viele Lücken im Verhalten liegen und nicht in der Technik.

---

## Kompetenz 3.1: Angriffsmethoden und Gegenmaßnahmen unterscheiden

Die Bearbeitungszeit für den Austausch in der Gruppe abgelaufen. Der Sicherheitsexperte der ChangeIT GmbH hat die gesammelten Angriffsszenarien aus dem Brainstorming an die Wand gehängt. Frau Weber blickt auf die lange Liste:

"Das sind viele Begriffe durcheinander. Ich möchte, dass jeder in der Schulung versteht, wie diese Angriffe ablaufen und was man dagegen tun kann."

---

### A|3.1: Steckbriefe zu Angriffsmethoden erstellen

#### Aufgabe 1

Bilden Sie Gruppen. Jedes Gruppenmitglied bearbeitet eine der vier Angriffsmethoden und liest das zugehörige Material:

- M|3.1.0: Malware und Ransomware
- M|3.1.1: Social Engineering
- M|3.1.2: Angriffe auf Netzwerke und WLAN
- M|3.1.3: Physischer Zutritt und Wechselmedien

#### Aufgabe 2

Erstellen Sie für Ihre Angriffsmethode einen Steckbrief. Übertragen Sie dazu die folgende Tabelle und füllen Sie sie aus.

| Feld | Ihr Eintrag |
| --- | --- |
| Name der Angriffsmethode |  |
| Ablauf in drei Schritten |  |
| Ziel des Angreifers |  |
| Angriffsvektor |  |
| Betroffenes Schutzziel |  |
| Phase im Penetrationstest (A|3.0) |  |
| Beispiel aus dem Fernsehbeitrag, aus Kapitel 2 oder aus dem Brainstorming |  |

#### Aufgabe 3

Ergänzen Sie Ihren Steckbrief um Gegenmaßnahmen. Informieren Sie sich dazu in M|3.1.4: Virenschutz und Personal Firewall und in Ihren Materialien aus Kapitel 2.

##### Aufgabenteil a

Nennen Sie eine technische Gegenmaßnahme.

##### Aufgabenteil b

Nennen Sie eine organisatorische Gegenmaßnahme.

##### Aufgabenteil c

Nennen Sie eine personelle Gegenmaßnahme.

#### Aufgabe 4

Stellen Sie Ihren Steckbrief Ihrer Gruppe in zwei Minuten vor und fügen Sie alle Steckbriefe in einer gemeinsamen Übersicht (in einer Datei) zusammen. Markieren Sie, welche Gegenmaßnahme bei mehreren Angriffsmethoden wirkt.

---

### M|3.1.0: Malware und Ransomware

Malware und Ransomware

Im Alltag spricht man von „Viren“, wenn auf dem Rechner etwas Schädliches läuft. Als Fachbegriff ist Malware (Schadsoftware) der Oberbegriff für alle Programme, die absichtlich entwickelt wurden, um Systeme zu stören, Daten zu stehlen oder Zugriff zu erlangen. Ransomware ist eine besonders folgenreiche Art davon: Sie verschlüsselt Daten und fordert Lösegeld für die Freigabe. Dabei kommt es weniger auf den Namen der Schadsoftware an als auf drei Fragen: Wie gelangt sie auf das System, was richtet sie an, und welches Schutzziel trifft sie?

Die zwei Bausteine

**Arten von Malware**

Malware wird nach Verbreitung und Wirkung unterschieden. Mehrere Funktionen können in einem Programm kombiniert sein.

- **Virus:** Hängt sich an andere Dateien und verbreitet sich, wenn diese weitergegeben oder geöffnet werden.
- **Wurm:** Verbreitet sich selbstständig über Netzwerke, ohne dass jemand eine Datei öffnen muss.
- **Trojaner:** Tarnt sich als nützliches Programm, etwa als Update, und führt im Hintergrund Schadfunktionen aus.
- **Spyware und Keylogger:** Spionieren Eingaben, Passwörter und Daten aus.
- **Backdoor und Botnet:** Öffnen einen Fernzugang oder machen den Rechner zum Teil eines ferngesteuerten Netzes, etwa für DDoS-Angriffe.

*💻 Beispiel aus der IT-Praxis: Ein Techniker lädt von einer unbekannten Webseite ein angebliches Treiber-Update für eine Industriesteuerung herunter. Das Programm funktioniert, installiert aber zusätzlich einen Keylogger. Der Angreifer liest wochenlang Zugangsdaten mit, ohne dass jemand etwas merkt.*

**Ransomware und Erpressung**

Ransomware verschlüsselt Dateien auf dem infizierten Rechner und auf erreichbaren Netzlaufwerken. Anschließend erscheint eine Lösegeldforderung, meist verbunden mit einer Frist. Heute stehlen die Täter die Daten häufig zusätzlich und drohen mit der Veröffentlichung (doppelte Erpressung). Damit trifft ein Angriff gleich zwei Schutzziele: Die Verfügbarkeit wird zerstört, und die Vertraulichkeit ist verletzt. Zahlung garantiert weder die Entschlüsselung noch die Löschung der Daten, und Fachstellen raten davon ab.

- **Infektionsweg:** Phishing-Mails mit Anhang oder Link, Dokumente mit Makros, ungepatchte Server, offene Fernzugänge, Wechselmedien.
- **Ausbreitung:** Der Angreifer sucht nach Rechten und Netzlaufwerken und verschlüsselt auch Server und Sicherungen, die erreichbar sind.
- **Folge für Dritte:** Fällt ein Lieferant oder Dienstleister aus, trifft der Schaden auch dessen Kunden (Lieferkette).
- **Schutz:** Aktuelle Updates, eingeschränkte Rechte, Netzwerksegmentierung und vor allem getrennte, getestete Backups (siehe M|2.17.0: Backup-Strategien).

*💻 Beispiel aus der IT-Praxis: Ein Mitarbeiter öffnet einen Rechnungsanhang, und Minuten später sind Freigaben und Datenbanken verschlüsselt. Das NAS mit den Backups hing im selben Netz und ist ebenfalls betroffen. Gerettet wird nur, was auf einem getrennten, unveränderbaren Speicher liegt.*

Praxisbeispiel: Der Ablauf eines Ransomware-Angriffs

+--------------------------------------------------------+
| Schritt 1 - Einstieg                                   |
| Mitarbeiterin öffnet einen präparierten Anhang aus     |
| einer Mail. Schadcode wird nachgeladen. (Vektor: Mail) |
+--------------------------------------------------------+
                           |
                           v
+--------------------------------------------------------+
| Schritt 2 - Ausbreitung                                |
| Angreifer erlangt höhere Rechte, durchsucht das Netz,  |
| kopiert Daten und löscht oder verschlüsselt Backups.   |
+--------------------------------------------------------+
                           |
                           v
+--------------------------------------------------------+
| Schritt 3 - Erpressung                                 |
| Dateien werden verschlüsselt, Lösegeld wird gefordert. |
| Betroffen: Verfügbarkeit und Vertraulichkeit.          |
+--------------------------------------------------------+

---

### M|3.1.1: Social Engineering

Social Engineering

Viele verbinden „Hacken“ mit Programmcode und Tastaturgeklapper. Als Fachbegriff bedeutet Social Engineering, dass Angreifer nicht die Technik, sondern den Menschen überlisten. Sie nutzen Vertrauen, Hilfsbereitschaft, Zeitdruck oder Neugier, um an Informationen, Zugänge oder Handlungen zu kommen. Das Material knüpft an M|2.8.1: Awareness-Schulungen an und stellt Methoden und Auslöser nebeneinander. Eine Mail, ein Anruf oder ein Besuch sind nur Kanäle. Entscheidend ist, wie der Angreifer eine Situation aufbaut, in der die Zielperson freiwillig handelt.

Die zwei Bausteine

**Methoden**

Social Engineering tritt in vielen Formen auf, die sich nach Kanal und Aufwand unterscheiden.

- **Phishing:** Massenhafte gefälschte Mails oder Webseiten, die zum Preisgeben von Zugangsdaten oder zum Öffnen eines Anhangs verleiten.
- **Spear-Phishing und CEO-Fraud:** Gezielte Nachrichten an eine bestimmte Person, oft mit Namen und Insiderwissen, etwa als angebliche Geschäftsführung mit Zahlungsauftrag.
- **Vishing und Smishing:** Betrug per Telefonanruf oder SMS.
- **Pretexting:** Ein erfundener Vorwand, etwa als IT-Support oder Wartungsfirma, um Informationen zu erhalten.
- **Baiting:** Ein Köder wie ein „verlorener“ USB-Stick, der Neugier weckt (siehe M|3.1.3).

*💻 Beispiel aus der IT-Praxis: Eine Buchhalterin erhält eine Mail der angeblichen Geschäftsführung mit der Bitte, eine dringende Überweisung an eine neue Bankverbindung zu veranlassen. Absender, Ton und Unterschrift wirken echt, denn der Täter hat sie aus Webseite und Netzwerkprofilen gesammelt.*

**Warum es funktioniert**

Die Angreifer nutzen psychologische Auslöser, die im Alltag nützlich sind und deshalb schwer abzulegen. Wer sie kennt, bemerkt sie eher.

- **Autorität:** Anweisungen von vermeintlich Vorgesetzten oder Behörden werden selten hinterfragt.
- **Zeitdruck:** „Sofort“, „heute noch“ und „sonst Sperrung“ verhindern Nachdenken.
- **Hilfsbereitschaft und Vertrauen:** Wer freundlich bittet, bekommt Hilfe.
- **Neugier und Angst:** Ein spannender Anhang oder eine angebliche Kontosperrung verleiten zum Klick.
- **Vorbereitung:** Mit Informationen aus öffentlichen Quellen (OSINT) wirkt der Angreifer glaubwürdig.

*💻 Beispiel aus der IT-Praxis: Ein Anrufer meldet sich als „externer IT-Techniker im Auftrag der Leitung“ und braucht dringend ein Passwort für ein Update. Autorität und Zeitdruck wirken zusammen. Der Angreifer kennt den Namen der Leiterin aus der Firmenwebseite.*

Praxisbeispiel: Der Ablauf eines Social-Engineering-Angriffs

+--------------------------------------------------------+
| Schritt 1 - Informationen sammeln                      |
| Namen, Rollen, Kontakte, Ausweisfotos, Firmenkultur    |
| aus Webseite und sozialen Netzwerken zusammentragen.   |
+--------------------------------------------------------+
                           |
                           v
+--------------------------------------------------------+
| Schritt 2 - Vorwand aufbauen und Kontakt aufnehmen     |
| Als Techniker, Lieferant oder Vorgesetzter auftreten,  |
| Druck oder Vertrauen erzeugen.                         |
+--------------------------------------------------------+
                           |
                           v
+--------------------------------------------------------+
| Schritt 3 - Ziel erreichen                             |
| Passwort, Zutritt oder Überweisung erhalten.           |
| Betroffen: meist Vertraulichkeit, oft auch Integrität. |
+--------------------------------------------------------+

Wirksame Gegenmaßnahmen sind einfache Regeln wie der Rückruf über eine bekannte Nummer, die Meldung verdächtiger Vorfälle ohne Schuldzuweisung und das Vier-Augen-Prinzip bei Zahlungen.

---

### M|3.1.2: Angriffe auf Netzwerke und WLAN

Angriffe auf Netzwerke und WLAN

Netzwerke und ihre Funkverbindungen bilden eine Angriffsfläche, über die Angreifer mitlesen, sich einschleichen oder Dienste lahmlegen können. Dabei kommt es darauf an, wo der Angreifer ansetzt: von außen über das Internet, von innen im Netz oder über die Funkschnittstelle in Reichweite des Gebäudes. Das Material ergänzt die Netzwerksegmentierung und die Schnittstellen aus M|2.1.0 und M|2.5.0.

Die zwei Bausteine

**Angriffe über das Netzwerk**

Netzwerkangriffe nutzen offene Zugänge, unverschlüsselte Verbindungen oder veraltete Systeme.

- **Scannen und Aufklären:** Angreifer suchen erreichbare Systeme, offene Ports und veraltete Dienste.
- **Mitlesen (Sniffing):** Unverschlüsselte Datenpakete werden abgehört, wenn der Angreifer im Netz sitzt.
- **Man-in-the-Middle:** Der Angreifer schaltet sich unbemerkt zwischen zwei Kommunikationspartner und liest oder verändert den Datenverkehr.
- **Ausnutzen von Schwachstellen:** Veraltete oder falsch konfigurierte Systeme und Fernwartungszugänge, besonders in Produktionsnetzen (OT).
- **Überlastung (DDoS):** Ein Dienst wird mit Anfragen überflutet, bis er nicht mehr erreichbar ist.

*💻 Beispiel aus der IT-Praxis: In einem Produktionsnetz läuft eine Steuerung seit Jahren ohne Updates und ist über einen Fernwartungszugang aus dem Internet erreichbar. Ein Scan findet den offenen Dienst, ein bekannter Fehler genügt für den Zugriff.*

**Angriffe über WLAN**

Funknetze reichen über die Gebäudegrenze hinaus, deshalb muss ein Angreifer nicht im Haus sein. Die Gefahr liegt oft in schwachen Einstellungen oder gefälschten Zugangspunkten.

- **Schwache Verschlüsselung und Passwörter:** Veraltete Verfahren oder kurze gemeinsame Schlüssel lassen sich knacken.
- **Rogue Access Point und Evil Twin:** Ein unerlaubter oder nachgebauter Zugangspunkt täuscht ein bekanntes Netz vor, die Geräte verbinden sich und der Verkehr läuft über den Angreifer.
- **Gäste im Firmennetz:** Wer im Gastnetz Zugang zum internen Netz hat, hat zu viele Rechte.
- **Schutz:** Aktuelle Verschlüsselung (WPA2/WPA3), individuelle Zugänge (WPA2/WPA3-Enterprise), getrenntes Gastnetz und Kontrolle fremder Zugangspunkte.

*💻 Beispiel aus der IT-Praxis: Ein Angreifer richtet im Besucherbereich einen Zugangspunkt mit dem Namen „RECPLAST-Gast“ ein. Mehrere Geräte verbinden sich automatisch. Er liest unverschlüsselte Verbindungen mit und fängt Anmeldedaten ab.*

Praxisbeispiel: Der Ablauf eines Angriffs über das Netzwerk

+--------------------------------------------------------+
| Schritt 1 - Erkunden                                   |
| Erreichbare Systeme, offene Ports und WLAN-Netze in    |
| Reichweite finden. (Vektor: Netzwerk oder Funk)        |
+--------------------------------------------------------+
                           |
                           v
+--------------------------------------------------------+
| Schritt 2 - Zugang erlangen                            |
| Veraltetes System ausnutzen, Passwort erraten oder     |
| Verbindung abfangen.                                   |
+--------------------------------------------------------+
                           |
                           v
+--------------------------------------------------------+
| Schritt 3 - Auswirkung                                 |
| Daten mitlesen (Vertraulichkeit), Steuerung verändern  |
| (Integrität) oder Dienste stören (Verfügbarkeit).      |
+--------------------------------------------------------+

---

### M|3.1.3: Physischer Zutritt und Wechselmedien

Physischer Zutritt und Wechselmedien

Zur IT-Sicherheit gehören nicht nur Bildschirm und Software, sondern auch Türen, Schlüssel und Datenträger, denn wer ein Gebäude oder einen Rechner betreten kann, umgeht viele digitale Schutzmaßnahmen. Zwei Wege sind besonders wichtig: der unbefugte Zutritt in Räume und das Einschleusen oder Mitnehmen von Daten über Wechselmedien wie USB-Sticks. Dieses Material knüpft an M|2.5.0, M|2.7.1 und M|2.7.2 an.

Die zwei Bausteine

**Unbefugter Zutritt**

Angreifer nutzen Lücken in der Bauweise, in Abläufen und im Verhalten der Beschäftigten, um Räume zu betreten.

- **Offene Zugänge:** Angelehnte Türen, offene Fenster, unbewachte Nebeneingänge.
- **Tailgating:** Ein Fremder folgt einer berechtigten Person durch eine gesicherte Tür, oft höflich mit vollen Händen.
- **Vorwand und Verkleidung:** Auftreten als Handwerker, Techniker oder Lieferant mit Warnweste und Werkzeug.
- **Schlüssel und Zutrittsmedien:** Unbewachte Schlüssel oder kopierbare Chipkarten (RFID) öffnen Türen ohne Gewalt.
- **Schutz:** Zutrittskontrolle mit Protokoll, Besucherausweis und Begleitpflicht, Schlüsselverwaltung, Aufmerksamkeit der Belegschaft.

*💻 Beispiel aus der IT-Praxis: Ein Mann in Warnweste und mit Werkzeugkasten läuft durch die Halle. Niemand fragt nach, weil Fremdfirmen häufig kommen. Er erreicht den unverschlossenen Verteilerraum und könnte dort Geräte anstecken oder manipulieren.*

**Wechselmedien und Geräte**

Auch kleine Geräte stellen ein Risiko dar, weil Rechner ihnen oft vertrauen. Ein USB-Stick kann Schadsoftware enthalten oder sich als Tastatur ausgeben und selbstständig Befehle eingeben. Umgekehrt lassen sich auf einem Stick unbemerkt Daten mitnehmen.

- **Baiting:** Ein „gefundener“ USB-Stick weckt Neugier, wer ihn einsteckt, startet womöglich Schadcode.
- **Manipulierte Geräte:** USB-Geräte, die sich als Tastatur ausgeben, oder angesteckte Hardware wie Keylogger an Schnittstellen.
- **Datenabfluss:** Vertrauliche Daten werden ohne Spuren auf Datenträger kopiert.
- **Schutz:** USB-Ports sperren oder nur freigegebene Geräte zulassen, Anwendungskontrolle, Regeln für Wechselmedien und klare Meldewege.

*💻 Beispiel aus der IT-Praxis: Ein Techniker steckt einen unbekannten Stick „nur kurz“ in einen Leitstand-PC, um ein Update einzuspielen. Das Gerät installiert im Hintergrund Schadcode, den der Virenschutz zunächst nicht erkennt.*

Praxisbeispiel: Der Ablauf eines Angriffs über physischen Zutritt

+--------------------------------------------------------+
| Schritt 1 - Einlass finden                             |
| Offenes Fenster, Tailgating oder Vorwand als           |
| Wartungsfirma. (Vektor: Mensch und Gebäude)            |
+--------------------------------------------------------+
                           |
                           v
+--------------------------------------------------------+
| Schritt 2 - Zugriff auf Geräte und Schlüssel           |
| Unbeaufsichtigte Rechner, Schlüsselbund oder Stick     |
| nutzen, um Schadcode zu starten oder Daten zu kopieren.|
+--------------------------------------------------------+
                           |
                           v
+--------------------------------------------------------+
| Schritt 3 - Auswirkung                                 |
| Daten abfließen (Vertraulichkeit), Konfiguration       |
| verändert (Integrität), Anlage gestört (Verfügbarkeit).|
+--------------------------------------------------------+

---

### M|3.1.4: Virenschutz und Personal Firewall

Virenschutz und Personal Firewall

Virenschutz und Personal Firewall sind technische Schutzmaßnahmen auf dem einzelnen Rechner (Endpoint), die Schadsoftware erkennen und Netzwerkverbindungen kontrollieren. Beide wirken vor allem gegen die technischen Teile eines Angriffs, aber nur begrenzt gegen Täuschung von Menschen oder gegen offene Türen. Deshalb ergänzen sie organisatorische und personelle Maßnahmen und ersetzen diese nicht.

Die zwei Bausteine

**Virenschutz**

Ein Virenschutz (Antivirus, heute oft als Endpoint Protection oder EDR) prüft Dateien und Prozesse auf Schadsoftware und blockiert sie.

- **Signaturbasiert:** Bekannte Schadsoftware wird anhand von Merkmalen erkannt. Die Signaturen müssen laufend aktualisiert werden.
- **Verhaltensbasiert:** Auffälliges Verhalten, etwa massenhaftes Verschlüsseln von Dateien, wird erkannt und gestoppt.
- **Zentrale Verwaltung:** Alle Geräte melden an eine Konsole, die Vorfälle und Updates im Überblick behält.
- **Grenzen:** Neue oder gezielt angepasste Schadsoftware wird teilweise nicht erkannt, und der Schutz greift nicht, wenn jemand Zugangsdaten freiwillig herausgibt.

*💻 Beispiel aus der IT-Praxis: Der Virenschutz auf einem Leitstand-PC meldet verdächtige Skriptaktivität nach dem Einstecken eines Sticks und isoliert den Rechner vom Netz. Der Admin sieht den Vorfall zentral in der Konsole und prüft ihn.*

**Personal Firewall**

Eine Personal Firewall läuft auf dem Endgerät selbst und entscheidet anhand von Regeln, welche Verbindungen erlaubt sind. Sie ergänzt die Firewall am Netzübergang und schützt auch dann, wenn ein Gerät außerhalb des Firmennetzes betrieben wird.

- **Eingehend:** Nur erforderliche Dienste und Ports sind erreichbar, alles andere wird blockiert.
- **Ausgehend:** Programme dürfen nur nach Freigabe ins Internet. So lässt sich verhindern, dass Schadsoftware Daten sendet oder Befehle nachlädt.
- **Regeln pro Anwendung:** Die Freigabe richtet sich nach Programm, Port und Netzwerkprofil (Büro, Produktion, öffentlich).
- **Grundsatz:** Wie beim Principle of Least Privilege gilt, dass nur erlaubt wird, was nötig ist.

*💻 Beispiel aus der IT-Praxis: Auf einem Industrieterminal sperrt die Windows-Firewall den Internetzugriff für alle Programme außer der Steuerungssoftware, die mit einem festen Server spricht. Ein eingeschleppter Trojaner kann dadurch seine Zentrale nicht erreichen.*

Zusammenspiel mit anderen Maßnahmen

Beide Werkzeuge helfen nur zusammen mit aktuellen Updates, eingeschränkten Rechten, Datensicherung und geschultem Personal. Wer sich nur auf die Software verlässt, wiegt sich in Scheinsicherheit.

---

## Kompetenz 3.2: Schadensszenarien einordnen und Bedrohungen gewichten

Die Steckbriefe aus der letzten Runde hängen an der Wand. Frau Weber nickt zufrieden, wendet sich dann aber an die Beschäftigten der RECPLAST GmbH:

“Jetzt wird es konkret. Zwei von Ihnen haben mir in der Pause von Vorfällen berichtet, die mich beschäftigen. Frau Keller, Herr Brandt, schildern Sie das bitte noch einmal für alle.”

Frau Keller aus dem Einkauf berichtet: “Unser wichtigster Lieferant für Additive hat sich heute Morgen gemeldet. Er ist von einem Ransomware-Angriff betroffen und kann vorerst weder Bestellungen annehmen noch liefern. Seine Mailadressen funktionieren nicht, wir erreichen ihn nur auf dem Handy. Wir haben Material für etwa vier Tage im Lager.”

Herr Brandt aus der Personalabteilung ergänzt: “Bei uns gehen täglich Initiativbewerbungen als Word-Dokumente ein. Wir öffnen sie, weil wir sie lesen müssen, und fragen nicht jedes Mal in der IT nach. Die Dokumente enthalten Lebensläufe, Zeugnisse und Fotos.”

Der Sicherheitsexperte der ChangeIT GmbH fasst zusammen: “Beide Berichte zeigen, dass die gleiche Bedrohung in jeder Abteilung etwas anderes anrichtet. Ordnen Sie ein, welche Schäden entstehen können, und gewichten Sie die Bedrohungen. Frau Weber braucht das als Grundlage für die weitere Planung.”

---

### A|3.2: Berichte aus den Abteilungen bewerten

#### Aufgabe 1

Fassen Sie die beiden Berichte der Beschäftigten kurz zusammen. Notieren Sie jeweils die Abteilung, die Bedrohung und die Schwachstelle.

#### Aufgabe 2

Informieren Sie sich in M|3.2.0: Schadenskategorien und ordnen Sie mögliche Schäden aus den beiden Berichten den Kategorien zu. Übertragen Sie dazu die folgende Tabelle und füllen Sie sie aus.

| Schadenskategorie | Einkauf (Lieferant mit Ransomware) | Personal (Word-Bewerbungen) | Direkt oder indirekt |
| --- | --- | --- | --- |
| Finanzielle Auswirkungen |  |  |  |
| Beeinträchtigung der Aufgabenerfüllung |  |  |  |
| Verstoß gegen Gesetze, Vorschriften oder Verträge |  |  |  |
| Negative Innen- oder Außenwirkung |  |  |  |

#### Aufgabe 3

Der Lieferant wurde angegriffen, nicht die RECPLAST GmbH. Informieren Sie sich in M|3.2.1: Lieferkette und Abhängigkeiten.

##### Aufgabenteil a

Erklären Sie, warum der Angriff trotzdem einen Schaden bei der RECPLAST GmbH verursacht.

##### Aufgabenteil b

Welche Schutzziele sind betroffen, wenn der Angreifer beim Lieferanten auch Daten abgreift, die RECPLAST betreffen?

#### Aufgabe 4

Gewichten Sie die Bedrohungen aus Ihren Steckbriefen für drei Abteilungen. Bewerten Sie den möglichen Schaden mit gering, mittel oder hoch und begründen Sie Ihre Einschätzung in einem Satz. Übertragen Sie dazu die folgende Tabelle und füllen Sie sie aus.

| Bedrohung | Produktion | Einkauf | Personal |
| --- | --- | --- | --- |
| Ransomware |  |  |  |
| Social Engineering (z. B. falscher Techniker, gefälschte Zahlungsaufforderung) |  |  |  |
| Angriff über Netzwerk oder WLAN |  |  |  |
| Unbefugter Zutritt oder Wechselmedien |  |  |  |

#### Aufgabe 5

Frau Weber fragt: “Welche Bedrohung wiegt für welche Abteilung am schwersten?”

##### Aufgabenteil a

Wählen Sie für jede Abteilung die Bedrohung mit dem höchsten möglichen Schaden aus.

##### Aufgabenteil b

Begründen Sie, warum dieselbe Bedrohung in den Abteilungen unterschiedlich gewichtet wird.

---

### M|3.2.0: Schadenskategorien

Schadenskategorien

Wenn nach einem Vorfall die Frage „Wie schlimm ist das?“ gestellt wird, antworten viele zuerst mit einer Geldsumme. Die Ausfallkosten sind wichtig, aber sie sind nur ein Teil des Schadens. Ein Sicherheitsvorfall kann Gesetze verletzen, Menschen gefährden, Aufträge kosten oder das Vertrauen von Kunden zerstören. Um solche Folgen vergleichbar zu machen, unterteilt der IT-Grundschutz des BSI Schäden in Kategorien. Mit ihnen lässt sich systematisch prüfen, wo ein Vorfall wirkt, statt nur auf das Offensichtliche zu schauen.

Drei Bausteine gehören zusammen. Die Schadenskategorien legen fest, wo nach Folgen gesucht wird. Die Unterscheidung nach direkt und indirekt, materiell und immateriell sowie nach Zeitverlauf zeigt, wie sich Schäden entwickeln. Die Gewichtung stuft die Schäden ein und bildet die Grundlage für spätere Entscheidungen. Fehlt der erste Baustein, übersieht man ganze Schadensarten, fehlt die Gewichtung, bleibt die Liste ohne Aussage.

Die drei Bausteine

**Die Schadenskategorien nach BSI**

Das BSI nennt sechs Kategorien. Ein Vorfall kann mehrere gleichzeitig betreffen, und jede Kategorie wird getrennt betrachtet.

- **Verstoß gegen Gesetze, Vorschriften oder Verträge:** Etwa Datenschutzverstöße, verletzte Meldepflichten, Vertragsstrafen bei Lieferverzug.
- **Beeinträchtigung des informationellen Selbstbestimmungsrechts:** Personenbezogene Daten werden unbefugt gelesen, weitergegeben oder verändert.
- **Beeinträchtigung der persönlichen Unversehrtheit:** Gefahr für Gesundheit oder Leben, etwa durch manipulierte Steuerungen oder ausgefallene Sicherheitseinrichtungen.
- **Beeinträchtigung der Aufgabenerfüllung:** Geschäftsprozesse oder die Produktion können nicht wie geplant durchgeführt werden.
- **Negative Innen- oder Außenwirkung:** Vertrauensverlust bei Beschäftigten, Kunden, Lieferanten und in der Öffentlichkeit, Imageschaden.
- **Finanzielle Auswirkungen:** Ausfallkosten, Wiederherstellung, entgangene Umsätze, Strafen, Lösegeld.

*💻 Beispiel aus der IT-Praxis: Eine Klinik wird durch Ransomware lahmgelegt. Betroffen sind die Aufgabenerfüllung (Aufnahme und Behandlung verzögern sich), die persönliche Unversehrtheit (Patienten müssen verlegt werden), das informationelle Selbstbestimmungsrecht (Patientendaten abgeflossen), die Außenwirkung (Schlagzeilen) und die Finanzen (Wiederherstellung und Ausfall).*

**Wie sich Schäden unterscheiden**

Neben der Kategorie hilft es, die Art des Schadens zu beschreiben. So erkennen Sie, dass sich Folgen oft erst Tage oder Monate später zeigen.

- **Direkt:** Entsteht unmittelbar durch den Vorfall, etwa Produktionsausfall, Ausschuss oder Wiederherstellungskosten.
- **Indirekt:** Entsteht als Folge, etwa verlorene Aufträge, Vertragsstrafen oder ein schlechterer Ruf.
- **Materiell:** Lässt sich in Geld oder Sachwerten angeben, etwa Maschinen, Material oder Daten.
- **Immateriell:** Lässt sich schwer beziffern, etwa Vertrauen, Ruf oder Persönlichkeitsrechte.
- **Zeitverlauf:** Nach Stunden stehen Betrieb und Ausfallkosten im Vordergrund, nach Tagen Lieferverzug, nach Monaten Rechtsfolgen und Imageschäden.

*💻 Beispiel aus der IT-Praxis: Ein Online-Shop fällt einen Tag aus. Direkt entgehen Umsätze. Indirekt wechseln einige Stammkunden zur Konkurrenz, und eine Bewertungsplattform zeigt Beschwerden an. Der Imageschaden wirkt noch Monate nach, obwohl die Technik längst wieder läuft.*

**Schäden gewichten**

Damit Schäden verglichen werden können, werden sie in Stufen eingeteilt. Der IT-Grundschutz verwendet dafür drei Schutzbedarfskategorien: normal, hoch und sehr hoch. Die Grenzen legt jedes Unternehmen selbst fest, denn ein Verlust von 50.000 Euro ist für einen kleinen Betrieb existenzbedrohend und für einen Konzern verkraftbar. In Kapitel 4 wenden Sie diese Einteilung mit den Vorgaben der RECPLAST GmbH an. Für die Gewichtung in diesem Auftrag genügt eine vorläufige Einschätzung in gering, mittel und hoch.

- **Maßstab:** Der Schaden wird immer aus Sicht des Unternehmens oder der Abteilung bewertet, nicht allgemein.
- **Ohne Wahrscheinlichkeit:** Die Gewichtung beantwortet „Wie schwer wäre es?“, nicht „Wie oft passiert es?“.
- **Begründung:** Jede Einstufung wird in einem Satz begründet, damit sie nachprüfbar bleibt.
- **Dieselbe Bedrohung, andere Wirkung:** Ein Ausfall der Mail trifft den Einkauf mit Lieferanten stärker als die Produktion, die lokal steuert.

*💻 Beispiel aus der IT-Praxis: Ein Admin bewertet den Ausfall des Dateiservers. Für die Buchhaltung ist der Schaden hoch, weil Fristen gelten. Für das Marketing ist er gering, weil es einen Tag mit lokalen Dateien arbeiten kann. Dieselbe Störung erhält so je Abteilung eine andere Gewichtung.*

Praxisbeispiel: Einen Vorfall auf Schadenskategorien prüfen

Ein Handwerksbetrieb erfährt, dass seine Auftragsdatenbank durch Schadsoftware verschlüsselt ist. So gehen Sie in drei Schritten vor:

+--------------------------------------------------------+
| Schritt 1 - Kategorien durchgehen                      |
| Aufgabenerfüllung: Aufträge können nicht geplant       |
| werden. Finanzen: Ausfall und Wiederherstellung.       |
| Gesetze/Verträge: Kundendaten betroffen, Termine.      |
+--------------------------------------------------------+
                           |
                           v
+--------------------------------------------------------+
| Schritt 2 - Art und Zeitverlauf bestimmen              |
| Direkt: Stillstand der Planung am ersten Tag.          |
| Indirekt: Verärgerte Kunden, abgesprungene Aufträge,   |
| Rufschaden nach Wochen.                                |
+--------------------------------------------------------+
                           |
                           v
+--------------------------------------------------------+
| Schritt 3 - Gewichten und begründen                    |
| Aufgabenerfüllung: hoch, da ohne Datenbank kein        |
| Betrieb. Außenwirkung: mittel, Kunden zeigen           |
| Verständnis. Jeweils in einem Satz begründen.          |
+--------------------------------------------------------+

---

### M|3.2.1: Lieferkette und Abhängigkeiten

Lieferkette

Ein Unternehmen arbeitet nie allein. Es bezieht Material, Software, Dienstleistungen und Wartung von Partnern und gibt Daten und Zugänge an sie weiter. Diese Verflechtung nennt man Lieferkette (Supply Chain). Sie macht den Betrieb effizient, schafft aber auch Abhängigkeiten: Fällt ein Partner aus oder wird er angegriffen, trifft das alle, die auf ihn angewiesen sind, auch wenn deren eigene IT unversehrt bleibt. Dieses Material zeigt, wie solche Schäden entstehen und wie sich ihre Wirkung begrenzen lässt.

Zwei Wege führen von einem Partner zu Ihnen. Der Ausfall des Partners unterbricht Ihre Abläufe. Der Angriff über den Partner nutzt dessen Zugänge, Software oder Daten als Einfallstor. Zusätzlich verlangt die Vorsorge, Abhängigkeiten zu kennen und zu steuern, denn Schäden lassen sich nur begrenzen, wenn vorab klar ist, wer wovon abhängt.

Die drei Bausteine

**Ausfall eines Partners**

Ist ein Lieferant oder Dienstleister betroffen, kann er seine Leistung nicht erbringen. Für den Kunden entsteht daraus ein Schaden, obwohl kein Angreifer in seinem Netz war.

- **Verfügbarkeit:** Bestellungen werden nicht angenommen, Material, Software oder Wartung bleiben aus.
- **Kommunikation:** Mailadressen und Systeme des Partners sind nicht erreichbar, Ansprechpersonen sind nur über Umwege erreichbar.
- **Zeitfaktor:** Der Schaden steigt, sobald Lagerbestände aufgebraucht sind.
- **Einzelner Lieferant:** Wer nur einen Lieferanten für ein wichtiges Teil hat, hat einen Single Point of Failure (siehe M|2.15.0: Redundanzkonzepte), diesmal nicht im Netz, sondern in der Beschaffung.

*💻 Beispiel aus der IT-Praxis: Ein Softwarehaus nutzt für seine Rechnungsstellung den Dienst eines einzigen Anbieters. Dieser wird durch einen Angriff lahmgelegt. Es kann zwei Wochen lang keine Rechnungen verschicken, und der Zahlungseingang verzögert sich spürbar.*

**Angriff über Partner**

Partner haben oft Zugänge, Rechte oder Daten, die auch Angreifer interessieren. Schlecht abgesicherte Dienstleister werden deshalb gezielt als Umweg genutzt.

- **Fernwartung und Zugänge:** Ein Wartungszugang, den ein Dienstleister nutzt, wird von Angreifern übernommen.
- **Manipulierte Software:** Ein Update oder eine Komponente des Herstellers enthält Schadcode und wird vertrauensvoll installiert.
- **Daten beim Partner:** Werden beim Lieferanten Daten abgegriffen, sind auch Ihre Konditionen, Bestellungen oder Personendaten betroffen (Vertraulichkeit).
- **Folgeangriffe:** Mit den erbeuteten Informationen entstehen glaubwürdige Mails, etwa mit „neuer Bankverbindung“. Dann ist auch die Integrität berührt.

*💻 Beispiel aus der IT-Praxis: Nach einem Angriff auf einen Zulieferer erhalten dessen Kunden Rechnungen, die echt aussehen, aber eine andere Bankverbindung enthalten. Die Täter kennen Bestellungen, Beträge und Ansprechpartner aus den erbeuteten Daten.*

**Abhängigkeiten steuern**

Vorsorge beginnt damit, dass Abhängigkeiten bekannt, vertraglich geregelt und durch Alternativen abgesichert sind. Das gilt für Lieferanten genauso wie für Fremdfirmen mit Zugang zur Anlage.

- **Überblick:** Liste der wichtigsten Lieferanten und Dienstleister mit Kritikalität und Ersatzmöglichkeiten.
- **Verträge:** Sicherheitsanforderungen, Meldepflichten bei Vorfällen und Reaktionszeiten (SLA) festlegen.
- **Alternativen:** Zweiter Lieferant, Sicherheitsbestand im Lager, Notfallplan für den Ausfall.
- **Zugänge:** Dienstleister erhalten nur die Rechte, die sie brauchen, zeitlich begrenzt und protokolliert (siehe M|2.4.0: Principle of Least Privilege).
- **Prüfung:** Nachfragen und Kontrollen zum Sicherheitsniveau wichtiger Partner.

*💻 Beispiel aus der IT-Praxis: Ein Admin pflegt eine Liste aller Dienstleister mit Fernzugang. Jeder Zugang ist personalisiert, mit Zwei-Faktor-Anmeldung gesichert und wird nur nach Anmeldung für einen vereinbarten Zeitraum freigeschaltet. Bei einem Vorfall beim Dienstleister lässt sich der Zugang sofort sperren.*

Praxisbeispiel: Wenn ein Lieferant ausfällt

Der wichtigste Lieferant eines Metallverarbeiters meldet einen Ransomware-Angriff. Die Folgen lassen sich in drei Schritten durchdenken:

+--------------------------------------------------------+
| Schritt 1 - Sofort                                     |
| Lieferant nimmt keine Bestellungen an, Mail fällt aus. |
| Betroffen: Verfügbarkeit der Beschaffung.              |
| Lagerbestand und Bedarf prüfen: Wie lange reicht es?   |
+--------------------------------------------------------+
                           |
                           v
+--------------------------------------------------------+
| Schritt 2 - Nach einigen Tagen                         |
| Lager ist leer, die Produktion steht oder drosselt.    |
| Lieferverzug, Vertragsstrafen, Ausfallkosten.          |
| Alternativen: Zweitlieferant, Eilbestellungen.         |
+--------------------------------------------------------+
                           |
                           v
+--------------------------------------------------------+
| Schritt 3 - Folgerisiken                               |
| Gefälschte Mails im Namen des Lieferanten, neue        |
| Bankverbindungen (Integrität), Datenabfluss beim       |
| Lieferanten (Vertraulichkeit). Rückruf über bekannte   |
| Nummer und Vier-Augen-Prinzip bei Zahlungen.           |
+--------------------------------------------------------+

---

## Kompetenz 3.3: Personenbezogene Daten schützen

Der Sicherheitsexperte der ChangeIT GmbH hängt die gewichtete Bedrohungsliste an die Wand. Herr Winter, der Datenschutzbeauftragte der RECPLAST GmbH, hat der Schulung zugehört und meldet sich:

“Bei beiden Berichten ging es auch um Menschen, nicht nur um Technik. In den Bewerbungen stehen Lebensläufe, Zeugnisse und Fotos. Beim Lieferanten sind Namen und Telefonnummern unserer Ansprechpartner betroffen. Datenschutz und Informationssicherheit hängen zusammen, aber sie sind nicht dasselbe. Klären Sie bitte, welche Daten betroffen sind, welche Rechte die Menschen dahinter haben und was passieren muss, wenn so etwas schiefgeht.”

Herr Brandt aus der Personalabteilung ergänzt: “Gestern hat mich eine abgelehnte Bewerberin gefragt, ob wir ihre Unterlagen noch haben, und verlangt, dass wir sie löschen. Ich weiß gar nicht genau, wo die überall liegen.”

---

### A|3.3: Datenschutzrisiken prüfen

#### Aufgabe 1

Informieren Sie sich in M|3.3.0: Personenbezogene Daten und DSGVO/BDSG. Entscheiden Sie, welche der folgenden Daten personenbezogen sind und ob sie zu den besonderen Kategorien gehören. Übertragen Sie dazu die folgende Tabelle und füllen Sie sie aus.

| Datum | Personenbezogen? | Besondere Kategorie? | Begründung |
| --- | --- | --- | --- |
| Name und Foto in einem Lebenslauf |  |  |  |
| Hinweis auf eine Schwerbehinderung in einer Bewerbung |  |  |  |
| Firmenanschrift des Lieferanten |  |  |  |
| Name und Mobilnummer der Ansprechperson beim Lieferanten |  |  |  |
| Statistik “40 Bewerbungen im Quartal” |  |  |  |

#### Aufgabe 2

Herr Brandt schildert die Anfrage der abgelehnten Bewerberin. Informieren Sie sich in M|3.3.1: Rechte der Betroffenen und Einwilligung.

##### Aufgabenteil a

Welche Rechte macht die Bewerberin geltend?

##### Aufgabenteil b

Wie muss die Personalabteilung der RECPLAST GmbH vorgehen? Beschreiben Sie die Schritte.

##### Aufgabenteil c

Die Personalabteilung möchte die Unterlagen abgelehnter Bewerbender ein Jahr in einem Bewerberpool behalten. Was ist dafür nötig, und welche Anforderungen muss das erfüllen?

#### Aufgabe 3

Angenommen, ein präpariertes Word-Dokument in einer Bewerbung installiert Schadsoftware, die die Bewerbungsunterlagen kopiert.

##### Aufgabenteil a

Welche Schutzziele sind betroffen?

##### Aufgabenteil b

Welche Pflichten hat die RECPLAST GmbH nach der Entdeckung, und welche Fristen gelten?

##### Aufgabenteil c

Welche Folgen drohen bei einem Verstoß gegen diese Pflichten?

#### Aufgabe 4

Die Personalabteilung soll der Geschäftsleitung berichten, aus welchen Regionen Bewerbungen eingehen. Informieren Sie sich in M|3.3.2: Anonymisierung und Pseudonymisierung und in M|3.3.3: IT-Sicherheitsbeauftragte/r und Datenschutzbeauftragte/r.

##### Aufgabenteil a

Erklären Sie den Unterschied zwischen Anonymisierung und Pseudonymisierung.

##### Aufgabenteil b

Welches Verfahren eignet sich für den Bericht? Begründen Sie Ihre Wahl.

##### Aufgabenteil c

Bei der Datenpanne aus Aufgabe 3 arbeiten Frau Weber (IT-Sicherheit) und Herr Winter (Datenschutz) zusammen. Wer übernimmt welche Aufgabe?

---

### M|3.3.0: Personenbezogene Daten und DSGVO/BDSG

Datenschutz

Ein Lebenslauf enthält weit mehr, als man ihm auf den ersten Blick ansieht: Name, Anschrift, Foto, Geburtsdatum, Schulnoten, frühere Arbeitgeber und manchmal Hinweise auf Gesundheit oder Familienstand. All das sind personenbezogene Daten, und für den Umgang damit gelten rechtliche Regeln, unabhängig davon, wie gut die IT geschützt ist. Der Datenschutz ergänzt die Informationssicherheit: Während die Sicherheit Daten vor Verlust und Missbrauch schützt, schützt der Datenschutz die Menschen, auf die sich die Daten beziehen.

Drei Dinge gehören zusammen. Die Definition legt fest, welche Daten überhaupt gemeint sind. Der Rechtsrahmen bestimmt, unter welchen Bedingungen sie verarbeitet werden dürfen. Die Pflichten bei Verstößen regeln, was nach einer Datenpanne zu tun ist und welche Folgen drohen. Wer die Definition nicht kennt, erkennt den Datenschutz nicht als Thema, und wer den Rechtsrahmen nicht kennt, kann Datenpannen nicht richtig einordnen.

Die drei Bausteine

**Was sind personenbezogene Daten?**

Personenbezogene Daten sind alle Informationen, die sich auf eine identifizierte oder identifizierbare natürliche Person beziehen (Art. 4 DSGVO). Es genügt, dass die Person mit zusätzlichen Informationen bestimmt werden kann. Daten von Unternehmen als solchen sind keine personenbezogenen Daten, die Namen und Kontaktdaten der Menschen dahinter schon.

- **Direkte Merkmale:** Name, Anschrift, Foto, Geburtsdatum, Telefonnummer, E-Mail-Adresse.
- **Indirekte Merkmale:** Kennzeichen, Personalnummer, IP-Adresse oder eine Kombination aus Funktion, Abteilung und Alter, wenn dadurch nur eine Person in Frage kommt.
- **Besondere Kategorien (Art. 9 DSGVO):** Gesundheitsdaten, Religion, politische Meinung, Gewerkschaftszugehörigkeit, biometrische und genetische Daten. Sie sind besonders schützenswert und dürfen nur unter engen Voraussetzungen verarbeitet werden.
- **Kein Personenbezug:** Reine Sachdaten wie Maschinenwerte oder anonymisierte Statistiken, aus denen sich keine Person ableiten lässt.

*💻 Beispiel aus der IT-Praxis: Ein Online-Shop speichert Bestellungen mit Namen und Lieferadresse. Beides ist personenbezogen. Sein Webserver protokolliert zusätzlich IP-Adressen der Besucher, die ebenfalls als personenbezogen gelten, weil sie über den Anbieter einer Person zugeordnet werden können.*

**DSGVO, BDSG und die Grundsätze**

Auf europäischer Ebene gilt die Datenschutz-Grundverordnung (DSGVO), in Deutschland ergänzt durch das Bundesdatenschutzgesetz (BDSG) und Landesgesetze. Das BDSG enthält unter anderem Regeln zum Beschäftigtendatenschutz, also zum Umgang mit Daten von Mitarbeitenden und Bewerbenden (§ 26 BDSG). Wer Daten verarbeitet, ist verantwortlich im Sinne des Gesetzes und muss die Grundsätze des Art. 5 DSGVO einhalten.

- **Rechtmäßigkeit:** Jede Verarbeitung braucht eine Rechtsgrundlage, etwa Einwilligung, Vertrag oder vorvertragliche Maßnahmen, gesetzliche Pflicht oder berechtigtes Interesse (Art. 6 DSGVO).
- **Zweckbindung:** Daten dürfen nur für den Zweck verwendet werden, für den sie erhoben wurden.
- **Datenminimierung:** Es werden nur so viele Daten erhoben, wie für den Zweck nötig.
- **Speicherbegrenzung:** Daten werden gelöscht, sobald der Zweck entfällt, etwa nach Abschluss eines Bewerbungsverfahrens.
- **Integrität und Vertraulichkeit:** Die Daten werden durch technische und organisatorische Maßnahmen geschützt (Art. 32 DSGVO). Hier greift die Informationssicherheit.
- **Rechenschaftspflicht:** Das Unternehmen muss nachweisen können, dass es die Regeln einhält.

*💻 Beispiel aus der IT-Praxis: Eine Personalabteilung speichert Bewerbungen in einem Postfach, das alle Beschäftigten der Abteilung lesen können. Es sind nur diejenigen zuständig, die im Verfahren mitwirken. Zugriffsrechte nach dem Minimalprinzip (siehe M|2.4.0: Principle of Least Privilege) erfüllen hier Datenschutz und Sicherheit zugleich.*

**Datenpannen und Konsequenzen**

Eine Datenpanne liegt vor, wenn die Sicherheit verletzt wird und personenbezogene Daten dadurch unbefugt offengelegt, verändert, verloren oder zerstört werden. Das kann ein Hackerangriff sein, aber auch eine falsch adressierte Mail oder ein verlorener Datenträger. Betrifft eine Panne Daten eines Unternehmens, muss dieses handeln.

- **Meldung an die Aufsichtsbehörde:** Wenn die Verletzung voraussichtlich zu einem Risiko für die Betroffenen führt, muss sie unverzüglich und möglichst binnen 72 Stunden nach Bekanntwerden gemeldet werden (Art. 33 DSGVO).
- **Information der Betroffenen:** Bei einem hohen Risiko sind auch die betroffenen Personen zu informieren (Art. 34 DSGVO).
- **Dokumentation:** Jede Datenpanne wird mit Ursache, Folgen und Gegenmaßnahmen dokumentiert, auch wenn sie nicht gemeldet wird.
- **Folgen bei Verstößen:** Bußgelder bis zu 20 Millionen Euro oder 4 Prozent des weltweiten Jahresumsatzes, Schadensersatzansprüche Betroffener und Imageverlust.

*💻 Beispiel aus der IT-Praxis: Ein Mitarbeiter verschickt versehentlich eine Tabelle mit den Daten aller Bewerbenden an einen externen Verteiler. Die IT-Leitung informiert sofort den Datenschutzbeauftragten, der die Meldung an die Aufsichtsbehörde vorbereitet. Die Uhr für die 72 Stunden läuft ab dem Moment, in dem die Panne bekannt wird.*

Praxisbeispiel: Eine Bewerbung datenschutzgerecht bearbeiten

Eine Initiativbewerbung geht per Mail in der Personalabteilung ein. So prüfen Sie in drei Schritten, was zu beachten ist:

+--------------------------------------------------------+
| Schritt 1 - Daten einordnen                            |
| Name, Anschrift, Foto, Lebenslauf: personenbezogen.    |
| Hinweis auf Behinderung oder Krankheit: besondere      |
| Kategorie, nur wenn nötig und rechtlich zulässig.      |
+--------------------------------------------------------+
                           |
                           v
+--------------------------------------------------------+
| Schritt 2 - Verarbeitung regeln                        |
| Zweck: Bewerbungsverfahren. Zugriff nur für die        |
| zuständigen Personen. Unterlagen sicher speichern.     |
| Keine Weitergabe ohne Rechtsgrundlage.                 |
+--------------------------------------------------------+
                           |
                           v
+--------------------------------------------------------+
| Schritt 3 - Aufbewahrung beenden                       |
| Nach Abschluss des Verfahrens löschen, außer es liegt  |
| eine Einwilligung vor (z. B. Aufnahme in den           |
| Bewerberpool). Löschen dokumentieren.                  |
+--------------------------------------------------------+

---

### M|3.3.1: Rechte der Betroffenen und Einwilligung

Betroffenenrechte und Einwilligung

Wer Daten über andere speichert, hat Pflichten, und wer betroffen ist, hat Rechte. Die DSGVO gibt Menschen die Kontrolle über ihre Daten und verpflichtet Unternehmen, diese Rechte zu erfüllen, in der Regel innerhalb eines Monats. Eine besondere Rolle spielt die Einwilligung, die als Rechtsgrundlage nur unter strengen Bedingungen wirksam ist. Dieses Material zeigt, welche Rechte es gibt, wie Unternehmen darauf reagieren und wann eine Einwilligung nötig ist.

Zwei Bereiche greifen ineinander. Die Betroffenenrechte beschreiben, was Personen verlangen können, und die Einwilligung regelt, wann eine Verarbeitung auf ihrer Zustimmung beruht. Fehlt die Kenntnis der Rechte, bleiben Anfragen liegen, und eine unwirksame Einwilligung macht die Verarbeitung rechtswidrig.

Die zwei Bausteine

**Die Rechte der Betroffenen**

Betroffene sind die Personen, deren Daten verarbeitet werden. Sie können sich an das Unternehmen wenden und bestimmte Dinge verlangen.

- **Auskunft (Art. 15):** Welche Daten werden gespeichert, wofür, wie lange, an wen gehen sie?
- **Berichtigung (Art. 16):** Falsche Daten müssen korrigiert werden.
- **Löschung (Art. 17):** Daten sind zu löschen, wenn der Zweck entfallen ist oder die Einwilligung widerrufen wurde.
- **Einschränkung der Verarbeitung (Art. 18):** Daten werden gesperrt, etwa bei Streit über die Richtigkeit.
- **Datenübertragbarkeit (Art. 20):** Daten werden in einem gängigen Format herausgegeben.
- **Widerspruch (Art. 21):** Betroffene können der Verarbeitung auf Grundlage eines berechtigten Interesses widersprechen.
- **Beschwerde (Art. 77):** Betroffene können sich an die Datenschutz-Aufsichtsbehörde wenden.

*💻 Beispiel aus der IT-Praxis: Eine abgelehnte Bewerberin schreibt an die Personalabteilung und fragt, welche ihrer Daten noch gespeichert sind, und verlangt deren Löschung. Das Unternehmen prüft alle Ablageorte, auch Postfächer und Sicherungen, teilt die Auskunft mit und löscht die Daten, sofern keine Aufbewahrungspflicht besteht.*

**Die Einwilligung**

Eine Einwilligung ist die freiwillige, vorab erteilte Zustimmung einer Person zu einer bestimmten Datenverarbeitung. Sie ist nur eine von mehreren Rechtsgrundlagen und passt vor allem dort, wo es keine andere Grundlage gibt. Im Beschäftigungsverhältnis ist die Freiwilligkeit wegen der Abhängigkeit besonders sorgfältig zu prüfen.

- **Freiwillig:** Es darf kein Nachteil drohen, wenn jemand nicht zustimmt.
- **Informiert und bestimmt:** Die Person weiß, wer welche Daten zu welchem Zweck verarbeitet.
- **Eindeutig:** Eine aktive Handlung ist nötig, vorangekreuzte Kästchen genügen nicht.
- **Widerruflich:** Die Person kann die Einwilligung jederzeit mit Wirkung für die Zukunft zurücknehmen (Art. 7 DSGVO).
- **Nachweisbar:** Das Unternehmen muss die Einwilligung belegen können.

*💻 Beispiel aus der IT-Praxis: Ein Unternehmen möchte abgelehnte Bewerbungen für ein Jahr in einem Bewerberpool behalten. Dazu holt es eine schriftliche Einwilligung mit Zweck, Dauer und Hinweis auf den Widerruf ein. Ohne diese Zustimmung müssten die Unterlagen nach dem Verfahren gelöscht werden.*

Praxisbeispiel: Eine Auskunfts- und Löschanfrage bearbeiten

Eine Bewerberin verlangt Auskunft und Löschung. So bearbeitet die Personalabteilung die Anfrage in drei Schritten:

+--------------------------------------------------------+
| Schritt 1 - Anfrage prüfen und Person identifizieren   |
| Ist die Person die Anfragende? Anfrage dokumentieren,  |
| Frist von einem Monat notieren.                        |
+--------------------------------------------------------+
                           |
                           v
+--------------------------------------------------------+
| Schritt 2 - Daten suchen                               |
| Postfach, Ablage, Bewerbungsportal, Notizen, Backups:  |
| Wo liegen Daten dieser Person?                         |
+--------------------------------------------------------+
                           |
                           v
+--------------------------------------------------------+
| Schritt 3 - Antworten und löschen                      |
| Auskunft erteilen, Daten löschen, soweit keine         |
| Aufbewahrungspflicht besteht, Ablauf dokumentieren.    |
+--------------------------------------------------------+

---

### M|3.3.2: Anonymisierung und Pseudonymisierung

Anonymisierung und Pseudonymisierung

Für viele Auswertungen werden Namen gar nicht gebraucht. Wer wissen möchte, wie viele Bewerbungen pro Monat eingehen, muss nicht wissen, wer sich beworben hat. Dort, wo Personenbezug nicht nötig ist, lässt er sich entfernen oder verschleiern. Das senkt das Risiko bei Verlust oder Missbrauch und entspricht dem Grundsatz der Datenminimierung. Zwei Verfahren spielen dabei eine Rolle: die Anonymisierung und die Pseudonymisierung. Sie klingen ähnlich, haben aber unterschiedliche Folgen.

Der Unterschied liegt in der Umkehrbarkeit. Bei der Pseudonymisierung kann der Personenbezug mit Zusatzinformationen wiederhergestellt werden, bei der Anonymisierung nicht mehr. Davon hängt ab, ob die DSGVO weiterhin gilt.

Die zwei Bausteine

**Pseudonymisierung**

Bei der Pseudonymisierung werden Merkmale wie Name oder Personalnummer durch ein Pseudonym ersetzt, etwa eine Kennziffer. Die Zuordnungstabelle wird getrennt und besonders geschützt aufbewahrt. Wer die Tabelle hat, kann die Person wieder zuordnen. Pseudonymisierte Daten bleiben deshalb personenbezogen, die DSGVO gilt weiter. Das Verfahren verringert aber das Risiko, weil Unbefugte mit den Daten allein wenig anfangen können.

- **Vorgehen:** Direkte Merkmale durch Kennziffer oder Code ersetzen, Zuordnungsliste getrennt speichern.
- **Umkehrbar:** Mit der Zuordnungsliste lässt sich die Person wieder bestimmen.
- **Einsatz:** Tests mit echten Datenbeständen, Studien, interne Auswertungen, Weitergabe an Dienstleister.
- **Grenze:** Ein Hash von Namen ist kein sicheres Pseudonym, wenn sich die möglichen Namen einfach durchprobieren lassen.

*💻 Beispiel aus der IT-Praxis: Ein Softwarehaus testet eine neue Auswertung mit Kundendaten. Statt der Namen stehen in den Testdaten Kundennummern, die Zuordnungsliste bleibt auf einem geschützten System der Produktion. Entwickler arbeiten mit den Testdaten, ohne die Personen zu kennen.*

**Anonymisierung**

Bei der Anonymisierung wird der Personenbezug so entfernt, dass er nicht oder nur mit unverhältnismäßigem Aufwand wiederherstellbar ist. Anonyme Daten fallen nicht mehr unter die DSGVO. Das ist schwieriger, als es klingt: Auch ohne Namen kann eine Person bestimmbar sein, wenn die Kombination der Merkmale selten ist, etwa Alter, Abteilung und Eintrittsdatum in einer kleinen Firma.

- **Vorgehen:** Direkte Merkmale löschen, Angaben vergröbern (Alter in Gruppen, Ort in Regionen), Werte zusammenfassen (Aggregation).
- **Nicht umkehrbar:** Es gibt keine Zuordnungstabelle.
- **Einsatz:** Veröffentlichte Statistiken, Berichte an die Geschäftsleitung, Forschungsdaten.
- **Prüffrage:** Könnte jemand mit zusätzlichen Informationen noch auf eine Person schließen? Bei sehr kleinen Gruppen ist das oft möglich.

*💻 Beispiel aus der IT-Praxis: Die Personalabteilung berichtet der Geschäftsleitung, dass im Quartal 40 Bewerbungen eingegangen sind, 25 davon für die Produktion. Namen, Orte und Geburtsdaten tauchen nicht auf. Bei einer Abteilung mit nur einer Bewerbung würde die Zahl jedoch auf eine Person hinweisen und wäre zusammenzufassen.*

Praxisbeispiel: Das passende Verfahren wählen

Die Personalabteilung soll auswerten, aus welchen Regionen Bewerbungen kommen, und der Geschäftsleitung berichten. Die Entscheidung läuft in drei Schritten:

+--------------------------------------------------------+
| Schritt 1 - Zweck klären                               |
| Wofür wird die Auswertung gebraucht? Reichen Zahlen    |
| je Region oder werden einzelne Personen benötigt?      |
+--------------------------------------------------------+
                           |
                           v
+--------------------------------------------------------+
| Schritt 2 - Verfahren wählen                           |
| Nur Zahlen nötig: anonymisieren (Namen entfernen,      |
| Regionen zusammenfassen, kleine Gruppen vermeiden).    |
| Einzelfälle nötig: pseudonymisieren, Liste getrennt.   |
+--------------------------------------------------------+
                           |
                           v
+--------------------------------------------------------+
| Schritt 3 - Ergebnis prüfen                            |
| Lässt sich noch auf eine Person schließen? Falls ja,   |
| Gruppen vergröbern. Verfahren dokumentieren.           |
+--------------------------------------------------------+

---

### M|3.3.3: IT-Sicherheitsbeauftragte/r und Datenschutzbeauftragte/r


IT-Sicherheitsbeauftragte und Datenschutzbeauftragte

Zwei Funktionen werden im Betrieb oft verwechselt, weil beide mit „Sicherheit“ zu tun haben: die oder der IT-Sicherheitsbeauftragte (ISB, bei RECPLAST Frau Weber als CISO) und die oder der Datenschutzbeauftragte (DSB). Sie arbeiten eng zusammen, haben aber unterschiedliche Ziele und Aufgaben. Ein Sicherheitsvorfall mit Personenbezug berührt beide Rollen zugleich, und wer die Zuständigkeiten kennt, weiß, an wen er sich wendet und wer was entscheidet.

Der Kern des Unterschieds liegt im Schutzgut. Die Informationssicherheit schützt Informationen und Systeme des Unternehmens, der Datenschutz schützt die Rechte der Menschen, deren Daten verarbeitet werden.

Die zwei Bausteine

**Aufgaben im Vergleich**

Beide Funktionen beraten und kontrollieren, doch ihre Rollen sind verschieden.

- **IT-Sicherheitsbeauftragte/r (ISB, CISO):** Entwickelt das Sicherheitskonzept und die Leitlinie, plant und überwacht technische und organisatorische Maßnahmen, bewertet Risiken und leitet die Reaktion auf Sicherheitsvorfälle. Die Funktion ergibt sich aus der Organisation des Unternehmens und aus Standards wie dem IT-Grundschutz.
- **Datenschutzbeauftragte/r (DSB):** Berät und überwacht die Einhaltung der DSGVO und des BDSG, schult Beschäftigte, ist Anlaufstelle für Betroffene und die Aufsichtsbehörde und wirkt bei Meldungen von Datenpannen mit (Art. 37 bis 39 DSGVO).
- **Benennung:** Ein DSB muss bei Vorliegen bestimmter Voraussetzungen benannt werden, in Deutschland etwa, wenn in der Regel mindestens 20 Personen ständig mit der automatisierten Verarbeitung personenbezogener Daten beschäftigt sind (§ 38 BDSG).
- **Unabhängigkeit:** Der DSB ist bei seiner Tätigkeit weisungsfrei und berichtet an die Unternehmensleitung.

*💻 Beispiel aus der IT-Praxis: Ein Admin entdeckt, dass ein Server mit Kundendaten von außen erreichbar war. Er meldet den Vorfall dem ISB, der die Sperrung und Ursachenanalyse leitet, und dem DSB, der beurteilt, ob eine Meldung an die Aufsichtsbehörde nötig ist.*

**Zusammenarbeit und Interessenkonflikt**

Die Rollen ergänzen sich: Der ISB sorgt für technische Schutzmaßnahmen, der DSB prüft, ob die Verarbeitung rechtmäßig ist und die Rechte der Betroffenen gewahrt bleiben. Dieselbe Person sollte nicht beide Funktionen übernehmen, weil der DSB die Maßnahmen des ISB auch kritisch bewerten muss. Das wäre ein Interessenkonflikt (Art. 38 DSGVO).

- **Gemeinsame Themen:** Datenpannen, Zugriffsrechte, Verschlüsselung, Löschkonzepte, Schulungen.
- **Entscheidung über die Meldung:** Der DSB berät, die Verantwortung trägt die Unternehmensleitung.
- **Dokumentation:** Beide arbeiten mit denselben Protokollen und Berichten, jeweils mit eigener Blickrichtung.
- **Kleine Unternehmen:** Wo die Pflicht zur Benennung fehlt, übernimmt die Geschäftsführung die Verantwortung für den Datenschutz, oft mit externer Beratung.

*💻 Beispiel aus der IT-Praxis: Ein mittelständisches Unternehmen hat einen internen ISB und beauftragt für den Datenschutz einen externen Berater als DSB. Bei der Einführung einer neuen Videoüberwachung prüft der ISB die technische Sicherheit der Aufzeichnungen, der DSB die Rechtmäßigkeit, die Hinweise für Betroffene und die Speicherdauer.*

Praxisbeispiel: Wer macht was bei einer Datenpanne?

Beschäftigte melden, dass nach dem Öffnen einer Bewerbung Schadsoftware auf einem Rechner der Personalabteilung lief. Die Zuständigkeiten verteilen sich in drei Schritten:

+--------------------------------------------------------+
| Schritt 1 - Sofortmaßnahmen (ISB)                      |
| Rechner vom Netz trennen, Ausbreitung stoppen, Spuren  |
| sichern, Ursache und betroffene Daten klären.          |
+--------------------------------------------------------+
                           |
                           v
+--------------------------------------------------------+
| Schritt 2 - Bewertung (DSB)                            |
| Sind personenbezogene Daten betroffen? Besteht ein     |
| Risiko für die Betroffenen? Meldung nötig (72 Stunden)?|
+--------------------------------------------------------+
                           |
                           v
+--------------------------------------------------------+
| Schritt 3 - Entscheidung und Nachbereitung             |
| Geschäftsleitung entscheidet über Meldung und          |
| Information der Betroffenen. Dokumentation, Maßnahmen  |
| zur Vorbeugung (Schulung, Technik) festlegen.          |
+--------------------------------------------------------+

---

## Handlungsergebnis

Die Schulung ist beendet, die Beschäftigten der RECPLAST GmbH verlassen den Raum. Frau Weber bleibt mit Ihnen und dem Sicherheitsexperten der ChangeIT GmbH zurück, die Wand ist voll mit Steckbriefen, Berichten und Gewichtungen.

“Das war aufschlussreich, vor allem die Berichte aus Einkauf und Personal. Ich muss der Geschäftsleitung morgen zeigen, was die Schulung ergeben hat und wo wir als Nächstes genauer hinsehen. Wir können nicht jede Abteilung auf einmal durchleuchten. Bringen Sie bitte alles auf eine übersichtliche Seite pro Abteilung und sagen Sie mir, wo wir anfangen sollten.”

---

### A|3.4: Bedrohungsübersicht für die Geschäftsleitung erstellen

Sie erstellen allein oder zu zweit eine Bedrohungsübersicht für die Abteilungen Produktion, Einkauf und Personal der RECPLAST GmbH. Nutzen Sie dafür das Material M|3.4.0: Vorlage Bedrohungsübersicht und Ihre Ergebnisse aus den Arbeitsaufträgen A|3.0 bis A|3.3.

#### Aufgabe 1

Übertragen Sie Ihre Ergebnisse aus A|3.2 (Gewichtung der Bedrohungen) in die Vorlage. Tragen Sie für jede der drei Abteilungen die Bedrohung mit dem höchsten möglichen Schaden ein.

#### Aufgabe 2

Ergänzen Sie für jede Abteilung die folgenden Angaben:

- die Schwachstelle, über die die Bedrohung wirkt
- das oder die betroffenen Schutzziele
- die Schadenskategorien, in denen ein Schaden entsteht
- die Gewichtung (gering, mittel oder hoch) mit Begründung in einem Satz
- ob personenbezogene Daten betroffen sind (ja oder nein)
- eine erste Idee für eine Gegenmaßnahme

#### Aufgabe 3

Frau Weber kann nur eine Abteilung zuerst genauer untersuchen lassen. Empfehlen Sie ihr eine Abteilung und begründen Sie Ihre Empfehlung in drei bis vier Sätzen. Berücksichtigen Sie dabei die Höhe des Schadens, die Abhängigkeit von anderen Abteilungen oder Lieferanten und den Datenschutz.

---

### M|3.4.0: Vorlage Bedrohungsübersicht

| Feld | Produktion | Einkauf | Personal |
|---|---|---|---|
| **Schwerste Bedrohung** |  |  |  |
| **Schwachstelle** |  |  |  |
| **Betroffene Schutzziele** |  |  |  |
| **Schadenskategorien** |  |  |  |
| **Gewichtung (gering, mittel, hoch) und Begründung** |  |  |  |
| **Personenbezogene Daten betroffen?** |  |  |  |
| **Erste Idee für eine Gegenmaßnahme** |  |  |  |

**Empfehlung an Frau Weber:** Abteilung: ______ , Begründung: ______

---