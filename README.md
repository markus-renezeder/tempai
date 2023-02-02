# tempml

## Berechnung Energieeinsparung
In der Excel-Datei soll das Potential für die Energieeinsparung bei Absenken der Heizung berechnet werden. 

### Grün hinterlegte Felder sind manuell einzugeben.
durchschn. Transmissionswärmeverlust: durchschnittlicher Wärmeverlust über alle Bauteile, die an außen grenzen (in Watt pro m² je K Temperaturunterschied)
Gesamtfläche: die gesamte Wand und Dachfläche der Bauteile, die an außen grenzen
Gesamtvolumen: das gesamte Volumen des Gebäudes (für die Berechnung des Energiebedarfs zum Aufheizen)
Raumtemperatur: aktuelle bzw. gewünschte Raumtemperatur
Außentemperatur: Tagesdurchschnitt
Dauer Nachtabsenkung: für diese Dauer ist die Heizung aus
Temperaturverlust w. Absenkung: die Raumtemperatur fällt bei ausgeschalteter Heizung um diesen Wert je Stunde
€ je Einheit: Pris für den Energieträger je angegebener Einheit (z. B. l, m³, kg ...)

### Berechnungen
Transmissionswärmeverlust: durchschn. Transmissionswärmeverlust * Gesamtfläche
Temperaturdifferenz: Raumtemperatur - Außentemperatur
Transmissionswärmeverlust gesamt: durchschn. Transmissionswärmeverlust * Gesamtfläche * Temperaturdifferenz
Eingesparte Leistung: Transmissionswärmeverlust gesamt * Dauer Nachtabsenkung / 1000
Raumtemperatur nach Absenkung: Raumtemperatur - Temperaturverlust w. Absenkung * Dauer Nachtabsenkung
Erwärmen von Luft (0,33Wh / m³ / K): (Raumtemperatur - Raumtemperatur nach Absenkung) * 0,33 * Gesamtvolumen
Gesparte Energie tatsächlich: Eingesparte Leistung - Erwärmen von Luft / 1000
Gespart: Heizwert (je Einheit wie l, m³, kg ...) / Gesparte Energie tatsächlich
€ gespart: Gespart * € je Einheit

### Unschärfen
Der Transmissionswärmeverlust gesamt ist nicht, wie hier angenommen, linear. Er ist abhängig von der Temperaturdifferenz. Je geringer die Differenz, desto geringer der Transmissionswärmeverlust. 
