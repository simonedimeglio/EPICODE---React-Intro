# REACT INTRO

## Differenza tra Libreria e Framework

Una libreria è come una scatola di attrezzi. Ti offre una serie di strumenti (funzioni, metodi, ecc.) che puoi usare per fare determinate cose. Sei tu a decidere come e quando usare quegli strumenti nel tuo progetto.

**React** è una libreria perché ti fornisce strumenti per costruire interfacce utente, ma sei tu a controllare come strutturare l’applicazione e cosa usare.

Un framework è più simile a una casa prefabbricata con un progetto già impostato. Ti dice come organizzare il tuo codice e offre un’architettura rigida.

Il framework prende il controllo e tu devi seguire le sue regole. Un esempio di framework è Angular o Vue.js, dove devi rispettare la struttura e il flusso imposto dal framework.

## Cosa è React?

React è una libreria JavaScript creata da Meta (_Facebook_), utilizzata per costruire interfacce utente (UI) in modo efficiente e interattivo. È particolarmente utile per creare applicazioni web moderne e dinamiche.

## Caratteristiche principali di React

- **Componenti**: React suddivide l’interfaccia utente in componenti riutilizzabili. Ogni componente è come un piccolo pezzo di un’applicazione (ad esempio, un pulsante, un modulo o una sezione di testo). Puoi combinare questi componenti per creare interfacce più grandi e complesse.
- **JSX**: React utilizza un linguaggio chiamato JSX che ti permette di scrivere HTML dentro JavaScript. Questo rende il codice più leggibile e ti consente di descrivere facilmente come dovrebbe apparire l’interfaccia utente.
- **Virtual DOM**: React usa il Virtual DOM per migliorare le prestazioni. Invece di aggiornare direttamente il DOM reale (che è più lento), React fa le modifiche nel Virtual DOM e poi aggiorna solo le parti necessarie del DOM reale. Questo rende l’applicazione più veloce e reattiva.
- **Stato**: rappresenta i dati che possono cambiare nel tempo e sono specifici di un componente.
- **Props**: sono i dati che vengono passati da un componente “genitore” a un componente “figlio” e sono immutabili (non possono essere modificati dal componente figlio).

## FOCUS - Componente

Un componente è come una funzione che dice a React cosa deve mostrare sullo schermo. Può essere un bottone, una lista, o un’intera pagina.

Ecco come fare un semplice componente che mostra un messaggio:

```jsx
function Saluto() {
  return <h1>Ciao, mondo!</h1>;
}
```

- `function Saluto()` crea un componente chiamato Saluto.
- `return <h1>Ciao, mondo!</h1>;` dice a React di mostrare questo messaggio.

### Per usare il componente

Una volta creato, puoi usare il componente Saluto come un normale tag HTML:

```jsx
function App() {
  return (
    <div>
      <Saluto />
    </div>
  );
}
```

> Dentro il return, usiamo `<Saluto />` per mostrare il nostro messaggio.

## FOCUS - Props

I Props sono come parametri che puoi passare a un componente per personalizzarlo:

```jsx
function Saluto(props) {
  return <h1>Ciao, {props.nome}!</h1>;
}

// Usare il componente con props
function App() {
  return (
    <div>
      <Saluto nome="Mario" />
      <Saluto nome="Luigi" />
    </div>
  );
}
```

- `props.nome` permette di passare un nome diverso al componente.
- `Saluto nome="Mario"` e `Saluto nome="Luigi"` mostrano messaggi personalizzati.

## FOCUS - Cartella progetto React

Quando crei un progetto con Create React App (CRA), viene generata una struttura di file e cartelle per aiutarti a iniziare rapidamente. Ecco una spiegazione semplice dei file e delle cartelle principali che vedrai:

- `node_modules`: Contiene tutte le dipendenze e i pacchetti installati tramite `npm`. Non devi modificare nulla qui. CRA gestisce questo per te.
- `public`: Questa cartella contiene i file che saranno accessibili pubblicamente. I file qui non vengono processati da Webpack (lo strumento che CRA usa per costruire l’app).
- `src`: Questa è la cartella principale dove scrivi il codice della tua applicazione.
- `index.js`: Il punto di ingresso dell’app. Qui React carica il componente principale (App.js) dentro il DOM.
- `App.js`: Il componente principale dell’app. Questo è il cuore della tua applicazione React.
- `App.css`: File CSS per stilizzare il componente App.
- `App.test.js`: File per i test del componente App (puoi rimuoverlo o modificarlo se non fai test).
- `logo.svg`: Un file SVG con il logo di React che viene mostrato per impostazione predefinita.
- `reportWebVitals.js`: Questo file è usato per misurare le prestazioni dell’app.
- `setupTests.js`: Configurazione per i test (usando Jest).
- `index.html`: La pagina HTML principale. React inserisce la tua applicazione dentro l’elemento `<div id="root"></div>`.
- `favicon.ico`: L’icona della scheda del browser.
- `manifest.json:`: Configura l’aspetto dell’app quando viene installata come una Web App su dispositivi mobili.
- `robots.txt:`: Dice ai motori di ricerca come indicizzare il sito.
- `package.json`: Contiene le informazioni sul progetto e le dipendenze. Importante per gestire pacchetti come React, React-DOM, ecc.
- `README.md`: Contiene le istruzioni su come avviare e sviluppare il progetto.
- `.gitignore`: Elenca i file e le cartelle che Git deve ignorare (come `node_modules/`).
- `package-lock.json`: Tiene traccia delle versioni esatte delle dipendenze installate.
