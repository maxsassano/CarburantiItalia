# 🚗 Carburanti Italia

App Android per consultare in tempo reale i **prezzi dei carburanti** in Italia, con ricerca per località o GPS, filtri avanzati, monitoraggio automatico e notifiche.

[![Android](https://img.shields.io/badge/Android-7.0%2B-green?logo=android)](https://www.android.com)
[![.NET MAUI](https://img.shields.io/badge/.NET%20MAUI-10-blue?logo=dotnet)](https://learn.microsoft.com/dotnet/maui)
[![License](https://img.shields.io/badge/license-MIT-orange)](LICENSE)
[![Version](https://img.shields.io/badge/version-1.0%20beta-yellow)](https://github.com/maxsassano/CarburantiItalia/releases)

---

## ✨ Funzionalità

- 🔍 **Ricerca per località** — Regione → Provincia → Comune
- 📍 **Ricerca GPS** — distributori intorno a te
- 📏 **Raggio configurabile** — 5, 10, 20, 30, 50 o 100 km
- ⛽ **Filtri** — Benzina, Gasolio, GPL, Metano / Self, Servito, Tutti
- 💰 **Ordinamento per prezzo** — dal più economico in alto
- 🗺️ **Apertura in Google Maps** dalla scheda distributore
- 🔔 **Monitoraggio automatico** — notifiche quando trova prezzi sotto la soglia, anche ad app chiusa
- 📖 **Guida e Info** integrate
- 🇮🇹 **Completamente in italiano**, Material Design

---

## 📸 Screenshot

<p align="center">
  <img src="docs/screenshots/home.png" width="220" alt="Home">
  <img src="docs/screenshots/risultati.png" width="220" alt="Risultati">
  <img src="docs/screenshots/dettaglio.png" width="220" alt="Dettaglio">
  <img src="docs/screenshots/monitoraggio.png" width="220" alt="Monitoraggio">
</p>

*(Aggiungi gli screenshot nella cartella `docs/screenshots/` e aggiorna i percorsi)*

---

## 📥 Download

Scarica l'ultima versione:

👉 [**Releases →**](https://github.com/maxsassano/CarburantiItalia/releases/latest)

**Requisiti:**
- Android 7.0 (API 24) o superiore
- Connessione internet
- GPS (opzionale, per la ricerca per posizione)

**Installazione:**
1. Scarica `CarburantiItalia.apk`
2. Sul telefono: **Impostazioni → Sicurezza → Origini sconosciute** (attiva)
3. Apri l'APK → **Installa**
4. Apri **Carburanti Italia**

---

## 🚀 Come si usa

### Prima ricerca
1. Seleziona **Regione, Provincia, Comune** dai menu a tendina.
2. Scegli la **distanza** di ricerca.
3. Tocca **Cerca per località**.
4. In alternativa, tocca **Usa la mia posizione GPS**.

### Filtri
- **Carburante**: Benzina, Gasolio, GPL, Metano
- **Modalità**: Self, Servito, Tutti
- Tocca **Applica Filtri** per aggiornare la lista.

### Monitoraggio automatico
1. Attiva lo switch **Monitoraggio**.
2. Imposta la **soglia prezzo** (in €).
3. L'app girerà in background ogni 5 minuti.
4. Riceverai una **notifica** se trova un distributore sotto la soglia.

> ⚠️ Il monitoraggio in background consuma batteria: attivalo solo quando ti serve.

---

## 🏗️ Build da sorgente

### Requisiti
- **Visual Studio 2022/2026** con workload **.NET MAUI**
- **.NET 10 SDK**
- **Android SDK** (API 34)
- **JDK 17**

### Compilazione debug
```bash
git clone https://github.com/maxsassano/CarburantiItalia.git
cd CarburantiItalia
dotnet restore
dotnet build -f net10.0-android
