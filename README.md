# 🏁 DIE KI'S - Formula 1 in Schools Website

## 📋 Übersicht

Dies ist eine moderne, responsive Website für das Formula 1 in Schools Team "DIE KI'S" der IGS Wilhelmshaven.

### ✨ Features
- ✅ Elegantes Dark-Mode Design
- ✅ Interaktive Tabs und Untertabs
- ✅ Anklickbare Sponsor-Links (öffnen in neuem Tab)
- ✅ Vollständig responsive (funktioniert auf allen Geräten)
- ✅ Einfach zu bearbeiten - keine Programmierkenntnisse nötig
- ✅ Schnell und optimiert

---

## 📁 Dateistruktur

```
/
├── index.html                 ← HAUPTDATEI (öffnen Sie diese im Browser)
├── config.js                  ← KONFIGURATION (für Sponsoren etc.)
├── README.md                  ← Diese Datei
│
└── Bilder/
    ├── logo-neu.png
    ├── violet viper.png
    ├── printuniq_logo_white.png
    ├── wz-logo.jpg
    ├── igs-logo.jpg
    ├── simscale-logo.jpg
    └── [weitere Bilder...]
```

---

## 🚀 Erste Schritte

1. **Website öffnen:**
   - Doppelklick auf `index.html`
   - Oder im Browser: `Datei > Öffnen`

2. **Website im Browser ansehen:**
   - Die Seite sollte sofort mit dem Design laden
   - Testen Sie die Tabs und Untertabs
   - Klicken Sie auf Sponsoren-Logos zum Überprüfen der Links

---

## ✏️ Website bearbeiten

### Option 1: Text-Inhalte ändern (einfach)

Öffnen Sie `index.html` mit einem Texteditor (z.B. Notepad++, VS Code) und suchen Sie nach dem Text, den Sie ändern möchten. Beispiele:

```html
<!-- Beispiel: Team-Namen ändern -->
<p>Wir sind eine Gruppe von drei ambitionierten Schülern...</p>

<!-- Beispiel: Erfolge aktualisieren -->
<div class="card-title">🥈 2. Platz in Niedersachsen</div>
```

### Option 2: Sponsoren verwalten (sehr einfach!)

**WICHTIG:** Die Sponsoren sind jetzt direkt in der HTML-Datei konfiguriert.

So fügen Sie einen neuen Sponsor hinzu:

1. Öffnen Sie `index.html` mit Texteditor
2. Suchen Sie nach `const CONFIG = {` (ungefähr Zeile 350)
3. Finden Sie die `sponsors:` Liste
4. Kopieren Sie einen bestehenden Sponsor-Block:

```javascript
{
    name: "PrintUniq",
    logo: "printuniq_logo_white.png",
    url: "https://printuniq.de",
    description: "Druck Partner"
},
```

5. Passen Sie an (Name, Logo, URL, Beschreibung)
6. Speichern Sie die Datei
7. Browser aktualisieren (F5) - fertig!

### Option 3: Bilder ändern

1. **Neues Logo-Bild hinzufügen:**
   - Datei im Ordner speichern (z.B. `mein-sponsor-logo.png`)
   - In der `sponsors` Liste eintragen: `logo: "mein-sponsor-logo.png"`

2. **Hauptbild (Auto) austauschen:**
   - Im Text nach `violet viper.png` suchen
   - Durch neuen Dateinamen ersetzen

### Option 4: Farben anpassen (fortgeschritten)

Am Anfang der HTML-Datei finden Sie die Farbdefinition:

```css
:root {
    --primary: #7000a3;        /* Purpur */
    --accent: #ff006e;         /* Neon-Pink */
    --dark-bg: #0f0f15;        /* Dunkler Hintergrund */
    ...
}
```

Sie können diese Hex-Codes ändern. Webseite für Farbwahl: [colorpicker.com](https://www.colorpicker.com/)

---

## 🔗 Sponsor-Links verwalten

### Anklickbare Sponsor-Logos

Alle Sponsor-Logos sind jetzt direkt anklickbar! Sie führen zur Website des Sponsors.

Die URLs werden in der `sponsors` Liste in der HTML-Datei definiert:

```javascript
url: "https://printuniq.de"  ← Diese URL wird besucht
```

**URLs ändern:**
1. Zeile mit `url:` finden
2. Neue Website eingeben (mit `https://`)
3. Speichern & Browser aktualisieren

---

## 📱 Responsive Design

Die Website funktioniert perfekt auf:
- ✅ Desktop & Laptops
- ✅ Tablets
- ✅ Smartphones

Testen Sie mit `F12` Browser-Entwicklungstools (Device Toolbar).

---

## 🎨 Design-Anpassungen

### Header Logo ändern
```html
<img src="logo-neu.png" alt="DIE KI'S Logo">
```
Ändern Sie `logo-neu.png` auf Ihren neuen Dateinamen.

### Team-Namen ändern
Suchen Sie nach diesem Block (Zeile ~570):
```javascript
const CONFIG = {
    teamName: "DIE KI'S",
    schoolName: "IGS Wilhelmshaven",
```

### Kontaktdaten aktualisieren
```javascript
contacts: {
    teamEmail: "die.kis.2022@gmail.com",
    teamEmailNote: "Wird mindestens jeden Freitag kontrolliert...",
    schoolContact: "f1@igs-whv.de"
}
```

---

## 🐛 Häufige Probleme

### Bilder werden nicht angezeigt
- ✅ Sind die Bild-Dateien im gleichen Ordner wie `index.html`?
- ✅ Ist der Dateiname korrekt geschrieben? (Beachten Sie Groß-/Kleinschreibung!)

### Sponsor-Links funktionieren nicht
- ✅ Beginnt die URL mit `https://`?
- ✅ Ist die URL korrekt geschrieben?

### Styling sieht seltsam aus
- ✅ Browser-Cache löschen: `Strg+Shift+Löschen` (Chrome) oder `Strg+F5`
- ✅ Browser neuladen

---

## 📤 Website online stellen

Die Website kann auf verschiedenen Plattformen kostenlos gehostet werden:

### Option 1: Netlify (empfohlen)
1. Alle Dateien in einen Ordner
2. Drag & Drop auf [netlify.com](https://www.netlify.com/)
3. Website ist online!

### Option 2: GitHub Pages
1. GitHub-Konto erstellen
2. Repository erstellen
3. Dateien hochladen
4. Settings > Pages aktivieren

### Option 3: Einfach verteilen
- Alle Dateien als ZIP-Datei versenden
- Empfänger entpackt und öffnet `index.html`

---

## 🛠️ Weitere Anpassungen

### Text auf Seiten ändern

Suchen Sie nach den Inhalten in den `content-X-X` divs:

```html
<div id="content-0-0" class="content-section active">
    <h2>Was ist Formula 1 in Schools?</h2>
    <!-- Hier Text ändern -->
</div>
```

### Neue Reiter/Tabs hinzufügen

1. Neuen Tab in Navigation hinzufügen:
```html
<li><a href="javascript:void(0)" class="tab-link" data-tab="4">Neuer Tab</a></li>
```

2. Neuen Inhalts-Bereich hinzufügen:
```html
<div id="content-4-0" class="content-section">
    <h2>Mein neuer Inhalt</h2>
    <!-- Inhalt hier -->
</div>
```

3. JavaScript anpassen (fortgeschritten - am besten einen Entwickler fragen)

---

## 📞 Support & Kontakt

**Für die Website:**
- E-Mail: die.kis.2022@gmail.com
- Schulkontakt: f1@igs-whv.de

**Technische Fragen:**
- Überlegen Sie, einen Webentwickler zu konsultieren
- Oder fragen Sie in Web-Entwickler-Communities

---

## 📝 Version & Changelog

**Version 2.0 - 28.03.2025**
- ✅ Alle Bilder integriert
- ✅ Anklickbare Sponsor-Links
- ✅ Konfigurierbare Daten
- ✅ Responsive Design
- ✅ Moderne Animationen

---

## ⚖️ Lizenz

Diese Website wurde speziell für DIE KI'S erstellt.
Alle Rechte vorbehalten © 2025 DIE KI'S

---

**Viel Spaß mit der Website! 🏁**
