# NOTE E APPUNTI DI VueJS


## FEDERICO AIROLDI


### 22-04-2023



---
___


## GETTING START

Per iniziare a usare VueJS, ci sono diversi modi possibili. Alcuni dei più comuni sono:

- Usare la CDN di VueJS per includere lo script di VueJS nel tuo codice HTML12. Questo è il modo più semplice e veloce per provare VueJS senza una fase di build.
<br>
- Usare npm per installare VueJS come una dipendenza del tuo progetto34. Questo ti permette di usare VueJS con un sistema di moduli e un bundler come webpack o rollup.
<br>
- Usare Vue CLI per creare e configurare il tuo progetto VueJS12. Questo ti offre una serie di strumenti e opzioni per personalizzare il tuo ambiente di sviluppo, come il supporto per TypeScript, ESLint, PWA, unit testing e altro.

---

## COME RICHIAMARE VueJS in HTML

**RICHIMARE NEL HEAD HTML I FILE JS E LA LIBRERIA CDN DI VUE**

```HTML
<head>
    <!-- VuejS -->
    <script src="https://unpkg.com/vue@3" defer></script>
    
    <!-- Javascript -->
    <script src="./asset/js/main.js" defer></script>
</head>
```
**NEL BODY HTML DOVVIAMO INSERIRE IL DIV CON ID UNIVOCO A CUI FARÀ RIFERIMENTO VUE**

```HTML
<body>
    <div id="app">

        <main>

            
        </main>

    </div>
</body>
```
**NEL FILE JS INVECE AVREMO UNA STRUTTURA BASE DI VUE**

```JS
const { createApp } = Vue

createApp({

  // VARIABILI VUE
  data() {
    return {
      



    }
  },

  //chiamata function al caricamento della pagina
  created(){
    
  },

  // FUNZIONI VUE
  methods: {



  }

}).mount('#app')
```
---

## HOOK E CICLO DI VITA DI Vue

Ogni istanza di componente Vue passa attraverso una serie di passaggi di inizializzazione quando viene creata - ad esempio, deve impostare l'osservazione dei dati, compilare il template, montare l'istanza sul DOM e aggiornare il DOM quando i dati cambiano. Lungo il percorso, esegue anche funzioni chiamate hook del ciclo di vita, dando agli utenti l'opportunità di aggiungere il proprio codice in specifiche fasi¹.

Ci sono diversi hook del ciclo di vita che vengono chiamati in diverse fasi del ciclo di vita dell'istanza, tra cui i più comunemente utilizzati sono `mounted`, `updated` e `unmounted`. Tutti gli hook del ciclo di vita vengono chiamati con il loro contesto `this` che punta all'istanza attiva corrente che lo invoca¹.

### HOOK

Gli hook del ciclo di vita disponibili in Vue.js sono i seguenti:
- `beforeCreate`: chiamato quando l'istanza viene inizializzata, dopo la risoluzione delle proprietà, prima di elaborare altre opzioni come `data()` o `computed`.
- `created`: chiamato dopo che l'istanza ha finito di elaborare tutte le opzioni relative allo stato.
- `beforeMount`: chiamato subito prima che il componente venga montato.
- `mounted`: chiamato dopo che il componente è stato montato.
- `beforeUpdate`: chiamato subito prima che il componente stia per aggiornare il suo albero DOM a causa di un cambiamento dello stato reattivo.
- `updated`: chiamato dopo che il componente ha aggiornato il suo albero DOM a causa di un cambiamento dello stato reattivo.
- `beforeUnmount`: chiamato subito prima che il componente venga smontato.
- `unmounted`: chiamato dopo che il componente è stato smontato.

---

## DICHIARAZIONE DELLE VARIABILI E INTERPOLAZIONE DEL TESTO

In Vue.js, puoi dichiarare le variabili all'interno dell'oggetto `data` quando crei un nuovo oggetto Vue o un componente Vue. L'oggetto `data` deve essere una funzione che restituisce un oggetto contenente le variabili che vuoi dichiarare.

Ecco un esempio di come dichiarare una variabile chiamata `message` all'interno di un nuovo oggetto Vue:
```javascript
...struttura Vue

  data: function() {
    return {
      message: 'Ciao Vue!'
    }
  }

...struttura Vue
```
In questo esempio, abbiamo dichiarato una variabile chiamata `message` e le abbiamo assegnato il valore `'Ciao Vue!'`. Ora puoi utilizzare questa variabile all'interno del tuo template HTML utilizzando l'interpolazione del testo:
```html
<div id="app">
  <h1>{{ message }}</h1>
</div>
```
In questo esempio, il tag mustache verrà sostituito con il valore della proprietà `message` sull'oggetto dati corrispondente.

## DICHIARAZIONE DELLE FUNZIONI
In Vue.js, puoi scrivere funzioni all'interno dell'oggetto `methods` quando crei un nuovo oggetto Vue o un componente Vue. L'oggetto `methods` contiene le funzioni che possono essere chiamate dall'interno del tuo template HTML o da altre funzioni all'interno del tuo componente.

Ecco un esempio di come scrivere una funzione chiamata `myFunction` all'interno di un nuovo oggetto Vue:
```javascript
...struttura Vue
methods: {
    myFunction: function() {
        console.log('Questa è la mia funzione!');
    }
}
...struttura Vue
```
In questo esempio, abbiamo scritto una funzione chiamata `myFunction` all'interno dell'oggetto `methods`. Questa funzione può essere chiamata dall'interno del tuo template HTML utilizzando un gestore di eventi come `v-on:click` o dalla tua istanza Vue utilizzando `this.myFunction()`.


---

## COME MANIPOLARE IL DOM CON LE DIRETTIVE VUE

Le direttive sono attributi speciali con il prefisso `v-` che indicano a Vue.js di fare qualcosa a un elemento DOM. Vue.js viene fornito con un set di direttive predefinite che puoi utilizzare subito. Alcune delle direttive predefinite più comuni sono:
<br>
- `v-model`: Crea un collegamento bidirezionale tra il valore dell'input del form e i dati dell'istanza Vue.
- `v-bind`: Associa dinamicamente uno o più attributi o una proprietà di componente a un'espressione.
- `v-for`: Rende un elenco di elementi basato su un array o un oggetto.
- `v-text`: Aggiorna il contenuto del testo dell'elemento.
- `v-html`: Aggiorna l'innerHTML dell'elemento.
- `v-show`: Alterna la visibilità dell'elemento in base alla veridicità del valore dell'espressione.
- `v-if`: Rende condizionalmente un elemento o un frammento di template in base alla veridicità del valore dell'espressione.
- `v-else`: Denota il "blocco else" per `v-if` o una catena `v-if` / `v-else-if`.
- `v-else-if`: Denota il "blocco else if" per `v-if`. Può essere concatenato.

Inoltre, Vue.js ti consente anche di registrare le tue direttive personalizzate se hai bisogno di una funzionalità che non è coperta dalle direttive predefinite.

---

### V-MODEL

La direttiva `v-model` in Vue.js crea un collegamento bidirezionale tra il valore dell'input del form e i dati dell'istanza Vue. Ciò significa che quando l'utente modifica il valore dell'input del form, il valore dei dati corrispondenti nell'istanza Vue viene aggiornato automaticamente e viceversa.

Ecco un esempio di come utilizzare la direttiva `v-model` per creare un collegamento bidirezionale tra un input di testo e una variabile chiamata `message`:
```html
<template>
  <div>
    <input type="text" v-model="message">
    <p>Il valore di message è: {{ message }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      message: ''
    }
  }
}
</script>
```
In questo esempio, quando l'utente digita qualcosa nell'input di testo, il valore della variabile `message` viene aggiornato automaticamente e visualizzato nel paragrafo sottostante.

### V-BIND

La direttiva `v-bind` in Vue.js ti consente di associare dinamicamente uno o più attributi o una proprietà di componente a un'espressione. Ad esempio, puoi utilizzare `v-bind` per associare dinamicamente il valore dell'attributo `src` di un'immagine al valore di una variabile.

Ecco un esempio di come utilizzare la direttiva `v-bind` per associare dinamicamente il valore dell'attributo `src` di un'immagine al valore di una variabile chiamata `imageSrc`:
```html
<template>
  <div>
    <img v-bind:src="imageSrc">
  </div>
</template>

<script>
export default {
  data() {
    return {
      imageSrc: 'https://picsum.photos/200'
    }
  }
}
</script>
```
In questo esempio, stiamo utilizzando la sintassi abbreviata `:src` al posto di `v-bind:src`. Quando il valore della variabile `imageSrc` cambia, il valore dell'attributo `src` dell'immagine viene aggiornato automaticamente.

### V-FOR

La direttiva `v-for` in Vue.js ti consente di rendere un elenco di elementi basato su un array o un oggetto. Ad esempio, puoi utilizzare `v-for` per generare un elenco di elementi `<li>` basato su un array di stringhe.

Ecco un esempio di come utilizzare la direttiva `v-for` per generare un elenco di elementi `<li>` basato su un array di stringhe:
```html
<template>
  <div>
    <ul>
      <li v-for="item in items" :key="item">{{ item }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: ['Mela', 'Arancia', 'Banana']
    }
  }
}
</script>
```
In questo esempio, stiamo utilizzando la direttiva `v-for` per generare un elemento `<li>` per ogni elemento nell'array `items`. Ogni elemento `<li>` visualizza il valore dell'elemento corrispondente nell'array `items`.

Nota che quando utilizzi `v-for` per rendere un elenco di elementi basato su un array o un oggetto, è consigliabile fornire una chiave univoca per ogni elemento utilizzando l'attributo `key`. In questo esempio, stiamo utilizzando il valore dell'elemento come chiave.

### V-IF V-ELSE-IF V-ELSE

Le direttive `v-if`, `v-else` e `v-else-if` in Vue.js ti consentono di rendere condizionalmente un elemento o un frammento di template in base alla veridicità del valore dell'espressione.

Ecco un esempio di come utilizzare le direttive `v-if`, `v-else` e `v-else-if` per rendere condizionalmente diversi elementi in base al valore di una variabile chiamata `value`:
```html
<template>
  <div>
    <div v-if="value === 'A'">Il valore è A</div>
    <div v-else-if="value === 'B'">Il valore è B</div>
    <div v-else>Il valore non è né A né B</div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      value: 'A'
    }
  }
}
</script>
```
In questo esempio, stiamo utilizzando la direttiva `v-if` per verificare se il valore della variabile `value` è uguale a `'A'`. Se è vero, viene visualizzato l'elemento `<div>` con il testo "Il valore è A".

Se la condizione `v-if` non è vera, viene valutata la condizione `v-else-if`. Se la condizione `v-else-if` è vera, viene visualizzato l'elemento `<div>` con il testo "Il valore è B".

Se nessuna delle condizioni `v-if` o `v-else-if` è vera, viene visualizzato l'elemento `<div>` con il testo "Il valore non è né A né B" utilizzando la direttiva `v-else`.

### V-SHOW

La direttiva `v-show` in Vue.js ti consente di alternare la visibilità di un elemento in base alla veridicità del valore dell'espressione. A differenza della direttiva `v-if`, che rimuove completamente l'elemento dal DOM quando la condizione non è vera, la direttiva `v-show` semplicemente alterna la proprietà CSS `display` dell'elemento tramite stili inline.

Ecco un esempio di come utilizzare la direttiva `v-show` per alternare la visibilità di un elemento in base al valore di una variabile booleana chiamata `show`:
```html
<template>
  <div>
    <button @click="show = !show">Mostra/Nascondi</button>
    <div v-show="show">Questo testo viene mostrato o nascosto</div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      show: true
    }
  }
}
</script>
```
In questo esempio, stiamo utilizzando la direttiva `v-show` per alternare la visibilità dell'elemento `<div>` in base al valore della variabile booleana `show`. Quando il valore di `show` è `true`, l'elemento `<div>` viene visualizzato. Quando il valore di `show` è `false`, l'elemento `<div>` viene nascosto.

Inoltre, stiamo utilizzando un gestore di eventi `@click` sul pulsante per alternare il valore della variabile booleana `show` quando l'utente fa clic sul pulsante.

### V-ON

La direttiva `v-on` in Vue.js ti consente di ascoltare gli eventi DOM e eseguire il codice quando si verificano. Puoi utilizzare `v-on` per aggiungere un gestore di eventi a un elemento specificando il tipo di evento da ascoltare e il codice da eseguire quando l'evento si verifica.

Ecco un esempio di come utilizzare la direttiva `v-on` per ascoltare l'evento `click` su un pulsante e aggiornare il valore di una variabile quando l'utente fa clic sul pulsante:
```html
<template>
  <div>
    <button v-on:click="incrementCount">Hai cliccato {{ count }} volte</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      count: 0
    }
  },
  methods: {
    incrementCount() {
      this.count++;
    }
  }
}
</script>
```
In questo esempio, stiamo utilizzando la direttiva `v-on` con l'argomento `click` per specificare che vogliamo ascoltare l'evento `click` sul pulsante. Quando l'utente fa clic sul pulsante, viene chiamato il metodo `incrementCount`, che incrementa il valore della variabile `count` di 1.

Nota che puoi anche utilizzare la sintassi abbreviata `@click` al posto di `v-on:click`.


---

## GESTORE DI EVENTI

In Vue.js, puoi utilizzare la direttiva `v-on` per ascoltare diversi tipi di eventi DOM. Ecco un elenco di alcuni eventi DOM comuni che puoi ascoltare utilizzando la direttiva `v-on`:

- `click`: si verifica quando l'utente fa clic su un elemento.
- `submit`: si verifica quando l'utente invia un modulo.
- `input`: si verifica quando l'utente modifica il valore di un input di testo o di una textarea.
- `change`: si verifica quando l'utente modifica il valore di un input, una textarea o un elemento select.
- `focus`: si verifica quando un elemento riceve il focus.
- `blur`: si verifica quando un elemento perde il focus.
- `keydown`: si verifica quando l'utente preme un tasto sulla tastiera.
- `keyup`: si verifica quando l'utente rilascia un tasto sulla tastiera.
- `mouseenter`: si verifica quando il puntatore del mouse entra nell'area di un elemento.
- `mouseleave`: si verifica quando il puntatore del mouse esce dall'area di un elemento.

Questi sono solo alcuni esempi di eventi DOM comuni che puoi ascoltare utilizzando la direttiva `v-on` in Vue.js. Ci sono molti altri eventi DOM disponibili e puoi trovare un elenco completo nella documentazione ufficiale del DOM.



---
---

# CODICE RICORRENTE

