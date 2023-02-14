# tempml

## Wie ich heize
2011 haben meine Familie und ich mit dem Neubau unseres Hauses (in Österreich) begonnen. Schon bei der Planung war uns ein bewusster Umgang mit Energie wichtig. Als Zentralheizung haben wir uns für eine Pelletheizung entschieden. Alle Räume sind mit Fußbodenheizung ausgestattet.

Uns war es wichtig, die Temperatur der Räume einzeln regeln zu können. Der Vorschlag unseres Installateurs, die Durchflussmenge der Fußbodenheizung so einzustellen, dass die gewünschte Temperatur erreicht beziehungsweise gehalten wird, erschien mir nicht sinvoll. Einzelne Räume, zum Beispiel die Werkstatt im Keller, sollen nur bei Bedarf geheizt werden. In anderen Räumen, etwa dem Wohnzimmer und den Kinderzimmern, soll die Temperatur auch bei Bedarf kurzfristig angepasst werden können.

Ein weiteres Problem bei der Durchlaufmenge ist, dass diese so eingestellt sein muss, dass die Wohlfühltemperatur gehalten wird. Das bedeutet aber im Umkehrschluss, dass das Aufheizen des Raumes länger dauert – noch länger als ohnehin schon über die Fußbodenheizung.

Meine Frau und ich sind berufstätig, die Kinder vormittags in der Schule. Während der Nachtstunden werden die meisten Räume ebenfalls nicht genutzt. Die Zeit, in der wir angenehme 22°C haben wollen, ist also kürzer als die Zeit, in der die Räume nicht genutzt werden. Auf der anderen Seite hat sich aber in Zeiten von Home-Office und Lockdowns gezeigt, wie angenehm es ist, die Heizung im Büro doch auch vormittags mal aufdrehen zu können.

Da ich beim Neubau sowieso eine Hausautomation installiert habe, habe ich natürlich auch eine Einzelraumtemperaturregelung umgesetzt.

## Kann ich dadurch Energie sparen?
Bei der Diskussion über die Sinnhaftigkeit einer Einzelraumtemperaturregelung mit unserem Installateur erklärte mir dieser, dass das Absenken der Raumtemperatur nichts bringen würde. Das Aufheizen des Raums würde mehr Energie benötigen als durch das Absenken gespart wird.

Da die Wärme, die durch Wände und Fenster nach außen abgegeben wird, aber unter anderem vom Temperaturunterschied abhängig ist, habe ich mich intensiver mit dem Thema beschäftigt und versucht, eine ungefähre Berechnung anzustellen, ob beziehungsweise wie viel ich dadurch sparen kann.

Für meine Berechnungen habe ich den Energieausweis von unserem Haus herangezogen, der in Österreich wie in Deutschland für Neubauten verpflichtend ist. Im Energieausweis wird die Gesamtenergieeffizienz eines Gebäudes angegeben. Eine der enthaltenen Kennzahlen ist der Heizwärmebedarf (HWB). 

Der HWB gibt die Wärmeenergie je m² an, die (rein rechnerisch) zur Beheizung der Räume hinzugefügt werden muss. Diese Kennzahl ist von der Bauausführung und den verwendeten Materialien (etwa Ziegel und Dämmung) und Bauteilen (etwa Fenster und Haustüren) abhängig. Wer mehr darüber wissen möchte, findet hier weitere Informationen für Österreich <#LINK TEXT="Inhalt eines Energieausweises (oesterreich.gv.at" URL="https://www.oesterreich.gv.at/themen/bauen_wohnen_und_umwelt/wohnen/1/Seite.210460.html">) und hier <#LINK TEXT="Informationen für Deutschland" URL="https://online-energieausweis.org/energieausweis-pflicht.php">.

Die zur Berechnung des HWB zugrunde liegende physikalische Größe ist der <#LINK TEXT="Transmissionswärmeverlust" URL="https://www.heizung.de/ratgeber/diverses/der-transmissionswaermeverlust-ht-von-gebaeuden.html">. Das ist jene Energie, die über Bauteile abgeführt wird, die an einen Bereich mit niedrigerer Temperatur (also Außenwände, Boden, Dach usw.) grenzen. Er ist abhängig von Faktoren wie den verwendeten Materialien, der Isolierung und natürlich dem Temperaturunterschied. In meinem Energieausweis ist der durchschnittliche Transmissionswärmeverlust mit 0,28 W/m²K angegeben. Das ist auch der Wert, mit dem ich rechne.

Der Einfachheit halber habe ich die Berechnung für diesen Artikel angepasst. Ich gehe von einem rechteckigen, eingeschoßigen Gebäude ohne Keller aus, in dem alle Räume die gleiche Temperatur haben. Für jene, die meine Berechnung nachvollziehen oder selbst ein wenig rechnen wollen, habe ich eine einfache <#LINK TEXT="Excel-Datei in meinem Git-Repository abgelegt" URL="https://github.com/markus-renezeder/tempml">.

Ein wichtiger Faktor ist der Temperaturunterschied zwischen innen und außen. Die <#LINK TEXT="durchschnittliche Außentemperatur liegt in den Monaten Januar bis März bei ca. 0,4°C" URL="https://www.laenderdaten.info/Europa/Oesterreich/Klima.php">. In milden Wintern liegt die durchschnittliche Temperatur über diese drei Monate knapp unter dem Gefrierpunkt. Deshalb rechne ich mit 0°C. Für die Raumtemperatur nehme ich 22°C an. Als Dauer für die Nachtabsenkung nehme ich fünf Stunden an. 

Unter Berücksichtigung der benötigten Energie, um das Gebäude nach dem Absenken wieder aufzuheizen, ergibt meine Berechnung ein Einsparungspotential von ca. 12 kWh Wärmeenergie pro Tag. Das entspricht etwa 2,5 kg Pellets oder ca. 1,36 Euro. Im Excel-File habe ich auch andere Energieträger wie Erdgas und Heizöl berücksichtigt. Die angenommenen Kosten sind gemäß österreichischen Preisen von Mitte Januar 2023.

Da ich mich bei der Berechnung ausschließlich auf den Winter konzentriere, gehe ich von 100 Tagen aus, an denen die angenommene Situation zutrifft. In diesem Zeitraum kann ich also durch das Abschalten der Heizung während der Nachtstunden ca. 250 kg Pellets sparen. Das entspricht etwas mehr als acht Prozent des Jahresverbrauchs oder rund 136,00 Euro.

Laut meiner Berechnung konnte ich mir also in den letzten Jahren mein Disney+-Abo (das ich als Star-Wars- und Marvel-Fan unbedingt brauche) so finanzieren. Wer Korrekturen oder Erweiterungen zu meiner Berechnung hat, kann sie mir gerne im Git-Repository mitteilen.

Was ich bei meiner Berechnung nicht berücksichtig habe, ist das Erwärmen der Wände oder des Fußbodens. Diese nehmen natürlich auch entsprechend Energie auf, um sich auf die Lufttemperatur zu erwärmen. Andererseits geben diese aber auch nach Abschalten der Heizung wieder Energie ab. Um das zu kompensieren, habe ich den Temperaturverlust von 0,5 K/h und die Nachtabsenkung von nur 5 Stunden recht großzügig angenommen. Nach meinen Aufzeichnungen liegt der Temperaturverlust tatsächlich etwa zwischen 0,2 und 0,4 K/h (je nach Außentemperatur). Die Heizung ist etwa 7 Stunden aus.

## Berechnung Energieeinsparung
In der Excel-Datei soll das Potential für die Energieeinsparung bei Absenken der Heizung berechnet werden. 

### Grün hinterlegte Felder sind manuell einzugeben.
* durchschn. Transmissionswärmeverlust: durchschnittlicher Wärmeverlust über alle Bauteile, die an außen grenzen (in Watt pro m² je K Temperaturunterschied)
* Gesamtfläche: die gesamte Wand und Dachfläche der Bauteile, die an außen grenzen
* Gesamtvolumen: das gesamte Volumen des Gebäudes (für die Berechnung des Energiebedarfs zum Aufheizen)
* Raumtemperatur: aktuelle bzw. gewünschte Raumtemperatur
* Außentemperatur: Tagesdurchschnitt
* Dauer Nachtabsenkung: für diese Dauer ist die Heizung aus
* Temperaturverlust w. Absenkung: die Raumtemperatur fällt bei ausgeschalteter Heizung um diesen Wert je Stunde
* € je Einheit: Pris für den Energieträger je angegebener Einheit (z. B. l, m³, kg ...)

### Berechnungen
* Transmissionswärmeverlust: durchschn. Transmissionswärmeverlust * Gesamtfläche
* Temperaturdifferenz: Raumtemperatur - Außentemperatur
* Transmissionswärmeverlust gesamt: durchschn. Transmissionswärmeverlust * Gesamtfläche * Temperaturdifferenz
* Eingesparte Leistung: Transmissionswärmeverlust gesamt * Dauer Nachtabsenkung / 1000
* Raumtemperatur nach Absenkung: Raumtemperatur - Temperaturverlust w. Absenkung * Dauer Nachtabsenkung
* Erwärmen von Luft (0,33Wh / m³ / K): (Raumtemperatur - Raumtemperatur nach Absenkung) * 0,33 * Gesamtvolumen
* Gesparte Energie tatsächlich: Eingesparte Leistung - Erwärmen von Luft / 1000
* Gespart: Heizwert (je Einheit wie l, m³, kg ...) / Gesparte Energie tatsächlich
* € gespart: Gespart * € je Einheit

### Unschärfen
Der Transmissionswärmeverlust gesamt ist nicht, wie hier angenommen, linear. Er ist abhängig von der Temperaturdifferenz. Je geringer die Differenz, desto geringer der Transmissionswärmeverlust. 
