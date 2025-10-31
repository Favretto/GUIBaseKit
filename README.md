# 🧩 GUIBaseKit

**Progetto base Win32 / VC++**  
**Autore:** Alessandro Favretto  
**Versione:** 1.0 — *25 ottobre 2025*

---

## 💡 Descrizione

**GUIBaseKit** è un progetto *base framework* per la creazione di applicazioni **Win32 in Visual C++**, pensato come punto di partenza per sviluppare GUI native, leggere e indipendenti da framework esterni (MFC, .NET, ecc.).  
Offre una struttura commentata e modulare, già dotata delle funzioni essenziali per applicazioni reali su Windows 10 e 11.

---

## ⚙️ Funzionalità principali

### 🪟 Gestione finestra
- Parametri configurabili:
  - `StartMinimized` → avvio ridotto a icona  
  - `MinimizeOnTNR` → minimizzazione nella **Tray Notification Region (TNR)**
- Opzione **Sempre in primo piano**
- Rilevamento esecuzione **con privilegi amministrativi**

### ⏱️ Timer principale
- Timer interno (500 ms) con label che mostra **data e ora aggiornate in tempo reale**

### 🧰 Gestione Tray Icon
- Icona nella system tray con tooltip personalizzato  
- Doppio click → ripristina la finestra  
- Click destro → menu rapido con comandi (“Apri GUI”, “Info”, “Esci”)

### 🚫 Istanza singola
- Controllo tramite `Mutex` nominato (`MyApp_Mutex_SingleInstance`)  
  → impedisce l’esecuzione multipla dell’applicazione

---

## 🧱 Elementi GUI dimostrativi
- **Label statiche** con colori personalizzati  
- **Button** con evento `CLICK` intercettato e cambio cursore dinamico  
- **Textbox multilinea** readonly con scrollbar verticale  
- **Menu a tendina** multilivello (“Vai a…”, “Finestra”, “?”)  
- **Disegno GDI** di un rettangolo con pattern obliquo e bordo Navy  

---

## 🧩 Integrazione Shell
- Apertura diretta di cartelle notevoli:

---

## 🎨 Aspetto grafico
- Finestra centrata automaticamente sullo schermo  
- Sfondo con **pattern obliquo** e bordo color Navy  
- Font personalizzato: `Courier New`, 15px, *italic*  
- Interfaccia pulita e immediata, ideale per test GUI o tool standalone

---

## 🧾 Architettura e codice

| Modulo | Descrizione |
|--------|-------------|
| `WinMain()` | Inizializzazione, setup GUI e ciclo messaggi |
| `WndProc()` | Gestione eventi finestra, comandi e tray |
| `SetAlwaysOnTop()` | Imposta o rimuove il comportamento topmost |
| `IsRunningAsAdmin()` | Rileva se il processo è avviato come amministratore |

---

## 🚀 Obiettivi del progetto
GUIBaseKit nasce come base di partenza per:
- creare **utility Win32 standalone**;
- integrare **interfacce native** senza framework aggiuntivi;
- fornire un **codice leggibile, commentato e facilmente estendibile**;
- mantenere **leggerezza e portabilità** su sistemi Windows moderni.

---

## 🧭 Possibili estensioni
- Logging eventi su file di testo  
- Integrazione MQTT / socket per diagnostica  
- Notifiche balloon o badge dinamici  
- Skin e temi personalizzabili  

---

## 🪶 Licenza
Questo progetto è distribuito liberamente per scopi educativi e sperimentali.  
© 2025 — *Alessandro Favretto*

