# App für die automatische Plangeneration fürs iPad

AR-basierte iOS-App zur Erkennung und Dokumentation von Lüftungsanlagen. Entwickelt als Bachelorarbeit von Marcel Hockmann.

## 🎯 Projektübersicht

Diese App nutzt ARKit und Machine Learning zur automatischen Erkennung von Lüftungskomponenten und generiert daraus technische 2D-Pläne.

### Erkannte Komponenten
- Rechteckige Kanäle
- Runde Rohre
- Lüftungsgeräte
- T-Verbindungen
- Luftauslässe

## 🏗️ Architektur

### Module
1. **Scanner-Modul**: ARKit + Kamera
2. **ML-Modul**: Core ML Object Detection
3. **Plan-Generator**: 2D Technical Plans
4. **Editing-Modul**: Manual Editing Interface
5. **Export-Modul**: PDF Generation

### Technologie-Stack
- **Platform**: iOS 15.0+
- **Language**: Swift + SwiftUI
- **AR**: ARKit, RealityKit
- **ML**: Core ML, Vision Framework
- **Export**: PDFKit, Core Graphics

## 📱 Systemanforderungen

- iOS 15.0 oder neuer
- ARKit-kompatibles Gerät
- iPhone/iPad mit A12 Bionic oder neuer
- Empfohlen: iPad Pro mit LiDAR

## 🚀 Installation

1. Repository klonen:
```bash
git clone https://github.com/verageA/VentilationScanner-iOS.git
cd VentilationScanner-iOS
```

2. Xcode-Projekt öffnen:
```bash
open VentilationScanner.xcodeproj
```

3. Developer Team in Xcode konfigurieren

4. App auf Gerät installieren (Simulator nicht für AR geeignet)

## 🔧 Development Setup

### Abhängigkeiten
Das Projekt nutzt Standard iOS-Frameworks:
- ARKit
- RealityKit
- Vision
- Core ML
- PDFKit
- SwiftUI

### ML-Modell Integration
Das YOLO-Modell für Objekterkennung muss noch trainiert und integriert werden:

1. Datensammlung für Lüftungskomponenten
2. YOLOv8 Training
3. Core ML Konvertierung
4. Integration in `VentilationDetector.swift`

## 📊 Projektstruktur

```
VentilationScanner/
├── VentilationScannerApp.swift     # App Entry Point
├── ContentView.swift               # Main TabView
├── Models/                         # Data Models
│   ├── VentilationComponent.swift
│   ├── Detection.swift
│   └── TechnicalPlan.swift
├── Modules/                        # Feature Modules
│   ├── Scanner/                    # AR Scanning
│   ├── ML/                         # Object Detection
│   ├── PlanGenerator/              # Plan Generation
│   ├── Editing/                    # Manual Editing
│   └── Export/                     # PDF Export
└── Views/                          # Supporting Views
    ├── PlanListView.swift
    └── SettingsView.swift
```

## 🎯 Roadmap

### Phase 1: MVP (Aktuell)
- [x] Grundlegende Projektstruktur
- [ ] RGB-basierte Objekterkennung
- [ ] Basic Plan-Generierung
- [ ] PDF-Export

### Phase 2: Erweiterungen
- [ ] LiDAR-Integration für präzise Maße
- [ ] Erweiterte Plan-Bearbeitung
- [ ] Cloud-Synchronisation

### Phase 3: Weitere Gewerke
- [ ] Heizung (Heating)
- [ ] Sanitär (Plumbing)
- [ ] CAD-Export (DWG)

## 📖 Verwendung

1. **Scannen**: AR-Scanner öffnen und Lüftungsanlage scannen
2. **Erkennung**: App erkennt automatisch Komponenten
3. **Plan generieren**: Aus Erkennungen 2D-Plan erstellen
4. **Bearbeiten**: Plan manuell nachbearbeiten
5. **Exportieren**: Als PDF speichern/teilen

## 🤝 Contributing

Dieses Projekt ist Teil einer Bachelorarbeit. Contributions sind willkommen:

1. Fork des Repositories
2. Feature Branch erstellen
3. Changes committen
4. Pull Request erstellen

## 📧 Kontakt

**Marcel Hockmann**
- GitHub: [@verageA](https://github.com/verageA)
- Email: marcelhockmann@yahoo.de

## 📄 Lizenz

Dieses Projekt ist für Bildungszwecke entwickelt. Alle Rechte vorbehalten.

---

*Entwickelt als Bachelorarbeit 2025*
