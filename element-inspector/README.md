# Element Inspector

Eine Chrome Extension, die es ermöglicht, HTML-Elemente auf Webseiten zu inspizieren und deren Informationen automatisch in die Zwischenablage zu kopieren.

## 🎯 Funktionen

- **Einfache Aktivierung**: Klicke auf das Extension-Icon, um den Inspektionsmodus zu starten
- **Element-Auswahl**: Bewege die Maus über beliebige Elemente auf der Webseite
- **Automatisches Kopieren**: Klicke auf ein Element, um folgende Informationen in die Zwischenablage zu kopieren:
  - **Outer HTML**: Der vollständige HTML-Code des Elements
  - **Computed Styles**: Alle berechneten CSS-Eigenschaften
  - **JS Path**: Der JavaScript-Selektor-Pfad zum Element

## 📦 Installation

### Aus dem Quellcode

1. Klone oder lade dieses Repository herunter
2. Öffne Chrome und navigiere zu `chrome://extensions/`
3. Aktiviere den **Entwicklermodus** (Toggle oben rechts)
4. Klicke auf **Entpackte Erweiterung laden**
5. Wähle den `element-inspector` Ordner aus

## 🚀 Verwendung

1. **Extension aktivieren**: Klicke auf das Element Inspector Icon in der Chrome-Toolbar
2. **Inspektionsmodus starten**: Klicke im Popup auf "Start Inspecting"
3. **Element auswählen**: Bewege die Maus über die Webseite - Elemente werden beim Hovern hervorgehoben
4. **Informationen kopieren**: Klicke auf das gewünschte Element
5. **Fertig**: Die Informationen sind jetzt in deiner Zwischenablage und können z.B. in AI-Prompts eingefügt werden

### Tipps

- Die kopierten Informationen sind formatiert und strukturiert für eine einfache Weiterverarbeitung
- Der Inspektionsmodus wird automatisch beendet, nachdem ein Element ausgewählt wurde
- Drücke `ESC`, um den Inspektionsmodus vorzeitig zu beenden

## 📁 Projektstruktur

```
element-inspector/
├── manifest.json          # Extension-Konfiguration
├── popup.html            # UI des Extension-Popups
├── popup.js              # Logik für das Popup
├── styles.css            # Styles für das Popup
├── content.js            # Content Script für die Webseiten-Interaktion
├── content-styles.css    # Styles für die Highlight-Overlays
├── icons/                # Extension-Icons
└── README.md             # Diese Datei
```

## 🛠️ Technische Details

- **Manifest Version**: 3
- **Permissions**: 
  - `activeTab`: Zugriff auf den aktiven Tab
  - `scripting`: Injection von Content Scripts
- **Content Script**: Wird dynamisch injiziert, wenn der Inspektionsmodus aktiviert wird
- **Kommunikation**: Verwendet Chrome's Message Passing API

## 🎨 Features im Detail

### Visual Feedback
- Elemente werden beim Hovern mit einem blauen Overlay hervorgehoben
- Smooth Transitions für ein angenehmes Benutzererlebnis
- Cursor ändert sich zu einem Crosshair im Inspektionsmodus

### Kopierte Daten
Die Extension kopiert die Daten in einem strukturierten Format:

```
=== OUTER HTML ===
<div class="example">...</div>

=== COMPUTED STYLES ===
color: rgb(0, 0, 0)
font-size: 16px
...

=== JS PATH ===
document.querySelector("div.example")
```

## 🔧 Entwicklung

### Voraussetzungen
- Google Chrome Browser
- Grundkenntnisse in HTML, CSS und JavaScript

### Lokale Änderungen testen
1. Nimm Änderungen am Code vor
2. Gehe zu `chrome://extensions/`
3. Klicke auf das Reload-Icon bei der Element Inspector Extension
4. Teste die Änderungen auf einer beliebigen Webseite

## 📝 Lizenz

Dieses Projekt steht zur freien Verfügung.

## 🤝 Beitragen

Feedback und Verbesserungsvorschläge sind willkommen!

---

**Version**: 1.0.0  
**Erstellt**: 2026
