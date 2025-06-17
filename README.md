# 📚 Generatore AI di Libri – HTML-Based + OpenAI API

Applicazione web standalone basata su HTML, CSS e JavaScript che consente la generazione automatica di libri completamente personalizzati tramite Intelligenza Artificiale. Grazie all'integrazione con l'API di OpenAI (modello GPT-4o), lo script costruisce dinamicamente la struttura del libro (capitoli, sezioni), genera l'indice e scrive i contenuti testuali in base a parametri definiti dall'utente.

L'interfaccia moderna e responsive guida l’utente nella definizione del progetto editoriale, mentre la logica interna si occupa di automatizzare l’intero flusso: dalla generazione dei titoli, all'elaborazione dei testi, fino all’esportazione del risultato in `.txt` o `.rtf`. Tutto funziona direttamente nel browser, senza necessità di backend o installazioni server-side.

## ✨ Funzionalità

- UI moderna con Bootstrap 5 e supporto mobile
- Input guidato con campi per:
  - Titolo del libro
  - Stile di scrittura (accademico, divulgativo, narrativo...)
  - Lingua (es. Italiano, Inglese)
  - Profilo del lettore (età, interessi, livello)
  - Obiettivi e preoccupazioni del lettore
  - Argomento principale
  - Numero totale di parole
- Calcolo automatico di:
  - Numero di capitoli
  - Numero di sezioni per capitolo
  - Parole per sezione
- Generazione dinamica dell’indice e dei contenuti con GPT-4o
- Log visivo di avanzamento per ogni fase
- Risultato esportabile in formato `.txt` o `.rtf`
- Sicurezza migliorata: offuscamento lato client della chiave API
- Nessuna dipendenza esterna oltre a OpenAI + Bootstrap (CDN)
- Completamente funzionante offline (dopo caricamento)

## 🚀 Requisiti

- Browser moderno (Chrome, Firefox, Edge)
- Chiave API OpenAI attiva (consigliato GPT-4o)

## 🔧 Come si usa

1. Inserisci la tua chiave API OpenAI (`sk-...`)
2. Compila i campi richiesti nel form
3. Clicca su **"Genera il Libro"**
4. Segui il progresso nella sezione log
5. Esporta il libro in `.txt` o `.rtf` con un clic

## 🛠 Architettura del codice

- **HTML/CSS**: struttura visiva + layout responsive
- **JavaScript (modulare)**:
  - `SecurityManager`: offuscamento e decodifica API Key
  - `LogManager`: gestione e visualizzazione dei log di avanzamento
  - `ResponseManager`: output dinamico dei contenuti generati
  - `APIManager`: interfaccia con `https://api.openai.com/v1/chat/completions`
  - `BookGenerator`: logica completa per analisi, struttura e generazione
  - `FormManager`: gestione dello stato UI e validazioni input
  - `TextProcessor`: supporto alla suddivisione dei testi
  - Funzioni `saveAsTxt()` e `saveAsRtf()` per esportazione locale

## 💻 Avvio locale

Puoi utilizzare il progetto localmente in pochi secondi copiando direttamnte il codice o salvandolo come file HTML.
