# 💰 Budget Tracker

Una moderna applicazione web per la gestione delle finanze personali con supporto cloud tramite PocketBase.

## 📋 Indice

- [Descrizione](#descrizione)
- [Caratteristiche Principali](#caratteristiche-principali)
- [Requisiti Funzionali](#requisiti-funzionali)
- [Requisiti Non Funzionali](#requisiti-non-funzionali)
- [Tecnologie Utilizzate](#tecnologie-utilizzate)
- [Installazione](#installazione)
- [Configurazione](#configurazione)
- [Utilizzo](#utilizzo)
- [Struttura del Progetto](#struttura-del-progetto)
- [Contribuire](#contribuire)
- [Licenza](#licenza)

## 🎯 Descrizione

Budget Tracker è un'applicazione web responsive progettata per aiutare gli utenti a gestire le proprie finanze personali in modo semplice ed efficace. L'app supporta sia l'utilizzo offline con localStorage che la sincronizzazione cloud tramite autenticazione PocketBase.

## ✨ Caratteristiche Principali

### 🔐 Gestione Utenti
- Autenticazione con PocketBase (registrazione e login)
- Modalità offline con localStorage
- Sincronizzazione automatica dei dati al login
- Gestione profilo utente

### 💳 Gestione Transazioni
- Registrazione entrate e uscite
- Categorizzazione automatica
- Visualizzazione cronologica
- Statistiche per categoria
- Report mensili dettagliati

### 🏦 Gestione Carte
- Supporto carte di credito e debito
- Monitoraggio limite di credito
- Tracciamento spese mensili
- Personalizzazione colori e icone
- Calcolo percentuale utilizzo

### 📊 Dashboard e Statistiche
- Visualizzazione saldo totale
- Grafici entrate/uscite
- Distribuzione spese per categoria
- Report mensili
- Statistiche carte attive

### 🎨 Interfaccia Utente
- Design mobile-first responsive
- Tema moderno con gradiente viola-blu
- Animazioni fluide
- Icone intuitive
- Esperienza utente ottimizzata

## 📝 Requisiti Funzionali

### RF1 - Gestione Utenti
Il sistema deve permettere agli utenti di autenticarsi tramite registrazione e login, mantenere sessioni attive e supportare l'utilizzo sia in modalità autenticata (con sincronizzazione cloud) che in modalità offline (con storage locale).

### RF2 - Gestione Transazioni Finanziarie
L'applicazione deve consentire la creazione, visualizzazione e organizzazione di transazioni finanziarie. Ogni transazione deve contenere informazioni essenziali come importo, tipo (entrata/uscita), categoria di appartenenza e data. Il sistema deve calcolare automaticamente i saldi e fornire visualizzazioni ordinate cronologicamente.

### RF3 - Sistema di Categorizzazione
Il sistema deve implementare un meccanismo di categorizzazione delle spese con categorie predefinite identificabili visivamente. Deve essere in grado di aggregare e calcolare totali per categoria, fornendo statistiche sulle principali aree di spesa.

### RF4 - Gestione Strumenti di Pagamento
L'applicazione deve permettere la gestione di diversi strumenti di pagamento (carte di credito e debito) con le relative informazioni identificative, limiti e saldi. Il sistema deve monitorare l'utilizzo di ciascuno strumento e fornire statistiche aggregate.

### RF5 - Reporting e Analisi
Il sistema deve generare report periodici che mostrano andamento finanziario, distribuzione delle spese e statistiche comparative. Deve calcolare metriche finanziarie significative e presentarle in forma comprensibile.

### RF6 - Persistenza e Sincronizzazione Dati
L'applicazione deve garantire la persistenza dei dati sia localmente che su cloud, gestendo automaticamente la sincronizzazione tra i due sistemi quando disponibile. Deve supportare la migrazione dei dati tra modalità offline e online.

### RF7 - Interfaccia e Navigazione
Il sistema deve fornire un'interfaccia organizzata in sezioni logiche facilmente navigabili, con accesso rapido alle funzionalità principali e visualizzazione chiara dello stato finanziario corrente.

## ⚙️ Requisiti Non Funzionali

### RNF1 - Usabilità
L'interfaccia deve essere intuitiva e facilmente comprensibile per utenti di diversi livelli di competenza tecnica. Il design deve seguire principi di user experience consolidati, con azioni principali facilmente accessibili e feedback immediato sulle operazioni effettuate.

### RNF2 - Performance
L'applicazione deve garantire tempi di risposta rapidi per tutte le operazioni, con caricamento iniziale ottimizzato e interazioni fluide. Le operazioni di lettura e scrittura dati devono essere efficienti e non bloccare l'interfaccia utente.

### RNF3 - Portabilità e Compatibilità
Il sistema deve funzionare correttamente su diverse piattaforme (desktop e mobile) e browser moderni, mantenendo consistenza nell'esperienza utente. Deve adattarsi a diverse risoluzioni di schermo garantendo leggibilità e usabilità.

### RNF4 - Sicurezza
I dati degli utenti devono essere protetti attraverso meccanismi di autenticazione sicuri e gestione appropriata delle sessioni. Le informazioni sensibili devono essere trattate con adeguate misure di protezione sia lato client che server.

### RNF5 - Affidabilità e Disponibilità
L'applicazione deve essere resiliente, garantendo la continuità del servizio anche in caso di problemi di connettività. I dati devono essere persistenti e recuperabili, con meccanismi di fallback che permettano l'utilizzo offline.

### RNF6 - Manutenibilità
Il codice deve essere organizzato in modo modulare, seguendo best practice e standard di sviluppo. La struttura del progetto deve facilitare l'aggiunta di nuove funzionalità e la correzione di eventuali problemi.

### RNF7 - Scalabilità
L'architettura deve supportare la crescita del numero di utenti e del volume di dati senza degradazione significativa delle performance. Il sistema deve gestire efficacemente grandi quantità di transazioni mantenendo tempi di risposta accettabili.

### RNF8 - Accessibilità
L'interfaccia deve rispettare standard di accessibilità, con contrasti adeguati, elementi interattivi di dimensioni appropriate e comunicazione chiara degli errori e delle conferme.

## 🛠️ Tecnologie Utilizzate

### Frontend
- **React 18.x** - Libreria UI
- **JavaScript ES6+** - Linguaggio di programmazione
- **CSS3** - Styling con Flexbox e Grid
- **HTML5** - Markup semantico

### Backend & Database
- **PocketBase** - Backend as a Service
- **localStorage** - Storage locale per modalità offline

### Build & Development
- **Vite** - Build tool e dev server
- **npm** - Package manager

## 📦 Installazione

### Prerequisiti
- Node.js >= 16.x
- npm >= 8.x
- PocketBase (opzionale, per funzionalità cloud)

### Passaggi

1. **Clona il repository**
```bash
git clone https://github.com/tuousername/budget-tracker.git
cd budget-tracker
```

2. **Installa le dipendenze**
```bash
npm install
```

3. **Configura le variabili d'ambiente** (opzionale)
```bash
cp .env.example .env
```

Modifica `.env` con le tue configurazioni PocketBase:
```
VITE_POCKETBASE_URL=http://localhost:8090
```

4. **Avvia il server di sviluppo**
```bash
npm run dev
```

5. **Apri il browser**
```
http://localhost:5173
```

## ⚙️ Configurazione

### Setup PocketBase (Opzionale)

1. Scarica PocketBase da [pocketbase.io](https://pocketbase.io)
2. Avvia PocketBase:
```bash
./pocketbase serve
```
3. Accedi a `http://localhost:8090/_/`
4. Crea le seguenti collection:

**Collection: transactions**
- Importo (number)
- Categoria (text)
- Data (date)
- Intestatario (text)
- tipo (text)
- user (relation)

**Collection: cards**
- nome (text)
- tipo (text)
- numero (text)
- scadenza (text)
- limite (number)
- saldo (number)
- spesaMensile (number)
- colore (text)
- icona (text)
- user (relation)

## 🚀 Utilizzo

### Modalità Offline
1. Apri l'app senza autenticazione
2. Tutti i dati vengono salvati in localStorage
3. Le funzionalità base sono completamente disponibili

### Modalità Cloud
1. Clicca su "Accedi / Registrati"
2. Crea un account o accedi
3. I dati vengono sincronizzati con PocketBase
4. Accedi da qualsiasi dispositivo

### Aggiungere una Transazione
1. Clicca sul pulsante "+" centrale
2. Compila il form (descrizione, importo, tipo, categoria, data)
3. Conferma l'aggiunta

### Gestire le Carte
1. Vai alla sezione "Carte" dalla quick action
2. Clicca "+ Aggiungi Carta"
3. Personalizza colore, icona e dettagli
4. Monitora il saldo e l'utilizzo

### Visualizzare Report
1. Clicca su "Report" nella quick action
2. Visualizza statistiche mensili
3. Analizza la distribuzione delle spese

## 📁 Struttura del Progetto

```
budget-tracker/
├── public/
│   └── favicon.ico
├── src/
│   ├── components/
│   │   ├── AuthModal.jsx      # Modal autenticazione
│   │   └── ...
│   ├── hooks/
│   │   └── usePocketBase.js   # Hook per PocketBase
│   ├── App.jsx                # Componente principale
│   ├── App.css                # Stili principali
│   ├── Carte.jsx              # Gestione carte
│   ├── index.css              # Stili globali
│   └── main.jsx               # Entry point
├── .env.example               # Template variabili ambiente
├── package.json
├── vite.config.js
└── README.md
```

## 🤝 Contribuire

I contributi sono benvenuti! Segui questi passaggi:

1. Fai un fork del progetto
2. Crea un branch per la tua feature (`git checkout -b feature/AmazingFeature`)
3. Committa le modifiche (`git commit -m 'Add some AmazingFeature'`)
4. Pusha al branch (`git push origin feature/AmazingFeature`)
5. Apri una Pull Request

### Linee Guida
- Segui lo stile del codice esistente
- Aggiungi commenti significativi
- Testa le modifiche prima del commit
- Aggiorna la documentazione se necessario

## 📄 Licenza

Questo progetto è distribuito sotto licenza MIT. Vedi il file `LICENSE` per maggiori dettagli.
