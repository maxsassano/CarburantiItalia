# 🚗 Carburanti Italia

App Android per consultare in tempo reale i **prezzi dei carburanti** in Italia.

[![Android](https://img.shields.io/badge/Android-7.0%2B-green)](https://www.android.com)
[![Version](https://img.shields.io/badge/version-1.0-yellow)](https://github.com/maxsassano/CarburantiItalia/releases)
[![License](https://img.shields.io/badge/license-MIT-orange)](LICENSE)

---

## ✨ Funzionalità

- 🔍 Ricerca per **località** (Regione → Provincia → Comune)
- 📍 Ricerca per **posizione GPS** con raggio configurabile (5-100 km)
- ⛽ Filtri: **Benzina, Gasolio, GPL, Metano** — Self, Servito, Tutti
- 💰 Risultati **ordinati per prezzo crescente**
- 🏷️ **Logo e bandiera** dei distributori
- 📞 Contatti **tappabili** (chiama, email, sito web)
- 🗺️ **Mappa** + **Navigazione** con Google Maps
- 🕒 **Orari di apertura** + badge **APERTO / CHIUSO**
- 🏢 Servizi disponibili (Bancomat, Autolavaggio, Bar…)
- 🔔 **Monitoraggio automatico** con notifiche in background
- 📖 Guida e Info integrate

---

## 📸 Screenshot

![Home](Screen/home.png)
![Risultati](Screen/dettagli.png)
![Dettaglio](Screen/ricerca.png)
![Monitoraggio](Screen/mappa.png)

---

## 📥 Download

👉 [**Scarica l'ultima versione**](https://github.com/maxsassano/CarburantiItalia/releases/latest)

**Requisiti:** Android 7.0 (API 24) o superiore, connessione internet, GPS (opzionale)

**Installazione:**
1. Scarica `CarburantiItalia.apk`
2. Sul telefono: **Impostazioni → Sicurezza → Origini sconosciute** (attiva)
3. Apri l'APK → **Installa**

---

## 🚀 Come si usa

**Prima ricerca**
1. Seleziona **Regione, Provincia, Comune**
2. Scegli la **distanza** (5-100 km)
3. Tocca **Cerca per località** oppure **Usa la mia posizione GPS**

**Filtri** — Carburante, Modalità (Self/Servito/Tutti) → **Applica Filtri**

**Dettaglio distributore** — Tocca una scheda per vedere:
- Prezzi completi di tutti i carburanti
- Orari di apertura
- Servizi disponibili
- Contatti tappabili (chiama, email, sito)
- Pulsanti Mappa e Naviga

**Monitoraggio** — Attiva lo switch, imposta la **soglia prezzo**. L'app girerà in background ogni 5 minuti e ti avviserà se trova un distributore sotto la soglia. Funziona anche ad app chiusa.

> ⚠️ Il monitoraggio in background consuma batteria.

---

## 🔌 Fonte dati

Tutti i prezzi provengono dall'**API pubblica del MIMIT** — Osservaprezzi Carburanti:
👉 https://carburanti.mise.gov.it

L'app **non è affiliata** al MIMIT né a marchi di carburante.

---

## 🏗️ Build da sorgente

### Requisiti
- Visual Studio 2022/2026 con workload **.NET MAUI**
- .NET 10 SDK
- Android SDK (API 34)
- JDK 17

### Compilazione APK arm64 (telefono)
```bash
dotnet publish -f net10.0-android -c Release \
  -p:AndroidPackageFormat=apk \
  -p:RuntimeIdentifier=android-arm64 \
  -p:AndroidKeyStore=true \
  -p:AndroidSigningKeyStore="percorso\keystore.keystore" \
  -p:AndroidSigningKeyAlias=alias \
  -p:AndroidSigningKeyPass=password \
  -p:AndroidSigningStorePass=password
