# Registro Presenze GOL (con Audit Forense)

> Un applicativo desktop Python/PyQt per la gestione dei registri formativi, progettato con un focus sulla sicurezza, la conformità e l'immodificabilità dei dati (valore probatorio).

---

## 💡 Il Problema (Perché questo progetto?)

La gestione dei registri formativi (come quelli per i corsi GOL) tramite fogli di calcolo (es. Excel) presenta enormi problemi di sicurezza e validità legale:
* **Manipolazione:** I dati possono essere alterati in qualsiasi momento senza lasciare traccia.
* **Mancanza di Prove:** È impossibile dimostrare in modo inconfutabile che una presenza sia stata registrata in una data specifica.
* **Inefficienza:** La creazione di report, il calcolo delle ore e la gestione degli argomenti sono processi manuali e lenti.

## 🚀 La Soluzione (Cosa fa il progetto?)

Ho sviluppato **Registro GOL**, un'applicazione desktop che trasforma il registro da un semplice foglio di calcolo a un sistema di archiviazione sicuro e **con valore probatorio**.

L'applicazione non si limita a salvare le presenze, ma implementa un **sistema forense** che "blinda" i dati una volta inseriti.

## 🎥 Demo Video


**[Guarda la Demo su YouTube] (link-demo-youtube)**

## 🛠️ Tecnologie Utilizzate (Skills Dimostrate)

* **Linguaggio:** Python
* **GUI:** PyQt6 (interfaccia a schede, griglie complesse, menu contestuali) 
* **Database:** SQLite
* **Sicurezza & Crittografia:** `hashlib` (per la creazione dell'hash-chain dell'audit log)
* **Invio Email:** `smtplib` e `ssl` (per l'integrazione sicura con Gmail tramite "Password per le App")
* **Reporting:** Generazione di PDF e CSV

## 🔑 Caratteristiche Principali (Dal Manuale Utente )

Questa applicazione va ben oltre la semplice registrazione, includendo tre livelli di sicurezza:

### 1. Livello Forense (Valore Probatorio)
* **Audit Log Immutabile:** Ogni singola azione (creazione corso, modifica presenza) viene registrata in un log "blockchain-like", dove ogni record è legato al precedente da un hash crittografico.
* **Verifica Integrità:** Uno strumento per verificare che la catena di hash non sia *mai* stata spezzata, garantendo che il database non sia stato manomesso.
* **Firma Digitale Lezioni:** I docenti possono "firmare" (bloccare) una lezione conclusa, impedendo qualsiasi modifica o cancellazione futura.

### 2. Livello di Automazione (Efficienza)
* **Report PDF via Email:** Funzionalità per inviare un report PDF del registro a un server esterno (es. Gmail) 
Questo crea una **prova temporale esterna** (timestamp di Google) che certifica lo stato del registro in quella data e ora.
* *Gestione Corsi Multi-Scheda:** Interfaccia intuitiva per gestire più corsi contemporaneamente, ognuno nella sua scheda.
* **Calcolo Automatico Ore:** Calcola automaticamente le ore di lezione dagli orari inseriti.

### 3. Livello Operativo (Gestione Completa)
* **Gestione Anagrafiche:** CRUD completo per Corsi, Corsisti e Lezioni.
* **Registrazione Rapida:** Inserimento presenze sia da tastiera (codici `P`, `A`, `AG`, `R`) sia da menu contestuale.
* **Reporting Completo:** Esportazione di PDF (A3/A4), CSV, Registro Argomenti e Attestati di Frequenza individuali.
* **Gestione Documentale:** Sezione per allegare file e annotazioni a ogni corso.

## 📜 Licenza e Proprietà

**© 2025 Dmitrij Musella - Tutti i diritti riservati.**

Il codice sorgente di questo progetto è **privato** e non può essere copiato, modificato o distribuito senza esplicito consenso scritto da parte dell'autore.

Le demo video sono fornite a solo scopo dimostrativo del portfolio.


> Developed with AI-assisted coding tools (Claude/Anthropic)
