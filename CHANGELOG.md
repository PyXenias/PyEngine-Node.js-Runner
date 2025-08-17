# Changelog

Alle wichtigen Änderungen an diesem Projekt werden in dieser Datei dokumentiert.

Das Format basiert auf [Keep a Changelog](https://keepachangelog.com/de/1.0.0/),
und dieses Projekt folgt [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [0.0.1] - 2025-08-17

### ✨ Hinzugefügt
- **Play Button Integration**: ▶️ Button in der Editor-Toolbar für schnelle JavaScript/TypeScript Ausführung
- **Output Channel**: Dedicated "Node.js Runner" Konsole mit formatierter Ausgabe
- **Multi-Format Support**: 
  - JavaScript (.js) Dateien mit direkter Node.js Ausführung
  - TypeScript (.ts) Dateien mit automatischer ts-node Integration
- **Smart File Detection**: Automatische Erkennung von ausführbaren Dateitypen
- **Context Menu Integration**: Rechtsklick-Optionen für JavaScript/TypeScript Dateien

### ⌨️ Keyboard Shortcuts
- `Ctrl+F5`: Aktuelle Datei ausführen
- `Ctrl+Shift+F5`: app.js aus Workspace-Root ausführen

### 🎛️ Commands
- `Run Node.js File`: Führt die aktuell geöffnete Datei aus
- `Run app.js`: Führt app.js aus dem Projekt-Root aus  
- `Clear Output`: Löscht die Konsole
- `Stop Running`: Stoppt laufende Prozesse

### ⚙️ Konfiguration
- `nodejs-runner.nodeExecutable`: Pfad zur Node.js Executable (Standard: "node")
- `nodejs-runner.clearOutputBeforeRun`: Ausgabe vor Ausführung löschen (Standard: true)
- `nodejs-runner.showRunningIndicator`: Status Bar Anzeige (Standard: true)
- `nodejs-runner.autoSaveBeforeRun`: Automatisches Speichern vor Ausführung (Standard: true)
- `nodejs-runner.nodeArguments`: Zusätzliche Node.js Argumente (Standard: [])

### 🎨 UI Features
- **Status Bar Integration**: Live-Status mit Play/Stop Buttons
- **Formatierte Ausgabe**: 
  - 🔄 Status-Indikatoren
  - 📁 Pfad-Anzeige
  - ⚙️ Konfiguration sichtbar
  - ✅/❌ Exit Code Anzeige
- **Real-time Output**: Live-Streaming der Programmausgabe
- **Error Handling**: Benutzerfreundliche Fehlermeldungen

### 🛠️ Process Management
- **Background Processes**: Unterstützung für länger laufende Prozesse
- **Kill Process**: Laufende Prozesse sicher beenden
- **Multiple Files**: Wechsel zwischen verschiedenen Dateien
- **Working Directory**: Korrekte Arbeitsverzeichnis-Behandlung

### 📦 TypeScript Support
- **ts-node Integration**: Automatische TypeScript Kompilierung
- **Fallback Handling**: Graceful Fallback zu npx ts-node
- **Type Safety**: Vollständige TypeScript Unterstützung

### 🔧 Technical Features
- **Webpack Bundling**: Optimierte Extension Performance
- **ESLint Integration**: Code Quality Checks
- **Test Framework**: Vorbereitet für Unit Tests
- **Modern APIs**: VS Code API Best Practices

### 📋 Example Files
- **app.js**: Vollständige Demo-Anwendung mit Node.js Features
- **test.ts**: TypeScript Beispiel mit Interfaces und Klassen
- **Icon Assets**: Professionelles Extension Icon

## [Geplant] - Zukünftige Versionen

### 🔮 Roadmap v0.1.0
- [ ] 🔧 Environment Variables Support
- [ ] 📦 NPM Script Integration
- [ ] 🧪 Testing Framework Integration
- [ ] 🔍 Debugging Support

### 🔮 Roadmap v0.2.0
- [ ] 📈 Performance Monitoring
- [ ] 🌐 Remote Execution
- [ ] 📊 Output Filtering
- [ ] 🎯 Multiple Node.js Versions

---

### Legende
- ✨ Neue Features
- 🐛 Bug Fixes  
- ⚡ Performance Verbesserungen
- 🔒 Security Updates
- 💥 Breaking Changes
- 📝 Dokumentation