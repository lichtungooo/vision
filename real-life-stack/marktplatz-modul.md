# Marktplatz-Modul

*Lokale Wertschöpfung ohne Geld - Begabungen & Bedürfnisse teilen*

**Version:** 1.0
**Datum:** 6. Februar 2026
**Status:** Konzeptphase

---

## 🎯 Vision

Der Marktplatz ist das **Herzstück für lokale Wertschöpfung ohne Geld**. Menschen in Gemeinschaften können ihre **Begabungen** (was sie geben können) und **Bedürfnisse** (was sie suchen) sichtbar machen. Durch Vertrauen zwischen Gemeinschaften entstehen **Netzwerke des Teilens** - Werkzeuge, Ressourcen, Wissen, Zeit.

**Kernprinzipien:**
- ❌ **Keine Bepreisung** - kein Geld, keine Tausch-1:1-Logik
- ✅ **Begabungen & Bedürfnisse** - was kann ich geben? Was brauche ich?
- ✅ **Vertrauen zwischen Gemeinschaften** - Web of Trust entscheidet, was geteilt wird
- ✅ **Lokale Kartierung** - wo sind Ressourcen? Wo ist der Apfelbaum?
- ✅ **Fofi-Integration** - QR-Codes für Empfangen/Geben dokumentieren
- ✅ **Einfachheit** - Einstieg muss kinderleicht sein

---

## 📖 Inhaltsverzeichnis

1. [Grundkonzept](#1-grundkonzept)
2. [User Stories](#2-user-stories)
3. [Datenmodell](#3-datenmodell)
4. [Begabungen & Bedürfnisse](#4-begabungen--bedürfnisse)
5. [Ressourcen & Werkzeuge](#5-ressourcen--werkzeuge)
6. [Gemeinschafts-Marktplätze](#6-gemeinschafts-marktplätze)
7. [Web of Trust Integration](#7-web-of-trust-integration)
8. [Fofi & QR-Code Integration](#8-fofi--qr-code-integration)
9. [Kartierung & Locations](#9-kartierung--locations)
10. [Kalender-Integration](#10-kalender-integration)
11. [Quest-Integration](#11-quest-integration)
12. [UI & Navigation](#12-ui--navigation)
13. [Usability & MVP](#13-usability--mvp)
14. [Offene Fragen](#14-offene-fragen)

---

## 1. Grundkonzept

### 1.1 Was ist der Marktplatz?

Der Marktplatz ist **kein Kleinanzeigen-Portal mit Preisen**. Er ist ein **Ort des Sichtbarmachens und Teilens**.

**Vier Säulen:**

#### 🎁 Begabungen (Was ich geben kann)
*"Ich kann Fahrräder reparieren, Sauerteigbrot backen, Gitarre spielen"*

- Fähigkeiten, die ich teilen möchte
- Wissen, das ich weitergeben kann
- Zeit, die ich schenken möchte

#### 🙏 Bedürfnisse (Was ich suche)
*"Ich brauche Hilfe beim Hausbau, suche jemanden für Buchhaltung, würde gerne Imkern lernen"*

- Was ich gerade brauche
- Was ich lernen möchte
- Wonach ich suche

#### 🛠️ Ressourcen & Werkzeuge (Was physisch da ist)
*"Motorsäge, Traktor, Lastenrad, Apfelbäume auf Wiese XY"*

- Werkzeuge, die geteilt werden können
- Infrastruktur (Werkstatt, Raum, Land)
- Natürliche Ressourcen (Obstbäume, Kräuter, Holz)

#### 🌍 Gemeinschafts-Angebote (Was wir zusammen machen)
*"Apfelernte in Niedermörig - kommt vorbei und pflückt mit!"*

- Gemeinsame Projekte
- Quests, an denen andere teilnehmen können
- Events, die Ressourcen erzeugen (z.B. Ernte)

### 1.2 Warum ohne Geld?

**Problem mit Geld:**
- Geld erzeugt **Knappheit** (ich gebe nur, wenn ich bekomme)
- Geld schafft **Hierarchien** (wer hat, wer hat nicht)
- Geld verhindert **echtes Teilen** (ich "verkaufe" statt zu geben)

**Lösung: Vertrauen + Sichtbarkeit**
- Ich sehe, wer was braucht → ich gebe, wenn ich kann
- Ich sehe, wer was kann → ich frage, wenn ich brauche
- **Web of Trust** regelt, wer mit wem teilt (nicht Geld)
- **Fofi-Token** dokumentieren Geben/Empfangen (ohne Schuld)

---

## 2. User Stories

### 2.1 Begabungen & Bedürfnisse

#### US-1: Begabung eintragen
**Als** Nutzer
**möchte ich** meine Begabungen eintragen
**damit** andere sehen, was ich geben kann.

**Akzeptanzkriterien:**
- Formular: Titel, Beschreibung (Markdown), Hashtags (#fahrrad, #handwerk)
- Optional: Bilder, Verfügbarkeit (wann habe ich Zeit?)
- Sichtbarkeit: Eigene Gemeinschaft, vertrauenswürdige Gemeinschaften, öffentlich

**Beispiel:**
```
Titel: "Fahrrad-Reparatur"
Beschreibung: "Ich repariere Fahrräder aller Art. Habe Werkstatt und Ersatzteile."
Hashtags: #fahrrad, #reparatur, #handwerk
Verfügbarkeit: "Samstags 10-16 Uhr"
Sichtbarkeit: Eigene Gemeinschaft + vertrauenswürdige
```

---

#### US-2: Bedürfnis eintragen
**Als** Nutzer
**möchte ich** meine Bedürfnisse eintragen
**damit** andere sehen, wobei sie mir helfen können.

**Akzeptanzkriterien:**
- Formular: Titel, Beschreibung, Hashtags
- Optional: Dringlichkeit (jetzt, bald, irgendwann)
- Optional: Mengenangabe (z.B. "Suche 50kg Äpfel")
- Sichtbarkeit wie bei Begabungen

**Beispiel:**
```
Titel: "Suche Hilfe beim Hausbau"
Beschreibung: "Baue Strohballenhaus, brauche Unterstützung beim Dach"
Hashtags: #bauen, #handwerk, #strohballenhaus
Dringlichkeit: "In 2 Wochen"
```

---

#### US-3: Nach Hashtags suchen
**Als** Nutzer
**möchte ich** nach Hashtags suchen
**damit** ich z.B. alle #fahrrad-Begabungen oder #äpfel-Bedürfnisse finde.

**Akzeptanzkriterien:**
- Suchfeld mit Hashtag-Autocomplete
- Ergebnisliste zeigt Begabungen + Bedürfnisse
- Filter: Nur Begabungen, nur Bedürfnisse, beides

---

#### US-4: Begabung & Bedürfnis matchen
**Als** Nutzer
**möchte ich** sehen, wenn meine Begabung zu einem Bedürfnis passt
**damit** ich proaktiv helfen kann.

**Akzeptanzkriterien:**
- Notification: "Teo sucht #fahrrad-Hilfe in deiner Gemeinschaft!"
- Optional: AI-basiertes Matching (später)

---

### 2.2 Ressourcen & Werkzeuge

#### US-5: Ressource eintragen
**Als** Nutzer
**möchte ich** Ressourcen (Werkzeuge, Infrastruktur, Natur) eintragen
**damit** andere wissen, was verfügbar ist.

**Akzeptanzkriterien:**
- Formular: Titel, Beschreibung, Typ (Werkzeug, Infrastruktur, Natur)
- Hashtags (#motorsäge, #traktor, #apfelbaum)
- **Ort/Location** (Kartierung!)
- **Verfügbarkeit** (Kalender-Integration: Wann ist Motorsäge frei?)
- Optional: Mengenangabe (z.B. "20 Apfelbäume")
- Optional: Zustand (neu, gut, ok, braucht Reparatur)

**Beispiel:**
```
Titel: "Motorsäge Stihl MS 261"
Typ: Werkzeug
Beschreibung: "Professionelle Motorsäge, gut gepflegt"
Hashtags: #motorsäge, #holz, #werkzeug
Ort: Werkstatt Vertrautloben (Karte)
Verfügbarkeit: Kalender (blockiert wenn verliehen)
Zustand: "Gut"
```

---

#### US-6: Werkzeug ausleihen
**Als** Nutzer
**möchte ich** ein Werkzeug ausleihen
**damit** ich es nicht kaufen muss.

**Akzeptanzkriterien:**
- In Ressourcen-Detailansicht: Button "Anfragen"
- Nachricht an Besitzer mit gewünschtem Zeitraum
- Optional: Kalender-Buchung (wenn Ressource kalenderbasiert)
- Nach Ausleihe: Fofi-Scan dokumentiert Empfangen

**Flow:**
1. Timo sieht "Motorsäge" in Niedermörig
2. Klickt "Anfragen" → wählt Zeitraum (15.-17. Feb)
3. Nachricht an Besitzer: "Kann ich die Motorsäge leihen?"
4. Besitzer sagt zu → Kalender-Eintrag wird erstellt
5. Am 15. Feb: Timo holt Motorsäge ab → Fofi-Scan
6. Am 17. Feb: Timo bringt zurück → Fofi-Scan

---

#### US-7: Wo ist das Werkzeug gerade?
**Als** Besitzer
**möchte ich** sehen, wo mein Werkzeug gerade ist
**damit** ich den Überblick behalte.

**Akzeptanzkriterien:**
- Ressourcen-Detailansicht zeigt: "Aktuell bei: Teo (zurück am 17. Feb)"
- Historie: Alle bisherigen Ausleihen (Fofi-Log)

---

### 2.3 Gemeinschafts-Marktplätze

#### US-8: Gemeinschafts-Marktplatz ansehen
**Als** Nutzer
**möchte ich** den Marktplatz meiner Gemeinschaft sehen
**damit** ich weiß, was verfügbar ist.

**Akzeptanzkriterien:**
- Übersicht: Begabungen, Bedürfnisse, Ressourcen
- Filter: Hashtags, Typ, Verfügbarkeit
- Sortierung: Neueste, Beliebteste, Dringlichkeit

---

#### US-9: Mehrere Gemeinschaften durchsuchen
**Als** Nutzer
**möchte ich** Marktplätze anderer Gemeinschaften sehen (wenn Vertrauen besteht)
**damit** ich z.B. in Niedermörig nach Äpfeln suche.

**Akzeptanzkriterien:**
- Dropdown "Gemeinschaft auswählen"
- Nur Gemeinschaften mit Vertrauensebene ≥ X
- Ergebnisse zeigen Gemeinschafts-Tag ("aus Niedermörig")

---

#### US-10: Gemeinschafts-Quest erstellen
**Als** Organisator
**möchte ich** eine Quest erstellen, die Ressourcen für die Gemeinschaft erzeugt
**damit** andere mitmachen können.

**Akzeptanzkriterien:**
- Quest-Formular (siehe Quest-Modul)
- Checkbox "Erzeugt Ressource" → verlinkt zu Marktplatz-Ressource
- Beispiel: "Apfelernte" → erzeugt "200kg Äpfel" als Ressource
- Nach Quest-Completion: Ressource wird auf Marktplatz sichtbar

**Beispiel:**
```
Quest: "Apfelernte in Niedermörig"
Beschreibung: "Wir ernten gemeinsam Äpfel. Jeder Teilnehmer bekommt einen Teil."
Ressource: "Äpfel (200kg geschätzt)"
Ort: Apfelwiese Niedermörig (Karte)
Datum: 20. September 2026
Teilnahme: Offen für vertrauenswürdige Gemeinschaften
```

---

### 2.4 Fofi & Transaktions-Log

#### US-11: Empfangen dokumentieren (Fofi-Scan)
**Als** Nutzer
**möchte ich** das Empfangen einer Ressource dokumentieren
**damit** es im Marktplatz-Log sichtbar ist.

**Akzeptanzkriterien:**
- Fofi hat QR-Code (verlinkt zu Profil über Web of Trust)
- Scan-Funktion: "Empfangen" oder "Gegeben"
- Nach Scan: Eintrag im Marktplatz-Log
- Zeigt: Was, von wem, wann

**Flow:**
1. Teo gibt Timo Äpfel (5kg)
2. Teo öffnet Marktplatz → "Geben"
3. Scannt Timos Fofi (QR-Code)
4. Wählt Ressource: "Äpfel" + Menge: "5kg"
5. Bestätigt → Eintrag im Log:
   ```
   Teo → Timo: 5kg Äpfel (6. Feb 2026, 14:30)
   ```

---

#### US-12: Marktplatz-Log ansehen
**Als** Nutzer
**möchte ich** mein Marktplatz-Log sehen
**damit** ich nachvollziehen kann, was ich gegeben/empfangen habe.

**Akzeptanzkriterien:**
- Profil → "Marktplatz-Log"
- Tabs: "Empfangen", "Gegeben", "Alles"
- Liste: Was, von wem/an wen, Menge, Datum
- Optional: Export als CSV/PDF

**Beispiel-Log:**
```
## Empfangen
- 5kg Äpfel (von Teo, 6. Feb 2026)
- Motorsäge (von Ida, 15. Feb - 17. Feb 2026)

## Gegeben
- Fahrrad-Reparatur für Ali (8. Feb 2026)
- 2h Gartenarbeit für Pia (10. Feb 2026)
```

---

### 2.5 Kartierung & Locations

#### US-13: Ressource auf Karte sehen
**Als** Nutzer
**möchte ich** Ressourcen auf einer Karte sehen
**damit** ich weiß, wo die Apfelbäume oder die Werkstatt sind.

**Akzeptanzkriterien:**
- Karten-Ansicht (OSM/Leaflet/Mapbox)
- Marker für Ressourcen (Icon nach Typ)
- Tippen auf Marker → Ressourcen-Detailansicht
- Zoom-Stufen: Gemeinschaft, Region, überregional

---

#### US-14: Mikro-Kartierung
**Als** Gemeinschafts-Admin
**möchte ich** eine Mikro-Karte unserer Ländereien erstellen
**damit** alle wissen, wo Infrastruktur/Ressourcen sind.

**Akzeptanzkriterien:**
- Karten-Editor (Marker setzen, Flächen markieren)
- Layered Map: Infrastruktur, Natur, Werkzeuge, Events
- Beispiel: "Apfelwiese" (Fläche), "Werkstatt" (Marker), "Kompost" (Marker)

---

### 2.6 Kalender-Integration

#### US-15: Ressourcen-Verfügbarkeit im Kalender
**Als** Besitzer
**möchte ich** die Verfügbarkeit meiner Ressource im Kalender pflegen
**damit** andere sehen, wann sie verfügbar ist.

**Akzeptanzkriterien:**
- Ressource hat Kalender (wie Location im Kalender-Modul)
- Ausleihen blockieren Zeiträume
- In Marktplatz: "Verfügbar ab 18. Feb"

---

#### US-16: Event mit Ressourcen-Erzeugung
**Als** Organisator
**möchte ich** ein Event anlegen, das Ressourcen erzeugt
**damit** z.B. Apfelernte im Kalender UND auf Marktplatz sichtbar ist.

**Akzeptanzkriterien:**
- Event-Formular (Kalender-Modul)
- Checkbox "Erzeugt Ressource" → Verknüpfung zu Marktplatz-Ressource
- Nach Event: Ressource wird automatisch im Marktplatz gelistet

---

## 3. Datenmodell

### 3.1 Entität "MarketplaceListing" (Angebot/Gesuch)

| Feld | Typ | Beschreibung |
|------|-----|--------------|
| `id` | string | Eindeutige ID |
| `type` | enum ("ability", "need", "resource", "community_offer") | Typ |
| `title` | string | Titel |
| `descriptionMarkdown` | string | Beschreibung (Markdown) |
| `plainDescription` | string | Aus Markdown generiert |
| `hashtags` | Array<string> | Hashtags (#fahrrad, #äpfel) |
| `coverImageUrl` | string (optional) | Coverbild |
| `galleryImageUrls` | Array<string> (optional) | Bildergalerie |
| `createdByUserId` | string | Ersteller |
| `communityId` | string | Zugehörige Gemeinschaft |
| `visibility` | enum ("community", "trusted_communities", "public") | Sichtbarkeit |
| `status` | enum ("active", "fulfilled", "archived") | Status |
| `createdAt` | datetime | Erstellungszeitpunkt |
| `updatedAt` | datetime | Letzte Änderung |

---

### 3.2 Entität "Ability" (Begabung) extends MarketplaceListing

| Feld | Typ | Beschreibung |
|------|-----|--------------|
| `availability` | string (optional) | Wann verfügbar (Freitext oder Kalender-Link) |
| `skillLevel` | enum ("beginner", "intermediate", "expert") | Erfahrungslevel |

---

### 3.3 Entität "Need" (Bedürfnis) extends MarketplaceListing

| Feld | Typ | Beschreibung |
|------|-----|--------------|
| `urgency` | enum ("now", "soon", "sometime") | Dringlichkeit |
| `quantity` | string (optional) | Mengenangabe (z.B. "50kg") |
| `deadline` | datetime (optional) | Bis wann gebraucht |

---

### 3.4 Entität "Resource" (Ressource/Werkzeug)

| Feld | Typ | Beschreibung |
|------|-----|--------------|
| `id` | string | Eindeutige ID |
| `type` | enum ("tool", "infrastructure", "nature") | Ressourcentyp |
| `title` | string | Titel |
| `descriptionMarkdown` | string | Beschreibung |
| `hashtags` | Array<string> | Hashtags |
| `coverImageUrl` | string (optional) | Bild |
| `locationId` | string (optional) | Ort (Referenz auf Location) |
| `geoLat` | number (optional) | Latitude |
| `geoLng` | number (optional) | Longitude |
| `quantity` | string (optional) | Mengenangabe (z.B. "20 Apfelbäume") |
| `condition` | enum ("new", "good", "ok", "needs_repair") | Zustand |
| `availability` | string (optional) | Verfügbarkeit (Freitext oder Kalender-ID) |
| `calendarId` | string (optional) | Kalender für Buchungen |
| `currentlyWith` | string (optional) | Aktuell bei (User-ID oder Freitext) |
| `ownedByUserId` | string | Besitzer |
| `communityId` | string | Zugehörige Gemeinschaft |
| `visibility` | enum ("community", "trusted_communities", "public") | Sichtbarkeit |
| `createdAt` | datetime | Erstellungszeitpunkt |
| `updatedAt` | datetime | Letzte Änderung |

---

### 3.5 Entität "MarketplaceTransaction" (Geben/Empfangen)

| Feld | Typ | Beschreibung |
|------|-----|--------------|
| `id` | string | Eindeutige ID |
| `type` | enum ("give", "receive") | Geben oder Empfangen |
| `fromUserId` | string | Geber |
| `toUserId` | string | Empfänger |
| `resourceId` | string (optional) | Referenz auf Ressource |
| `listingId` | string (optional) | Referenz auf Listing (Ability/Need) |
| `itemDescription` | string | Was wurde gegeben/empfangen |
| `quantity` | string (optional) | Mengenangabe |
| `timestamp` | datetime | Zeitpunkt |
| `fofiQrCodeScanned` | boolean | Wurde via Fofi-Scan erfasst? |
| `location` | string (optional) | Wo (Freitext oder Geo) |
| `notes` | string (optional) | Notizen |

---

### 3.6 Entität "CommunityMarketplace"

| Feld | Typ | Beschreibung |
|------|-----|--------------|
| `id` | string | Eindeutige ID |
| `communityId` | string | Referenz auf Community |
| `name` | string | Name (z.B. "Marktplatz Vertrautloben") |
| `description` | string (optional) | Beschreibung |
| `coverImageUrl` | string (optional) | Coverbild |
| `mapCenterLat` | number (optional) | Karten-Zentrum (Latitude) |
| `mapCenterLng` | number (optional) | Karten-Zentrum (Longitude) |
| `mapZoomLevel` | number (optional) | Standard-Zoom |
| `settings` | object | Einstellungen (z.B. Sichtbarkeit, Freigabe-Regeln) |

---

### 3.7 Entität "ResourceBooking" (Werkzeug-Ausleihe)

| Feld | Typ | Beschreibung |
|------|-----|--------------|
| `id` | string | Eindeutige ID |
| `resourceId` | string | Referenz auf Resource |
| `borrowerUserId` | string | Ausleiher |
| `startDateTime` | datetime | Von wann |
| `endDateTime` | datetime | Bis wann |
| `status` | enum ("requested", "approved", "active", "returned", "cancelled") | Status |
| `pickupTransactionId` | string (optional) | Fofi-Scan bei Abholung |
| `returnTransactionId` | string (optional) | Fofi-Scan bei Rückgabe |
| `notes` | string (optional) | Notizen |
| `createdAt` | datetime | Anfrage-Zeitpunkt |

---

## 4. Begabungen & Bedürfnisse

### 4.1 Wie funktionieren Begabungen?

**Ziel:** Sichtbar machen, was ich kann und teilen möchte.

**Beispiele:**
- "Ich kann Fahrräder reparieren"
- "Ich backe Sauerteigbrot"
- "Ich gebe Gitarrenunterricht"
- "Ich helfe bei Gartenarbeit"
- "Ich kann Webseiten bauen"

**Wichtig:**
- **Keine Preisangabe!** (nicht "20€/Stunde")
- **Verfügbarkeit optional:** "Samstags 10-16 Uhr" oder Kalender-Link
- **Erfahrungslevel:** Anfänger, Fortgeschritten, Experte (zur Orientierung)

### 4.2 Wie funktionieren Bedürfnisse?

**Ziel:** Sichtbar machen, wobei ich Hilfe brauche.

**Beispiele:**
- "Suche Hilfe beim Hausbau"
- "Brauche 50kg Äpfel für Apfelsaft"
- "Möchte Imkern lernen - suche Mentor"
- "Suche jemanden für Buchhaltung"

**Wichtig:**
- **Dringlichkeit:** Jetzt, bald, irgendwann
- **Mengenangabe optional:** "50kg", "2 Stunden", "1x pro Woche"
- **Deadline optional:** "Bis Ende März"

### 4.3 Matching

**Automatisches Matching (später):**
- AI erkennt: "Teo hat #fahrrad-Begabung, Ida sucht #fahrrad-Hilfe"
- Notification: "Ida braucht Hilfe - passt zu deiner Begabung!"

**Manuelles Matching:**
- Hashtag-Suche: #fahrrad → zeigt alle Begabungen + Bedürfnisse
- Filter: Nur Begabungen / Nur Bedürfnisse

---

## 5. Ressourcen & Werkzeuge

### 5.1 Ressourcen-Typen

#### 🛠️ **Werkzeuge**
*Dinge, die ausgeliehen werden können*

Beispiele:
- Motorsäge
- Rasenmäher
- Lastenrad
- Bohrmaschine
- Holzofen
- Leiter

**Eigenschaften:**
- Zustand (neu, gut, ok, braucht Reparatur)
- Verfügbarkeit (Kalender: wann ist es frei?)
- Aktuell bei (wer hat es gerade?)

---

#### 🏗️ **Infrastruktur**
*Orte/Räume, die genutzt werden können*

Beispiele:
- Werkstatt
- Gemeinschaftsküche
- Seminarraum
- Lagerraum
- Fahrzeug (Traktor, Bulldog)

**Eigenschaften:**
- Kapazität (wie viele Personen/Dinge passen rein?)
- Ausstattung (was ist vorhanden?)
- Buchungskalender

---

#### 🌳 **Natur-Ressourcen**
*Natürliche Ressourcen, die geteilt werden können*

Beispiele:
- Apfelbäume (20 Bäume auf Wiese XY)
- Kräutergarten (Thymian, Rosmarin, Salbei)
- Holzlager (5 Raummeter Brennholz)
- Quelle / Brunnen

**Eigenschaften:**
- Menge (geschätzt oder genau)
- Saisonalität (wann verfügbar?)
- Ort (Kartierung!)

---

### 5.2 Ressourcen-Verwaltung

**Erstellen:**
1. Typ wählen (Werkzeug, Infrastruktur, Natur)
2. Titel, Beschreibung, Hashtags
3. Ort/Location (Karte oder Adresse)
4. Optional: Kalender erstellen (für Buchungen)
5. Optional: Bilder hochladen
6. Sichtbarkeit wählen (Gemeinschaft, vertrauenswürdig, öffentlich)

**Ausleihen:**
1. Nutzer sieht Ressource (z.B. Motorsäge)
2. Klickt "Anfragen"
3. Wählt Zeitraum (Kalender)
4. Nachricht an Besitzer
5. Besitzer bestätigt → Buchung erstellt
6. Bei Abholung: Fofi-Scan ("Empfangen")
7. Bei Rückgabe: Fofi-Scan ("Gegeben")

**Verfolgung:**
- Besitzer sieht: "Aktuell bei: Teo (zurück am 17. Feb)"
- Historie: Alle Ausleihen (Fofi-Log)
- Optional: Bewertung/Feedback ("War alles ok?")

---

### 5.3 Wo ist was? (Kartierung)

**Problem:** "Wo ist die Motorsäge gerade?"

**Lösung:**
- **Ressource hat Standort** (Location oder Geo-Koordinaten)
- **Karten-Ansicht** zeigt alle Ressourcen
- **Filter:** Werkzeuge, Infrastruktur, Natur
- **Mikro-Kartierung:** Gemeinschaft kann eigene Karte pflegen

**Beispiel:**
```
Karte Vertrautloben:
- Werkstatt (Marker)
- Apfelwiese (Fläche)
- Komposthaufen (Marker)
- Lagerraum (Marker)
- Traktor (Marker) → "Aktuell bei: Teo (Feld 3)"
```

---

## 6. Gemeinschafts-Marktplätze

### 6.1 Was ist ein Gemeinschafts-Marktplatz?

**Jede Gemeinschaft hat einen eigenen Marktplatz.**

**Inhalt:**
- Alle Begabungen der Mitglieder
- Alle Bedürfnisse der Mitglieder
- Alle Ressourcen der Gemeinschaft
- Alle Gemeinschafts-Angebote (Quests, Events)

**Sichtbarkeit:**
- **Eigene Gemeinschaft:** Alle Mitglieder sehen alles
- **Vertrauenswürdige Gemeinschaften:** Sehen, was freigegeben ist
- **Öffentlich:** Externe sehen, was als öffentlich markiert ist

### 6.2 Gemeinschafts-übergreifend

**Beispiel:**
- Vertrautloben & Niedermörig haben Vertrauen zueinander (Web of Trust)
- Vertrautloben sucht Äpfel (#äpfel)
- Suchergebnisse zeigen:
  - Vertrautloben: 0 Treffer
  - Niedermörig: "Apfelernte-Quest am 20. Sept" (200kg erwartet)

**Flow:**
1. Timo (Vertrautloben) sieht Apfelernte in Niedermörig
2. Klickt "Teilnehmen" → Quest-Teilnahme (siehe Quest-Modul)
3. Am 20. Sept: Timo hilft bei Ernte
4. Am Ende: Timo bekommt 10kg Äpfel → Fofi-Scan
5. Marktplatz-Log: "Empfangen: 10kg Äpfel von Niedermörig"

### 6.3 Gemeinschafts-Angebote

**Was sind Gemeinschafts-Angebote?**
- Quests/Events, die **Ressourcen erzeugen**
- Andere Gemeinschaften können teilnehmen (wenn Vertrauen besteht)

**Beispiele:**
- "Apfelernte" → erzeugt 200kg Äpfel
- "Holz-Schlag-Aktion" → erzeugt 10 Raummeter Brennholz
- "Imker-Workshop" → gibt Wissen weiter (Begabung)
- "Gemeinschafts-Werkstatt bauen" → erzeugt Infrastruktur

**Integration mit Quest-Modul:**
- Quest hat Checkbox "Erzeugt Ressource"
- Verlinkt zu Marktplatz-Ressource
- Nach Quest-Completion: Ressource wird auf Marktplatz sichtbar

---

## 7. Web of Trust Integration

### 7.1 Vertrauen entscheidet, was geteilt wird

**Problem:** Nicht jeder soll alles sehen/nutzen können.

**Lösung: Web of Trust**

**Vertrauensebenen:**
```
Ebene 0: Fremde (kein Vertrauen)
Ebene 1: Bekannte (Basis-Vertrauen)
Ebene 2: Freunde (mittleres Vertrauen)
Ebene 3: Enge Freunde (hohes Vertrauen)
Ebene 4: Familie/Kernteam (volles Vertrauen)
```

**Sichtbarkeit nach Vertrauen:**

| Listing-Typ | Sichtbarkeit-Optionen |
|-------------|----------------------|
| Begabung | Gemeinschaft, ≥ Ebene 1, ≥ Ebene 2, öffentlich |
| Bedürfnis | Gemeinschaft, ≥ Ebene 1, ≥ Ebene 2, öffentlich |
| Ressource (Werkzeug) | Gemeinschaft, ≥ Ebene 2 (Vertrauen nötig!) |
| Ressource (Natur) | Gemeinschaft, ≥ Ebene 1, öffentlich |
| Gemeinschafts-Angebot | Gemeinschaft, ≥ Ebene 1, öffentlich |

**Beispiel:**
```
Motorsäge (Vertrautloben):
Sichtbarkeit: "≥ Ebene 2" (Freunde)

→ Niedermörig hat Ebene 2 mit Vertrautloben
→ Niedermörig sieht Motorsäge
→ Kann anfragen, auszuleihen
```

### 7.2 Gemeinschafts-Vertrauen

**Neben individuellem Vertrauen gibt es Gemeinschafts-Vertrauen:**

**Community-to-Community Trust:**
```
Vertrautloben ↔ Niedermörig: Ebene 2 (Freunde)
Vertrautloben ↔ Nachbardorf: Ebene 1 (Bekannte)
Vertrautloben ↔ Fremdes Dorf: Ebene 0 (kein Vertrauen)
```

**Auswirkung:**
- Niedermörig sieht Marktplatz von Vertrautloben (Ebene ≥2)
- Nachbardorf sieht nur öffentliche Angebote (Ebene 1)
- Fremdes Dorf sieht gar nichts (Ebene 0)

**Verwaltung:**
- Community-Admins können Vertrauensebenen zu anderen Communities setzen
- Optional: Demokratische Abstimmung (DAO-Mechanismus)

---

## 8. Fofi & QR-Code Integration

### 8.1 Was ist ein Fofi?

**Fofi = Persönlicher Token mit QR-Code**

**Eigenschaften:**
- Jeder Nutzer hat einen Fofi (physisch oder digital)
- Fofi hat QR-Code → verlinkt zu Profil (verschlüsselt über Web of Trust)
- Fofi dokumentiert: Geben & Empfangen

**Wichtig:**
- Fofi ist **KEIN Geld** (keine Schuld, kein Tausch)
- Fofi ist **Dokumentations-Tool** (Sichtbarkeit schaffen)
- Fofi ist **Vertrauens-Anker** (wer gibt, wer empfängt)

### 8.2 Fofi-Scan im Marktplatz

**Use Case: Ressource empfangen**

**Flow:**
1. Teo gibt Timo 5kg Äpfel
2. Teo öffnet Marktplatz → "Geben"
3. Scannt Timos Fofi (QR-Code)
4. App erkennt: Timo (via Web of Trust)
5. Teo wählt: Ressource "Äpfel", Menge "5kg"
6. Bestätigt
7. Eintrag im Marktplatz-Log:
   ```
   Transaktion:
   Geber: Teo
   Empfänger: Timo
   Ressource: Äpfel
   Menge: 5kg
   Zeitpunkt: 6. Feb 2026, 14:30
   Ort: Niedermörig (optional)
   ```

**Use Case: Werkzeug ausleihen**

**Flow:**
1. Timo leiht Motorsäge von Ida
2. Bei Abholung: Ida scannt Timos Fofi → "Gegeben: Motorsäge"
3. Bei Rückgabe: Ida scannt Timos Fofi → "Empfangen: Motorsäge"
4. Marktplatz-Log zeigt:
   ```
   Ausleihe:
   Werkzeug: Motorsäge
   Ausleiher: Timo
   Besitzer: Ida
   Abholung: 15. Feb 2026, 10:00
   Rückgabe: 17. Feb 2026, 16:00
   ```

### 8.3 Verschlüsselung & Web of Trust

**Problem:** QR-Code soll nicht öffentlich Profile offenlegen.

**Lösung: Web of Trust Verschlüsselung**

**Mechanismus:**
1. Fofi-QR-Code enthält: `encrypted_profile_id`
2. Nur Nutzer mit Vertrauensebene ≥1 können entschlüsseln
3. Scanner-App prüft: "Habe ich Vertrauen zu dieser Person?"
4. Wenn ja: Profil wird geladen
5. Wenn nein: "Kein Vertrauen - Transaktion nicht möglich"

**Details (für Anton & Web of Trust Team):**
- Verschlüsselung via Public-Key Cryptography
- Fofi-QR enthält: `{ encrypted_id, public_key }`
- Scanner-App entschlüsselt mit eigenem Private Key (wenn Vertrauen besteht)
- Falls kein Vertrauen: Anfrage möglich ("Möchtest du Vertrauen aufbauen?")

---

## 9. Kartierung & Locations

### 9.1 Warum Kartierung?

**Problem:** "Wo ist der Apfelbaum? Wo ist die Werkstatt? Wo treffen wir uns?"

**Lösung: Ressourcen, Locations, Events auf Karte**

**Use Cases:**
- "Wo sind die Apfelbäume in Niedermörig?"
- "Wo ist die Werkstatt?"
- "Wo steht der Traktor gerade?"
- "Wo treffen wir uns zur Apfelernte?"

### 9.2 Karten-Ansicht

**Technologie:**
- OpenStreetMap (OSM) oder Mapbox
- Leaflet.js oder Mapbox GL JS (Web)
- Native Map-Komponenten (Mobile)

**Inhalte:**

#### Layer 1: Infrastruktur
- Werkstatt (Marker: 🛠️)
- Gemeinschaftsküche (Marker: 🍴)
- Lagerraum (Marker: 📦)

#### Layer 2: Natur-Ressourcen
- Apfelwiese (Fläche, grün)
- Kräutergarten (Fläche, grün)
- Holzlager (Marker: 🪵)

#### Layer 3: Werkzeuge (aktuell)
- Traktor (Marker: 🚜) → "Bei Teo, Feld 3"
- Motorsäge (Marker: 🪚) → "Bei Timo, zurück am 17. Feb"

#### Layer 4: Events/Quests
- Apfelernte (Marker: 🍎, Datum: 20. Sept)
- Holzschlag (Marker: 🪵, Datum: 5. März)

**Interaktion:**
- Tippen auf Marker → Detailansicht
- Filter: Infrastruktur, Natur, Werkzeuge, Events
- Zoom-Stufen: Gemeinschaft (nah), Region (mittel), überregional (weit)

### 9.3 Mikro-Kartierung

**Was ist Mikro-Kartierung?**
- Gemeinschaft erstellt **eigene detaillierte Karte** ihrer Ländereien
- Zeigt: Felder, Wege, Gebäude, Ressourcen, Infrastruktur

**Beispiel Vertrautloben:**
```
- Haupthaus (Marker)
- Werkstatt (Marker)
- Feld 1 (Fläche: Kartoffeln)
- Feld 2 (Fläche: Gemüse)
- Feld 3 (Fläche: Traktor aktuell hier)
- Apfelwiese (Fläche: 20 Bäume)
- Kompost (Marker)
- Brunnen (Marker)
- Feuerstelle (Marker)
```

**Editor:**
- Marker setzen (Icon wählen, Name, Beschreibung)
- Flächen markieren (Polygon zeichnen, Farbe, Name)
- Verbindungen (Wege, Grenzen)

**Sichtbarkeit:**
- Gemeinschaft: Volle Karte sichtbar
- Vertrauenswürdige: Nur öffentlich markierte Bereiche
- Fremde: Keine Mikro-Karte

---

## 10. Kalender-Integration

### 10.1 Ressourcen-Verfügbarkeit

**Problem:** "Wann ist die Motorsäge frei?"

**Lösung: Ressource hat Kalender**

**Mechanismus:**
1. Ressource (z.B. Motorsäge) bekommt Kalender (wie Location im Kalender-Modul)
2. Ausleihen blockieren Zeiträume
3. In Marktplatz-Ansicht: "Verfügbar ab 18. Feb"

**Integration:**
- Ressourcen-Detailansicht zeigt Kalender
- Nutzer kann freie Zeiträume sehen
- Bei Buchung: Kalender-Eintrag wird erstellt

**Beispiel:**
```
Ressource: Motorsäge
Kalender:
- 15. Feb - 17. Feb: Ausgeliehen (Timo)
- 20. Feb - 22. Feb: Ausgeliehen (Ida)
- 25. Feb - 28. Feb: Wartung (Teo)
→ Nächster freier Zeitraum: ab 1. März
```

### 10.2 Events mit Ressourcen-Erzeugung

**Problem:** Apfelernte ist Event UND erzeugt Ressource.

**Lösung: Event-Quest-Verknüpfung**

**Flow:**
1. Organisator erstellt Quest/Event "Apfelernte"
2. Checkbox "Erzeugt Ressource"
3. Verknüpft zu Marktplatz-Ressource "Äpfel (200kg)"
4. Quest wird im Kalender angezeigt (Datum, Ort)
5. Nutzer können teilnehmen (Quest-Modul)
6. Nach Quest-Completion: Ressource "Äpfel" wird auf Marktplatz sichtbar

**Vorteil:**
- Event ist im Kalender sichtbar (Teilnahme)
- Ressource ist im Marktplatz sichtbar (Verfügbarkeit)
- Verknüpfung ist transparent (woher kommen die Äpfel?)

---

## 11. Quest-Integration

### 11.1 Quests als Ressourcen-Erzeuger

**Konzept:** Quests können Ressourcen erzeugen, die auf Marktplatz geteilt werden.

**Beispiele:**

#### Quest: "Apfelernte in Niedermörig"
```
Beschreibung: "Wir ernten gemeinsam Äpfel. Jeder Teilnehmer bekommt einen Teil."
Ort: Apfelwiese Niedermörig (Karte)
Datum: 20. September 2026
Teilnahme: Offen für vertrauenswürdige Gemeinschaften
Erzeugt: Ressource "Äpfel (200kg geschätzt)"
```

**Flow:**
1. Quest wird erstellt (Quest-Modul)
2. Checkbox "Erzeugt Ressource" aktiviert
3. Ressource "Äpfel" wird angelegt (Marktplatz-Modul)
4. Verknüpfung: Quest ↔ Ressource
5. Quest erscheint im Kalender + auf Marktplatz
6. Nutzer nehmen teil
7. Nach Completion: Ressource wird auf Marktplatz aktiviert
8. Teilnehmer bekommen Anteil → Fofi-Scan dokumentiert

---

#### Quest: "Gemeinschafts-Werkstatt bauen"
```
Beschreibung: "Wir bauen eine Werkstatt für die Gemeinschaft."
Dauer: 2 Wochen (5.-19. Mai 2026)
Teilnahme: Gemeinschaft Vertrautloben
Erzeugt: Infrastruktur "Werkstatt" (Marktplatz)
```

**Flow:**
1. Quest "Werkstatt bauen" wird erstellt
2. Ressource "Werkstatt" (Typ: Infrastruktur) wird angelegt
3. Nach Quest-Completion: Werkstatt wird auf Marktplatz sichtbar
4. Werkstatt kann ab jetzt gebucht werden (Kalender)

---

### 11.2 Quests als Gemeinschafts-Angebote

**Konzept:** Andere Gemeinschaften können an Quests teilnehmen (wenn Vertrauen besteht).

**Beispiel:**
- Niedermörig macht "Apfelernte-Quest"
- Vertrautloben hat Vertrauen (Ebene 2)
- Vertrautloben-Mitglieder sehen Quest auf Marktplatz
- Können teilnehmen
- Bekommen Anteil (Äpfel)

**Vorteil:**
- Gemeinschafts-übergreifende Zusammenarbeit
- Ressourcen werden geteilt (nicht verkauft)
- Fofi dokumentiert Geben/Empfangen

---

## 12. UI & Navigation

### 12.1 Haupt-Navigation

**Tabs:**
1. **Marktplatz** (Übersicht)
2. **Begabungen** (Fähigkeiten)
3. **Bedürfnisse** (Gesuche)
4. **Ressourcen** (Werkzeuge, Infrastruktur, Natur)
5. **Karte** (Kartierung)
6. **Mein Log** (Geben/Empfangen)

### 12.2 Marktplatz-Übersicht

**Filter:**
- Gemeinschaft (Dropdown: Eigene, Niedermörig, Alle vertrauenswürdigen)
- Typ (Begabungen, Bedürfnisse, Ressourcen, Gemeinschafts-Angebote)
- Hashtags (Autocomplete)
- Verfügbarkeit (Jetzt, Bald, Irgendwann)

**Sortierung:**
- Neueste
- Dringlichkeit (bei Bedürfnissen)
- Beliebteste (nach Anfragen/Interaktionen)

**Kachel-Ansicht:**
```
┌─────────────────────────────────┐
│ 🛠️ Fahrrad-Reparatur           │
│ Teo • Vertrautloben             │
│ #fahrrad #reparatur #handwerk   │
│ Verfügbar: Samstags 10-16 Uhr   │
└─────────────────────────────────┘
```

### 12.3 Detailansicht

**Inhalt:**
- Titel
- Beschreibung (Markdown gerendert)
- Bilder (Coverbild, Galerie)
- Hashtags (anklickbar)
- Ersteller (Profil-Link)
- Gemeinschaft
- **Bei Ressourcen:**
  - Typ (Werkzeug, Infrastruktur, Natur)
  - Ort (Karte)
  - Verfügbarkeit (Kalender)
  - Zustand
  - Aktuell bei (falls ausgeliehen)
- **Bei Bedürfnissen:**
  - Dringlichkeit
  - Deadline
  - Menge

**Aktionen:**
- "Anfragen" (bei Ressourcen)
- "Kontaktieren" (bei Begabungen/Bedürfnissen)
- "Auf Karte zeigen"
- "Teilen"

### 12.4 Karten-Ansicht

**Toolbar:**
- Filter (Layer: Infrastruktur, Natur, Werkzeuge, Events)
- Suche (Hashtags, Name)
- Gemeinschaft wählen

**Karte:**
- Marker (Icons nach Typ)
- Flächen (für Natur-Ressourcen)
- Tippen → Detailansicht

**Zoom-Stufen:**
- Nah (Gemeinschaft): Mikro-Kartierung sichtbar
- Mittel (Region): Gemeinschafts-Zentren + große Ressourcen
- Weit (überregional): Nur Gemeinschafts-Standorte

### 12.5 Marktplatz-Log

**Tabs:**
- **Empfangen** (was habe ich bekommen)
- **Gegeben** (was habe ich gegeben)
- **Alles** (chronologisch)

**Liste:**
```
┌─────────────────────────────────┐
│ Empfangen                       │
├─────────────────────────────────┤
│ 5kg Äpfel                       │
│ von Teo (Niedermörig)           │
│ 6. Feb 2026, 14:30              │
│ [Fofi-Scan]                     │
├─────────────────────────────────┤
│ Motorsäge                       │
│ von Ida (Vertrautloben)         │
│ 15. Feb - 17. Feb 2026          │
│ [Fofi-Scan: Abholung, Rückgabe] │
└─────────────────────────────────┘
```

**Export:**
- CSV
- PDF
- ICS (für Kalender-Integration)

---

## 13. Usability & MVP

### 13.1 Einfachheit ist kritisch

**Problem:** Zu viele Felder, zu komplex → Nutzer steigen nicht ein.

**Lösung: MVP-Ansatz**

**MVP = Minimal Viable Product (erste Version)**

### 13.2 MVP-Features

**Was muss im MVP drin sein:**

✅ **Begabungen & Bedürfnisse:**
- Erstellen (Titel, Beschreibung, Hashtags)
- Suchen (Hashtags, Volltextsuche)
- Kontaktieren (Nachricht schreiben)

✅ **Ressourcen:**
- Erstellen (Titel, Beschreibung, Typ, Hashtags)
- Optional: Ort (Freitext, KEINE Karte im MVP)
- Optional: Verfügbarkeit (Freitext, KEIN Kalender im MVP)

✅ **Marktplatz-Log:**
- Manuell eintragen (KEIN Fofi-Scan im MVP)
- Liste: Was, von wem/an wen, Menge, Datum

✅ **Einfache Suche:**
- Hashtags
- Volltextsuche
- Filter: Typ (Begabung, Bedürfnis, Ressource)

---

**Was NICHT im MVP (kommt später):**

❌ Fofi-Scan (zu komplex für Start)
❌ Karten-Integration (zu aufwändig)
❌ Kalender-Integration für Ressourcen (zu komplex)
❌ Web of Trust Verschlüsselung (später)
❌ AI-basiertes Matching (später)
❌ Mikro-Kartierung (später)

---

### 13.3 MVP-Flow: Begabung eintragen

**Schritt 1: Typ wählen**
```
Was möchtest du eintragen?
[ ] Begabung (was du geben kannst)
[ ] Bedürfnis (was du suchst)
[ ] Ressource (Werkzeug, Infrastruktur, Natur)
```

**Schritt 2: Titel**
```
Titel:
[Fahrrad-Reparatur]
```

**Schritt 3: Beschreibung**
```
Beschreibung:
[Ich repariere Fahrräder aller Art. Habe Werkstatt und Ersatzteile.]

Optional: Markdown-Editor aktivieren [ ]
```

**Schritt 4: Hashtags**
```
Hashtags (mit # beginnen, z.B. #fahrrad):
[#fahrrad #reparatur #handwerk]

Vorschläge: #werkzeug, #mechanik, #hilfe
```

**Schritt 5: Sichtbarkeit**
```
Wer soll das sehen?
( ) Nur meine Gemeinschaft
( ) Vertrauenswürdige Gemeinschaften (Ebene ≥2)
( ) Öffentlich
```

**Schritt 6: Fertig!**
```
✅ Begabung "Fahrrad-Reparatur" erstellt!

Was jetzt?
- Auf Marktplatz sichtbar
- Andere können dich kontaktieren
- Du bekommst Benachrichtigung bei Anfragen
```

---

### 13.4 MVP-Flow: Ressource ausleihen

**Schritt 1: Ressource finden**
```
Suche: "Motorsäge"
→ Ergebnis: "Motorsäge Stihl MS 261" (Ida, Vertrautloben)
```

**Schritt 2: Details ansehen**
```
Motorsäge Stihl MS 261
Besitzer: Ida (Vertrautloben)
Typ: Werkzeug
Zustand: Gut
Verfügbarkeit: "Meistens verfügbar, einfach fragen"

[Anfragen]
```

**Schritt 3: Nachricht schreiben**
```
Nachricht an Ida:

Hallo Ida,
kann ich die Motorsäge vom 15.-17. Feb ausleihen?
Brauche sie für Holzarbeiten.

Danke!
Timo

[Senden]
```

**Schritt 4: Ida antwortet**
```
Nachricht von Ida:

Klar, kein Problem! Komm am 15. Feb um 10 Uhr vorbei.
Bring sie bitte am 17. Feb bis 18 Uhr zurück.

Grüße, Ida

[Bestätigen]
```

**Schritt 5: Nach Abholung (manuell eintragen)**
```
Marktplatz-Log → "Empfangen eintragen"

Was: Motorsäge Stihl MS 261
Von: Ida
Datum: 15. Feb 2026, 10:00
Notizen: "Bis 17. Feb zurückbringen"

[Speichern]
```

**Schritt 6: Nach Rückgabe (manuell eintragen)**
```
Marktplatz-Log → "Gegeben eintragen"

Was: Motorsäge Stihl MS 261
An: Ida
Datum: 17. Feb 2026, 17:30
Notizen: "Alles gut gelaufen, danke!"

[Speichern]
```

---

### 13.5 Usability-Prinzipien

**1. So wenig Felder wie möglich**
- Pflichtfelder: Titel, Beschreibung, Typ
- Rest optional

**2. Klare Sprache**
- Nicht "Listing erstellen" → "Was möchtest du teilen?"
- Nicht "Resource Allocation" → "Wann ist verfügbar?"

**3. Vorschläge & Autocomplete**
- Hashtag-Vorschläge (häufig genutzte)
- Gemeinschafts-Vorschläge (vertrauenswürdige)

**4. Feedback & Bestätigung**
- "✅ Begabung erstellt!"
- "📬 Nachricht gesendet!"
- "📝 Eintrag im Log gespeichert!"

**5. Mobile-First**
- Große Buttons
- Swipe-Gesten
- Keine langen Formulare (Schritte aufteilen)

---

## 14. Offene Fragen

### 14.1 Fofi-Scan Implementierung

**Frage:** Wie genau funktioniert die QR-Code-Verschlüsselung über Web of Trust?

**Kontext:**
- Fofi hat QR-Code → soll zu Profil verlinken
- Aber: Nicht öffentlich (nur bei Vertrauen)
- Verschlüsselung nötig

**Für Anton & Web of Trust Team:**
- Public-Key Cryptography?
- Challenge-Response-Mechanismus?
- Wie wird Vertrauensebene geprüft (Client-side oder Server-side)?

---

### 14.2 Gemeinschafts-Vertrauen

**Frage:** Wer legt Vertrauensebenen zwischen Communities fest?

**Optionen:**
1. **Community-Admins:** Admin A + Admin B vereinbaren Ebene
2. **Demokratisch:** Mitglieder stimmen ab (DAO)
3. **Automatisch:** Basierend auf individuellen Vertrauensebenen (Durchschnitt)

**Empfehlung:** Hybrid (Admins schlagen vor, Mitglieder stimmen ab)

---

### 14.3 Ressourcen-Verfügbarkeit

**Frage:** MVP mit Freitext oder direkt Kalender-Integration?

**Option A (MVP):** Freitext
- "Meistens verfügbar, einfach fragen"
- Einfach, aber ungenau

**Option B (später):** Kalender
- Ressource hat Kalender (wie Location)
- Nutzer sehen freie Zeiträume
- Buchungen blockieren Zeiträume

**Empfehlung:** MVP mit Freitext, Kalender in v2

---

### 14.4 AI-basiertes Matching

**Frage:** Wann kommt automatisches Matching?

**Beispiel:**
- Teo hat Begabung: #fahrrad #reparatur
- Ida hat Bedürfnis: #fahrrad #hilfe
- → AI schlägt vor: "Teo, Ida braucht deine Hilfe!"

**Technologie:**
- Hashtag-Matching (einfach)
- Semantisches Matching (NLP, komplexer)
- Kontext-basiert (Ort, Zeit, Vertrauen)

**Empfehlung:** Hashtag-Matching in v2, Semantik später

---

### 14.5 Kartierung im MVP?

**Frage:** Karte im MVP oder später?

**Pro Karte im MVP:**
- "Wo ist was?" ist Killer-Feature
- Visualisierung hilft Verständnis
- Locations/Ressourcen machen mehr Sinn

**Contra Karte im MVP:**
- Komplex (Map-Integration, Markers, Layers)
- Usability-Risiko (zu viel auf einmal)
- Freitext-Ort reicht erstmal

**Empfehlung:** Karte in v1.5 (nach MVP-Launch, vor v2)

---

### 14.6 Mengenangaben

**Frage:** Wie werden Mengenangaben gehandhabt?

**Beispiel:**
- Bedürfnis: "50kg Äpfel"
- Ressource: "200kg Äpfel verfügbar"
- → Matching: "Niedermörig hat 200kg, Timo braucht 50kg"

**Optionen:**
1. **Freitext:** "50kg" (einfach, unstrukturiert)
2. **Strukturiert:** Zahl + Einheit (15, "kg") (komplex, präzise)
3. **Optional:** Erst Freitext, später strukturiert

**Empfehlung:** Freitext im MVP, strukturiert in v2

---

### 14.7 Bewertungen / Feedback?

**Frage:** Soll es Bewertungen geben?

**Beispiel:**
- Timo leiht Motorsäge von Ida
- Nach Rückgabe: "War alles ok?" (Feedback)

**Pro:**
- Qualitätskontrolle (wer gibt Werkzeuge gut zurück?)
- Vertrauen stärken

**Contra:**
- Druck (Bewertungs-Angst)
- Würde-Verletzung (schlechte Bewertung = Ausschluss?)
- Widerspricht "Teilen ohne Schuld"

**Empfehlung:** KEINE Bewertungen (passt nicht zur Philosophie)
Alternative: "Danke sagen" (positiv, freiwillig, kein Druck)

---

## 15. Nächste Schritte

### 15.1 Was jetzt zu tun ist

**Design-Phase:**
- [ ] Mit Anton besprechen: Web of Trust Integration, QR-Code-Verschlüsselung
- [ ] MVP-Features finalisieren (was rein, was raus)
- [ ] UI-Mockups erstellen (Wireframes für Haupt-Ansichten)

**Technische Vorbereitung:**
- [ ] Datenbank-Schema finalisieren
- [ ] API-Endpunkte definieren
- [ ] Kalender-Integration klären (Ressourcen-Verfügbarkeit)
- [ ] Karten-Technologie wählen (OSM, Mapbox)

**MVP-Entwicklung:**
- [ ] Begabungen & Bedürfnisse (CRUD)
- [ ] Ressourcen (CRUD, ohne Kalender)
- [ ] Marktplatz-Log (manuell, ohne Fofi-Scan)
- [ ] Suche & Filter (Hashtags, Volltextsuche)
- [ ] Einfache Sichtbarkeits-Regeln (Gemeinschaft, vertrauenswürdig, öffentlich)

**Post-MVP (v1.5 - v2):**
- [ ] Fofi-Scan Integration
- [ ] Karten-Ansicht
- [ ] Kalender-Integration (Ressourcen-Verfügbarkeit)
- [ ] Mikro-Kartierung
- [ ] AI-basiertes Matching
- [ ] Quest-Integration (Ressourcen-Erzeugung)

---

### 15.2 Offene Fragen für Anton & Timo

1. **Fofi-QR-Code:** Wie genau funktioniert die Verschlüsselung? (Anton)
2. **Gemeinschafts-Vertrauen:** Wer legt Ebenen fest? Admin, Demokratie, Hybrid? (Timo + Anton)
3. **MVP-Scope:** Karte im MVP oder später? (Timo)
4. **Mengenangaben:** Freitext oder strukturiert? (Timo)
5. **Bewertungen:** Ja oder Nein? (Timo - meine Empfehlung: NEIN)
6. **Kalender-Integration:** Wann? MVP, v1.5, v2? (Timo)

---

## 16. Zusammenfassung

### Was ist der Marktplatz?

Ein **Ort des Sichtbarmachens und Teilens** - ohne Geld, ohne Tausch, ohne Schuld.

**Kern-Features:**
- **Begabungen** (was ich geben kann)
- **Bedürfnisse** (was ich suche)
- **Ressourcen** (Werkzeuge, Infrastruktur, Natur)
- **Gemeinschafts-Angebote** (Quests, die Ressourcen erzeugen)

**Philosophie:**
- **Vertrauen** (Web of Trust) entscheidet, wer mit wem teilt
- **Fofi-Token** dokumentieren Geben/Empfangen (ohne Schuld)
- **Kartierung** zeigt, wo Ressourcen sind
- **Einfachheit** ermöglicht niedrigschwelligen Einstieg

**Vision:**
Lokale Gemeinschaften können **autark** werden - durch Teilen statt Kaufen, durch Vertrauen statt Geld, durch Sichtbarkeit statt Knappheit.

---

*Dokumentiert am 6. Februar 2026*
*Für das RealStack-Projekt und alle Gemeinschaften, die entstehen werden*

🌍 **Zusammen bauen wir eine neue Erde - eine Gemeinschaft nach der anderen.**
