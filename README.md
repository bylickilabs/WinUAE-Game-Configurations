| <img width="1280" height="640" alt="UAE" src="https://github.com/user-attachments/assets/1f21224a-e499-4c69-bd8d-0c30b421d94b" /> |
|---|

| 🕹️ WinUAE Game Configurations |
|---|

- Präzise abgestimmte WinUAE-Profile für klassische Amiga-Spiele

[![WinUAE](https://img.shields.io/badge/Emulator-WinUAE-2B2B2B?style=for-the-badge)](https://www.winuae.net/)
![Platform](https://img.shields.io/badge/Plattform-Windows-0078D4?style=for-the-badge&logo=windows)
![Amiga](https://img.shields.io/badge/System-Amiga%20500-EA4E00?style=for-the-badge)
![Configs](https://img.shields.io/badge/Configs-5-success?style=for-the-badge)

| Klassische Spiele. Passende Hardwareprofile. Reproduzierbare Emulation. |
|---|

━━━━━━━━━━━━━━━━━━━━━━━━ ◆ ━━━━━━━━━━━━━━━━━━━━━━━━

## 📌 Projektübersicht

| WinUAE Game Configurations ist eine Sammlung speziell abgestimmter |
|---|

- `.uae`-Konfigurationsdateien für klassische Amiga-Spiele unter **WinUAE**.
- Das Ziel dieses Repositories ist nicht, einen einzigen maximal schnellen virtuellen Amiga zu bauen.
  - Stattdessen erhält jedes Spiel ein eigenes Profil, das sich möglichst eng an der für den jeweiligen Titel sinnvollen Amiga-Hardware orientiert.

| Die Konfigurationen definieren unter anderem: |
|---|

- CPU-Modell und CPU-Geschwindigkeit
- OCS- bzw. ECS-Chipsatz
- Chip RAM, Slow RAM und Fast RAM
- 24-Bit-Adressierung
- Cycle-Exact-Timing
- Blitter-Timing
- JIT-Status
- Kickstart-Ziel
- Anzahl der Diskettenlaufwerke
- Eingabeports
- PAL-Betrieb
- Audio-, Display- und Host-Grundeinstellungen

> [!IMPORTANT]
> Dieses Repository enthält **ausschließlich WinUAE-Konfigurationsdateien und Dokumentation**.  
> Es enthält **keine Kickstart-ROMs, keine ADF-Dateien, keine Spiele, keine WHDLoad-Images und keine sonstigen urheberrechtlich geschützten Softwareabbilder**.

━━━━━━━━━━━━━━━━━━━━━━━━ ◆ ━━━━━━━━━━━━━━━━━━━━━━━━

## 🎯 Ziel des Repositories

- Ein Amiga-Spiel aus den 1980er- oder 1990er-Jahren benötigt normalerweise **keinen 68040, kein JIT und keine 128 MB Z3 RAM**.
- Im Gegenteil: Zu moderne oder zu schnelle emulierte Hardware kann bei älteren Titeln zu Problemen führen.
  - Dieses Repository verfolgt deshalb einen anderen Ansatz:

| Nicht maximale virtuelle Leistung entscheidet, sondern die richtige emulierte Hardware für das jeweilige Spiel. |
|---|

- Die Konfigurationen sollen:
  - reproduzierbare WinUAE-Setups bereitstellen
  - klassische A500-Hardware möglichst sinnvoll abbilden
  - unnötiges manuelles Konfigurieren reduzieren
  - typische Inkompatibilitäten durch zu schnelle Hardware vermeiden
  - Spieleprofile sauber voneinander trennen
  - eine langfristig erweiterbare Config-Sammlung schaffen

> [!TIP]
> Ein separates Profil pro Spiel ist besonders sinnvoll, wenn verschiedene Titel unterschiedliche Anforderungen an RAM, Chipsatz, Timing oder Eingabegeräte stellen.

━━━━━━━━━━━━━━━━━━━━━━━━ ◆ ━━━━━━━━━━━━━━━━━━━━━━━━

## 🎮 Enthaltene Konfigurationen

| Spiel / Profil | Konfigurationsdatei | Zielsystem | Status |
|---|---|---|---|
| 🍄 **The Great Giana Sisters** | `Giana_Sisters_A500.uae` | Amiga 500 / OCS | ✅ Erstellt |
| 🪖 **Cannon Fodder** | `Cannon_Fodder_A500.uae` | Amiga 500 / ECS Agnus | ✅ Erstellt |
| 🧱 **Arkanoid** | `Arkanoid_A500.uae` | Amiga 500 / OCS | ✅ Erstellt |
| ✈️ **Wings of Fury** | `Wings_of_Fury_A500.uae` | Amiga 500 / OCS | ✅ Erstellt |

> [!NOTE]
> Das ursprüngliche **High-Performance-Profil** dient in dieser Dokumentation als technische Referenz. Es gehört konzeptionell nicht zu den klassischen A500-Spielprofilen.

━━━━━━━━━━━━━━━━━━━━━━━━ ◆ ━━━━━━━━━━━━━━━━━━━━━━━━

## ⚙️ Technischer Gesamtvergleich

| Eigenschaft | 🚀 High Performance | 🍄 Giana Sisters | 🪖 Cannon Fodder | 🧱 Arkanoid | ✈️ Wings of Fury |
|---|---:|---:|---:|---:|---:|
| **CPU** | 68040 | 68000 | 68000 | 68000 | 68000 |
| **CPU Speed** | Maximum | Real / A500 | Real / A500 | Real / A500 | Real / A500 |
| **Chipset** | AGA | OCS | ECS Agnus | OCS | OCS |
| **A500 Compatible** | Ja | Ja | Ja | Ja | Ja |
| **Kickstart-Ziel** | Nicht festgelegt | 1.3 | 1.3 | 1.3 | 1.3 |
| **Chip RAM** | 2 MB | 512 KB | 1 MB | 512 KB | 512 KB |
| **Slow RAM** | 0 MB | 512 KB | 512 KB | 0 MB | 512 KB |
| **Fast RAM** | 8 MB | 0 MB | 0 MB | 0 MB | 0 MB |
| **Z3 Fast RAM** | 128 MB | 0 MB | 0 MB | 0 MB | 0 MB |
| **JIT / Cache** | 8 MB | Aus | Aus | Aus | Aus |
| **24-Bit Addressing** | Aus | Ein | Ein | Ein | Ein |
| **CPU Cycle Exact** | Aus | Ein | Ein | Ein | Ein |
| **Memory Cycle Exact** | Aus | Ein | Ein | Ein | Ein |
| **Blitter Cycle Exact** | Aus | Ein | Ein | Ein | Ein |
| **Global Cycle Exact** | Aus | Ein | Ein | Ein | Ein |
| **Immediate Blitter** | Ein | Aus | Aus | Aus | Aus |
| **PAL** | Ja | Ja | Ja | Ja | Ja |
| **DF0** | Aktiv | Aktiv | Aktiv | Aktiv | Aktiv |
| **DF1** | Inaktiv | Inaktiv | Aktiv | Inaktiv | Inaktiv |
| **DF2** | Inaktiv | Inaktiv | Aktiv | Inaktiv | Inaktiv |
| **Aktive Floppy Drives** | 1 | 1 | 3 | 1 | 1 |
| **Port 1** | Maus | Maus | Maus | Maus | Maus |
| **Port 2** | Keyboard | Keyboard | Keyboard | Keyboard | Keyboard |

━━━━━━━━━━━━━━━━━━━━━━━━ ◆ ━━━━━━━━━━━━━━━━━━━━━━━━

# 🔬 Die Profile im Detail

## 🍄 The Great Giana Sisters

**Datei:** `Giana_Sisters_A500.uae`

> Das Profil bildet einen klassischen Amiga 500 mit OCS-Chipsatz und einem typischen Speicheraufbau aus 512 KB Chip RAM und 512 KB Slow RAM ab.

| Komponente | Einstellung |
|---|---|
| CPU | Motorola 68000 |
| CPU Speed | Real / A500 |
| Chipset | OCS |
| Chip RAM | 512 KB |
| Slow RAM | 512 KB |
| Fast RAM | 0 MB |
| Z3 RAM | 0 MB |
| Kickstart | 1.3 vorgesehen |
| JIT | Aus |
| 24-Bit Addressing | Ein |
| Cycle Exact | Ein |
| Memory Cycle Exact | Ein |
| Blitter Cycle Exact | Ein |
| Immediate Blitter | Aus |
| Floppy Drives | 1 |
| PAL | Ein |

> [!NOTE]
> Dieses Profil ist bewusst deutlich konservativer als das High-Performance-Profil. Für ein klassisches A500-Spiel ist Timing-Kompatibilität wichtiger als zusätzliche emulierte Rechenleistung.

---

## 🪖 Cannon Fodder

**Datei:** `Cannon_Fodder_A500.uae`

| Cannon Fodder erhält innerhalb der aktuellen Sammlung das umfangreichste klassische A500-Profil. |
|---|

| Komponente | Einstellung |
|---|---|
| CPU | Motorola 68000 |
| CPU Speed | Real / A500 |
| Chipset | ECS Agnus |
| Chip RAM | 1 MB |
| Slow RAM | 512 KB |
| Fast RAM | 0 MB |
| Z3 RAM | 0 MB |
| Kickstart | 1.3 vorgesehen |
| JIT | Aus |
| 24-Bit Addressing | Ein |
| Cycle Exact | Ein |
| Memory Cycle Exact | Ein |
| Blitter Cycle Exact | Ein |
| Immediate Blitter | Aus |
| Floppy Drives | 3 |
| PAL | Ein |

### Besonderheit

- Cannon Fodder ist aktuell die einzige Config dieser Sammlung mit:
  - **ECS Agnus**
  - **1 MB Chip RAM**
  - **drei aktiven Diskettenlaufwerken**
  - **DF0, DF1 und DF2**

> [!TIP]
> Bei einer mehrteiligen Diskettenversion können die vorhandenen Images direkt auf DF0, DF1 und DF2 verteilt werden. Dadurch lässt sich der manuelle Diskettenwechsel reduzieren.

---

## 🧱 Arkanoid

**Datei:** `Arkanoid_A500.uae`

| Arkanoid verwendet das schlankste Speicherprofil der aktuellen Sammlung. |
|---|

| Komponente | Einstellung |
|---|---|
| CPU | Motorola 68000 |
| CPU Speed | Real / A500 |
| Chipset | OCS |
| Chip RAM | 512 KB |
| Slow RAM | 0 MB |
| Fast RAM | 0 MB |
| Z3 RAM | 0 MB |
| Kickstart | 1.3 vorgesehen |
| JIT | Aus |
| 24-Bit Addressing | Ein |
| Cycle Exact | Ein |
| Memory Cycle Exact | Ein |
| Blitter Cycle Exact | Ein |
| Immediate Blitter | Aus |
| Floppy Drives | 1 |
| Port 1 | Maus |
| PAL | Ein |

> [!IMPORTANT]
> Für Arkanoid ist die Mauskonfiguration relevant. Das Profil lässt deshalb Port 1 explizit als Maus-Eingabe bestehen.

---

## ✈️ Wings of Fury

**Datei:** `Wings_of_Fury_A500.uae`

| Wings of Fury verwendet wie Giana Sisters ein klassisches 1-MB-A500-Speicherprofil. |
|---|

| Komponente | Einstellung |
|---|---|
| CPU | Motorola 68000 |
| CPU Speed | Real / A500 |
| Chipset | OCS |
| Chip RAM | 512 KB |
| Slow RAM | 512 KB |
| Fast RAM | 0 MB |
| Z3 RAM | 0 MB |
| Kickstart | 1.3 vorgesehen |
| JIT | Aus |
| 24-Bit Addressing | Ein |
| Cycle Exact | Ein |
| Memory Cycle Exact | Ein |
| Blitter Cycle Exact | Ein |
| Immediate Blitter | Aus |
| Floppy Drives | 1 |
| PAL | Ein |

> Das Profil konzentriert sich auf klassische A500-Kompatibilität und verzichtet vollständig auf moderne Erweiterungen wie JIT, Z3 RAM oder eine 68040-CPU.

━━━━━━━━━━━━━━━━━━━━━━━━ ◆ ━━━━━━━━━━━━━━━━━━━━━━━━

# 🚀 High-Performance-Referenz

| Das High-Performance-Profil war die technische Ausgangsbasis, aus der die spielespezifischen Configs abgeleitet wurden. |
|---|

> Es verwendet:

```text
CPU:                  Motorola 68040
CPU Speed:            Maximum
Chipset:              AGA
Chip RAM:             2 MB
Fast RAM:             8 MB
Z3 RAM:               128 MB
JIT Cache:            8 MB
24-Bit Addressing:    Aus
CPU Cycle Exact:      Aus
Blitter Cycle Exact:  Aus
Immediate Blitter:    Ein
PAL:                  Ein
```

> [!WARNING]
> Das High-Performance-Profil ist **kein universelles A500-Spieleprofil**.  
> Eine schnellere emulierte CPU und große RAM-Erweiterungen garantieren bei älteren Spielen keine bessere Kompatibilität.

### Der zentrale Unterschied

```diff
- High Performance: maximale virtuelle Leistung
+ Game Configs:      maximale praktische Spielkompatibilität
```

━━━━━━━━━━━━━━━━━━━━━━━━ ◆ ━━━━━━━━━━━━━━━━━━━━━━━━

# 📥 Installation und Verwendung

## Variante A – Config direkt über WinUAE laden

1. Gewünschte `.uae`-Datei aus diesem Repository herunterladen.
2. **WinUAE** starten.
3. Links den Bereich **Configurations** öffnen.
4. Die gewünschte Konfiguration laden.
5. Prüfen, ob das benötigte Kickstart-ROM erkannt wurde.
6. Unter **Floppy Drives** die eigenen ADF-Dateien einlegen.
7. Auf **Start** klicken.

### Beispiel

```text
WinUAE
  └─ Configurations
       └─ Load
            └─ Giana_Sisters_A500.uae
                 └─ Floppy Drives
                      └─ DF0: eigene Spiel-Diskette.adf
                           └─ Start
```

> [!TIP]
> Die `.uae`-Dateien können zusätzlich in den von WinUAE verwendeten Configurations-Ordner kopiert werden. Der genaue Speicherort kann je nach Installation und WinUAE-Konfiguration variieren.

━━━━━━━━━━━━━━━━━━━━━━━━ ◆ ━━━━━━━━━━━━━━━━━━━━━━━━

# 💾 Kickstart-ROMs

- Die Configs enthalten **kein Kickstart-ROM**.
  - Sie enthalten lediglich die Konfigurationsinformation, dass für die klassischen A500-Profile **Kickstart 1.3** vorgesehen ist.

```ini
kickstart_rom_file=
kickstart_rom_file_id=C4F0F55F,KS ROM v1.3 (A500,A1000,A2000)
```

| Das eigentliche ROM muss lokal und legal vorhanden sein. |
|---|

> [!CAUTION]
> Ein Kickstart-ROM darf nicht einfach aus diesem Repository bezogen oder ohne entsprechende Berechtigung weitergegeben werden.  
> Dieses Projekt liefert deshalb bewusst **keine ROM-Dateien** aus.

- Wenn WinUAE dein ROM nicht automatisch findet:
  - WinUAE öffnen
  - **ROM** auswählen
  - unter **Main ROM File** dein vorhandenes Kickstart-ROM auswählen
  - Config anschließend erneut speichern, wenn du den lokalen Pfad dauerhaft übernehmen möchtest

━━━━━━━━━━━━━━━━━━━━━━━━ ◆ ━━━━━━━━━━━━━━━━━━━━━━━━

# 💿 Disketten und ADF-Dateien

| Die Konfigurationsdateien enthalten keine Spiel-Disketten. |
|---|

> Ein Eintrag wie:

```ini
floppy0=
floppy1=
floppy2=
```

> bedeutet, dass das Laufwerk konfiguriert sein kann, aber **kein Diskettenabbild fest in die veröffentlichte Config eingebunden wurde**.
  - Das ist beabsichtigt.

### Beispiel für Cannon Fodder

```text
DF0 → eigene Cannon-Fodder-Disk 1
DF1 → eigene Cannon-Fodder-Disk 2
DF2 → eigene Cannon-Fodder-Disk 3
```

> [!IMPORTANT]
> Verwende ausschließlich Spielabbilder, für deren Besitz und Nutzung du die erforderlichen Rechte besitzt.

━━━━━━━━━━━━━━━━━━━━━━━━ ◆ ━━━━━━━━━━━━━━━━━━━━━━━━

# 🎛️ Eingabegeräte

| Die aktuellen Profile verwenden folgende Grundzuordnung: |
|---|

| Port | Standard |
|---|---|
| Port 1 | Maus |
| Port 2 | Keyboard-Mapping |

- Dies ist besonders für Titel wie **Arkanoid** und **Cannon Fodder** sinnvoll, bei denen die Maus eine zentrale Rolle spielen kann.
  - Bei anderen Spielen kann die Belegung in WinUAE jederzeit angepasst werden.

```text
Game Ports
├─ Port 1 → Mouse
└─ Port 2 → Keyboard / Joystick Mapping
```

> [!TIP]
> Ein physischer USB-Controller oder Joystick kann in WinUAE nach dem Laden der Config zusätzlich ausgewählt werden, ohne die grundlegenden Hardwareparameter des Profils verändern zu müssen.

━━━━━━━━━━━━━━━━━━━━━━━━ ◆ ━━━━━━━━━━━━━━━━━━━━━━━━

# 🧠 Warum eigene Profile pro Spiel?

| Die Amiga-Plattform existierte über viele Jahre in zahlreichen Hardwarevarianten. |
|---|

- Ein Titel kann beispielsweise für folgende Bedingungen entwickelt worden sein:
  - Motorola 68000
  - OCS
  - 512 KB Chip RAM
  - 512 KB Slow RAM
  - Kickstart 1.2 oder 1.3
  - PAL-Timing
  - bestimmtes Blitter-Verhalten

| Ein anderer Titel kann dagegen: |
|---|

- 1 MB Chip RAM bevorzugen
- ECS-Komponenten verwenden
- mehrere Diskettenlaufwerke unterstützen
- mit abweichenden CPU-Timings reagieren
- eine bestimmte Maus- oder Joystickbelegung benötigen

| Deshalb gilt für dieses Projekt: |
|---|

> **Eine funktionierende WinUAE-Konfiguration ist nicht automatisch die optimale Konfiguration für jedes Spiel.**

━━━━━━━━━━━━━━━━━━━━━━━━ ◆ ━━━━━━━━━━━━━━━━━━━━━━━━

# ⏱️ Cycle Exact und JIT

## Cycle Exact

| Bei allen aktuellen klassischen Spieleprofilen sind folgende Optionen aktiviert: |
|---|

```ini
cpu_cycle_exact=true
cpu_memory_cycle_exact=true
blitter_cycle_exact=true
cycle_exact=true
```

| Dadurch orientiert sich WinUAE stärker am Timing realer Amiga-Hardware. |
|---|

### Vorteile

- höhere Timing-Treue
- bessere Kompatibilität mit hardwarenaher Software
- weniger Probleme durch übermäßig schnelle CPU-Emulation
- sinnvoll für klassische Diskettenspiele

## JIT

| JIT wird in den Spieleprofilen nicht verwendet. |
|---|

```ini
cachesize=0
```

| Das High-Performance-Profil verwendet dagegen: |
|---|

```ini
cachesize=8192
```

> [!NOTE]
> JIT ist hervorragend für leistungsorientierte Amiga-Konfigurationen mit geeigneten CPUs, aber nicht das primäre Ziel einer klassischen 68000-A500-Emulation.

━━━━━━━━━━━━━━━━━━━━━━━━ ◆ ━━━━━━━━━━━━━━━━━━━━━━━━

# 🧾 Projekt-Metadaten

```yaml
project:
  name: WinUAE Game Configurations
  language: Deutsch
  platform: Windows
  emulator: WinUAE
  target_system: Commodore Amiga
  primary_target: Amiga 500
  configuration_format: .uae

configs:
  total: 4

games:
  - The Great Giana Sisters
  - Cannon Fodder
  - Arkanoid
  - Wings of Fury

distribution:
  kickstart_roms: false
  adf_images: false
  game_files: false
  whdload_images: false
```

> Der Workflow ist bewusst einfach gehalten: **Config laden, eigene Medien zuweisen, starten.**

━━━━━━━━━━━━━━━━━━━━━━━━ ◆ ━━━━━━━━━━━━━━━━━━━━━━━━

# 🛠️ Fehlerbehebung

## Spiel startet nicht

- Prüfe zuerst:
  - Ist das richtige Kickstart-ROM vorhanden?
  - Wurde die richtige Config geladen?
  - Ist die ADF-Datei in DF0 eingelegt?
  - Handelt es sich um eine funktionierende Diskettenversion?
  - Wurde PAL versehentlich auf NTSC umgestellt?

---

## Schwarzer Bildschirm

- Mögliche Ursachen:
  - inkompatibles oder fehlendes Kickstart-ROM
  - defektes Diskettenabbild
  - falsche Diskette eingelegt
  - geänderte Chipset-Einstellung
  - abweichende Speicherbelegung
  - Timing-Optionen wurden verändert

> [!WARNING]
> Wenn ein Spiel mit der bereitgestellten Config funktioniert, sollten CPU-, RAM-, Chipset- und Cycle-Exact-Werte nicht ohne konkreten Grund verändert werden.

---

## Spiel läuft zu schnell

- Prüfe:
  - cpu_speed=real
  - cpu_model=68000
  - cachesize=0
  - cpu_cycle_exact=true


| Bei den bereitgestellten Spielprofilen sind diese Werte bereits entsprechend gesetzt. |
|---|

---

## Spiel ruckelt oder Audio stottert

> Das kann auch durch das Host-System entstehen.

- Prüfe:
  - Hintergrundprogramme
  - Audio-Puffer
  - Windows-Energiesparmodus
  - Grafiktreiber
  - VSync-Einstellungen
  - ungewöhnlich hohe Filter- oder Shader-Einstellungen

> [!NOTE]
> Cycle-Exact-Emulation kann mehr Rechenleistung benötigen als eine vereinfachte Emulation. Auf einem modernen PC sollte das bei einem A500-Profil normalerweise kein Problem darstellen.

---

## Cannon Fodder verlangt eine andere Diskette

Prüfe die Laufwerksbelegung:

```text
DF0 → Disk 1
DF1 → Disk 2
DF2 → Disk 3
```

> Falls deine konkrete Version keine zusätzlichen Laufwerke korrekt nutzt, können DF1 und DF2 deaktiviert und die Disketten manuell gewechselt werden.

━━━━━━━━━━━━━━━━━━━━━━━━ ◆ ━━━━━━━━━━━━━━━━━━━━━━━━

# ✅ Kompatibilitätsgrundsätze

- Bei neuen Configs sollten folgende Grundsätze gelten:
  - So wenig emulierte Zusatzhardware wie nötig
  - So viel RAM wie erforderlich, nicht pauschal so viel wie möglich
  - Passender Chipsatz statt grundsätzlich AGA
  - 68000 für klassische A500-Titel, sofern kein anderer Prozessor benötigt wird
  - JIT nur dort, wo es technisch sinnvoll ist
  - Cycle Exact für hardwarenahe klassische Spiele bevorzugen
  - PAL/NTSC entsprechend der vorgesehenen Version konfigurieren
  - Eingabegeräte an das jeweilige Spiel anpassen
  - Keine ROM- oder Spieldateien fest in veröffentlichte Configs eintragen
  - Jede Config separat dokumentieren

> [!IMPORTANT]
> **Mehr RAM + schnellere CPU = nicht automatisch bessere Emulation.**

━━━━━━━━━━━━━━━━━━━━━━━━ ◆ ━━━━━━━━━━━━━━━━━━━━━━━━

# 🔐 Was dieses Repository bewusst NICHT enthält

```diff
- Kickstart-ROMs
- ADF-Spieldateien
- IPF-Spieldateien
- WHDLoad-Spielpakete
- kommerzielle Software
- BIOS-/Firmware-Abbilder aus nicht freigegebenen Quellen
- Cracks oder Warez
```

Enthalten sind ausschließlich:

```diff
+ WinUAE-Konfigurationsdateien
+ technische Dokumentation
+ Konfigurationsvergleiche
+ Kompatibilitätshinweise
```

━━━━━━━━━━━━━━━━━━━━━━━━ ◆ ━━━━━━━━━━━━━━━━━━━━━━━━

# ⚖️ Rechtliche Hinweise

**Amiga**, **Commodore**, die jeweiligen Spielnamen sowie weitere Marken und Produktbezeichnungen können Marken oder geschützte Bezeichnungen ihrer jeweiligen Rechteinhaber sein.

| Dieses Repository ist ein unabhängiges Konfigurations- und Dokumentationsprojekt. |
|---|

- Es besteht keine offizielle Verbindung zu:
  - den Rechteinhabern der genannten Spiele
  - den Rechteinhabern der Amiga-Plattform
  - den Anbietern kommerzieller Kickstart-ROM-Pakete
  - dem WinUAE-Projekt

> [!CAUTION]
> Die Bereitstellung einer Emulator-Konfiguration bedeutet nicht automatisch, dass dazugehörige ROM- oder Spielabbilder frei verteilt werden dürfen.

━━━━━━━━━━━━━━━━━━━━━━━━ ◆ ━━━━━━━━━━━━━━━━━━━━━━━━

# 🧪 Konfigurationsphilosophie

```text
ORIGINALNÄHE
     │
     ├── CPU
     ├── CHIPSET
     ├── RAM
     ├── TIMING
     ├── INPUT
     └── KICKSTART
          │
          ▼
   SPIELKOMPATIBILITÄT
```

> **Die optimale Emulation entsteht nicht durch maximale Werte, sondern durch passende Werte.**

━━━━━━━━━━━━━━━━━━━━━━━━ ◆ ━━━━━━━━━━━━━━━━━━━━━━━━

# 📊 Aktueller Projektstatus

| Bereich | Status |
|---|---|
| Repository-Konzept | 🟢 Bereit |
| README | 🟢 Bereit |
| Giana Sisters | 🟢 Config vorhanden |
| Cannon Fodder | 🟢 Config vorhanden |
| Arkanoid | 🟢 Config vorhanden |
| Wings of Fury | 🟢 Config vorhanden |
| Kickstart-ROMs | 🔴 Nicht enthalten |
| Spiele / ADF-Dateien | 🔴 Nicht enthalten |
| Open-Source-Lizenz | 🔴 Nicht vergeben |
| Erweiterung um weitere Spiele | 🟡 Geplant |

━━━━━━━━━━━━━━━━━━━━━━━━ ◆ ━━━━━━━━━━━━━━━━━━━━━━━━

# 💡 Kurzfassung

> [!NOTE]
> **WinUAE Game Configurations** stellt vorkonfigurierte `.uae`-Profile für klassische Amiga-Spiele bereit.

- Jede Config ist auf ein konkretes Spiel zugeschnitten.
- Klassische A500-Profile verwenden einen 68000.
- JIT ist bei diesen Profilen deaktiviert.
- Cycle Exact ist aktiviert.
- OCS oder ECS wird passend zum Profil verwendet.
- Kickstart 1.3 ist für die aktuellen Profile vorgesehen.
- ROMs und Spieldateien werden nicht mitgeliefert.
- Das Repository besitzt aktuell keine Open-Source-Lizenz.

━━━━━━━━━━━━━━━━━━━━━━━━ ◆ ━━━━━━━━━━━━━━━━━━━━━━━━

<div align="center">

## 🕹️ WINUAE GAME CONFIGURATIONS

**CLASSIC AMIGA // PRECISE CONFIGURATION // CLEAN EMULATION**

`68000` • `OCS` • `ECS` • `PAL` • `CYCLE EXACT` • `A500`

━━━━━━━━━━━━━━━━━━━━━━━━ ◆ ━━━━━━━━━━━━━━━━━━━━━━━━

</div>
