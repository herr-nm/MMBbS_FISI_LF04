# Kapitel 2: Schutzziele der Informationssicherheit sicherstellen 

![Kapitelbild](bilder/02_kapitelbild.png)

In diesem Kapitel werden Sie ...

- ... die Schutzziele der Informationssicherheit kennenlernen.
- ... in der Vertiefung Maßnahmen zur Sicherstellung der Vertraulichkeit kennenlernen.
- ... in der Vertiefung Maßnahmen zur Sicherstellung der Integrität kennenlernen.
- ... in der Vertiefung Maßnahmen zur Sicherstellung der Verfügbarkeit kennenlernen.

---

## Handlungssituation

Sie sind Auszubildende/Auszubildender der ChangeIT GmbH, dem IT-Dienstleister der RECPLAST GmbH. Sie werden kurzfristig zum Kunden gerufen: Am Montagmorgen um 07:30 Uhr herrscht Hektik in der IT-Abteilung der RECPLAST GmbH. Die neue, vollautomatische Extrusionsanlage 4 in Werkhalle 2 sollte heute nach dreiwöchiger Testphase offiziell in den Regelbetrieb gehen.

Gegen 06:45 Uhr traten jedoch zwei gravierende Vorfälle auf:

**1. Ausfall der Steuerung (Extruder 4):**

Das zentrale Leitstand-Terminal meldet einen Verbindungsabbruch zur SPS-Steuerung von Extruder 4. Die Anlage steht still. Bei der ersten Fehlersuche stellt der Betriebstechniker fest, dass der Haupt-Switch im Hallenverteiler stromlos ist, weil das Netzteil ausgefallen ist. Ein redundantes Netzteil oder eine USV war für diesen Switch laut Dokumentation nicht vorgesehen. Die Produktionsleitung schätzt den Ausfallschaden derzeit auf ca. 12.000 € pro Stunde.

**2. Unstimmigkeiten bei den Mischungsverhältnissen:**

Parallel meldet die Qualitätskontrolle ein Problem bei Extruder 2: Die Mischungsrezeptur für die Herstellung der Recycling-Kunststoffgranulate stimmte in den letzten Nachtschicht-Protokollen nicht mit den Vorgaben des Labor-ERP-Systems überein. Der Anteil des Additivs REC-Poly-3 wurde im System von 4,5% auf 14,5% geändert. Niemand aus der Laborleitung hat diese Änderung freigegeben oder durchgeführt. Durch das falsche Mischungsverhältnis ist eine Charge von 8 Tonnen Granulat unbrauchbar geworden.

Als Sie zusammen mit Frau Weber, der CISO der RECPLAST GmbH, den Vorfall im Leitstand von Extruder 4 untersuchen, fällt Ihnen ein USB-Stick auf, der am USB-Port des Leitstand-PCs steckt. Auf dem Gehäuse steht handschriftlich "Update_Extruder4_v2.4". Ein Schichtleiter erklärt: "Der Stick lag Ende letzter Woche auf dem Tisch. Ein Kollege aus der Fremdfirma für die Anlagenwartung Krämer Anlagenservice GmbH hat gemeint, da seien die neuen Kennlinien drauf, und hat ihn kurz eingesteckt." Ob der Stick mit den beiden Vorfällen zusammenhängt, ist zu diesem Zeitpunkt noch unklar.

Zudem wird festgestellt, dass sich alle Techniker für die Bedienung der Terminals ein gemeinsames Gruppenkonto `betrieb_halle2` mit dem Passwort `Recplast2024!` teilen. Das Passwort steht auf einem Notizzettel, der am Monitor des Leitstand-PCs klebt.

 <figure style="max-width: 100%; margin: 1em 0; text-align: center;"> 
 	 <img src="bilder/02_handlungssituation.png" alt="Produktionshalle im Chaos" style="width: 100%; height: auto; border-radius: 6px;"> 
 	 <figcaption style="font-size: 0.85em; color: #555555; margin-top: 6px; font-style: italic;"> 
 	 	 Abb.: Produktionshalle im Chaos <span style="font-style: normal; opacity: 0.8;">(🤖 KI-generiert)</span> 
 	 </figcaption> 
 </figure> 
 
---

## Kompetenz 2.0: Schutzziele identifizieren

Die RECPLAST GmbH hat Ihren Arbeitgeber, die ChangeIT GmbH, mit der Aufarbeitung beauftragt. Frau Weber übergibt Ihnen die Protokolle der Vorfälle und ergänzt:

*"Das ist ein Totalschaden für unsere Prozesse. Wir müssen der Geschäftsleitung bis heute Nachmittag eine erste Analyse vorlegen. Bitte arbeiten Sie die Vorfälle systematisch auf: Welche Schutzziele wurden hier verletzt, an welchen Stellen haben unsere Maßnahmen versagt und wie verhindern wir so etwas für die Zukunft?"*

 <figure style="max-width: 100%; margin: 1em 0; text-align: center;"> 
 	 <img src="bilder/02_schutzziele.png" alt="Übergabe an ChangeIT" style="width: 100%; height: auto; border-radius: 6px;"> 
 	 <figcaption style="font-size: 0.85em; color: #555555; margin-top: 6px; font-style: italic;"> 
 	 	 Abb.: Übergabe an ChangeIT <span style="font-style: normal; opacity: 0.8;">(🤖 KI-generiert)</span> 
 	 </figcaption> 
 </figure> 

---

### Arbeitsauftrag A|2.0: CIA-Triade analysieren

#### Aufgabe 1

Analysieren Sie die Vorfälle bei Extruder 2 und 4, den USB-Stick am Leitstand sowie die Bedienung der Terminals. Welche Probleme sind hier aus Sicht der Informationssicherheit aufgetreten?

#### Aufgabe 2

Erstellen Sie sich eine Übersicht der Schutzziele der Informationssicherheit mithilfe des Materials M|2.0.0: CIA-Triade. Notieren Sie sich die drei übergeordneten Schutzziele auf Deutsch und Englisch. Fertigen Sie anschließend eine Liste der Thematiken an, die dem jeweiligen Bereich zuzuordnen sind.

#### Aufgabe 3

Ordnen Sie die in Aufgabe 1 identifizierten Probleme den Schutzzielen und, wenn möglich, den nachgeordneten Themenschwerpunkten zu.

---

### Material M|2.0.0: CIA-Triade

In einer zunehmend vernetzten Welt verarbeiten Organisationen täglich riesige Mengen sensibler Daten. Um Systeme, Prozesse und Informationen wirksam vor Bedrohungen zu schützen, bildet die sogenannte CIA-Triade das theoretische und praktische Fundament der modernen IT-Sicherheit. Das Akronym leitet sich aus den englischen Begriffen Confidentiality (Vertraulichkeit), Integrity (Integrität) und Availability (Verfügbarkeit) ab. Diese drei Schutzziele definieren die grundlegenden Anforderungen an einen sicheren Umgang mit Daten und IT-Infrastrukturen.

#### Vertraulichkeit (Confidentiality)

Das Schutzziel der Vertraulichkeit stellt sicher, dass Informationen ausschließlich Personen, Systemen oder Prozessen zugänglich sind, die eine ausdrückliche Berechtigung besitzen. Unbefugte Einblicke – sei es durch externe Angreifer oder nicht autorisierte interne Mitarbeitende – müssen konsequent verhindert werden. Dies betrifft insbesondere sensible Betriebsgeheimnisse, personenbezogene Daten, Finanzkennzahlen sowie Zugangsdaten.

Um Vertraulichkeit in der Praxis zu gewährleisten, kommen sowohl technische als auch organisatorische Schutzmaßnahmen zum Einsatz. Auf technischer Ebene sichern kryptografische Verfahren Daten in allen Zuständen: ob ruhend (Data at Rest), während der Übertragung (Data in Transit) oder bei der Verarbeitung (Data in Use). Ergänzt wird dies durch ein striktes Rechtemanagement nach dem Principle of Least Privilege (Minimalprinzip), rollenbasierte Zugriffskontrollen (RBAC) sowie die Pflicht zur Multi-Faktor-Authentifizierung (MFA) für alle Systemzugänge. Auf organisatorischer Seite unterstützen Vertraulichkeitsvereinbarungen (NDAs), die systematische Klassifizierung von Dokumenten (etwa in öffentlich, intern oder streng vertraulich) sowie physische Zutrittskontrollen zu Rechenzentren und Leitständen diesen Schutz.

#### Integrität (Integrity)

Während die Vertraulichkeit vor unbefugtem Lesen schützt, garantiert das Schutzziel der Integrität die Korrektheit, Vollständigkeit und Unversehrtheit von Daten und Systemfunktionen. Es stellt sicher, dass Informationen nicht unbefugt, unbeabsichtigt oder unbemerkt verändert, gelöscht oder gefälscht werden können. Dies ist essenziell für die Zuverlässigkeit von Buchhaltungsdaten, Produktionsrezepturen, Steuerungsbefehlen in Industrieanlagen sowie für die Gültigkeit von Systemkonfigurationen.

Zur Sicherung der Integrität dienen kryptografische Prüfsummen (wie Hashwerte mit SHA-256) und digitale Signaturen, die jede Modifikation an Daten unverzüglich erkennbar machen. Auf Prozessebene verhindern das Vier-Augen-Prinzip bei kritischen Freigaben sowie die strikte Trennung von Entwicklungs-, Test- und Produktionsumgebungen ungewollte oder manipulierte Eingriffe. Zudem fangen automatische Plausibilitätsprüfungen in Anwendungen fehlerhafte Eingaben ab, während revisionssichere WORM-Speichermedien (Write-Once-Read-Many) und Versionierungssysteme eine lückenlose Historisierung aller Änderungen gewährleisten.

#### Verfügbarkeit (Availability)

Das dritte Schutzziel, die Verfügbarkeit, gewährleistet, dass autorisierte Nutzerinnen und Nutzer jederzeit und störungsfrei auf benötigte Daten, IT-Systeme und Dienstleistungen zugreifen können. Da ein Systemausfall ganze Geschäftsprozesse oder Produktionsstraßen vollständig lähmen kann, steht die Minimierung von ungeplanten Ausfallzeiten (Downtime) im Zentrum dieser Säule.

Die technische Ausfallsicherheit wird vor allem durch Redundanz erreicht: Kritische Komponenten wie Netzteile, Festplattenverbünde (RAID), Netzwerkpfade, Server-Cluster und gesamte Rechenzentren werden mehrfach ausgelegt, um sogenannte Single Points of Failure konsequent zu vermeiden. Ergänzend sichern unterbrechungsfreie Stromversorgungen (USV), Notstromaggregate und redundante Klimaanlagen die physische Betriebsbereitschaft von Serverräumen. Gegen Datenverlust und Großschadenslagen schützen regelmäßige Datensicherungen (beispielsweise nach der bewährten 3-2-1-Regel) sowie ausgearbeitete Wiederherstellungs- und Notfallpläne (Disaster Recovery und Business Continuity Plans). Zusätzlich fangen Load Balancer und automatisierte Überlastungsschutzsysteme (DDoS-Protection) Angriffe ab, die darauf abzielen, Dienste durch gezielte Datenüberflutung außer Betrieb zu setzen.

---

## Kompetenz 2.1: Vertraulichkeit sicherstellen

Während Sie noch am Leitstand stehen, weist Frau Weber auf den eingesteckten USB-Stick und den Notizzettel mit dem gemeinsamen Passwort: "Dass hier jeder ungehindert reinschauen und Daten abgreifen kann, ist ein untragbarer Zustand für die Vertraulichkeit unserer Daten. Lassen Sie uns diesen Bereich jetzt gründlich durchleuchten: Welche technischen und organisatorischen Möglichkeiten haben wir überhaupt, um Vertraulichkeit herzustellen, und welche davon passen zu den Abläufen hier bei RECPLAST?"

 <figure style="max-width: 100%; margin: 1em 0; text-align: center;"> 
 	 <img src="bilder/02_vertraulichkeit.png" alt="Alles für die Vertraulichkeit" style="width: 100%; height: auto; border-radius: 6px;"> 
 	 <figcaption style="font-size: 0.85em; color: #555555; margin-top: 6px; font-style: italic;"> 
 	 	 Abb.: Alles für die Vertraulichkeit <span style="font-style: normal; opacity: 0.8;">(🤖 KI-generiert)</span> 
 	 </figcaption> 
 </figure> 

--- 

### Arbeitsauftrag A|2.1: Maßnahmen zur Vertraulichkeit kennenlernen

#### Aufgabe 1

Fassen Sie kurz in eigenen Worten zusammen, welche der Probleme in der RECPLAST GmbH den Bereich der Vertraulichkeit betreffen.

#### Aufgabe 2

Welche Maßnahmen können in einem Unternehmen ergriffen werden, um die Vertraulichkeit sicherzustellen? Informieren Sie sich in M|2.1.0: Deep Dive – Schutzziel Vertraulichkeit hierüber.

#### Aufgabe 3

Wählen Sie aus den Maßnahmen die am besten geeigneten aus, um die Vertraulichkeit im Leitstand und an den Extrusionsanlagen der RECPLAST GmbH nachhaltig herzustellen.

Begründen Sie Ihre Auswahl gegenüber Frau Weber (CISO der RECPLAST GmbH):

- Warum sind genau diese Maßnahmen für die RECPLAST GmbH verhältnismäßig und realistisch?
- Welche Maßnahmen aus dem Katalog würden Sie für die Fertigungshalle eher nicht empfehlen und warum?

---

### Material M|2.1.0: Deep Dive – Schutzziel Vertraulichkeit

#### 1. Was bedeutet Vertraulichkeit?

Das Schutzziel **Vertraulichkeit** fordert, dass Informationen, Daten und IT-Systeme **ausschließlich autorisierten Personen, Prozessen oder IT-Systemen** zugänglich sind. Unbefugte – egal ob externe Angreifer oder nicht-berechtigte Kolleginnen und Kollegen im eigenen Unternehmen – dürfen keinen Einblick erhalten.

Ein Verlust der Vertraulichkeit liegt bereits dann vor, wenn vertrauliche Daten gelesen, kopiert oder offengelegt werden, ohne dass dabei zwangsläufig Daten verändert oder gelöscht werden müssen.

#### 2. Wie stellen wir Vertraulichkeit sicher?

Um Vertraulichkeit in einer modernen IT- und Produktionsumgebung (OT) durchzusetzen, kombinieren IT-Sicherheitsverantwortliche **technische und organisatorische Maßnahmen (TOMs)**.

##### A. Technische Maßnahmen

* **Verschlüsselung (Kryptografie):**
  * **Data in Transit (Übertragung):** Verschlüsselung von Netzwerkverbindungen (z.B. via TLS/HTTPS, IPsec, SSH), damit Datenpakete auf dem Leitungsweg nicht mitgeschnitten werden können.
  * **Data at Rest (Speicherung):** Festplatten- und Datenbankverschlüsselung (z.B. BitLocker, LUKS, AES-256), damit Daten bei Verlust oder Diebstahl von Datenträgern unlesbar bleiben.
  * **Data in Use (Verarbeitung):** Schutz von Daten im Arbeitsspeicher vor unbefugtem Auslesen anderer Prozesse.
* **Identitäts- und Zugriffsmanagement (IAM):**
  * **Personalisierte Accounts:** Jede Person erhält ein individuelles Benutzerkonto. Shared Accounts (gemeinsam genutzte Konten) sind strikt verboten.
  * **Starke Authentifizierung:** Einsatz von Multi-Faktor-Authentifizierung (MFA/2FA) mittels Passwörtern, Hardware-Token oder Biometrie.
  * **Rechtestrukturierung:** Rechtevergabe nach dem **Principle of Least Privilege** (Minimalprinzip) über Rollen-basierte Zugriffskontrollen (RBAC). Jede/r sieht nur das, was für die tägliche Arbeit zwingend notwendig ist (*Need-to-know-Prinzip*).
* **Netzwerksegmentierung:**
  * Trennung von Office-Netzen, Produktionsnetzen (OT/VLANs) und Gast-WLANs durch Firewalls, um unbefugte Datenströme zwischen den Segmenten zu blockieren.
* **Schnittstellen- und Endgeräteschutz (Endpoint Security):**
  * Logische Sperrung ungenutzter Ports (z.B. USB-Ports per Group Policy oder Endpoint-Protection-Software deaktivieren).

##### B. Organisatorische & Physische Maßnahmen

* **Klassifizierung von Informationen:** Einstufung von Dokumenten und Daten in Vertraulichkeitsstufen (z.B. *Öffentlich*, *Intern*, *Vertraulich*, *Streng vertraulich*) inklusive entsprechender Handhabungsvorschriften.
* **Physische Zutrittskontrollen:** Sicherung von Serverräumen, Leitständen und Archiven durch Schließanlagen, RFID-Chipkarten, Biometrie und Besucherdokumentation.
* **Betriebsvereinbarungen & Guidelines:** Verpflichtung auf das Datengeheimnis, Sicherheitsrichtlinien zur Nutzung von Wechselmedien und Clean-Desk-Policies.
* **Awareness-Schulungen:** Regelmäßige Trainings der Belegschaft gegen Social-Engineering-Angriffe (z.B. Phishing, Shoulder Surfing, Tailgating/Huckepackmitnahme).

---

### Arbeitsauftrag A|2.2: Asymmetrische und symmetrische Verschlüsselung unterscheiden

Frau Weber hat die bisherigen Ergebnisse der ChangeIT GmbH gesichtet und kommt auf einen weiteren Punkt zu sprechen:

*"Ein wichtiger Punkt für die Vertraulichkeit ist die Verschlüsselung. Wir müssen künftig die Übertragung der hochsensiblen Rezepturdaten vom zentralen Labor-ERP-System zu den Leitständen in Werkhalle 2 absichern. Wenn hier jemand im Netzwerk mithört, liegen unsere Firmengeheimnisse offen.*

*Ein Kollege schlägt vor, die Daten einfach mit einem Passwort per symmetrischer Verschlüsselung zu sichern. Ein anderer möchte lieber asymmetrische Verschlüsselung einsetzen, weil er meint, das wäre viel sicherer."*

#### Aufgabe 1

Beschreiben Sie kurz, welche Gefahr für die Vertraulichkeit besteht, wenn das Labor-ERP-System die neuen Kunststoff-Rezepturen im Klartext an die Extrusionsanlagen sendet.

#### Aufgabe 2

Erläutern Sie das grundlegende Problem des Schlüsselaustauschs (Key Distribution Problem), wenn das Labor und alle 12 Leitstände in den Hallen ausschließlich ein einziges, gemeinsames symmetrisches Passwort nutzen würden.

#### Aufgabe 3

Informieren Sie sich in den bereitgestellten Materialien über die Funktionsweisen der Kryptografie und bearbeiten Sie folgende Punkte:

- M|2.2.0: Symmetrische Verschlüsselung: Erklären Sie in eigenen Worten das Funktionsprinzip sowie die wesentlichen Vor- und Nachteile.
- M|2.2.1: Asymmetrische Verschlüsselung: Erläutern Sie das Konzept des Schlüsselpaares (Public Key und Private Key). Gehen Sie darauf ein, welcher Schlüssel zum Verschlüsseln und welcher zum Entschlüsseln genutzt wird.
- M|2.2.2: Hybride Verschlüsselung: Stellen Sie dar, wie das hybride Verfahren die Vorteile beider Ansätze kombiniert und wo es eingesetzt wird.

#### Aufgabe 4

Welches Verschlüsselungsverfahren (symmetrisch, asymmetrisch oder hybrid) empfehlen Sie Frau Weber für die automatische Übertragung der Rezepturdaten über das Firmennetzwerk?

---

### Material M|2.2.0: Symmetrische Verschlüsselung

Die symmetrische Verschlüsselung gehört zu den ältesten und grundlegendsten Verfahren der Kryptografie. Ihr zentrales Funktionsprinzip beruht auf der Verwendung eines einzigen, identischen Schlüssels (*Secret Key*) für sowohl die Ver- als auch die Entschlüsselung einer Nachricht. Wenn ein Klartext in einen unlesbaren Chiffretext umgewandelt werden soll, verarbeitet ein mathematischer Algorithmus die Ursprungsdaten zusammen mit diesem geheimen Schlüssel. Auf der Empfängerseite wird exakt derselbe Schlüssel benötigt, um den Chiffretext mithilfe des umgekehrten Algorithmus wieder in den ursprünglichen Klartext zurückzuverwandeln. Sender und Empfänger müssen somit zwingend über denselben geheimen Schlüssel verfügen.

In der modernen Informationstechnik findet die symmetrische Verschlüsselung breite Anwendung, insbesondere dort, wo große Datenmengen effizient geschützt werden müssen. Typische Einsatzbereiche sind die Festplatten- und Datenverschlüsselung im Ruhezustand (*Data at Rest*), beispielsweise durch Technologien wie BitLocker unter Windows oder LUKS unter Linux. Ebenso werden symmetrische Verfahren wie der AES-Standard (*Advanced Encryption Standard*) genutzt, um die eigentlichen Nutzdaten in gesicherten Netzwerkverbindungen (z.B. bei VPN-Tunneln via IPsec oder HTTPS-Verbindungen im Web) zu übertragen.

Der größte Vorteil symmetrischer Verschlüsselungsverfahren liegt in ihrer extrem hohen Rechengeschwindigkeit und Effizienz. Da die zugrundeliegenden mathematischen Operationen vergleichsweise einfach aufgebaut sind, können selbst riesige Dateien oder kontinuierliche Datenströme in Echtzeit und ohne spürbare Verzögerung ver- und entschlüsselt werden. Zudem bieten moderne Standardverfahren wie AES bei ausreichender Schlüssellänge (z.B. 256 Bit) ein extrem hohes Sicherheitsniveau gegen Brute-Force-Angriffe.

Dem steht jedoch ein gravierender Nachteil gegenüber: das sogenannte Schlüsselverteilungsproblem (*Key Distribution Problem*). Bevor zwei Parteien vertraulich miteinander kommunizieren können, muss der geheime Schlüssel über einen absolut sicheren Kanal ausgetauscht werden. Wird der Schlüssel während der Übertragung von dritter Seite abgefangen, ist die gesamte Vertraulichkeit kompromittiert. Zudem skaliert das Verfahren in Netzwerken schlecht: Sollen viele Parteien paarweise vertraulich miteinander kommunizieren, steigt die Anzahl der benötigten geheimen Schlüssel quadratisch an: Bei n Teilnehmern werden n·(n−1)/2 Schlüssel benötigt, bei 10 Teilnehmern also 45, bei 100 bereits 4.950. Das erschwert die Schlüsselverwaltung im Betrieb enorm.

---

### Material M|2.2.1: Asymmetrische Verschlüsselung

Die asymmetrische Verschlüsselung – auch bekannt als Public-Key-Kryptografie – löst das fundamentale Problem des sicheren Schlüsselaustauschs, indem sie ein mathematisch verknüpftes Schlüsselpaar einsetzt. Dieses Paar besteht aus einem öffentlichen Schlüssel (*Public Key*) und einem privaten Schlüssel (*Private Key*). Während der öffentliche Schlüssel gefahrlos allen Kommunikationspartnern zugänglich gemacht werden darf, muss der private Schlüssel streng geheim bleiben und darf seinen Besitzer niemals verlassen. Das zentrale Funktionsprinzip lautet: Eine Nachricht, die mit einem bestimmten öffentlichen Schlüssel verschlüsselt wurde, kann ausschließlich mit dem dazugehörigen, einzigartigen privaten Schlüssel wieder entschlüsselt werden. Ein Rückschluss vom öffentlichen auf den privaten Schlüssel ist nach heutigem Stand der Technik mathematisch praktisch unmöglich.

Eingesetzt wird die asymmetrische Verschlüsselung vorrangig überall dort, wo Partner ohne vorherigen sicheren Kontakt vertraulich miteinander kommunizieren müssen oder die Identität der Gegenseite nachgewiesen werden soll. Neben der reinen Datenverschlüsselung bildet sie das Fundament für digitale Signaturen (z.B. im E-Mail-Verkehr mit S/MIME oder PGP) sowie für digitale Zertifikate im Web. Wenn ein Browser eine sichere HTTPS-Verbindung zu einem Webserver aufbaut, wird die Identität des Anbieters über asymmetrische Zertifikate (Public Key Infrastructure, PKI) nachgewiesen und der erste Kontaktaufbau abgesichert.

Der herausragende Vorteil dieses Verfahrens liegt in der eleganten Lösung des Schlüsselverteilungsproblems. Da der öffentliche Schlüssel überall frei verteilt werden kann, entfällt die Notwendigkeit eines geheimen Kanals für den Schlüsselaustausch. Zudem skaliert das System hervorragend: Jede Komponente im Netzwerk benötigt lediglich ihr eigenes Schlüsselpaar, um vertraulich mit beliebig vielen anderen Partnern zu kommunizieren.

Hauptnachteil der asymmetrischen Verschlüsselung ist jedoch ihre sehr geringe Rechengeschwindigkeit. Die zugrundeliegenden komplexen mathematischen Operationen (wie das Zerlegen sehr großer Zahlen in ihre Primfaktoren oder Berechnungen auf elliptischen Kurven) erfordern erhebliche Rechenleistung. Für das Ver- und Entschlüsseln großer Datenmengen oder kontinuierlicher Datenströme ist das Verfahren daher viel zu langsam und im Betriebsalltag unpraktikabel.

---

### Material M|2.2.2: Hybride Verschlüsselung

Die hybride Verschlüsselung vereint die spezifischen Stärken der symmetrischen und der asymmetrischen Verschlüsselung in einem gemeinsamen Verfahren. Sie löst damit das grundlegende Dilemma der modernen Kryptografie: die Wahl zwischen der hohen Rechengeschwindigkeit symmetrischer Algorithmen und dem komfortablen, sicheren Schlüsselaustausch asymmetrischer Verfahren. Das Funktionsprinzip teilt den Verschlüsselungsprozess in zwei Schritte auf. Für die eigentliche Nachricht wird zunächst ein einmaliger, zufällig generierter symmetrischer Schlüssel erzeugt – der sogenannte Sitzungsschlüssel (*Session Key*). Die eigentlichen Nutzdaten werden mit diesem Sitzungsschlüssel extrem schnell symmetrisch verschlüsselt. Anschließend wird der Sitzungsschlüssel selbst mit dem öffentlichen Schlüssel (*Public Key*) des Empfängers asymmetrisch verschlüsselt. Beide Teile – der symmetrisch verschlüsselte Text und der asymmetrisch verschlüsselte Sitzungsschlüssel – werden zusammen an den Empfänger übertragen.

Der Empfänger nutzt nach dem Empfang seinen eigenen privaten Schlüssel (*Private Key*), um den Sitzungsschlüssel zu entschlüsseln. Mit dem so gewonnenen Klartext-Sitzungsschlüssel kann er im nächsten Schritt die eigentliche Nachricht blitzschnell symmetrisch entschlüsseln. Durch diese Kombination entfällt die Notwendigkeit, vorab einen geheimen Schlüssel über einen unsicheren Kanal auszutauschen, während gleichzeitig die hohe Verarbeitungsgeschwindigkeit für große Datenmengen erhalten bleibt.

In der Praxis ist die hybride Verschlüsselung der weltweite Standard für fast alle modernen Kommunikationsprotokolle. Sie bildet das Rückgrat der Transport Layer Security (TLS/SSL) bei HTTPS-Verbindungen im Internet, sichert den Datenaustausch in Virtual Private Networks (VPNs) ab und kommt bei der verschlüsselten E-Mail-Übertragung (z.B. via S/MIME oder PGP) sowie bei sicheren SSH-Verbindungen zur Serververwaltung zum Einsatz.

Der entscheidende Vorteil dieses Verfahrens ist die optimale Kombination aus Effizienz und Sicherheit. Selbst riesige Datenmengen oder kontinuierliche Datenströme können ohne spürbare Performance-Einbußen geschützt werden, während das Schlüsselverteilungsproblem vollständig gelöst ist. Als einziger relativer Nachteil kann der leicht erhöhte organisatorische und technische Systemaufwand genannt werden, da beide Verschlüsselungsarten implementiert und eine geeignete Infrastruktur zur Verwaltung der öffentlichen Schlüssel (PKI) bereitgestellt werden muss.

---

### Arbeitsauftrag A|2.3: Multi-Faktor-Authentifizierung durchführen

Frau Weber ruft Sie an ihren Bildschirm im IT-Büro: 

"Wir haben den Vorfall in Werkhalle 2 weiter analysiert. Dass sich alle Techniker das Sammelkonto betrieb_halle2 mit dem Passwort Recplast2024! teilen, war ein offenes Scheunentor für den unbefugten Zugriff. Jeder, der den Zettel am Leitstand liest, kann sich als Hallenpersonal ausgeben. Wir müssen auf individuelle Benutzerkonten umstellen. Aber ein einfaches Passwort reicht mir für den Zugriff auf die Steuerungsterminals nicht mehr aus – Passwörter werden aufgeschrieben, erraten oder weitergegeben. Wir müssen eine Multi-Faktor-Authentifizierung (MFA) einführen. Vor allem für den Schnellzugriff an den Terminals in der Fertigung und den Remote-Zugriff der externen Wartungstechniker müssen wir entscheiden, wie wir die drei Kategorien der Authentifizierung sinnvoll kombinieren."

#### Aufgabe 1

Erläutern Sie, warum die bisherige Authentifizierung über das alleinige Passwort `Recplast2024!` am Leitstand das Schutzziel Vertraulichkeit (sowie die Zurechenbarkeit) verletzt.

#### Aufgabe 2

Beschreiben Sie das fundamentale Sicherheitsrisiko, wenn sich ein Authentifizierungsverfahren ausschließlich auf den Faktor Wissen (also das Passwort wissen) stützt.

#### Aufgabe 3

Informieren Sie sich in den bereitgestellten Materialien über die drei Kategorien der Authentifizierung und bearbeiten Sie folgende Punkte:

- M|2.3.0: Faktor Wissen (Passwörter und Geheimnisse): Erklären Sie das Funktionsprinzip dieser Kategorie. Beschreiben Sie, welche Kriterien ein sicheres Passwort erfüllen muss und warum Hashfunktionen bei der Speicherung auf Servern eingesetzt werden.
- M|2.3.1: Faktor Besitz (Hardware-Token, TOTP und Passkeys): Erläutern Sie das Prinzip des Besitz-Nachweises. Stellen Sie die Funktionsweisen von physischen Token (z.B. RFID-Chips/Hardware-Keys) sowie den logischen Verfahren TOTP (zeitbasierte Einmalpasswörter) und Passkey (FIDO2/WebAuthn) dar.
- M|2.3.2: Faktor Biometrie / Inhärenz (Körperliche Merkmale): Erklären Sie, wie die Identifikation über körperliche Merkmale funktioniert. Nennen Sie die wesentlichen Vorteile und Risiken.

#### Aufgabe 4

Definieren Sie kurz, ab wann eine Anmeldung formal als Multi-Faktor-Authentifizierung (MFA) bzw. Zwei-Faktor-Authentifizierung (2FA) gilt.

#### Aufgabe 5

Kommen Sie zurück auf die Bedienung der Leitstände in Werkhalle 2 sowie den Remote-Zugriff der externen Wartungsfirma:

- Szenario A (Leitstand in der Fertigungshalle): Wählen Sie eine geeignete Kombination aus zwei Faktoren (aus Wissen, Besitz oder Biometrie) für die Schichtarbeiter direkt an den Extrusionsanlagen. Begründen Sie Ihre Wahl im Hinblick auf Praxistauglichkeit (z.B. Arbeiten mit Handschuhen, schnelle Anmeldung) und Sicherheit.
- Szenario B (Remote-Zugriff der Wartungsfirma): Welches MFA-Verfahren empfehlen Sie für den externen Fernzugriff von Wartungstechnikern der Krämer Anlagenservice GmbH auf die Steuerungssysteme der RECPLAST GmbH?

Begründen Sie Ihre Entscheidungen.

---

### Material M|2.3.0: Faktor Wissen (Passwörter und Geheimnisse)

#### Die drei Faktoren und MFA im Überblick

Bei der Authentifizierung weist eine Person nach, dass sie wirklich die ist, für die sie sich ausgibt. Dafür gibt es drei Kategorien (Faktoren): Wissen (etwas, das man weiß), Besitz (etwas, das man hat) und Inhärenz bzw. Biometrie (etwas, das man ist).

Von Multi-Faktor-Authentifizierung (MFA) spricht man, wenn sich eine Person mit mindestens zwei Faktoren aus unterschiedlichen Kategorien ausweist. Bei genau zwei Faktoren heißt das Zwei-Faktor-Authentifizierung (2FA). Entscheidend ist die Kategorie, nicht die Anzahl der Abfragen: Ein Passwort plus eine Sicherheitsfrage sind keine MFA, weil beide zum Faktor Wissen gehören. Ein Passwort plus ein TOTP-Code vom Smartphone (Wissen und Besitz) sind dagegen 2FA.

Dieses Material und die beiden folgenden stellen die drei Faktoren nacheinander vor.

#### Faktor Wissen

Die Authentifizierung über den Faktor Wissen ist das historisch älteste und am weitesten verbreitete Verfahren zur Identitätsprüfung in der IT. Das Grundprinzip ist simpel: Ein Benutzer beweist seine Identität gegenüber einem System, indem er eine Information angibt, die theoretisch nur ihm allein bekannt sein sollte. Die typischsten Vertreter dieser Kategorie sind Passwörter, Passphrasen, PINs (Personal Identification Numbers) oder Antworten auf Sicherheitsfragen. Da der Server die eingegebene Information mit dem hinterlegten Soll-Wert vergleicht, findet bei erfolgreicher Übereinstimmung der Zugriff statt.

In der Unternehmenspraxis stellt der Faktor Wissen jedoch eine der größten Schwachstellen für die Vertraulichkeit dar. Passwörter werden von Nutzern häufig zu kurz gewählt, für mehrere Dienste wiederverwendet, auf Notizzettel geschrieben oder fallen Social-Engineering-Angriffen (wie Phishing) zum Opfer. Ein sicheres Passwort sollte daher eine ausreichende Länge (mindestens 12 bis 16 Zeichen) aufweisen und eine Kombination aus Groß- und Kleinbuchstaben, Zahlen sowie Sonderzeichen enthalten. Noch sicherer sind sogenannte Passphrasen – lange, leicht merkbare Satzkonstruktionen.

Um das Risiko von gestohlenen oder erratenen Kennwörtern zu minimieren, dürfen Passwörter auf Servern niemals im Klartext gespeichert werden. Stattdessen werden sie mithilfe kryptografischer Einwegfunktionen (Hashfunktionen wie bcrypt oder Argon2) unter Beigabe eines zufälligen Werts (Salt) verarbeitet. Der größte systematische Nachteil des Faktors Wissen bleibt jedoch bestehen: Sobald eine andere Person das Geheimnis erfährt – sei es durch Blicke über die Schulter (Shoulder Surfing), Datenlecks oder Schwachstellen im System – kann sie sich ohne jegliche Hürde für den rechtmäßigen Nutzer ausgeben.

---

### Material M|2.3.1: Faktor Besitz (Hardware-Token, TOTP und Passkeys)

Der Faktor Besitz basiert darauf, dass der Benutzer seine Identität durch den physikalischen oder logischen Nachweis eines Gegenstandes belegt, den nur er besitzt. Das Funktionsprinzip verlangt, dass der Benutzer Zugriff auf dieses spezifische Objekt hat, um eine Authentifizierung erfolgreich abzuschließen. Klassische physische Beispiele hierfür sind RFID-Chipkarten für Schließsysteme, USB-Hardware-Token (z.B. YubiKeys) oder Chipkartenleser.

In der modernen IT-Sicherheit haben sich vor allem zwei besitzbasierte Verfahren etabliert:

- **Time-based One-time Password (TOTP):** Hierbei generiert eine App auf einem registrierten Gerät (z.B. Smartphone) alle 30 bis 60 Sekunden einen neuen, einmalig gültigen 6-stelligen Code. Dies geschieht auf Basis eines gemeinsamen Geheimnisses (Shared Secret) und der exakten Uhrzeit. Der Code beweist, dass der Nutzer das registrierte Gerät aktuell besitzt.
- **Passkey:** Dies ist ein hochmoderner Standard (FIDO2/WebAuthn), der das klassische Passwort vollständig ersetzt. Das Gerät des Nutzers (z.B. Smartphone, Laptop oder Security-Key) speichert einen eindeutigen privaten Schlüssel (Private Key). Bei der Anmeldung fordert der Server das Gerät auf, eine Challenge kryptografisch zu signieren. Der Nachweis erfolgt ausschließlich über den Besitz dieses kryptografischen Schlüssels auf dem physikalischen Gerät.

Der entscheidende Vorteil des Faktors Besitz liegt in seiner Resistenz gegen reine Online-Passwort-Diebstähle oder Phishing-Angriffe (insbesondere bei FIDO2/Passkeys). Ein Angreifer, der lediglich ein Passwort kennt, kann sich ohne das physische Gerät nicht anmelden. Ein Nachteil besteht im logistischen Aufwand: Geht der Gegenstand verloren, beschädigt oder wird das Smartphone gestohlen, sind strukturierte Wiederherstellungsprozesse (Recovery-Prozesse) erforderlich, um den Nutzer nicht dauerhaft auszusperren.

---

### Material M|2.3.2: Faktor Biometrie / Inhärenz (Körperliche Merkmale)

Der Faktor Biometrie (auch als Inhärenz bezeichnet) nutzt unverwechselbare, körperliche oder verhaltensbedingte Eigenschaften eines Menschen zur Authentifizierung. Das zugrundeliegende Prinzip lautet: Der Benutzer weist nach, wer er ist. Da biometrische Merkmale fest mit der Person verbunden sind, können sie im Gegensatz zu Passwörtern nicht vergessen und im Gegensatz zu Hardware-Token nicht zu Hause liegen gelassen werden. Zu den am häufigsten genutzten biometrischen Verfahren gehören der Fingerabdruckscan, die Gesichtserkennung (Face ID), der Iris-Scan sowie die Venenerkennung.

Eingesetzt wird die Biometrie heute flächendeckend bei der Freischaltung von mobilen Endgeräten (Smartphones, Tablets), an modernen Zutrittskontrollsystemen für Sicherheitsbereiche (z.B. Rechenzentren) sowie als lokaler Freigabemechanismus bei Passkey-Anmeldungen. Die Sensoren erfassen die biologischen Daten, wandeln sie in ein mathematisches Muster (Template) um und vergleichen dieses mit dem lokal abgespeicherten Referenzmuster.

Der größte Vorteil der Biometrie liegt in der hervorragenden Benutzerfreundlichkeit und Schnelligkeit. Die Freigabe erfolgt in Sekundenbruchteilen, ohne dass sich der Nutzer komplexe Zeichenfolgen merken muss. Zudem ist eine Weitergabe der Zugangsdaten an Kollegen (z.B. im Schichtbetrieb) nahezu ausgeschlossen.

Dennoch birgt die Biometrie spezifische Nachteile und Risiken: Ein biometrisches Merkmal ist niemals geheim – Fingerabdrücke werden auf Oberflächen hinterlassen und Gesichter sind öffentlich sichtbar. Wird ein biometrischer Datensatz einmal kompromittiert oder nachgebildet (z.B. durch hochauflösende Attrappen), kann das Merkmal im Gegensatz zu einem Passwort niemals geändert werden – ein Mensch hat schließlich nur einen Satz Fingerabdrücke. Zudem müssen bei der Speicherung und Verarbeitung biometrischer Daten strengste Datenschutzanforderungen eingehalten werden.

---

### Arbeitsauftrag A|2.4: Benutzer und Rechtevergabe planen

Nachdem Sie gemeinsam mit Frau Weber die Multi-Faktor-Authentifizierung (MFA) für die Terminals in Werkhalle 2 geplant haben, steht der nächste Schritt an: Das gemeinsame Sammelkonto `betrieb_halle2` muss endgültig gelöscht und durch ein strukturiertes, individuelles Benutzermanagement ersetzt werden.

Frau Weber erklärt das Ziel der Maßnahme:

*"MFA nützt uns nichts, wenn am Ende zwar jeder Techniker sein eigenes Login hat, aber alle dieselben Vollzugriffsrechte besitzen. Letzte Woche hat ein Azubi aus Versehen die Extruder-Temperatureinstellungen einer Anlage im System überschrieben – einfach, weil sein Account dieselben Rechte hatte wie der des Fertigungsleiters. Wir brauchen ein klares Berechtigungskonzept: Jeder Mitarbeiter darf nur genau das tun und sehen, was er für seine tägliche Arbeit wirklich braucht. Zudem können wir nicht für jeden einzelnen Mitarbeiter händisch Rechte vergeben und pflegen – bei Personalwechseln blickt sonst keiner mehr durch. Wir müssen Rollen definieren und Berechtigungen über Gruppen steuern."*

#### Aufgabe 1

Erläutern Sie, welche Risiken entstehen, wenn allen Benutzern im Unternehmen standardmäßig administrative Schreib- oder Konfigurationsrechte eingeräumt werden.

#### Aufgabe 2

Informieren Sie sich im M|2.4.0: Principle of Least Privilege und erklären Sie das Principle of Least Privilege (Prinzip der minimalen Rechtevergabe). Begründen Sie, warum dieses Prinzip für das Schutzziel der Integrität und Vertraulichkeit bei RECPLAST essenziell ist.

#### Aufgabe 3

Arbeiten Sie anhand des M|2.4.1: Berechtigungen und Gruppen folgende Grundlagen heraus:

- Benutzerverwaltung vs. Rechtesteuerung: Unterscheiden Sie zwischen der Identität eines Benutzers (User Account) und seinen Berechtigungen (Permissions).
- Rollenbasierte Zugriffskontrolle (RBAC - Role-Based Access Control):
  - Erklären Sie das Funktionsprinzip von RBAC (Zuordnung von Benutzern zu Gruppen/Rollen und Rollen zu Berechtigungen).
  - Welche administrativen Vorteile bietet RBAC gegenüber der direkten Zuweisung von Rechten an einzelne Personen (z.B. bei Neueinstellungen, Abteilungswechseln oder Kündigungen)?
- Rechte-Arten: Differenzieren Sie kurz zwischen Lese- (Read), Schreib- (Write), Ausführ- (Execute) und Administrationsrechten im Kontext von Anwendungs- und Dateisystemzugriffen.

#### Aufgabe 4

In Werkhalle 2 arbeiten verschiedene Personengruppen an den Steuerungsterminals. Erstellen Sie ein Berechtigungskonzept nach dem RBAC-Prinzip für folgende Rollen:

- Maschinenbediener / Techniker (Schichtbetrieb)
- Fertigungsleitung / Schichtführer
- Auszubildende / Praktikanten
- Externe Wartungs-Techniker

Erstellen Sie eine Übersicht (z.B. als Berechtigungsmatrix), aus der hervorgeht:

- Welche Rolle welche Lese-, Schreib- oder Sonderrechte auf die Anlagensteuerung und Rezepturdatenbank besitzt. Sie können die Kürzel (r=read, w=write, x=execute) verwenden.
- Wie Sie das Principle of Least Privilege speziell für die Gruppe der Auszubildenden und der externen Wartungstechniker umsetzen?

---

### Material M|2.4.0: Principle of Least Privilege

Das Principle of Least Privilege (PoLP) – im Deutschen auch als Prinzip der minimalen Rechtevergabe oder Minimalprinzip bezeichnet – ist eines der wichtigsten Grundprinzipien der Informationssicherheit. Das Prinzip besagt, dass jeder Benutzer, jeder Prozess und jedes IT-System nur exakt diejenigen Zugriffsrechte und Befugnisse erhalten darf, die für die ordnungsgemäße Erfüllung der jeweiligen spezifischen Aufgabe zwingend erforderlich sind. Jegliche darüber hinausgehenden Rechte sind konsequent zu verweigern (Default Deny).

In vielen Unternehmensnetzwerken herrscht in der Praxis das Antipattern vor, Benutzern aus Bequemlichkeit globale Administratorrechte einzuräumen. Dies birgt enorme Sicherheitsrisiken: Erlangt ein Schädling (z.B. Ransomware) Zugriff auf einen Account mit erweiterten Rechten, kann sich die Schadsoftware ungehindert im gesamten System ausbreiten, Daten verschlüsseln oder vertrauliche Informationen entwenden. Wenden IT-Verantwortliche das PoLP konsequent an, wird der mögliche Schaden im Falle eines Sicherheitsvorfalls auf den unmittelbaren Wirkungsbereich des betroffenen Kontos begrenzt (Schadenseindämmung / Blast Radius Reduction).

Neben dem Schutz vor Schadsoftware schützt das Principle of Least Privilege das Unternehmen auch vor unbeabsichtigten Fehlern durch eigenes Personal – wie etwa dem versehentlichen Löschen von Systemkonfigurationen oder dem Überschreiben kritischer Produktionsdaten. Zudem unterstützt es das Schutzziel der Vertraulichkeit, da Mitarbeiter nur Einblick in diejenigen Daten erhalten, die für ihre Rolle zwingend notwendig sind (Need-to-know-Prinzip). Die Vergabe von Rechten sollte daher stets temporär beschränkt, regelmäßig überprüft (Access Review) und nach Beendigung einer Aufgabe sofort wieder auf das Minimum zurückgesetzt werden.

---

### Material M|2.4.1: Berechtigungen und Gruppen

Um das Principle of Least Privilege in einem Unternehmen effizient umzusetzen, reicht eine rein individuelle Rechtevergabe pro Person nicht aus. Wenn Systemadministratoren jedem einzelnen Mitarbeiter händisch Lese-, Schreib- oder Ausführungsrechte zuweisen müssten, würde dies bei Personalwechseln, Neueinstellungen oder Vertretungen schnell zu einem unüberschaubaren Verzeichnis- und Rechtechaos (Privilege Creep) führen. Die Lösung hierfür ist die Einführung von Berechtigungskonzepten auf Basis von Gruppen und Rollen.

Dabei sind zwei Dinge zu unterscheiden: Die Identität eines Benutzers wird durch sein Benutzerkonto (User Account) festgelegt und durch die Authentifizierung nachgewiesen. Sie beantwortet die Frage, wer jemand ist. Die Berechtigungen (Permissions) legen fest, was dieses Konto im System lesen, ändern oder ausführen darf (Autorisierung). Ein Konto allein verleiht also noch keine Rechte, erst die Zuweisung von Berechtigungen bestimmt den Handlungsspielraum.

In der IT-Sicherheit unterscheidet man grundlegend zwischen verschiedenen Zugriffsarten auf Dateien, Datenbanken oder Systemfunktionen:

- Lesen (Read / r): Berechtigt zum Einsehen und Auslesen von Daten, Dokumenten oder Konfigurationen, ohne diese verändern zu können.
- Schreiben (Write / w): Erlaubt das Erstellen, Ändern, Überschreiben oder Löschen von Daten und Einstellungen.
- Ausführen (Execute / x): Gestattet das Starten von Programmen, Skripten oder Steuerungsbefehlen auf Systemen.
- Vollzugriff / Administration: Erlaubt zusätzlich das Ändern von Berechtigungen und das Ändern der Eigentümerschaft an Ressourcen.

Der weltweite Standard zur effizienten Verwaltung dieser Rechte ist die Rollenbasierte Zugriffskontrolle (engl. Role-Based Access Control, RBAC). Bei RBAC werden Berechtigungen nicht direkt an einzelne Personen vergeben, sondern an logische Rollen (bzw. Benutzergruppen), die den Aufgaben im Betrieb entsprechen (z.B. Gruppe_Fertigung, Gruppe_Labor, Gruppe_Azubis).

Das Verfahren folgt einem Drei-Stufen-Modell:

- Rechte den Rollen zuweisen: Der Rolle Gruppe_Fertigung werden exakt die Lese- und Schreibrechte zugewiesen, die in der Halle benötigt werden.
- Benutzer den Rollen zuweisen: Einzelne Mitarbeiterkonten (z.B. k.müller) werden Mitglied der jeweiligen Gruppe.
- Vererbung nutzen: Der Benutzer k.müller erbt automatisch alle Rechte der Rolle Gruppe_Fertigung.

Der zentrale Vorteil von RBAC liegt in der enormen administrativen Erleichterung und Übersichtlichkeit. Tritt ein neuer Mitarbeiter in das Unternehmen ein, muss er lediglich der passenden Gruppe hinzugefügt werden und besitzt sofort alle notwendigen Rechte. Wechselt ein Kollege die Abteilung, wird er aus der alten Gruppe entfernt und der neuen hinzugefügt – ein mühsames Suchen und Entfernen einzelner Altrechte entfällt vollständig. Dadurch wird die Compliance gewahrt, und es wird verhindert, dass Konten im Laufe der Jahre unbemerkt immer mehr Rechte ansammeln.

---

### Arbeitsauftrag A|2.5: Endpoint Security planen

Wenige Tage nach dem ersten Vorfall hat ein Wartungstechniker der Krämer Anlagenservice GmbH am Leitstand in Werkhalle 2 einen eigenen USB-Stick eingesteckt, um ein Software-Update aufzuspielen. Kurze Zeit später meldet die Antiviren-Software verdächtige Skriptaktivitäten im Hintergrund des Steuerungsterminals. Frau Weber reagiert sofort und bittet Sie, ein kompaktes Sicherheitskonzept zur Absicherung aller Endgeräte (Büro-PCs und Fertigungsterminals) auszuarbeiten.

#### Aufgabe 1

Erläutern Sie zwei konkrete Sicherheitsrisiken, die von ungeschützten USB-Schnittstellen und Drahtlosverbindungen an den Terminals in der Fertigung ausgehen.

#### Aufgabe 2

Informieren Sie sich im M|2.5.0: Endgeräte und ihre Schnittstellen absichern und beschreiben Sie den Unterschied zwischen einer rein physischen Schnittstellensperre (z.B. USB-Port-Blocker) und einer softwareseitigen Schnittstellensteuerung.

#### Aufgabe 3

Erstellen Sie für die Terminals in Werkhalle 2 einen konkreten 3-Punkte-Plan zur Härtung der Endgeräte. Berücksichtigen Sie dabei:

- Den Umgang mit USB-Ports und Wechselmedien.
- Den Schutz vor Schadsoftware und verzögerten Updates.
- Den Schutz mobiler Endgeräte (z.B. Laptops der Schichtleitung) bei Verlust oder Diebstahl.

---

### Material M|2.5.0: Endgeräte und ihre Schnittstellen absichern

Jedes Endgerät (engl. Endpoint) – ob Büro-PC, Industrieterminal, Smartphone oder Laptop – stellt ein mögliches Einfallstor in das Unternehmensnetzwerk dar. Unter Endpoint Security versteht man die Gesamtheit aller Maßnahmen, die ein solches System vor unbefugtem Zugriff, Schadsoftware und Datenabfluss (Data Loss Prevention) schützen.

Ein zentraler Angriffspfad führt über physische und logische Schnittstellen:

- USB-Ports & Wechselmedien: Über ungeschützte USB-Schnittstellen kann leicht Schadsoftware (z.B. Malware, Keylogger) eingeschleust werden. Zudem können vertrauliche Unternehmensdaten unbemerkt auf externe Datenträger kopiert werden.
- Drahtlose Schnittstellen (WLAN / Bluetooth / NFC): Nicht benötigte Funkverbindungen bieten Angreifern Angriffsflächen für Man-in-the-Middle-Attacken oder das Auslesen von Signalen in unmittelbarer Nähe.
- Netzwerkschnittstellen (LAN): Unbeaufsichtigte Netzwerkdosen in öffentlich zugänglichen Bereichen ermöglichen das Anstecken fremder Geräte (Rogue Devices).

Zur Absicherung von Endgeräten werden technische und organisatorische Maßnahmen kombiniert:

- Schnittstellen-Härtung (Hardening): Physische Sperren (z.B. USB-Port-Blocker) oder softwareseitige Richtlinien (z.B. Deaktivierung von USB-Datenträgern via Gruppenrichtlinien/GPO). Deaktivierung aller ungenutzten Schnittstellen (Bluetooth, WLAN).
- Endpoint Detection & Response (EDR) / Antivirus: Einsatz zentral verwalteter Schutzsoftware, die verhaltensbasiert Schadsoftware erkennt, isoliert und dem Sicherheitsteam meldet.
- Patch-Management & Betriebssystem-Updates: Regelmäßiges Schließen von Sicherheitslücken in Betriebssystemen und Anwendungen.
- Festplattenverschlüsselung: Schutz von Daten auf mobilen Geräten bei Verlust oder Diebstahl (z.B. via BitLocker).
- Anwendungskontrolle (Application Whitelisting): Auf dem Endgerät dürfen nur ausdrücklich freigegebene Programme ausgeführt werden (z.B. über AppLocker). Unbekannte oder nicht signierte Dateien, etwa von einem fremden USB-Stick, werden blockiert.

---

### Arbeitsauftrag A|2.6: Klassifizierung von Informationen durchführen

Frau Weber entdeckt bei einem Rundgang durch Werkhalle 2 auf einem Drucker einen unbedeckten Ausdruck der exakten Mischungsverhältnisse für die Granulat-Serie REC-Poly-3. Gleichzeitig liegen im Büro der Schichtleitung ausgedruckte Wartungsprotokolle und Dienstpläne offen herum.

Frau Weber stellt fest: *"Unsere Mitarbeiter wissen gar nicht, welche Dokumente wie geschützt werden müssen. Ein Auszubildender hat letzte Woche sogar einen Entwurf unseres neuen Fertigungsverfahrens per unverschlüsselter Mail an einen externen Lieferanten geschickt. Wir müssen eine klare Datenklassifizierung einführen, damit jedem im Betrieb sofort bewusst ist, wie mit welchen Informationen umzugehen ist."*

#### Aufgabe 1

Erläutern Sie den Zweck einer Informationsklassifizierung im Unternehmen.

#### Aufgabe 2

Informieren Sie sich mittels M|2.6.0: Vertraulichkeitsstufen definieren und nennen Sie die vier gängigen Vertraulichkeitsstufen und beschreiben Sie kurz den jeweiligen Schutzbedarf.

#### Aufgabe 3

Ordnen Sie die folgenden bei RECPLAST vorkommenden Daten und Dokumente einer passenden Vertraulichkeitsstufe (Öffentlich, Intern, Vertraulich, Streng vertraulich) zu und begründen Sie Ihre Entscheidung anhand möglicher Folgeschäden bei Offenlegung:

- Sicherheitsdatenblatt für Granulate (auf der RECPLAST-Website abrufbar).
- Der aktuelle Schichtplan der Werkhalle 2.
- Die chemische Zusammensetzung und Mischungsrezeptur des Additivs REC-Poly-3.
- Gehaltsabrechnungen und Personalakten der Schichtleiter.

#### Aufgabe 4

Erstellen Sie für Frau Weber eine kurze Richtlinie zur Handhabung für die Stufe "Streng vertraulich" (z.B. bezüglich der Rezepturen). Legen Sie fest:

- Wie müssen digitale Dateien (z.B. beim Versand per E-Mail) und Papierdokumente geschützt werden?
- Welche Regeln gelten für die Lagerung und Vernichtung dieser Unterlagen?

---

### Material M|2.6.0: Vertraulichkeitsstufen definieren

Nicht alle Informationen in einem Unternehmen sind gleich schützenswert. Während eine Pressemitteilung oder eine Broschüre für die Öffentlichkeit bestimmt ist, können verloren gegangene Kundendaten, Finanzzahlen oder Produktionsrezepturen existenzbedrohende Schäden nach sich ziehen. Die Klassifizierung von Informationen ist ein zentraler Prozess der Informationssicherheit, um Daten systematisch nach ihrem Schutzbedarf einzustufen und mit entsprechenden Schutzmaßnahmen zu belegen.

Ein typisches Schema gliedert Informationen in vier Vertraulichkeitsstufen:

- Öffentlich (Public): Daten, deren Offenlegung dem Unternehmen nicht schadet und die für die Allgemeinheit bestimmt sind (z.B. Produktkataloge, Stellenausschreibungen, Marketing-Flyer).
- Intern (Internal): Daten für den normalen Geschäftsbetrieb, die nur für Mitarbeiter bestimmt sind. Eine Weitergabe an Dritte ist nicht vorgesehen, der Schaden bei Offenlegung wäre jedoch gering (z.B. internes Telefonverzeichnis, Kantinenplan, allgemeine Arbeitsanweisungen).
- Vertraulich (Confidential): Sensible Daten, deren unbefugte Weitergabe dem Unternehmen erheblichen finanziellen, rechtlichen oder Reputationsschaden zufügen könnte (z.B. Kunden- und Lieferantenverträge, Personalakten, Quellcodes, detaillierte Kennzahlen).
- Streng vertraulich (Restricted / Strictly Confidential): Höchste Schutzstufe für kritische Kerninformationen (Betriebsgeheimnisse). Eine Kompromittierung bedroht den Fortbestand des Unternehmens oder verletzt Gesetze massiv (z.B. patentfähige Erfindungen, exklusive chemische Rezepturen, Zugangsdaten zu Kernsystemen).

Für jede Stufe müssen eindeutige Handhabungsvorschriften festgelegt werden. Diese regeln, wie Dokumente gekennzeichnet (z.B. Wasserzeichen, Kopfzeilen), wie sie gespeichert und übertragen (z.B. Pflicht zur Verschlüsselung) und wie sie entsorgt werden dürfen (z.B. Aktenvernichter nach DIN 66399).

---

### Arbeitsauftrag A|2.7: Physische Zutrittskontrollen einrichten

Bei einer Überprüfung der Aufnahmen der Flur-Kamera stellt Frau Weber fest, dass letzte Woche ein externer Handwerker ohne Begleitung durch Werkhalle 2 spaziert ist. Er blieb kurz am unbesetzten Leitstand stehen, blickte auf den Monitor der Extrusionsanlage und ging anschließend weiter in Richtung des Hallenverteiler-Raums, dessen Tür angelehnt war.

Frau Weber ist alarmiert: "Digitale Sperren nützen nichts, wenn jeder Hinz und Kunz physisch an unsere Terminals und Hallenverteiler herankommen kann! Wir müssen die physische Sicherheit bei RECPLAST von der Werkseinfahrt bis zum Serverraum komplett neu organisieren."

#### Aufgabe 1

Erläutern Sie, warum physische Zutrittskontrollen eine zwingende Voraussetzung für die digitale Vertraulichkeit von Daten sind.

#### Aufgabe 2

Differenzieren Sie die Schutzanforderungen für folgende drei Zonen bei RECPLAST:

- Der zentrale Serverraum der IT.
- Der Leitstand in Werkhalle 2.
- Der Besucher- und Verwaltungsbereich.

#### Aufgabe 3

Identifizieren Sie im obigen Szenario mindestens drei Verstöße gegen physische Sicherheitsprinzipien und ordnen Sie diese den jeweils verletzten Regeln aus M|2.7.0: Sicherung von Serverräumen, M|2.7.1: Sicherung von Arbeitsplätzen sowie M|2.7.2: Besucher im Unternehmen zu.

#### Aufgabe 4

Entwerfen Sie für Frau Weber einen 3-Punkte-Maßnahmenkatalog, um die physische Sicherheit bei RECPLAST nachhaltig zu verbessern:

- Maßnahme 1 (Server- & Technikräume): Welche baulichen und technischen Zutrittssicherungen empfehlen Sie für den Serverraum und die Hallenverteiler? (M|2.7.0: Sicherung von Serverräumen)
- Maßnahme 2 (Arbeitsplätze & Terminals): Welche Verhaltensregeln und technischen Einstellungen müssen für die Leitstände und Büros durchgesetzt werden? (M|2.7.1: Sicherung von Arbeitsplätzen)
- Maßnahme 3 (Besuchermanagement): Welche konkreten Regeln müssen ab sofort für fremde Personen auf dem Werksgelände gelten? (M|2.7.2: Besucher im Unternehmen)

---

### Material M|2.7.0: Sicherung von Serverräumen

Der Serverraum ist das physische Herzstück der Unternehmens-IT. Schlägt die physische Sicherheit fehl, greifen selbst die stärksten digitalen Schutzmaßnahmen wie Firewalls oder komplexe Passwörter nicht mehr: Wer physischen Zugriff auf Server, Switche oder Speichergeräte hat, kann Hardware unbemerkt manipulieren, Festplatten entnehmen oder direkte Kabelverbindungen herstellen.

Die Absicherung eines Serverraums erfordert daher ein umfassendes Schutzkonzept:

- Zutrittskontrolle & Dokumentation: Der Zutritt darf ausschließlich befugtem IT-Personal gestattet sein. Die Verriegelung erfolgt über mechatronische Schließsysteme, RFID-Chipkarten oder biometrische Lesegeräte. Jedes Öffnen der Tür wird elektronisch protokolliert.
- Bauliche & Raumphysische Maßnahmen: Der Serverraum sollte sich in einem inneren Kernbereich des Gebäudes (ohne Außenfenster) befinden. Wände und Türen müssen widerstandsfähig gegen Einbruch und Feuer sein.
- Umgebungsüberwachung (Monitoring): Sensoren überwachen Temperatur, Luftfeuchtigkeit, Rauchentwicklung und Wasserlecks. Redundante Klimaanlagen verhindern Hitzeschäden, während automatische, personenverträgliche Gaslöschanlagen (z.B. Novec 1230 oder Stickstoff) Brände löschen, ohne die Elektronik durch Wasser zu zerstören.

---

### Material M|2.7.1: Sicherung von Arbeitsplätzen

Neben zentralen Serverräumen bilden reguläre Arbeitsplätze in Büros, Leitständen und Fertigungshallen ein Hauptziel für Angriffe vor Ort. Angreifer nutzen dort Unachtsamkeiten aus, um im Vorbeigehen vertrauliche Informationen abzulesen (Shoulder Surfing) oder offene Sessions zu übernehmen.

Zur Sicherung von Arbeitsplätzen haben sich zwei grundlegende Richtlinien etabliert:

- Clear Screen Policy (Bildschirmsperre): Wird ein Arbeitsplatz verlassen – auch nur für wenige Minuten –, muss der Bildschirm umgehend gesperrt werden (z.B. via Tastenkombination Win + L oder automatische Inaktivitäts-Sperre nach 2–3 Minuten). Bildschirme in öffentlich oder von Besuchern einsehbaren Bereichen sollten zudem mit Blickschutzfolien (Privacy Filters) ausgestattet werden.
- Clean Desk Policy (Aufgeräumter Arbeitsplatz): Nach Arbeitsende oder beim Verlassen des Büros dürfen keine vertraulichen Dokumente, Notizbücher, Speichermedien (USB-Sticks, externe Festplatten) oder Schlüssel offen auf dem Tisch liegen. Alle physischen Unterlagen sind in verschließbaren Schränken oder Rollcontainern zu verwahren. Notizzettel mit Passwörtern am Monitor stellen einen eklatanten Verstoß gegen die Informationssicherheit dar.

Zusätzlich müssen Arbeitsstationen in Fertigungsbereichen physisch geschützt werden (z.B. durch verschließbare Terminal-Gehäuse), um unbefugtes Umstecken von Kabeln oder das Anbringen harter Keylogger an USB-Ports zu verhindern.

---

### Material M|2.7.2: Besucher im Unternehmen

Besucher, Dienstleister, Handwerker und externe Reinigungskräfte halten sich täglich in Unternehmensgebäuden auf. Ohne klare Prozesse zur Besuchersteuerung entsteht ein erhebliches Sicherheitsrisiko durch unbefugtes Eindringen (Tailgating / Huckepackmitnahme) oder Spionage.

Ein strukturierter Besucherprozess stützt sich auf folgende Regeln:

- Anmeldung & Identifikation: Jeder Besucher muss sich am Empfang ausweisen, wird im Besucherbuch (oder einem elektronischen Besuchermanagementsystem) mit Name, Firma, Ansprechpartner sowie Ankunfts- und Abreisezeit registriert und erhält einen gut sichtbaren Besucherausweis.
- Begleitpflicht (Escort Policy): Fremde Personen dürfen sich in geschützten Unternehmensbereichen (insbesondere in Produktionshallen, Büros und Technikräumen) niemals unbeaufsichtigt bewegen. Sie sind während des gesamten Aufenthalts von einem internen Mitarbeiter zu begleiten.
- Zonenbeschränkung: Besucherausweise gewähren keinen Zutritt zu sensitiven Bereichen wie Serverräumen, Entwicklungsabteilungen oder Leitständen.
- Sensibilisierung des Personals: Mitarbeiter müssen angewiesen werden, unbekannte Personen ohne sichtbaren Mitarbeiter- oder Besucherausweis freundlich, aber bestimmt anzusprechen und zum Empfang zu begleiten.

---

### Arbeitsauftrag A|2.8: Awareness-Schulungen und Betriebsvereinbarungen nutzen

Wenige Tage nach dem Schließen der technischen Lücken in Werkhalle 2 erhält ein Schichtleiter am Leitstand einen Anruf: Der Anrufer gibt sich als externer IT-Techniker aus und behauptet, er müsse im Auftrag von Frau Weber dringend ein Sicherheits-Update einspielen. Dazu benötigt er sofort das neu vergebene Passwort des Schichtleiters. Der Schichtleiter wird unsicher, gibt das Passwort aber schließlich heraus, um den Produktionsablauf nicht zu behindern.

Als Frau Weber davon erfährt, wird ihr klar: "Wir können noch so viele Passkey-Systeme, Firewalls und USB-Sperren installieren – wenn unsere Belegschaft auf einfache Social-Engineering-Tricks hereinfällt, stehen die Türen für Angreifer weiterhin offen. Wir müssen die menschliche Komponente absichern und gleichzeitig klare rechtliche Rahmenbedingungen schaffen!"

#### Aufgabe 1

Informieren Sie sich in den Materialien M|2.8.0: Betriebsvereinbarungen und Guidelines sowie M|2.8.1: Awareness-Schulungen über Best Practice in Unternehmen.

#### Aufgabe 2

Benennen Sie die Methode, mit der der Anrufer an das Passwort des Schichtleiters gelangt ist, und erklären Sie das zugrundeliegende Prinzip dieser Angriffstechnik.

#### Aufgabe 3

Erläutern Sie die Begriffe Guideline (IT-Sicherheitsrichtlinie) und Betriebsvereinbarung. Warum sind beide Instrumente für eine rechtssichere und nachhaltige Umsetzung von IT-Sicherheit erforderlich?

#### Aufgabe 4

Formulieren Sie für die RECPLAST GmbH drei konkrete Verhaltensregeln für eine Guideline zur Passwort- und Identitätssicherheit, die künftig Verunsicherungen wie im obigen Szenario verhindern.

#### Aufgabe 5

Entwerfen Sie für Frau Weber ein kurzes Konzept für eine Awareness-Schulung zur Stärkung der Human Firewall bei RECPLAST. Berücksichtigen Sie dabei folgende Fragen:

- Zielgruppen: Warum sollten Schichtleiter in der Produktion anders geschult werden als Mitarbeiter in der Verwaltung?
- Methoden: Welche Schulungsmethoden (z.B. Simulationen, E-Learnings, Kurz-Checklisten) empfehlen Sie für den Schichtbetrieb, um die Arbeitsprozesse nicht zu überlasten?
- Fehlerkultur: Wie sollte die Schichtleitung reagieren, wenn einem Mitarbeiter dennoch ein Fehler unterläuft (z.B. Anklicken eines verdächtigen Links)?

---

### Material M|2.8.0: Betriebsvereinbarungen und Guidelines

Die technisch ausgereiftesten Schutzmaßnahmen bleiben wirkungslos, wenn im Unternehmen keine verbindlichen Spielregeln für deren Nutzung existieren. Organisatorische Richtlinien schaffen den rechtlichen und verhaltensbezogenen Rahmen für die Informationssicherheit und machen Sicherheit im Arbeitsalltag verbindlich.

- **IT-Sicherheitsrichtlinien (Guidelines):** Guidelines definieren konkrete Verhaltensregeln für die Beschäftigten. Dazu gehören Richtlinien zur Passworterstellung, Vorgaben zur Nutzung von Wechselmedien (z.B. USB-Sticks), Regeln für mobiles Arbeiten sowie Clean-Desk- und Clear-Screen-Policies. Sie vermitteln den Mitarbeitenden klar, was erlaubt ist und wie im Vorfallsfall (z.B. bei Verlust eines Dienst-Smartphones) zu reagieren ist.
- **Betriebsvereinbarungen:** Sobald technische Sicherheitsmaßnahmen eingeführt werden, die das Verhalten oder die Leistung der Arbeitnehmer überwachen können (z.B. Protokollierung von Logfiles, Auswertung von Zeiterfassungssystemen, Zugriffsüberwachung an Leitständen oder Einsatz von Data-Loss-Prevention-Software), berührt dies die Mitbestimmungsrechte des Betriebsrates (z.B. nach [§ 87 BetrVG](https://www.gesetze-im-internet.de/betrvg/__87.html) in Deutschland). In einer Betriebsvereinbarung regeln Unternehmensleitung und Betriebsrat gemeinsam den Zweck, den Umfang und die Grenzen solcher Systeme. Sie stellt sicher, dass Sicherheitsmaßnahmen datenschutzkonform eingesetzt werden, ohne die Belegschaft unter unzulässige Totalüberwachung zu stellen.

---

### Material M|2.8.1: Awareness-Schulungen

Der Mensch gilt in der IT-Sicherheit häufig als das schwächste Glied – gleichzeitig ist eine gut geschulte Belegschaft die stärkste Verteidigungslinie (Human Firewall). Technische Schutzsysteme wie Spam-Filter oder Firewalls bieten keinen hundertprozentigen Schutz. Kriminelle nutzen daher gezielt das menschliche Verhalten aus, um technische Sperren zu umgehen (Social Engineering).

Typische Angriffsmethoden des Social Engineering sind:

- Phishing: Täuschung per E-Mail oder Chat, um Zugangsdaten abzugreifen oder Schadsoftware zu verbreiten.
- Shoulder Surfing & Tailgating: Unbefugtes Mitlesen auf Bildschirmen oder unbemerktes Nachfolgen durch gesicherte Türen.
- Pretexting & CEO-Fraud: Das Vorspiegeln einer falschen Identität (z.B. als IT-Support oder Geschäftsführung), um vertrauliche Informationen zu erschleichen oder Überweisungen auszulösen.

Awareness-Schulungen zielen darauf ab, das Sicherheitsbewusstsein der Mitarbeiter nachhaltig zu schärfen. Effektive Schulungskonzepte setzen nicht auf einmalige, trockene Theorievorträge, sondern auf kontinuierliche und praxisnahe Formate:

- Regelmäßige, interaktive E-Learning-Module mit Alltagsszenarien.
- Simulationen von Phishing-Mails im laufenden Betrieb mit direktem Feedback.
- Erstellung von prägnanten, leicht verständlichen Verhaltensregeln (z.B. "Spickzettel" an Arbeitsplätzen oder Notfall-Ansprechpartner).

Das Ziel einer gelebten Sicherheitskultur ist es, Fehler nicht zu bestrafen, sondern Mitarbeiter zu ermutigen, verdächtige Beobachtungen oder eigene Missgeschicke unverzüglich der IT-Sicherheit zu melden.

---

## Kompetenz 2.2: Integrität sicherstellen

Die größten Lücken bei der Vertraulichkeit (u.a. das gemeinsame Gruppenkonto und die ungesicherten Zugänge) sind inzwischen analysiert und die ersten Maßnahmen angestoßen. Nun richtet sich der Blick auf das nächste Kernschutzziel der Informationssicherheit: Integrität.

Frau Weber holt noch einmal die Protokolle der Qualitätskontrolle hervor und legt sie auf den Tisch:

"Dass Daten nicht nur eingesehen, sondern unbemerkt manipuliert werden können, zeigt der Vorfall an Extruder 2 überdeutlich. Eine eigenmächtige Rezepturänderung von 4,5 % auf 14,5 % beim Additiv REC-Poly-3 – ohne Freigabe im Labor-ERP – hat mal eben 8 Tonnen Granulat vernichtet. Dazu kommt der fremde USB-Stick mit dem unklaren Update und das geteilte Gruppenkonto, bei dem niemand nachvollziehen kann, wer welche Eingabe getätigt hat. Integrität bedeutet für uns: Unversehrtheit, Verlässlichkeit und Verbindlichkeit von Daten und Systemen. Wir müssen jetzt klären: Wie stellen wir sicher, dass Daten und Konfigurationen manipulationssicher bleiben und Änderungen lückenlos nachvollziehbar sind?"

 <figure style="max-width: 100%; margin: 1em 0; text-align: center;"> 
 	 <img src="bilder/02_integritaet.png" alt="Integrität sicherstellen" style="width: 100%; height: auto; border-radius: 6px;"> 
 	 <figcaption style="font-size: 0.85em; color: #555555; margin-top: 6px; font-style: italic;"> 
 	 	 Abb.: Integrität sicherstellen <span style="font-style: normal; opacity: 0.8;">(🤖 KI-generiert)</span> 
 	 </figcaption> 
 </figure> 
 
---

### Arbeitsauftrag A|2.9: Die Bedeutung des Schutzziels Integrität

Nach dem Vorfall an Extruder 2 bei der RECPLAST GmbH (eigenmächtige Rezepturänderung von 4,5 % auf 14,5 % beim Additiv REC-Poly-3, unbemerkt vernichtete 8 Tonnen Granulat sowie unklare Datenherkunft durch geteilte Gruppenkonten) stehen Sie vor der Aufgabe, das grundlegende Schutzziel der Integrität systematisch zu durchdringen.

#### Aufgabe 1

Informieren Sie sich über das Schutzziel der Integrität in M|2.9.0: Deep Dive - Schutzziel Integrität und beschreiben Sie dieses mit eigenen Worten. Unterscheiden Sie dabei direkt die drei Kernaspekte (Unversehrtheit, Verlässlichkeit, Verbindlichkeit).

#### Aufgabe 2

An welchen Stellen wurde das Schutzziel der Integrität bei der RECPLAST GmbH verletzt?

#### Aufgabe 3

Welche schwerwiegenden Konsequenzen drohen der RECPLAST GmbH, wenn die Integrität von Maschinenparametern, Software und Protokollen nicht gewährleistet ist? Ordnen Sie Ihre Ergebnisse in folgende Kategorien ein:

- Wirtschaftliche Folgen
- Sicherheits- und Qualitätsrisiken
- Rechtliche und organisatorische Folgen

---

### Material M|2.9.0: Deep Dive - Schutzziel Integrität

Neben der Vertraulichkeit bildet die Integrität eine der wesentlichen Säulen der Informationssicherheit. Während es bei der Vertraulichkeit darum geht, wer Zugriff auf Informationen hat, dreht sich bei der Integrität alles darum, ob die Informationen überhaupt noch stimmen.

#### Was bedeutet Integrität in der IT?

Im Kern beschreibt Integrität die Unversehrtheit und Verlässlichkeit von Daten, Programmen und Systemkonfigurationen sowie die Verbindlichkeit von Änderungen. Ein System gilt dann als integritätsgewahrt, wenn sichergestellt ist, dass:

- Unversehrtheit: Daten werden nicht unbemerkt verändert. Weder während der Speicherung noch während der Übertragung dürfen Inhalte manipuliert, ergänzt oder gelöscht worden sein.
- Verlässlichkeit: Programme und Steuerungen arbeiten korrekt. Software, Firmware oder maschinelle Steuerbefehle müssen exakt das tun, was von ihnen erwartet wird, ohne unerwünschte oder fremdgesteuerte Programmcodes auszuführen.
- Verbindlichkeit: Handlungen sind nachvollziehbar. Es muss jederzeit fälschungssicher feststellbar sein, wer eine Änderung vorgenommen hat.

Die Verbindlichkeit wird auch als Zurechenbarkeit oder Nicht-Abstreitbarkeit bezeichnet: Eine Handlung lässt sich eindeutig einer Person zuordnen, und diese kann sie nicht glaubhaft bestreiten. Eng damit verwandt ist die Authentizität, also die Echtheit des Urhebers (siehe M|2.11.1: Code Signing).

#### Integrität in der Praxis: Warum Manipulationen weitreichende Folgen haben

Besonders in vernetzten Industrie- und Verwaltungsumgebungen kann der Verlust der Integrität gravierende Kettenreaktionen auslösen. Wenn beispielsweise Steuerungsdaten von Produktionsanlagen oder Rezepturen in einer Fabrik unbemerkt verändert werden, führt das oft nicht nur zu Datenfehlern, sondern direkt zu physikalischem Ausschuss, beschädigten Maschinen oder gefährlichen Betriebszuständen.

Ebenso stellt sich die Frage der Integrität bei Software-Updates oder Konfigurationsänderungen. Gelangen ungeprüfte Dateien über externe Datenträger oder unsichere Netzwerke in ein System, ist die Vertrauenswürdigkeit des gesamten Systems gefährdet. Geteilte Benutzerkonten verstärken dieses Problem zusätzlich, da sie jegliche individuelle Zurechenbarkeit von Eingaben verhindern – es lässt sich im Nachhinein schlicht nicht mehr klären, ob ein Fehler menschliches Versehen, ein technischer Defekt oder eine bewusste Manipulation war.

#### Herausforderungen für die Praxis

Unternehmen stehen vor der ständigen Aufgabe, technische und organisatorische Barrieren zu errichten, die unbemerkte Eingriffe unmöglich machen. Dazu gehört, genau zu überwachen, wer Daten verändern darf, wie Änderungen protokolliert werden und ob eingespielte Updates tatsächlich aus einer vertrauenswürdigen Quelle stammen. Gelingt dies nicht, verliert das Unternehmen die Kontrolle über die Richtigkeit seiner eigenen Geschäftsprozesse.

---

### Arbeitsauftrag A|2.10: Zurechenbarkeit und Logging nutzen

Bei der RECPLAST GmbH hat sich gezeigt, dass Änderungen an den Rezepturen (wie bei Extruder 2) unbemerkt und ohne Dokumentation erfolgen konnten. Zudem arbeitet das Bedienpersonal an den Terminals mit einem gemeinsamen Gruppenkonto `betrieb_halle2`. Um künftig Manipulationen und Fehler lückenlos aufdecken zu können, sind personalisierte Zugänge und ein lückenloses Logging & Auditing unumgänglich.

Informieren Sie sich im M|2.10.0: Zurechenbarkeit und Logging.

#### Aufgabe 1

Welche Voraussetzungen müssen geschaffen werden, damit jede Eingabe am Leitstand eindeutig einer konkreten Person zugeordnet werden kann (Prinzip der Nicht-Abstreitbarkeit)?

#### Aufgabe 2

Was versteht man unter einem Audit-Trail (Revisionsprotokoll) in industriellen Steuerungs- und ERP-Systemen?

#### Aufgabe 3

Warum ist es wichtig, dass Logdaten manipulationssicher (z.B. durch Auslagerung auf einen zentralen, schreibgeschützten Syslog-Server) gespeichert werden?

---

### Material M|2.10.0: Zurechenbarkeit und Logging

Wenn Daten oder Systemkonfigurationen verändert werden, reicht es für die Sicherheit nicht aus, dies einfach nur zu erlauben oder zu verbieten. Um die Integrität dauerhaft zu wahren, muss ein Unternehmen nachvollziehen können, wer wann welche Änderung vorgenommen hat. Dafür braucht es zwei Bausteine: personalisierte Benutzerkonten, die jede Handlung einer Person zuordnen, und eine lückenlose Protokollierung (Logging).

#### Das Problem der Anonymität: Warum Gruppenkonten die Integrität gefährden

In vielen Arbeitsumgebungen – insbesondere in der Produktion oder an Maschinenleitständen – werden aus Bequemlichkeit oft gemeinsame Benutzerkonten (Gruppenkonten) verwendet. Das führt jedoch zu einem massiven Sicherheitsproblem: Wenn sich mehrere Personen denselben Benutzernamen und dasselbe Passwort teilen, ist jede Handlung völlig anonym.

Tritt ein Fehler auf oder werden Parameter unbefugt verändert, lässt sich im Nachhinein nicht mehr feststellen, wer am Terminal saß. Das Prinzip der Verbindlichkeit (Nicht-Abstreitbarkeit) wird dadurch komplett ausgehebelt. Für eine funktionierende Integrität sind daher personalisierte Zugänge und eine eindeutige Authentifizierung zwingend erforderlich.

#### Lückenlose Protokollierung (Logging und Audit-Trails)

Damit Änderungen nicht im Verborgenen bleiben, zeichnen moderne Systeme alle sicherheitsrelevanten Ereignisse in sogenannten Logdateien oder Audit-Trails auf. Ein guter Audit-Trail funktioniert wie ein digitales Fahrtenbuch und dokumentiert typischerweise:

- Den genauen Zeitstempel (Datum und Uhrzeit).
- Die eindeutige Benutzer-ID der handelnden Person.
- Die Art der Aktion (z.B. Erstellen, Ändern oder Löschen eines Datensatzes).
- Den genauen Vorher- und Nachher-Wert (z.B. welche Rezepturparameter konkret verändert wurden).

Damit diese Protokolle ihren Zweck erfüllen, müssen sie manipulationssicher gespeichert werden – etwa auf einem separaten, gegen nachträgliche Änderungen geschützten Server. Werden Logs auf demselben System gespeichert, das ein Angreifer oder Täter kompromittiert, besteht die Gefahr, dass die Spuren im Nachhinein einfach gelöscht oder umgeschrieben werden.

Durch das Zusammenspiel aus personengebundenen Konten und lückenlosem Logging lässt sich jede Änderung eindeutig einer Person zuordnen und nachträglich überprüfen.

#### Ausblick: Geregelte Änderungsprozesse

Technische Protokolle zeigen, was geschehen ist. Sie verhindern aber nicht, dass Änderungen spontan und ohne Freigabe erfolgen. Dafür braucht ein Unternehmen zusätzlich einen festgelegten organisatorischen Ablauf, das Change Management. Wie dieser aufgebaut ist, erarbeiten Sie in A|2.12.

---

### Arbeitsauftrag A|2.11: Integritätsprüfung und Kryptografie einsetzen

In industriellen Umgebungen ist blindes Vertrauen in mitgebrachte Datenträger ein enormes Sicherheitsrisiko. Um zu verhindern, dass manipulierte Software oder schadhafter Code in Steuerungssysteme gelangt, müssen IT-Systeme kryptografische Prüfmechanismen wie Hashes und Code Signing einsetzen.

#### Aufgabe 1

Der Vorfall: Ein Schichtleiter meinte, der USB-Stick mit dem Update liege schon ein paar Tage herum und der Servicetechniker habe ihn "kurz eingesteckt". Erklären Sie aus Sicht der Informationssicherheit, warum dieses Vorgehen brandgefährlich für die Integrität der Anlage ist.

#### Aufgabe 2

Welche technischen Schutzmechanismen müssten an den Leitstands-PCs aktiv sein, um das unautorisierte Einstecken von USB-Medien oder das Ausführen fremder Dateien technisch zu unterbinden? Nutzen Sie dazu M|2.5.0: Endgeräte und ihre Schnittstellen absichern.

#### Aufgabe 3

Was versteht man unter einer kryptografischen Hash-Funktion (z.B. SHA-256) und welche zentralen Eigenschaften besitzt sie (Einwegfunktion, Kollisionsresistenz)? Informieren Sie sich im M|2.11.0: Prüfsummen (Hashes).

#### Aufgabe 4

Angenommen, im Update auf dem USB-Stick wurde auch nur ein einziges Byte im Programmcode manipuliert. Was passiert mit dem berechneten Hash-Wert der Datei?

#### Aufgabe 5

Wie kann der Hersteller einer Software oder Firmware (oder die interne IT von RECPLAST) Hash-Werte nutzen, um sicherzustellen, dass eine heruntergeladene oder angelieferte Datei während des Transports nicht verändert wurde?

#### Aufgabe 6

Ein Hash-Wert allein beweist nur, dass eine Datei unverändert ist – er sagt jedoch nichts darüber aus, wer sie erstellt hat (Authentizität). Hier kommt Code Signing ins Spiel. Informieren Sie sich im M|2.11.1: Code Signing.

##### Aufgabenteil a

Erklären Sie das Prinzip des Code Signings mithilfe asymmetrischer Kryptografie.

##### Aufgabenteil b

Wie hätte das Einspielen des Updates von Extruder 4 verhindert werden müssen, wenn ein strenges Code-Signing-Konzept im Unternehmen aktiv gewesen wäre? (Was würde das Leitstand-System tun, wenn es auf den USB-Stick zugreift?)

---

### Material M|2.11.0: Prüfsummen (Hashes)

Wenn Software-Updates, Firmware-Dateien oder wichtige Dokumente übertragen werden, stellt sich immer dieselbe Frage: Wurden die Daten auf dem Weg manipuliert oder beschädigt? Um die Integrität von Dateien zu garantieren, nutzt die IT mathematische Werkzeuge – die sogenannten Hash-Funktionen.

#### Was ist ein Hash (eine kryptografische Prüfsumme)?

Eine Hash-Funktion ist ein mathematischer Algorithmus, der eine Datei beliebiger Größe (egal ob ein einzelnes Textdokument oder ein riesiges Anlagen-Update) einliest und daraus eine feste Zeichenkette von bestimmter Länge berechnet – den Hash-Wert (oft auch Prüfsumme genannt).

Dieser Hash-Wert funktioniert wie ein digitaler Fingerabdruck der Datei. Er besitzt vier entscheidende Eigenschaften:

- Determinismus: Dieselbe Datei ergibt immer denselben Hash-Wert.
- Der Lawineneffekt: Verändert man in der Ausgangsdatei auch nur ein einziges Zeichen, einen einzigen Buchstaben oder ein einziges Byte, sieht der daraus berechnete Hash-Wert komplett anders aus.
- Einwegfunktion: Aus dem Hash-Wert lässt sich niemals die ursprüngliche Datei rekonstruieren.
- Kollisionsresistenz: Es ist praktisch unmöglich, zwei verschiedene Dateien zu finden, die denselben Hash-Wert ergeben.

#### Beispiel aus dem Alltag: Der Datei-Download

Stellen Sie sich vor, Sie laden ein großes Service-Pack für Ihre Industriesteuerung aus dem Internet herunter. Der Hersteller gibt auf seiner Website den offiziellen SHA-256-Hash-Wert an (hier vereinfacht am Beispiel des Textes RECPLAST-Update):
`5f1bb53406911fa714973f0d4228888f2b2a933fc0224754ad10a162a9561e97`

Bevor Sie das Update installieren, berechnet Ihr Computer den Hash-Wert der heruntergeladenen Datei. Stimmt die Zeichenkette Ihres Computers exakt mit der des Herstellers überein, ist die Datei mit an Sicherheit grenzender Wahrscheinlichkeit unbeschädigt und unmanipuliert auf Ihrem Rechner angekommen. Weicht auch nur ein einziges Zeichen ab, bricht das System die Installation ab, weil ein Integritätsbruch vorliegt.

#### Das Problem mit Passwörtern und die Lösung: "Salzen" (Salt)

Hashes werden nicht nur für Dateien, sondern vor allem für die sichere Speicherung von Passwörtern in Datenbanken genutzt. Ein System speichert niemals das echte Passwort im Klartext, sondern nur dessen Hash-Wert. Gibt ein Nutzer sein Passwort ein, wird es gehasht und das System prüft, ob die Hashes übereinstimmen.

Dabei gab es früher ein großes Problem: Hacker nutzten sogenannte Rainbow Tables (große vorgefertigte Tabellen, in denen Millionen von Klartext-Passwörtern und deren Hashes gespeichert sind), um gehackte Passwort-Hashes blitzschnell im Klartext zu erraten.

Um diesen Angriffen einen Strich durch die Rechnung zu machen, fügt man dem Passwort vor dem Hashen einen zufälligen, einzigartigen Zeichenblock hinzu – den Salt.

- Ohne Salt: Das Passwort `geheim123` ergibt immer denselben Hash-Wert. Hat ein Angreifer diesen Hash, kennt er die Lösung für alle Nutzer, die dieses Passwort verwenden.
- Mit Salt: Dem Passwort wird ein zufälliger Wert (z.B. `x7T9!`) vorangestellt: `x7T9!geheim123`. Selbst wenn zwei Nutzer exakt dasselbe Passwort geheim123 wählen, sorgt der individuelle Salt dafür, dass völlig unterschiedliche Hash-Werte in der Datenbank landen.

#### Wie wird der Salt gespeichert?

Der individuelle Salt wird zusammen mit dem Hash-Wert des Passworts im Klartext in der Benutzerdatenbank (oder der Passwort-Tabelle) gespeichert. Das sieht in einer Datenbanktabelle meist so aus:

| Benutzer | Eingetragener Salt (im Klartext) | Gespeicherter Hash-Wert (Password + Salt) |
| :--- | :---: | :---: |
|Max | `x7T9!` | `8f4b2c...` |
|Anna | `m2K1$` | `3a9e7d...` |

Wenn ein Angreifer Zugriff auf die Datenbank erlangt, sieht er den Salt von Max (`x7T9!`) und den Salt von Anna (`m2K1$`) im vollkommen unverschlüsselten Klartext.

Das ist aber kein Sicherheitsfehler, sondern vom System so einkalkuliert. Um zu verstehen, warum der Salt trotzdem extrem wirksam schützt, muss man sich ansehen, wie ein Angreifer Passwörter knackt:

- Der Angriff ohne Salt (mit Rainbow Tables): Ein Hacker klaut die Datenbank. Da er keine Passwörter im Klartext hat, muss er raten. Er nimmt eine riesige vorberechnete Tabelle (Rainbow Table) mit Milliarden von gängigen Passwörtern und deren fertigen Hashes. Er muss in dieser Tabelle nur nach dem geklauten Hash-Wert suchen. Das dauert Bruchteile von Sekunden – selbst für Millionen von Usern gleichzeitig, weil man die Tabelle universell für diesen Hash-Algorithmus nutzen kann.
- Der Angriff mit individuellen Salts: Wenn jede Zeile in der Datenbank einen anderen zufälligen Salt hat, nützt dem Hacker seine universelle Rainbow Table überhaupt nichts mehr. Selbst wenn er den Salt (x7T9!) in der Datenbank abliest, kann er die fertige Tabelle nicht mehr verwenden. Er müsste für jeden einzelnen Benutzer in der Datenbank die Rainbow Table komplett neu berechnen (unter Einbeziehung des jeweiligen Salts) oder für jeden Versuch das Passwort mühsam einzeln per Brute-Force durchprobieren.

---

### Material M|2.11.1: Code Signing

Ein kryptografischer Hash (wie wir ihn von Prüfsummen kennen) ist wie ein digitaler Fingerabdruck. Er beweist zwar, dass eine Datei unversehrt ist – aber er hat einen entscheidenden Haken: Er beweist nicht, wer die Datei geschrieben hat.

Stellen Sie sich vor, ein Angreifer manipuliert eine Software, berechnet für seine veränderte (schädliche) Version einen neuen Hash-Wert und veröffentlicht diesen im Internet. Wenn Sie nun das Update herunterladen und den Hash-Wert prüfen, stimmt er überein – weil Sie ja den Hash der manipulierten Datei mit der manipulierten Datei vergleichen. Ihnen fehlt die Gewissheit, ob die Datei wirklich vom legitimen Hersteller stammt.

#### Das Prinzip des Code Signings (asymmetrische Kryptografie)

Hier schließt Code Signing die Lücke. Es verbindet Integrität mit Authentizität (Echtheitsnachweis) und Nicht-Abstreitbarkeit, indem es auf asymmetrische Verschlüsselung setzt. Dabei nutzt der Software-Hersteller ein echtes Schlüsselpaar:

- Der Private Key (Geheimer Schlüssel): Dieser Schlüssel liegt streng geschützt beim Software-Hersteller (oder in einem Hardware Security Module wie ein USB-Krypto-Stick oder ein TPM-Chip). Nur mit diesem Schlüssel kann der Hersteller eine digitale Signatur für den Programmcode erzeugen.
- Der Public Key (Öffentlicher Schlüssel): Dieser Schlüssel ist weltweit frei verfügbar und oft fest in Betriebssystemen, Browsern oder Maschinensteuerungen einprogrammiert.

#### Der Ablauf in der Praxis:

- Beim Hersteller (Signieren): Der Hersteller nimmt die fertige Software-Datei, erstellt davon einen Hash-Wert und verschlüsselt diesen Hash-Wert mit seinem Private Key. Das Ergebnis ist die digitale Signatur, die fest an die Software angehängt wird.
- Beim Endgerät / in der Anlage (Verifizieren): Bevor das Gerät das Update installiert, prüft es die Signatur mithilfe des Public Key. Das System entschlüsselt die Signatur und vergleicht den herausgerechneten Hash mit dem tatsächlichen Hash der Datei.

#### Was passiert, wenn etwas nicht stimmt?

Das System führt beim Code Signing zwei automatische Kontrollen durch:

- Stimmt die Identität? Wenn die Signatur nicht mit dem hinterlegten Public Key des echten Herstellers übereinstimmt, war der Urheber ein Fremder. Das System schlägt Alarm.
- Wurde etwas verändert (Integrität)? Selbst wenn die Signatur vom echten Hersteller stammt, aber ein Angreifer auch nur ein einziges Byte im Programmcode verändert hat, passt der Hash-Wert nicht mehr zur Signatur.

---

### Arbeitsauftrag A|2.12: Change-Management-Prozesse umsetzen

Bei der RECPLAST GmbH haben unkoordinierte Eingriffe gravierende Spuren hinterlassen: Die eigenmächtige Rezepturänderung an Extruder 2 und der blind eingesteckte USB-Stick mit dem Update für Extruder 4 zeigen, dass Änderungen bislang "ad hoc", unkontrolliert und ohne Freigabe durchgeführt wurden. In modernen Produktions- und IT-Umgebungen (Operational Technology / IT) führt dieser Wildwuchs unweigerlich zu Sicherheitslücken, Ausschuss und Produktionsstillständen. Um die Integrität dauerhaft zu sichern, muss ein professionelles Änderungsmanagement (Change Management) etabliert werden.

Informieren Sie sich im M|2.12.0: Change Management.

#### Aufgabe 1

Welchen Konflikt gibt es im Alltag zwischen der Flexibilität der Produktion ("Der Techniker muss schnell handeln können") und der Sicherheit durch Change Management?

#### Aufgabe 2

Entwerfen Sie für die RECPLAST GmbH einen strukturierten Prozess (Lifecycle) für zukünftige Änderungen an Rezepturen und Steuerungssoftware. Beschreiben Sie die folgenden Schritte:

1. Change Request (Antrag): Wer stellt den Antrag und welche Informationen müssen zwingend enthalten sein?
2. Review & Freigabe (Prüfung): Wer muss den Antrag prüfen und freigeben?
3. Test & Vorbereitung: Warum sollte eine Änderung vor dem echten Betrieb in einer Testumgebung (Staging) validiert werden?
4. Implementierung & Dokumentation: Wie wird die Änderung durchgeführt und wo wird sie revisionssicher protokolliert?

#### Aufgabe 3

Wie kann ein beschleunigter Prozess für Notfall-Änderungen (Emergency Changes) aussehen, der einerseits schnell reagiert, aber andererseits Missbrauch verhindert?

#### Aufgabe 4

Welche Rolle spielen nachträgliche Audits (Review nach dem Notfalleinsatz)?

---

### Material M|2.12.0: Change Management

Technische Schutzmaßnahmen wie Passwörter, Hashes oder USB-Sperren sind wirkungslos, wenn die Menschen, die mit den Systemen arbeiten, Änderungen unkontrolliert, spontan oder im Alleingang durchführen. Ohne einen festen organisatorischen Rahmen entsteht ein enormes Sicherheitsrisiko.

Hier greift das Change Management (Änderungsmanagement) als disziplinierter Prozess zur Steuerung aller Anpassungen in IT- und Produktionsumgebungen.

#### Was ist Change Management und warum wird es benötigt?

Unter Change Management versteht man im Bereich der IT-Sicherheit einen standardisierten, dokumentierten Ablauf für die Planung, Prüfung, Freigabe, Durchführung und Nachbereitung von Änderungen (Changes).

Das Ziel ist es, den Konflikt zwischen zwei Gegensätzen zu lösen:

- Produktionsdruck: Techniker und Schichtleiter wollen schnell auf Probleme reagieren, Maschinen anpassen oder Updates einspielen, um Stillstände zu vermeiden.
- Sicherheit und Integrität: Jede unüberlegte Änderung birgt das Risiko von Fehlern, Datenverlust, Sabotage oder Produktionsausschuss.

Ein professioneller Change-Prozess sorgt dafür, dass Änderungen nicht verhindert, sondern kontrolliert und sicher gemacht werden.

#### Der klassische Change-Management-Lifecycle

Damit eine Änderung (z.B. eine neue Rezeptur im Labor-ERP oder ein Firmware-Update für eine SPS) fehlerfrei und nachvollziehbar umgesetzt wird, durchläuft sie in der Regel vier Phasen:

1. Der Change Request (Antragstellung): Niemand ändert einfach so etwas. Jede Anpassung beginnt mit einem formalen Antrag. Darin wird präzise beschrieben: Was soll geändert werden, warum ist das notwendig, welche Systeme sind betroffen und welches Risiko besteht bei einem Fehlschlag?
2. Review und Freigabe (Prüfung): Der Antrag wird von zuständigen Stellen (z.B. Laborleitung, IT-Sicherheit/CISO oder dem Change Advisory Board) geprüft. Hier gilt häufig das Vier-Augen-Prinzip: Eine zweite Person kontrolliert den Plan, bevor er genehmigt wird. Damit wird verhindert, dass Fehler oder Manipulationen unentdeckt bleiben.
3. Test und Validierung: Bevor eine neue Software oder eine veränderte Rezeptur auf die echten Produktionsanlagen losgelassen wird, erfolgt ein Test in einer isolierten Testumgebung (Staging), um unerwartete Nebenwirkungen auszuschließen.
4. Implementierung und Dokumentation: Nach erfolgreicher Freigabe und Testphase wird die Änderung zum geplanten Zeitpunkt durchgeführt und lückenlos im System protokolliert (Audit-Trail).

#### Der Notfall-Change (Emergency Change)

In einer Fabrik wie bei der RECPLAST GmbH kann es vorkommen, dass ein akuter Fehler auftritt, der sofort behoben werden muss, um einen teuren Stillstand (wie den drohenden Ausfallschaden von 12.000 € pro Stunde) abzuwenden. Für solche Situationen gibt es den Emergency Change:

- Der normale, langwierige Freigabeprozess wird temporär verkürzt, indem beispielsweise telefonisch oder über eine Notfall-Schleife der Betriebskontrolleur und der CISO parallel informiert werden.
- Die goldene Regel: Auch ein Notfall entbindet niemals von der Dokumentation. Sobald die Krise abgewendet ist, muss die Notfall-Änderung innerhalb kurzer Zeit formal nachgeprüft und im System lückenlos dokumentiert werden (Post-Implementation Review).

---

## Kompetenz 2.3: Verfügbarkeit sicherstellen

Bleibt noch der Ausfall von Extruder 4 vom Montag. Frau Weber steht mit Ihnen vor dem Hallenverteiler, in dem der defekte Switch inzwischen ersetzt wurde, und blickt ernst auf die Anlage:

"Der Ausfall am Montag hat uns 12.000 Euro pro Stunde gekostet – und das nur, weil ein einfaches Netzteil am Hallenverteiler ausgefallen ist und weder ein redundantes Netzteil noch eine USV eingeplant war. Verfügbarkeit heißt für uns, dass IT-Systeme, Netzwerke und Maschinen dann einsatzbereit sein müssen, wenn sie gebraucht werden. Ein einzelner ausgefallener Netzstecker darf nicht gleich die gesamte Produktion lahmlegen. Lassen Sie uns erarbeiten: Mit welchen technischen und organisatorischen Maßnahmen sichern wir unsere Anlagen gegen Ausfälle ab?"

 <figure style="max-width: 100%; margin: 1em 0; text-align: center;"> 
 	 <img src="bilder/02_verfuegbarkeit.png" alt="Verfügbarkeit sicherstellen" style="width: 100%; height: auto; border-radius: 6px;"> 
 	 <figcaption style="font-size: 0.85em; color: #555555; margin-top: 6px; font-style: italic;"> 
 	 	 Abb.: Verfügbarkeit sicherstellen <span style="font-style: normal; opacity: 0.8;">(🤖 KI-generiert)</span> 
 	 </figcaption> 
 </figure> 

---

### Arbeitsauftrag A|2.13: Die Bedeutung des Schutzziels Verfügbarkeit

Am Montagmorgen stand Extruder 4 still. Bevor Sie Maßnahmen planen, klären Sie, was Verfügbarkeit bedeutet und warum es zum Ausfall kam.

#### Aufgabe 1

Lesen Sie M|2.13.0: Deep Dive – Schutzziel Verfügbarkeit. Erklären Sie in zwei bis drei Sätzen mit eigenen Worten, was Verfügbarkeit bedeutet.

#### Aufgabe 2

Analysieren Sie den Ausfall von Extruder 4.

##### Aufgabenteil a

Was war die technische Ursache des Stillstands?

##### Aufgabenteil b

Warum konnte dieses eine Bauteil die ganze Anlage lahmlegen?

#### Aufgabe 3

Welche Folgen hat der Ausfall für die RECPLAST GmbH? Nennen Sie je eine Folge aus den drei Bereichen:

- Wirtschaftliche Folgen
- Sicherheits- und Qualitätsrisiken
- Rechtliche und organisatorische Folgen

---

### Material M|2.13.0: Deep Dive – Schutzziel Verfügbarkeit

Im Alltag bedeutet "verfügbar" oft nur, dass etwas irgendwie vorhanden ist oder meistens funktioniert. In der IT-Sicherheit ist Verfügbarkeit dagegen ein messbares Schutzziel: Gemeint ist, dass IT-Systeme, Netzwerke, Maschinen und Daten genau dann nutzbar sind, wenn berechtigte Personen oder Prozesse sie benötigen – im vereinbarten Umfang und in der vereinbarten Zeit. Anders als die Vertraulichkeit (Schutz vor unbefugtem Lesen) und die Integrität (Schutz vor unbemerkter Veränderung) geht es hier also darum, dass ein Dienst überhaupt läuft. Bei der RECPLAST GmbH betrifft das zum Beispiel den Leitstand-PC (IT-System), das Produktionsnetz (Netzwerk) und die Extruder (Maschine).

Ein einzelner Baustein genügt dafür nicht. Zuerst muss die Anforderung definiert und messbar gemacht werden, damit Sie wissen, wie viel Ausfall tolerierbar ist. Redundanz verhindert, dass ein einzelnes defektes Bauteil alles lahmlegt, und eine geplante Wiederherstellung begrenzt den Schaden, wenn es doch zum Ausfall kommt. Fehlt einer dieser Bausteine, entsteht eine Lücke: Ohne Anforderung weiß niemand, wie viel Redundanz nötig ist, ohne Redundanz hängt alles an einem Bauteil, und ohne Wiederherstellung dauert der Stillstand unnötig lange.

#### Verfügbarkeit als Anforderung

Verfügbarkeit beschreibt den Anteil der Zeit, in dem ein System seine Funktion wie vereinbart erfüllt. Sie wird meist in Prozent der Betriebszeit angegeben und lässt sich aus der mittleren Zeit zwischen zwei Ausfällen (MTBF) und der mittleren Reparaturzeit (MTTR) berechnen. Schon kleine Prozentunterschiede haben große Wirkung: 99 % bedeuten rund 3,65 Tage Ausfall pro Jahr, 99,9 % noch etwa 8,8 Stunden und 99,99 % nur noch rund 53 Minuten. Welche Stufe sinnvoll ist, richtet sich nach dem Schaden, den ein Ausfall verursacht.

- **Kennzahl:** Verfügbarkeit = MTBF / (MTBF + MTTR) × 100 %
- **Schutzbedarf:** Kritische Systeme (z.B. Leitstand) erhalten höhere Anforderungen als Büro-PCs.
- **SLA:** Zusagen werden vertraglich fixiert, etwa mit Reaktions- und Wiederherstellungszeiten.
- **Wartungsfenster:** Geplante Ausfälle werden abgestimmt und möglichst außerhalb der Produktion gelegt.

> **Beispiel aus der IT-Praxis:** Ein Admin überwacht mit Zabbix den OPC-UA-Server, der die Maschinendaten sammelt. Das Monitoring misst Antwortzeiten und Ausfälle, wertet sie monatlich aus und vergleicht sie mit dem zugesagten SLA-Wert von 99,9 %. Wird der Wert unterschritten, wird die Ursache analysiert und die Architektur angepasst.

#### Redundanz und Ausfallsicherheit

Redundanz bedeutet, kritische Komponenten mehrfach vorzuhalten, sodass beim Ausfall eines Teils ein anderes automatisch übernimmt. Ziel ist es, sogenannte Single Points of Failure zu beseitigen, also einzelne Bauteile, deren Ausfall das gesamte System lahmlegt. Dies betrifft nicht nur Server, sondern ebenso Stromversorgung, Netzwerkgeräte, Leitungen und Speicher. Redundanz kostet zusätzliches Geld und Pflege, sie muss daher passend zum Schutzbedarf geplant und regelmäßig getestet werden.

- **Strom:** Online-USV (Doppelwandler) und Netzteile mit zwei Einspeisungen.
- **Netzwerk:** Doppelte Switches und Uplinks mit Link Aggregation oder Spanning Tree.
- **Systeme:** Cluster mit automatischem Failover und RAID für Datenträger.
- **Wartung:** Ersatzteile vorhalten und Failover regelmäßig testen.

> **Beispiel aus der IT-Praxis:** Zwei Core-Switches sind per Stacking gekoppelt, jeder Access-Switch hängt über je einen Uplink an beiden Geräten. Die Gateway-Redundanz übernimmt VRRP, die Server laufen auf einem VMware-HA-Cluster mit zwei Hosts. Fällt ein Switch oder Host aus, läuft der Betrieb ohne manuellen Eingriff weiter.

#### Wiederherstellung und Notfallvorsorge

Keine Redundanz schützt vor jedem Ausfall, deshalb muss geplant sein, wie Systeme nach einer Störung schnell wieder in Betrieb gehen. Dazu legen Organisationen fest, wie lange ein Ausfall höchstens dauern darf (RTO) und wie viel Datenverlust tolerierbar ist (RPO). Diese Zielwerte bestimmen Backup-Intervalle, Verfahren und Zuständigkeiten. Entscheidend ist, dass die Wiederherstellung dokumentiert ist und regelmäßig geübt wird, denn ein ungetestetes Backup ist im Ernstfall keine verlässliche Sicherung.

- **Backup:** 3-2-1-Regel mit drei Kopien auf zwei Medien, davon eine extern oder offline.
- **Restore-Test:** Wiederherstellung regelmäßig prüfen und Dauer messen.
- **Notfallplan:** Kontakte, Reihenfolge und Zuständigkeiten schriftlich festhalten.
- **Handlungsfähigkeit:** Notbetrieb oder manuelle Rückfallebene definieren.

> **Beispiel aus der IT-Praxis:** Veeam Backup & Replication sichert die virtuellen Maschinen alle 15 Minuten (RPO) auf ein NAS und täglich auf ein externes Ziel. Quartalsweise wird eine VM testweise wiederhergestellt und die Dauer gemessen. So ist belegt, dass die Vorgabe von vier Stunden (RTO) eingehalten werden kann.

#### Praxisbeispiel: Ein Core-Switch fällt aus

Am Montagmorgen fällt in einem Produktionsnetz der primäre Core-Switch aus. Der Ablauf zeigt, wie die drei Bausteine nacheinander zusammenwirken:

```
+------------------------------------------------------+
| Schritt 1 - Erkennen                                 |
| Monitoring meldet den Ausfall binnen Sekunden an die |
| IT-Bereitschaft, der Alarm wird protokolliert.       |
+------------------------------------------------------+
                          |
                          v
+------------------------------------------------------+
| Schritt 2 - Überbrücken                              |
| Der zweite Switch übernimmt per Failover, die        |
| Maschinen bleiben im Netz, die Produktion läuft.     |
+------------------------------------------------------+
                          |
                          v
+------------------------------------------------------+
| Schritt 3 - Wiederherstellen                         |
| Ersatzgerät einbauen, gesicherte Konfiguration       |
| einspielen, Redundanz wiederherstellen.              |
+------------------------------------------------------+
```

---

### Arbeitsauftrag A|2.14: Verfügbarkeit berechnen und Ausfallkosten bewerten

Frau Weber möchte der Geschäftsleitung zeigen, was ein Ausfall kostet. Dafür brauchen Sie Zahlen. Lesen Sie zuerst M|2.14.0: Verfügbarkeitsklassen und Kennzahlen.

#### Aufgabe 1

Erklären Sie mit eigenen Worten, was die Begriffe Verfügbarkeit (in Prozent), MTBF und MTTR bedeuten. Nennen Sie anschließend die zwei Stellschrauben, mit denen man die Verfügbarkeit eines Systems erhöhen kann.

#### Aufgabe 2

Extruder 4 läuft rund um die Uhr (8.760 Stunden pro Jahr). Der Schaden bei Stillstand beträgt 12.000 € pro Stunde.

##### Aufgabenteil a

Berechnen Sie die maximale Ausfallzeit pro Jahr und die maximalen Ausfallkosten. Übertragen Sie die Tabelle und füllen Sie sie aus.

Formel: Ausfallzeit = 8.760 h × (1 − Verfügbarkeit)

| Verfügbarkeit | Ausfallzeit pro Jahr | Ausfallkosten pro Jahr |
| :--- | :--- | :--- |
| 99 % | | |
| 99,9 % | | |
| 99,99 % | | |

##### Aufgabenteil b

Welche der drei Verfügbarkeiten halten Sie für eine vollautomatische Extrusionsanlage für angemessen? Begründen Sie in zwei bis drei Sätzen.

#### Aufgabe 3

Für den ausgefallenen Hallenverteiler-Switch gelten diese Werte:

- MTBF: 40.000 Stunden
- MTTR im Ist-Zustand: 5 Stunden (Fehlersuche, Ersatzteil beschaffen, Einbau)
- MTTR mit Ersatzgerät vor Ort: 0,5 Stunden

Formeln:

- Ausfälle pro Jahr = 8.760 h ÷ MTBF
- Ausfallzeit pro Jahr = Ausfälle pro Jahr × MTTR

##### Aufgabenteil a

Berechnen Sie für beide Fälle die Ausfallzeit pro Jahr und die Ausfallkosten pro Jahr.

##### Aufgabenteil b

Was zeigt der Vergleich über die Wirkung einer kürzeren Reparaturzeit?

#### Aufgabe 4

Ein Ersatzgerät mit redundantem Netzteil und USV für den Hallenverteiler kostet einmalig 2.500 €.

##### Aufgabenteil a

Nach wie vielen Minuten Stillstand hat sich die Investition bezahlt gemacht?

##### Aufgabenteil b

Formulieren Sie in zwei bis drei Sätzen eine Empfehlung an die Geschäftsleitung. Nennen Sie dabei einen Grund, der über die reinen Ausfallkosten hinausgeht (z.B. Vertragsstrafen oder Image).

---

### Material M|2.14.0: Verfügbarkeitsklassen und Kennzahlen

Im Alltag heißt "Das System läuft meistens" oft schlicht, dass es selten auffällt. Als Fachbegriff ist Verfügbarkeit dagegen eine Zahl: Sie gibt an, welchen Anteil der vereinbarten Betriebszeit ein System tatsächlich funktionsfähig war. Erst mit dieser Zahl können Sie Systeme vergleichen, Anforderungen festlegen und Zusagen wie ein Service Level Agreement (SLA) überprüfen. Wer nur "sehr hoch" oder "möglichst immer" fordert, kann weder planen noch kontrollieren.

Dafür greifen drei Bausteine ineinander. Die Verfügbarkeit in Prozent und die zugehörigen Klassen legen das Ziel fest. Die Kennzahlen MTBF und MTTR erklären, wie dieser Wert zustande kommt und woran Sie drehen können, um ihn zu verbessern. Die Wirtschaftlichkeitsbetrachtung schließlich beantwortet, ob sich der Aufwand für eine höhere Verfügbarkeit lohnt. Nur zusammen liefern sie eine belastbare Entscheidungsgrundlage für die Geschäftsleitung.

#### Verfügbarkeit und Verfügbarkeitsklassen

Die Verfügbarkeit gibt in Prozent an, wie groß der Anteil der Betriebszeit ist, in dem ein System seine Funktion erfüllt. Aus ihr folgt die höchstens zulässige Ausfallzeit: Sie ergibt sich aus dem Anteil (1 − Verfügbarkeit), multipliziert mit der Betriebszeit. Üblich ist die Einteilung in "Neunerklassen" (99 %, 99,9 %, 99,99 % usw.), bei denen jede zusätzliche Neun die zulässige Ausfallzeit auf ein Zehntel senkt. Entscheidend ist dabei der Bezugszeitraum: Ein Dauerbetrieb rund um die Uhr hat andere Folgen als ein Betrieb nur zu Bürozeiten.

- **Berechnung:** Ausfallzeit = (1 − Verfügbarkeit) × Betriebszeit.
- **Neunerklassen:** Jede weitere Neun bedeutet ein Zehntel der Ausfallzeit, aber meist deutlich höhere Kosten.
- **Bezugszeitraum:** Betriebszeit (24/7 oder Betriebszeiten) und Messzeitraum (Monat, Jahr) müssen festgelegt sein.
- **Geplante Wartung:** Wird sie nicht als Ausfall gewertet, muss das ausdrücklich vereinbart sein.

> **Beispiel aus der IT-Praxis:** Ein Cloud-Anbieter sichert für einen virtuellen Server im SLA 99,9 % pro Monat zu. Bei 30 Tagen (720 Stunden) sind das rund 43 Minuten zulässige Ausfallzeit. Der Admin vergleicht diesen Wert mit seinem Monitoring und kann bei einer Überschreitung eine Gutschrift laut SLA geltend machen.

#### MTBF und MTTR

Die MTBF (Mean Time Between Failures) ist die mittlere Betriebsdauer zwischen zwei Ausfällen und sagt aus, wie zuverlässig ein System ist. Die MTTR (Mean Time To Repair) ist die mittlere Zeit vom Eintritt einer Störung bis zur Wiederherstellung des Betriebs. Sie umfasst nicht nur den Austausch, sondern auch Fehlersuche, Beschaffung des Ersatzteils und Konfiguration. Die Verfügbarkeit steigt, wenn die MTBF wächst oder die MTTR sinkt – das sind die beiden Stellschrauben.

- **MTBF erhöhen:** Hochwertige Komponenten, Redundanz, Wartung und Klimatisierung.
- **MTTR senken:** Ersatzgeräte vor Ort, dokumentierte Konfigurationen und feste Bereitschaft.
- **Früh erkennen:** Monitoring verkürzt die Zeit bis zur Störungserkennung.
- **Messen:** Beide Werte stammen aus Herstellerangaben oder aus der eigenen Störungsstatistik.

> **Beispiel aus der IT-Praxis:** In einem Ticketsystem wie GLPI erfasst der Support für jede Störung Meldezeit und Zeitpunkt der Wiederherstellung. Der Mittelwert aus diesen Zeiträumen ergibt die MTTR, die Zeitabstände zwischen den Störungen laut Zabbix-Verlauf liefern die MTBF. Beide Werte werden quartalsweise ausgewertet und im Team besprochen.

#### Wirtschaftlichkeit

Höhere Verfügbarkeit kostet Geld, deshalb braucht eine Investition eine nachvollziehbare Begründung. Dazu werden die erwarteten Ausfallkosten, also erwartete Ausfallstunden mal Schaden pro Stunde, den Kosten der Maßnahme gegenübergestellt. Der Break-even-Punkt zeigt, nach welcher Stillstandsdauer sich die Investition bezahlt gemacht hat. Neben diesen direkten Kosten gehören auch Folgeschäden und weiche Faktoren in die Betrachtung, weil sie den Nutzen einer Maßnahme oft erheblich erhöhen.

- **Ausfallkosten:** Erwartete Ausfallstunden × Schaden pro Stunde.
- **Break-even:** Investition ÷ Schaden pro Stunde = Stillstandsdauer, ab der sich die Maßnahme lohnt.
- **Weitere Kosten:** Folgeschäden, Vertragsstrafen und Imageverlust.
- **Gegenseite:** Anschaffung, Betrieb, Wartung und Tests der Maßnahme.

> **Beispiel aus der IT-Praxis:** Ein Admin plant für die Firewall ein zweites Gerät als HA-Paar (z.B. mit pfSense oder FortiGate). Er stellt die Mehrkosten für Gerät und Lizenz den erwarteten Ausfallkosten bei einem Gateway-Defekt gegenüber und legt das Ergebnis mit Break-even der Geschäftsleitung zur Entscheidung vor.

#### Die beiden Grundformeln

- Verfügbarkeit = MTBF / (MTBF + MTTR) × 100 %
- Ausfallzeit = (1 − Verfügbarkeit) × Betriebszeit

#### Praxisbeispiel: Lohnt sich ein Ersatzgerät für den Hypervisor-Host?

Ein Hypervisor-Host der Verwaltung hat eine MTBF von 20.000 Stunden und im Ist-Zustand eine MTTR von 4 Stunden. Ein Ausfall verursacht einen Schaden von 2.000 € pro Stunde. Mit einem Ersatzgerät und dokumentierter Konfiguration sinkt die MTTR auf 1 Stunde, die Investition beträgt 1.200 €. Der Rechenweg läuft in drei Schritten ab:

```
+--------------------------------------------------------+
| Schritt 1 - Verfügbarkeit berechnen                    |
| Ist:           20.000 / (20.000 + 4) = 99,980 %        |
| Mit Ersatzgerät: 20.000 / (20.000 + 1) = 99,995 %      |
+--------------------------------------------------------+
                           |
                           v
+--------------------------------------------------------+
| Schritt 2 - Ausfallzeit und Kosten                     |
| Erwartete Ausfälle pro Jahr: 8.760 / 20.000 = 0,438    |
| Ist:             0,438 x 4 h = 1,752 h  ->  3.504 EUR  |
| Mit Ersatzgerät: 0,438 x 1 h = 0,438 h  ->    876 EUR  |
+--------------------------------------------------------+
                           |
                           v
+--------------------------------------------------------+
| Schritt 3 - Break-even bewerten                        |
| Ersparnis: 2.628 EUR pro Jahr                          |
| Break-even: 1.200 EUR / 2.000 EUR pro h = 0,6 h        |
|             = 36 Minuten Stillstand                    |
+--------------------------------------------------------+
```

---

### Arbeitsauftrag A|2.15: Single Points of Failure erkennen und Redundanzen planen

Ein einzelnes, günstiges Bauteil hat die Anlage lahmgelegt. Frau Weber möchte wissen, an welchen weiteren Stellen die Produktion an einem einzigen Bauteil hängt. Lesen Sie zuerst M|2.15.0: Redundanzkonzepte.

#### Aufgabe 1

Erklären Sie mit eigenen Worten, was ein Single Point of Failure (SPOF) ist und was Redundanz bedeutet. Nennen Sie ein Beispiel für Redundanz.

#### Aufgabe 2

Die Anbindung von Extruder 4 sieht vereinfacht so aus:

Steuerungs-PC (Leitstand) → Haupt-Switch im Hallenverteiler → SPS-Steuerung → Extruder 4

Jedes Gerät hat ein Netzteil, jede Verbindung ein Netzwerkkabel. Das Labor-ERP läuft auf einem einzigen Server.

##### Aufgabenteil a

Zeichnen Sie diese Anbindung als Skizze und markieren Sie alle Single Points of Failure.

##### Aufgabenteil b

Legen Sie für jeden SPOF eine Maßnahme fest (z.B. zweites Netzteil, zweiter Switch, zweites Kabel, zweiter Server). Welche Maßnahme würden Sie zuerst umsetzen? Begründen Sie in einem Satz.

#### Aufgabe 3

Erklären Sie, was man unter Failover versteht und warum man es regelmäßig testen sollte.

---

### Material M|2.15.0: Redundanzkonzepte

Im Alltag genügt oft der Satz "Wir haben ja Ersatz", um sich sicher zu fühlen. Als Fachbegriff ist Redundanz strenger: Kritische Komponenten sind so mehrfach und unabhängig voneinander vorhanden, dass der Ausfall eines Teils den Betrieb nicht unterbricht. Das Gegenstück ist der Single Point of Failure (SPOF), eine einzelne Komponente, deren Ausfall das gesamte System oder einen ganzen Prozess lahmlegt. Dabei ist es unerheblich, ob das Bauteil teuer oder billig ist.

Drei Fragen müssen gemeinsam beantwortet werden. Erstens: Wo liegen die SPOFs, und mit welcher Art von Redundanz lassen sie sich beseitigen? Zweitens: Wie schnell und wie zuverlässig übernimmt das Ersatzsystem, was durch die Standby-Stufe und das Failover bestimmt wird? Drittens: Was schützt die Daten, wenn Hardware ausfällt oder Dateien verloren gehen? Erst die Antworten auf alle drei Fragen ergeben ein Redundanzkonzept, das im Ernstfall trägt.

#### Single Point of Failure und Redundanz

Ein SPOF entsteht überall dort, wo ein Teil der Kette nur einmal vorhanden ist: ein Netzteil, ein Switch, ein Kabel, ein Server, aber auch ein Standort oder eine einzelne Person mit Spezialwissen. Je länger die Kette, desto schlechter wird die Gesamtverfügbarkeit, weil sich die Verfügbarkeiten der Glieder multiplizieren. Redundanz begegnet dem durch parallele, voneinander unabhängige Ersatzkomponenten. Man unterscheidet vor allem Hardware-, Netzwerk- und Standortredundanz, wobei die Ersatzkomponente nicht denselben Defekt oder dieselbe Ursache teilen darf wie das Original.

- **Hardware:** Doppelte Netzteile, gespiegelte Datenträger oder zusätzliche Server im Cluster.
- **Netzwerk:** Zweite Switches, doppelte Verkabelung und mehrere Uplinks auf getrennten Wegen.
- **Standort:** Zweites Rechenzentrum, Cloud-Region oder ausgelagerte Systeme außerhalb des Gebäudes.
- **Unabhängigkeit:** Gemeinsame Stromleiste oder gemeinsamer Verteiler machen Redundanz wirkungslos.

> **Beispiel aus der IT-Praxis:** Ein mittelständisches Unternehmen hat nur einen Internetanschluss. Fällt die Leitung aus, sind VPN-Zugänge, SIP-Telefonie und Cloud-Dienste gleichzeitig weg. Die Lösung ist eine zweite Leitung eines anderen Anbieters, die ein Router mit Failover automatisch nutzt.

#### Standby-Stufen und Failover

Redundanz ist nicht gleich Redundanz: Wie schnell ein Ersatzsystem einspringt, hängt von seiner Bereitschaftsstufe ab. Beim Cold Standby liegt das Ersatzgerät ausgeschaltet bereit und muss im Ernstfall erst eingebaut, gestartet und konfiguriert werden. Beim Warm Standby läuft es bereits, ist aber nicht auf dem aktuellen Stand und braucht noch einige Schritte. Beim Hot Standby läuft es parallel mit aktuellen Daten und übernimmt automatisch. Mit steigender Stufe sinkt die Umschaltzeit, die Kosten für Beschaffung, Betrieb und Pflege steigen.

- **Cold Standby:** Günstig, aber lange Umschaltzeit, da manuell bereitgestellt.
- **Warm Standby:** Mittlere Kosten, Umschaltung nach kurzer Vorbereitung.
- **Hot Standby:** Höchste Kosten, Umschaltung in Sekunden und meist automatisch.
- **Failover:** Der Übergang vom ausgefallenen auf das Ersatzsystem; er muss regelmäßig getestet werden.

> **Beispiel aus der IT-Praxis:** Zwei Linux-Server teilen sich per Keepalived eine virtuelle IP-Adresse. Fällt der aktive Knoten aus, übernimmt der Standby-Knoten die Adresse binnen weniger Sekunden. Der Admin zieht quartalsweise testweise den Stecker des aktiven Knotens, um zu prüfen, ob der Failover wirklich funktioniert.

#### Datenträger-Redundanz und Backup

Festplatten und SSDs gehören zu den Bauteilen, die am häufigsten ausfallen. Mit RAID werden mehrere Datenträger zu einem Verbund zusammengefasst, sodass beim Defekt eines Datenträgers der Betrieb ohne Datenverlust weiterläuft. Das ist eine Redundanzmaßnahme, die die Verfügbarkeit erhöht. Ein RAID speichert jedoch alles, was geschrieben wird, also auch Fehler, versehentliche Löschungen oder Schadsoftware, und es liegt am selben Ort im selben Gerät. Ein Backup ist deshalb eine eigene Maßnahme, die nicht durch RAID ersetzt wird.

- **RAID schützt vor:** Dem Ausfall einzelner Datenträger.
- **RAID schützt nicht vor:** Löschen, Ransomware, Fehlbedienung, Controller-Defekt, Brand oder Diebstahl.
- **Backup:** Getrennte Kopien in der Vergangenheit, idealerweise nach der 3-2-1-Regel.
- **Restore-Test:** Erst die getestete Wiederherstellung macht ein Backup verlässlich.

> **Beispiel aus der IT-Praxis:** Ein NAS mit gespiegelten Platten stellt eine Netzwerkfreigabe bereit. Ein Client wird mit Ransomware infiziert und verschlüsselt die Freigabe, und die Spiegelplatte enthält sofort dieselben verschlüsselten Dateien. Gerettet werden die Daten nur durch das getrennte Backup, das z.B. mit Veeam auf ein externes Ziel läuft.

#### Die beiden Grundformeln

- Reihenschaltung (jedes Glied nötig): A = A1 × A2 × A3 ...
- Parallelschaltung (redundant): A = 1 − (1 − A1) × (1 − A2)

#### Praxisbeispiel: Ein Kundenportal absichern

Ein Kundenportal besteht aus einer Kette: Internetleitung → Firewall → Webserver → Datenbankserver. Jedes Glied existiert nur einmal. Die Schwachstellenanalyse läuft in drei Schritten ab:

```
+--------------------------------------------------------+
| Schritt 1 - SPOFs erkennen                             |
| Pfad vollständig aufzeichnen, jede einfach vorhandene  |
| Komponente und Verbindung markieren (hier: alle vier   |
| Glieder).                                              |
+--------------------------------------------------------+
                           |
                           v
+--------------------------------------------------------+
| Schritt 2 - Maßnahmen zuordnen                         |
| Zweite Leitung eines anderen Anbieters, Firewall als   |
| HA-Paar, zwei Webserver hinter Load Balancer,          |
| Datenbank-Replikation auf Hot-Standby-Server.          |
+--------------------------------------------------------+
                           |
                           v
+--------------------------------------------------------+
| Schritt 3 - Priorisieren und testen                    |
| Hoher Schaden bei geringem Aufwand zuerst: Webserver,  |
| Datenbank, Firewall, zuletzt zweite Leitung.           |
| Jede Maßnahme per Failover-Test prüfen.                |
+--------------------------------------------------------+
```

--- 

### Arbeitsauftrag A|2.16: Stromversorgung absichern (USV)

Der Stillstand begann bei der Stromversorgung des Switches. Ein defektes Netzteil lässt sich durch Redundanz abfangen, ein Ausfall der Netzspannung nur durch eine USV. Frau Weber möchte, dass kritische Geräte bei Stromausfall weiterlaufen oder zumindest geordnet heruntergefahren werden. Lesen Sie zuerst M|2.16.0: USV-Systeme.

#### Aufgabe 1

Erklären Sie mit eigenen Worten, wozu eine unterbrechungsfreie Stromversorgung (USV) dient.

##### Aufgabenteil a

Nennen Sie drei Netzprobleme, vor denen eine USV schützen kann.

##### Aufgabenteil b

Warum ist eine USV nur eine Überbrückung für Minuten und keine dauerhafte Stromquelle?

#### Aufgabe 2

Im Hallenverteiler sollen drei Geräte abgesichert werden:

- Haupt-Switch: 150 W
- SPS-Steuerung: 250 W
- Leitstand-PC mit Monitor: 300 W

##### Aufgabenteil a

Berechnen Sie die Gesamtleistung der Geräte.

##### Aufgabenteil b

Berechnen Sie die Energiemenge in Wattstunden (Wh), die die USV für 30 Minuten liefern muss.

#### Aufgabe 3

Warum ist ein geordnetes Herunterfahren bei Stromausfall besonders für das Labor-ERP und die SPS-Steuerung wichtig? Berücksichtigen Sie das Schutzziel Integrität.

#### Aufgabe 4

Eine USV, die nie geprüft wurde, ist nur scheinbar eine Absicherung. Nennen Sie zwei Prüfmaßnahmen, die regelmäßig durchgeführt werden sollten (z.B. Batterietest).

---

### Material M|2.16.0: USV-Systeme

Im Alltag kennt man die USV als "Batterie unter dem PC", die bei einem Stromausfall kurz weiterpiept. Als Fachbegriff beschreibt die unterbrechungsfreie Stromversorgung ein Gerät, das Verbraucher bei Störungen im Stromnetz ohne oder mit minimaler Unterbrechung weiter versorgt und sie zugleich vor schädlichen Netzeinflüssen schützt. Sie ist kein Ersatz für ein Kraftwerk, sondern ein Puffer, der Zeit verschafft: Zeit, um sauber herunterzufahren, oder Zeit, bis ein Notstromaggregat übernimmt.

Damit dieser Puffer im Ernstfall trägt, müssen drei Dinge zusammenpassen. Die Bauform bestimmt, wie gut und wie schnell die USV schützt. Die richtige Dimensionierung stellt sicher, dass Leistung und Überbrückungszeit zu den angeschlossenen Geräten passen. Das Betriebskonzept aus Notstrom, geordnetem Shutdown und regelmäßiger Wartung sorgt dafür, dass die gewonnene Zeit auch sinnvoll genutzt wird. Fehlt eines davon, wiegt sich das Unternehmen in einer Scheinsicherheit.

#### USV und Bauformen

Eine USV besteht im Kern aus einer Batterie, einem Gleichrichter bzw. Ladegerät und einem Wechselrichter, der bei Bedarf aus der Batterie wieder Wechselspannung erzeugt. Sie schützt nicht nur vor Stromausfall, sondern je nach Bauform auch vor Unter- und Überspannung, Spannungsspitzen und Frequenzabweichungen. Die Norm IEC 62003 unterscheidet drei Bauformen, die sich in Schutzwirkung, Umschaltzeit und Preis deutlich unterscheiden. Die Batterie ist aus Kosten-, Platz- und Wärmegründen auf wenige Minuten ausgelegt, eine USV bleibt deshalb eine Überbrückungslösung.

- **Offline (VFD):** Die Last hängt direkt am Netz, erst bei Ausfall wird mit kurzer Umschaltzeit auf Batterie gewechselt. Günstig, mit geringem Schutz.
- **Line-Interactive (VI):** Zusätzlich gleicht eine Spannungsregelung (AVR) Schwankungen aus, ohne die Batterie zu nutzen.
- **Online (VFI):** Die Last wird dauerhaft über den Wechselrichter versorgt, es gibt keine Umschaltzeit und die Netzstörungen werden vollständig entkoppelt.
- **Netzprobleme:** Stromausfall, Unter- und Überspannung, Spannungsspitzen, Frequenzschwankungen.

> **Beispiel aus der IT-Praxis:** In einem Serverraum fällt die Netzspannung wegen einer Umschaltung beim Energieversorger für einen Moment aus. Die Online-USV (z.B. von APC oder Eaton) speist die Server unterbrechungsfrei weiter. Der Admin bemerkt den Vorfall nur durch eine SNMP-Meldung im Monitoring.

#### Dimensionierung und Überbrückungszeit

Bei der Auswahl einer USV zählen zwei Größen: die Leistung, die sie gleichzeitig liefern kann, und die Energie, die in der Batterie für die gewünschte Überbrückungszeit gespeichert ist. Die Leistung ergibt sich aus der Summe der tatsächlich aufgenommenen Leistung aller Verbraucher, die Energie aus Leistung mal Zeit. Weil USV-Geräte ihre Leistung in Voltampere (VA) angeben, muss zusätzlich der Leistungsfaktor berücksichtigt werden, der Wirk- und Scheinleistung verbindet. Eine Reserve von etwa einem Viertel, Platz für Erweiterungen und die Alterung der Batterie verhindern, dass die USV schon am ersten Tag an ihrer Grenze arbeitet.

- **Gesamtleistung:** Summe der tatsächlichen Leistungsaufnahme, nicht der Nennleistung auf dem Typenschild.
- **Energiebedarf:** Wh = W × Stunden, Minuten müssen dafür in Stunden umgerechnet werden.
- **Reserve und Leistungsfaktor:** Ca. 25 % Aufschlag und Umrechnung von Watt in VA.
- **Verluste und Alterung:** Wirkungsgrad des Wechselrichters und alternde Batterien verkürzen die reale Laufzeit.

> **Beispiel aus der IT-Praxis:** Ein Admin liest über die Verwaltungsschnittstelle (BMC, z.B. iDRAC) die tatsächliche Leistungsaufnahme eines Servers aus. Das Gerät hat ein 750-W-Netzteil, zieht im Betrieb aber nur etwa 220 W. Mit diesem Messwert und dem Laufzeitdiagramm im Datenblatt wählt er die USV passend aus, statt nach dem Netzteil-Aufdruck zu überdimensionieren.

#### Notstrom, Shutdown und Wartung

Bei längeren Ausfällen übernimmt ein Notstromaggregat (Generator) die Versorgung, die USV überbrückt dabei die Zeit, bis der Generator angelaufen ist und stabile Spannung liefert. Ist kein Generator vorhanden, dient die Batteriezeit dazu, Systeme geordnet herunterzufahren. Dafür meldet die USV ihren Zustand per USB, serieller Schnittstelle oder SNMP-Netzwerkkarte an die Systeme, die daraufhin automatisch den Shutdown einleiten. Ein ungeordnetes Abschalten kann Dateisysteme und Datenbanken beschädigen und gefährdet damit die Integrität der Daten. Weil Batterien altern, ist die USV nur mit regelmäßigen Tests und Wartung eine echte Absicherung.

- **Generator:** Übernimmt die lange Versorgung, die USV überbrückt den Anlauf.
- **Shutdown:** Auslösung über USB, seriell oder SNMP, gesteuert von einer Agent-Software.
- **Integrität:** Geordnetes Beenden schützt Dateisysteme, Datenbanken und Steuerprogramme vor Beschädigung.
- **Wartung:** Batterietest, Lasttest, Austauschintervalle (z.B. Bleiakkus nach etwa 3 bis 5 Jahren) und Monitoring.

> **Beispiel aus der IT-Praxis:** Auf einem Linux-Server ist die USV per USB angeschlossen und wird mit NUT (Network UPS Tools) ausgewertet. Der NUT-Server meldet den Status an weitere Rechner im Netz, die bei einer Restlaufzeit unter fünf Minuten herunterfahren. Zabbix überwacht zusätzlich den Batteriezustand und warnt, bevor eine Batterie getauscht werden muss.

#### Die drei Grundformeln

- Gesamtleistung: P = P1 + P2 + P3 ...
- Energie (Wh) = P (W) × t (h)
- Scheinleistung (VA) = P (W) / Leistungsfaktor

#### Praxisbeispiel: Eine USV für den Serverschrank planen

In einem kleinen Serverschrank hängen ein NAS (80 W), eine Firewall (40 W) und ein Switch (60 W). Bei einem Stromausfall sollen sie 15 Minuten durchhalten und danach geordnet herunterfahren. Die Planung läuft in drei Schritten ab:

```
+--------------------------------------------------------+
| Schritt 1 - Bedarf ermitteln                           |
| Gesamtleistung: 80 W + 40 W + 60 W = 180 W             |
| Energie für 15 Min.: 180 W x 0,25 h = 45 Wh            |
+--------------------------------------------------------+
                           |
                           v
+--------------------------------------------------------+
| Schritt 2 - USV auswählen                              |
| Mit 25 % Reserve: 180 W x 1,25 = 225 W                 |
| Bei Leistungsfaktor 0,9: 225 W / 0,9 = 250 VA          |
| Gerät oberhalb wählen, Laufzeit bei 180 W im           |
| Datenblatt prüfen (mind. 15 Minuten).                  |
+--------------------------------------------------------+
                           |
                           v
+--------------------------------------------------------+
| Schritt 3 - Shutdown einrichten und testen             |
| Anbindung per USB oder SNMP, NAS fährt nach fünf       |
| Minuten Batteriebetrieb herunter. Vor Inbetriebnahme   |
| Netzstecker ziehen und Ablauf prüfen.                  |
+--------------------------------------------------------+
```

---

### Arbeitsauftrag A|2.17: Datensicherung und Wiederherstellung planen

Die Produktion hängt auch an Daten: Rezepturen im Labor-ERP, SPS-Programme und Netzwerkkonfigurationen. Es gibt bisher nur eine einzige Sicherung auf einem NAS in Werkhalle 2, und niemand weiß, ob sie sich zurückspielen lässt. Lesen Sie zuerst M|2.17.0: Backup-Strategien.

#### Aufgabe 1

Warum ersetzt Redundanz (z.B. ein zweiter Server) kein Backup? Nennen Sie zwei Ursachen für Datenverlust, vor denen nur ein Backup schützt. Beziehen Sie sich dabei auch auf die manipulierte Rezeptur von Extruder 2.

#### Aufgabe 2

Es gibt drei Backup-Arten: Voll-, differenzielles und inkrementelles Backup.

##### Aufgabenteil a

Beschreiben Sie jede Art in ein bis zwei Sätzen. Übertragen Sie die Tabelle und bewerten Sie jeweils mit niedrig, mittel oder hoch.

| Backup-Art | Beschreibung | Speicherbedarf | Sicherungsdauer | Wiederherstellungsaufwand |
| :--- | :--- | :--- | :--- | :--- |
| Vollbackup | | | | |
| Differenziell | | | | |
| Inkrementell | | | | |

##### Aufgabenteil b

Am Sonntag wird ein Vollbackup erstellt, von Montag bis Freitag jeweils ein weiteres Backup. Am Donnerstagmorgen fällt der Server aus, bevor die Sicherung dieses Tages läuft. Welche Backups werden für die Wiederherstellung benötigt, wenn (1) differenziell und (2) inkrementell gesichert wurde?

#### Aufgabe 3

Eine bewährte Richtlinie ist die 3-2-1-Regel.

##### Aufgabenteil a

Erläutern Sie, wofür die Ziffern 3, 2 und 1 stehen.

##### Aufgabenteil b

Bewerten Sie das bisherige Backup der RECPLAST GmbH (eine einzige Kopie auf einem NAS in Werkhalle 2) anhand der drei Ziffern.

#### Aufgabe 4

Erstellen Sie für Frau Weber einen einfachen Backup-Plan. Übertragen Sie die Tabelle und ergänzen Sie Rhythmus, Backup-Art und Speicherort. Achten Sie auf die 3-2-1-Regel.

| Daten | Rhythmus | Backup-Art | Speicherort |
| :--- | :--- | :--- | :--- |
| Rezepturen im Labor-ERP | | | |
| SPS-Programme | | | |
| Konfiguration der Netzwerkgeräte | | | |

#### Aufgabe 5

Ein Backup ist nur so gut wie seine Wiederherstellung.

##### Aufgabenteil a

Warum ist ein regelmäßiger Wiederherstellungstest nötig? Nennen Sie zwei Dinge, die dabei geprüft werden sollten.

##### Aufgabenteil b

Bei der Wiederherstellung stellt sich heraus, dass die Rezeptur in den letzten drei Backups bereits manipuliert ist. Was bedeutet das für die Aufbewahrungsdauer Ihrer Backups?

---

### Material M|2.17.0: Backup-Strategien

Im Alltag heißt "Wir haben ja eine Kopie" oft nur, dass die Daten irgendwo ein zweites Mal liegen. Als Fachbegriff ist ein Backup dagegen eine geplante, vom Original getrennte Sicherung früherer Datenstände, aus der sich Daten und Systeme nachweislich wiederherstellen lassen. Der Unterschied ist entscheidend: Eine bloße Kopie, die ständig mitgeschrieben wird, enthält jeden Fehler sofort mit, ein Backup bewahrt dagegen einen Zustand von früher auf.

Für ein tragfähiges Backup-Konzept greifen drei Bausteine ineinander. Zuerst müssen Sie verstehen, warum Redundanz und Backup unterschiedliche Aufgaben haben. Danach legen die Backup-Arten fest, wie viel gesichert wird und wie aufwendig die Wiederherstellung ist. Schließlich sorgen eine bewährte Regel, regelmäßige Tests und Prüfsummen dafür, dass die Sicherung im Ernstfall auch funktioniert und unverändert ist. Ein Backup, das nie zurückgespielt wurde, ist nur eine Hoffnung.

#### Backup und Redundanz

Redundanz sorgt dafür, dass ein System weiterläuft, wenn ein Bauteil ausfällt, und spiegelt dabei immer den aktuellen Zustand. Genau darin liegt ihre Grenze: Wird eine Datei gelöscht, verschlüsselt oder verfälscht, erscheint die Änderung sofort auch auf der Spiegelplatte oder dem Ersatzserver. Ein Backup bewahrt getrennte, ältere Datenstände auf, zu denen Sie zurückkehren können. Es stützt damit die Verfügbarkeit, weil Daten nach einem Verlust wieder nutzbar werden, und die Integrität, weil sich ein unveränderter Stand wiederherstellen lässt.

- **Logische Fehler:** Versehentliches Löschen, Fehlbedienung und Softwarefehler werden von Redundanz mitgespiegelt.
- **Angriffe:** Ransomware und Manipulation durch Innentäter verändern alle Kopien, die ständig synchron sind.
- **Katastrophen:** Brand, Wasserschaden oder Diebstahl treffen Original und Spiegel am selben Ort.
- **Zeitreise:** Nur ein Backup erlaubt die Rückkehr zu einem früheren, unveränderten Stand.

> **Beispiel aus der IT-Praxis:** Ein Entwickler führt in der Produktionsdatenbank versehentlich ein `DELETE` ohne `WHERE`-Klausel aus. Der Hot-Standby-Server übernimmt die Löschung sofort. Nur die Wiederherstellung aus dem Backup mit archivierten Transaktionslogs (Point-in-Time-Recovery) bringt den Stand von kurz vor dem Fehler zurück.

#### Backup-Arten und Wiederherstellungskette

Ein Vollbackup sichert alle ausgewählten Daten vollständig, braucht am meisten Platz und Zeit und ist bei der Wiederherstellung am einfachsten. Ein differenzielles Backup sichert alles, was sich seit dem letzten Vollbackup geändert hat, und wird deshalb von Tag zu Tag größer. Ein inkrementelles Backup sichert nur, was sich seit der letzten Sicherung irgendeiner Art geändert hat, und ist daher klein und schnell. Dafür muss bei der Wiederherstellung die gesamte Kette aus Vollbackup und allen Inkrementen eingespielt werden. Die Wahl ist immer ein Kompromiss aus Speicherbedarf, Sicherungsdauer und Wiederherstellungsdauer.

- **Voll:** Alles in jeder Sicherung, höchster Speicherbedarf, einfachste Wiederherstellung.
- **Differenziell:** Änderungen seit dem letzten Vollbackup, zur Wiederherstellung genügen Voll- und letztes Differenz-Backup.
- **Inkrementell:** Änderungen seit der letzten Sicherung, geringster Speicherbedarf, längste Wiederherstellungskette.
- **Kettenrisiko:** Fehlt ein Glied in der Kette, sind die folgenden Sicherungen unbrauchbar.

> **Beispiel aus der IT-Praxis:** Ein Admin sichert mit Veeam wöchentlich per Vollbackup und täglich inkrementell. Ein beschädigtes Inkrement in der Mitte der Kette macht alle späteren Wiederherstellungspunkte unbrauchbar. Deshalb prüft er die Kette regelmäßig mit einem Wiederherstellungstest und beginnt wöchentlich eine neue Kette.

#### 3-2-1-1-0-Regel und Wiederherstellung

Die 3-2-1-1-0-Regel fasst bewährte Grundsätze zusammen: drei Kopien der Daten, auf zwei verschiedenen Medien, eine davon an einem anderen Ort, eine offline oder unveränderbar (immutable) und null Fehler bei der Überprüfung. Die Offline- bzw. Immutable-Kopie schützt davor, dass Ransomware oder ein Innentäter auch die Sicherungen löscht oder verändert. Die Null steht für verifizierte Backups: Nur ein erfolgreich getesteter Restore beweist, dass die Sicherung brauchbar ist. Prüfsummen (Hashes) zeigen, ob eine Sicherung seit der Erstellung unverändert ist, und eine ausreichend lange Aufbewahrung mit mehreren Versionen erlaubt den Rückgriff auf einen sauberen Stand, wenn eine Manipulation erst spät auffällt.

- **3-2-1:** Drei Kopien, zwei Medien, eine Kopie an einem anderen Standort.
- **Immutable:** Eine Kopie offline oder unveränderbar, damit sie auch bei Angriffen erhalten bleibt.
- **0 Fehler:** Überwachung der Jobs und regelmäßiger Wiederherstellungstest.
- **Hash und Versionen:** Prüfsumme gegen Veränderung, lange Aufbewahrung gegen spät erkannte Manipulation.

> **Beispiel aus der IT-Praxis:** Ein Admin sichert virtuelle Maschinen mit Veeam auf ein NAS (anderes Medium) und repliziert sie in einen S3-kompatiblen Cloud-Speicher mit Object Lock (extern und unveränderbar). Eine automatische Wiederherstellungsprüfung läuft monatlich und meldet Fehler per E-Mail.

#### Simulator-Ersatz: Backup-Arten im Wochenverlauf

Am Montag wird ein Vollbackup mit 100 GB erstellt. Von Dienstag bis Samstag folgt jeden Tag eine weitere Sicherung. Die Daten ändern sich täglich um 5, 8, 4, 6 und 3 GB, wobei einige Dateien an mehreren Tagen geändert werden. Deshalb ist eine differenzielle Sicherung kleiner als die Summe der einzelnen Tagesänderungen. Die beiden Tabellen zeigen, was der Simulator in der interaktiven Ansicht anzeigt. Angenommen werden 1 GB pro Minute beim Sichern und beim Zurückspielen.

**Größe der Sicherung je Tag (in GB):**

| Tag | Voll | Differenziell | Inkrementell |
|-----|-----:|--------------:|-------------:|
| Mo (Vollbackup) | 100 | 100 | 100 |
| Di | 100 | 5 | 5 |
| Mi | 100 | 11 | 8 |
| Do | 100 | 14 | 4 |
| Fr | 100 | 19 | 6 |
| Sa | 100 | 21 | 3 |
| **Summe Mo–Sa** | **600 GB** | **170 GB** | **126 GB** |

**Wiederherstellung, wenn der Server nach der Sicherung des jeweiligen Tages ausfällt:**

| Ausfall nach | Voll (Dateien / GB) | Differenziell (Dateien / GB) | Inkrementell (Dateien / GB) |
|--------------|---------------------|------------------------------|-----------------------------|
| Mo | Mo / 100 | Mo / 100 | Mo / 100 |
| Di | Di / 100 | Mo+Di / 105 | Mo+Di / 105 |
| Mi | Mi / 100 | Mo+Mi / 111 | Mo+Di+Mi / 113 |
| Do | Do / 100 | Mo+Do / 114 | Mo+Di+Mi+Do / 117 |
| Fr | Fr / 100 | Mo+Fr / 119 | Mo bis Fr (5) / 123 |
| Sa | Sa / 100 | Mo+Sa / 121 | Mo bis Sa (6) / 126 |

Daraus ergibt sich: Das Vollbackup braucht immer nur eine Datei, aber am meisten Speicher. Beim differenziellen Backup genügen stets das Vollbackup und die letzte Sicherung, die Dateien werden dafür täglich größer. Beim inkrementellen Backup bleiben die Einzelsicherungen klein, die Wiederherstellungskette wird aber jeden Tag länger, und jedes Glied muss intakt sein.

#### Praxisbeispiel: Backup-Konzept für ein Softwarehaus

Ein kleines Softwarehaus betreibt eine Kundendatenbank, Git-Repositories und einen Büro-Fileserver. Das Backup-Konzept entsteht in drei Schritten:

```
+--------------------------------------------------------+
| Schritt 1 - Daten und Kritikalität                     |
| Kundendatenbank: sehr kritisch, max. 15 Min. Verlust   |
| Git-Repositories: kritisch, 1 Tag tolerierbar          |
| Fileserver: mittel, 1 Tag tolerierbar                  |
+--------------------------------------------------------+
                           |
                           v
+--------------------------------------------------------+
| Schritt 2 - Verfahren festlegen                        |
| Datenbank: nachts Voll + Logs alle 15 Minuten          |
| Git, Fileserver: wöchentlich Voll, täglich inkrementell|
| Kopie 1: NAS. Kopie 2: S3 mit Object Lock, extern.     |
+--------------------------------------------------------+
                           |
                           v
+--------------------------------------------------------+
| Schritt 3 - Überwachen und testen                      |
| Alarm bei Fehlern und zu alten Backups per E-Mail      |
| Monatlicher Restore-Test mit SHA-256-Prüfsumme         |
| Backup-Speicher nur über separates Konto erreichbar    |
+--------------------------------------------------------+
```

---

## Handlungsergebnis

Wenige Tage nach den Vorfällen ruft Frau Weber Sie erneut in den Besprechungsraum. Die Geschäftsleitung hat entschieden, die Technik zu verbessern, aber nicht nur die Technik:

*"Das Passwort am Monitor, der fremde USB-Stick, der ungesicherte Hallenverteiler: Das waren keine Fehler der Technik, sondern Gewohnheiten. Die ändern wir nicht mit einer einmaligen Schulung. Wir hängen deshalb ab dem nächsten Jahr einen IT-Security-Kalender im Leitstand, in der Werkhalle und in den Büros aus. Jeden Monat ein Thema, das jeder in zwei Minuten versteht und sofort umsetzen kann.  Sie haben alle drei Schutzziele durchgearbeitet, also bringen Sie sie bitte in Form."*

 <figure style="max-width: 100%; margin: 1em 0; text-align: center;"> 
 	 <img src="bilder/02_kalender.png" alt="IT-Security-Kalender im Leitstand" style="width: 100%; height: auto; border-radius: 6px;"> 
 	 <figcaption style="font-size: 0.85em; color: #555555; margin-top: 6px; font-style: italic;"> 
 	 	 Abb.: IT-Security-Kalender im Leitstand <span style="font-style: normal; opacity: 0.8;">(🤖 KI-generiert)</span> 
 	 </figcaption> 
 </figure> 

---

### Arbeitsauftrag A|2.18: IT-Security-Kalender für die RECPLAST GmbH erstellen

Sie erstellen in Ihrer Gruppe (drei bis vier Personen) einen IT-Security-Kalender mit zwölf Monatsblättern für die Beschäftigten der RECPLAST GmbH. Nutzen Sie dafür das Material M|2.18.0: Vorlage IT-Security-Kalender und Ihre Ergebnisse aus den Arbeitsaufträgen A|2.0 bis A|2.17.

#### Aufgabe 1

Stellen Sie zwölf Themen zusammen, die einigermaßen gleichmäßig aus den drei Schutzzielen ableitbar sind. Ordnen Sie die Themen den Monaten zu. Achten Sie darauf, dass die drei Schutzziele im Jahresverlauf abwechselnd vorkommen.

#### Aufgabe 2

Erstellen Sie die zwölf Monatsblätter auf der Vorlage aus M|2.18.0: Vorlage IT-Security-Kalender. Jedes Blatt enthält:

- das Thema und die Kennzeichnung des Schutzziels
- eine Kernbotschaft in einem Satz
- zwei konkrete Verhaltensregeln für den Alltag, jeweils in einem Satz
- eine passende Abbildung

Schreiben Sie so, dass auch Personen ohne IT-Vorwissen Ihre Texte verstehen, und formulieren Sie die Verhaltensregeln als konkrete Handlungsanweisungen ("Sperren Sie Ihren Bildschirm, bevor Sie den Platz verlassen"). Kennzeichnen Sie KI-generierte Abbildungen und verwenden Sie keine echten Personen, Firmen oder Passwörter.

#### Aufgabe 3

Kontrollieren Sie Ihre Blätter. Tauschen Sie die Blätter innerhalb der Gruppe, sodass jedes Blatt von einer Person geprüft wird, die es nicht erstellt hat. Prüfen Sie:

- Ist die Aussage fachlich richtig, und passt sie zum gekennzeichneten Schutzziel?
- Sind die Regeln im Alltag der Beschäftigten umsetzbar?
- Versteht auch eine Person ohne IT-Kenntnisse das Blatt in zwei Minuten?
- Sind Rechtschreibung und Abbildungskennzeichnung in Ordnung?

Überarbeiten Sie Ihre Blätter anhand der Rückmeldung und erstellen Sie den fertigen Kalender als PDF-Datei.

#### Aufgabe 4

Bewerten Sie Ihren Kalender.

##### Aufgabenteil a

Wählen Sie das Blatt aus, das Beschäftigte Ihrer Meinung nach am ehesten zu einer anderen Handlung bewegt, und begründen Sie Ihre Wahl in zwei bis drei Sätzen.

##### Aufgabenteil b

Ein Kalender allein verhindert keine Vorfälle. Nennen Sie eine technische Maßnahme aus diesem Kapitel, die den Kalender ergänzen muss, und begründen Sie, warum.

---

{%
   include-markdown "inhalte/lizenzhinweis.md"
   start="<!--include-start-->"
   end="<!--include-end-->"
%}