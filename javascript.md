
# NOTE E APPUNTI DI JAVASCRIPT


## FEDERICO AIROLDI


### 09-04-2023



---
___


## DOVE INSERIRE JAVASCRIPT

### SCRIPT TAG HTML
```js
<script>
document.getElementById("demo").innerHTML = "My First JavaScript";
</script>
```


### EXTERNAL FILE
```js
<script src="myScript.js"></script>
```
### EXTERNAL FILE EXECUTE LAST, DECLEAR IN HEAD
```js
<script src="./asset/js/main.js" defer></script>
```
---

## Variabili

- let
- const
- var

## Tipi di variabili

- Number (intero, float)
- String
- Boolean
- Array
- Object
- Function
- Undefined
- Null



#### Numbers:
```js
let length = 16;
let weight = 7.5;
```

#### Strings:
```js
let color = "Yellow";
let lastName = "Johnson";
```

#### Booleans
```js
let x = true;
let y = false;
```

#### Object:
```js
const person = {firstName:"John", lastName:"Doe"};
```

#### Array object:
```js
const cars = ["Saab", "Volvo", "BMW"];
```

#### Date object:
```js
const date = new Date("2022-03-25"####
```

---

## OUTPUT JS

In JavaScript, ci sono diversi modi per generare output. Ecco alcuni esempi:

`console.log()`: stampa l’output nella console del browser o del terminale.
`alert()`: mostra un messaggio di avviso all’utente.
`document.write()`: scrive l’output direttamente sulla pagina HTML.
`innerHTML`: modifica il contenuto HTML di un elemento.


## INPUT JS

In JavaScript, ci sono diversi modi per ottenere input dall’utente. Ecco alcuni esempi:

`prompt()`: mostra una finestra di dialogo all’utente per inserire un valore.
`confirm()`: mostra una finestra di dialogo all’utente con due opzioni (di solito “OK” e “Annulla”).
`addEventListener()`: ascolta gli eventi dell’utente come il clic del mouse o la pressione di un tasto.
`value`: ottiene il valore di un elemento di input come una casella di testo o una casella di controllo.

### Esempi

`prompt()`:
```js
let name = prompt("Inserisci il tuo nome:");
console.log("Ciao " + name);
```

`confirm()`:
```js
let result = confirm("Sei sicuro di voler continuare?");
if (result) {
    console.log("Hai scelto di continuare.");
} else {
    console.log("Hai scelto di non continuare.");
}
```
`addEventListener()`:
```js
let button = document.querySelector("button");
button.addEventListener("click", function() {
    console.log("Hai cliccato il pulsante.");
});
```
`value`:
```js
let input = document.querySelector("input");
let value = input.value;
console.log("Hai inserito: " + value);
```

---

## OPERATORI ARITMETICI

In JavaScript, ci sono diversi operatori aritmetici che possono essere utilizzati per eseguire operazioni matematiche. Ecco una lista degli operatori aritmetici in JavaScript:

`+`: Addizione. Esempio:` let sum = 3 + 2; // sum è 5`

`-`: Sottrazione. Esempio: `let difference = 3 - 2; // difference è 1`

`*`: Moltiplicazione. Esempio: `let product = 3 * 2; // product è 6`

`/`: Divisione. Esempio: `let quotient = 3 / 2; // quotient è 1.5`

`%`: Modulo (resto della divisione). Esempio: `let remainder = 3 % 2; // remainder è 1`

`++`: Incremento. Esempio: `let x = 3; x++; // x è ora 4`

`--`: Decremento. Esempio: `let x = 3; x--; // x è ora 2`


---

## FUNZIONI

In JavaScript, una funzione è un blocco di codice che può essere definito una volta e richiamato più volte. Una funzione può accettare parametri di input e restituire un valore.

Ecco un esempio di come definire e richiamare una funzione in JavaScript:

```JS
function add(a, b) {
    return a + b;
}

let sum = add(3, 2);
console.log(sum); // stampa 5
```

### FUNZIONI FRECCIA

Le funzioni freccia sono una sintassi più concisa per scrivere funzioni in JavaScript. Sono particolarmente utili quando si scrivono funzioni brevi e semplici.

Ecco un esempio di come definire una funzione freccia:

```JS
let add = (a, b, c) => a + b + c;

let sum = add(3, 2, 1);
console.log(sum); // stampa 6
```

---

## SELEZIONARE ELEMENTI HTML

In JavaScript, document è un oggetto che rappresenta la pagina HTML corrente. Può essere utilizzato per accedere e manipolare il contenuto della pagina.

document ha molte proprietà e metodi che possono essere utilizzati per interagire con la pagina. Ecco alcuni esempi:

`document.getElementById()`: restituisce un elemento della pagina con un determinato ID.
`document.getElementsByTagName()`: restituisce una lista di elementi della pagina con un determinato nome di tag.
`document.getElementsByClassName()`: restituisce una lista di elementi della pagina con una determinata classe.
`document.querySelector()`: restituisce il primo elemento della pagina che corrisponde a un determinato selettore CSS.
`document.querySelectorAll()`: restituisce una lista di elementi della pagina che corrispondono a un determinato selettore CSS.
`document.createElement()`: crea un nuovo elemento HTML.

---

## FUNZIONI MATEMATICHE

In JavaScript, Math è un oggetto che fornisce funzioni matematiche e costanti. Può essere utilizzato per eseguire operazioni matematiche più avanzate rispetto agli operatori aritmetici di base.

Ecco alcuni esempi di proprietà e metodi disponibili sull’oggetto Math:

`Math.PI`: restituisce il valore di π (pi greco).
`Math.E`: restituisce il valore di e (base dei logaritmi naturali).
`Math.abs()`: restituisce il valore assoluto di un numero.
`Math.ceil()`: restituisce il più piccolo intero maggiore o uguale a un numero.
`Math.floor()`: restituisce il più grande intero minore o uguale a un numero.
`Math.round()`: restituisce il valore intero più vicino a un numero.
`Math.sqrt()`: restituisce la radice quadrata di un numero.
`Math.pow()`: restituisce la potenza di un numero elevato a un esponente.
`Math.random()`: restituisce un numero casuale compreso tra 0 e 1.

---

## IF, ELSE IF, ELSE

In JavaScript, if...else if...else è una struttura di controllo del flusso che consente di eseguire blocchi di codice in base a una o più condizioni.

Ecco un esempio di come utilizzare if...else if...else in JavaScript:

```JS
let x = 3;

if (x > 5) {
    console.log("x è maggiore di 5");
} else if (x > 2) {
    console.log("x è maggiore di 2 ma minore o uguale a 5");
} else {
    console.log("x è minore o uguale a 2");
}
```
---
## SWITCH CASE

L’istruzione switch può essere utile per rimpiazzare multipli if. È infatti un metodo molto più descrittivo per lavorare con un elemento che può avere svariati valori1. La sintassi di un’istruzione switch è la seguente:

```JS
switch (expression) {
  case x:
    // codice
    break;
  case y:
    // codice
    break;
  default:
    // codice
}
```

Ecco come funziona: l’espressione switch viene valutata una volta. Il valore dell’espressione viene confrontato con i valori di ogni caso. Se c’è una corrispondenza, il blocco di codice associato viene eseguito. Se non c’è corrispondenza, viene eseguito il blocco di codice predefinito2.

Ecco un esempio di come si usa l’istruzione switch in JavaScript:

```JS
const expr = 'Papayas';

switch (expr) {

  case 'Oranges':
    console.log('Oranges are $0.59 a pound.');
    break;
  case 'Mangoes':
  case 'Papayas':
    console.log('Mangoes and papayas are $2.79 a pound.');
    break;
  default:
    console.log(`Sorry, we are out of ${expr}.`);
}
```



---

## CICLI FOR

In JavaScript, il ciclo for è una struttura di controllo del flusso che consente di ripetere un blocco di codice per un numero specificato di volte.

Ecco un esempio di come utilizzare il ciclo for in JavaScript:

```JS
for (let i = 0; i < 5; i++) {
    console.log(i);
}
```
### CICLARE UN ARRAY

Per utilizzare il ciclo for con un array in JavaScript, puoi utilizzare l’indice dell’array per accedere ai singoli elementi. Ecco un esempio:

```JS
let myArray = ["a", "b", "c"];

for (let i = 0; i < myArray.length; i++) {
    console.log(myArray[i]);
}
``` 

---

## CICLO WHILE

Il ciclo while è un costrutto pre-condizionale in JavaScript. Ciò significa che il controllo della condizione avviene prima dell’esecuzione delle istruzioni indicate tra parentesi graffe1. La sintassi del ciclo while è la seguente

```js
let i = 0;
while (i < 3) {
  // mostra 0, poi 1, poi 2
  alert(i);
  i++;
}
``` 

### DO WHILE

Il ciclo do...while è un’altra forma di ciclo in JavaScript. La differenza sostanziale rispetto al ciclo while classico consiste nel fatto che la condizione viene valutata dopo aver eseguito le istruzioni. Questo garantisce che il blocco di codice verrà eseguito almeno una volta1. La sintassi del ciclo do...while è la seguente:
```js
do {
  // istruzioni
} while (condizione); 
```

Ecco un esempio di come si usa il ciclo do...while in JavaScript:

```js
var c = 0;
do {
  document.write(c + '');
  c++;
} while (c < 10);
```

---

## ARRAY

Un array è una variabile speciale che può contenere più di un valore. In JavaScript, gli array possono essere creati utilizzando la sintassi letterale dell’array o utilizzando il costruttore Array1.

Ecco un esempio di come si crea un array in JavaScript utilizzando la sintassi letterale dell’array:

```JS
const cars = ["Saab", "Volvo", "BMW"];\
```
Ecco un esempio di come si accede agli elementi di un array in JavaScript:
```JS
const cars = ["Saab", "Volvo", "BMW"];
let car1 = cars[0]; // "Saab"
let car2 = cars[1]; // "Volvo"
let car3 = cars[2]; // "BMW"
``` 

Ci sono molte operazioni che possono essere eseguite con gli array in JavaScript. Alcune delle operazioni più comuni includono:

- **Aggiungere elementi**: è possibile aggiungere elementi a un array utilizzando i metodi `push()` e `unshift()`. Il metodo `push()` aggiunge uno o più elementi alla fine di un array, mentre il metodo `unshift()` aggiunge uno o più elementi all’inizio di un array.

- **Rimuovere elementi**: è possibile rimuovere elementi da un array utilizzando i metodi `pop()` e `shift()`. Il metodo `pop()` rimuove l’ultimo elemento di un array e restituisce il valore rimosso, mentre il metodo `shift()` rimuove il primo elemento di un array e restituisce il valore rimosso.

- **Ordinare gli elementi**: è possibile ordinare gli elementi di un array utilizzando il metodo `sort()`. Il metodo `sort()` ordina gli elementi di un array in base alla loro posizione nell’ordinamento Unicode.

- **Cercare elementi**: è possibile cercare elementi in un array utilizzando i metodi `indexOf()` e `lastIndexOf()`. Il metodo `indexOf()` restituisce l’indice del primo elemento dell’array che corrisponde al valore specificato, mentre il metodo `lastIndexOf()` restituisce l’indice dell’ultimo elemento dell’array che corrisponde al valore specificato.

- **Iterare sugli elementi**: è possibile iterare sugli elementi di un array utilizzando i metodi `forEach()`, `map()`, `filter()`, `reduce()` e altri. Questi metodi consentono di eseguire una funzione per ogni elemento dell’array o di creare un nuovo array basato sugli elementi dell’array originale.

Ecco alcuni esempi di operazioni comuni che possono essere eseguite con gli array in JavaScript:

**Aggiungere elementi:**
```js
const fruits = ["banana", "apple", "orange"];
fruits.push("mango"); // aggiunge "mango" alla fine dell'array
fruits.unshift("kiwi"); // aggiunge "kiwi" all'inizio dell'array
console.log(fruits); // ["kiwi", "banana", "apple", "orange", "mango"]
```

**Rimuovere elementi:**
```js
const fruits = ["banana", "apple", "orange"];
const lastFruit = fruits.pop(); // rimuove e restituisce l'ultimo elemento dell'array
const firstFruit = fruits.shift(); // rimuove e restituisce il primo elemento dell'array
console.log(lastFruit); // "orange"
console.log(firstFruit); // "banana"
console.log(fruits); // ["apple"]
```

**Ordinare gli elementi:**
```js
const fruits = ["banana", "apple", "orange"];
fruits.sort(); // ordina gli elementi dell'array in ordine alfabetico
console.log(fruits); // ["apple", "banana", "orange"]
```

**Cercare elementi:**
```js
const fruits = ["banana", "apple", "orange"];
const index = fruits.indexOf("apple"); // restituisce l'indice del primo elemento che corrisponde al valore specificato
console.log(index); // 1
```

**Iterare sugli elementi:**
```js
const fruits = ["banana", "apple", "orange"];
fruits.forEach(function (fruit) {
  console.log(fruit);
});
// stampa:
// banana
// apple
// orange
```

### METODI DEGLI ARRAY

Ci sono molti metodi disponibili per gli array in JavaScript. Alcuni dei metodi più comuni sono:

- `concat()`: unisce due o più array e restituisce un nuovo array.
- `every()`: verifica se tutti gli elementi di un array soddisfano una condizione specificata da una funzione fornita.
- `filter()`: crea un nuovo array con tutti gli elementi di un array che soddisfano una condizione specificata da una funzione fornita.
- `find()`: restituisce il valore del primo elemento di un array che soddisfa una condizione specificata da una funzione fornita.
- `findIndex()`: restituisce l'indice del primo elemento di un array che soddisfa una condizione specificata da una funzione fornita.
- `forEach()`: esegue una funzione fornita per ogni elemento di un array.
- `includes()`: determina se un array contiene un elemento specificato.
- `indexOf()`: restituisce l'indice del primo elemento di un array uguale a un valore specificato.
- `join()`: unisce tutti gli elementi di un array in una stringa.
- `lastIndexOf()`: restituisce l'indice dell'ultimo elemento di un array uguale a un valore specificato.
- `map()`: crea un nuovo array con i risultati della chiamata di una funzione fornita su ogni elemento di un array.
- `pop()`: rimuove l'ultimo elemento di un array e restituisce quel valore.
- `push()`: aggiunge uno o più elementi alla fine di un array e restituisce la nuova lunghezza dell'array.
- `reduce()`: applica una funzione a un accumulatore e a ogni elemento di un array (da sinistra a destra) per ridurlo a un singolo valore.
- `reduceRight()`: applica una funzione a un accumulatore e a ogni elemento di un array (da destra a sinistra) per ridurlo a un singolo valore.
- `reverse()`: inverte l'ordine degli elementi di un array.
- `shift()`: rimuove il primo elemento di un array e restituisce quel valore.
- `slice()`: restituisce una porzione superficiale di un array in un nuovo array.
- `some()`: verifica se almeno uno degli elementi di un array soddisfa una condizione specificata da una funzione fornita.
- `sort()`: ordina gli elementi di un array in loco e restituisce l'array ordinato.
- `splice()`: aggiunge/rimuove elementi da/in un array e restituisce gli elementi rimossi.
- `toString()`: converte un array in una stringa e restituisce il risultato.
- `unshift()`: aggiunge uno o più elementi all'inizio di un array e restituisce la nuova lunghezza dell'array.

Questi sono solo alcuni dei metodi disponibili per gli array in JavaScript. Puoi trovare una lista completa dei metodi degli array nella documentazione ufficiale di JavaScript.

---

## FUNZIONI TEMPORALI

In JavaScript, ci sono diverse funzioni che possono essere utilizzate per gestire il tempo. Alcune delle funzioni più comuni includono setTimeout(), setInterval() e clearInterval().

**setTimeout()**: questa funzione viene utilizzata per eseguire una funzione o un blocco di codice una volta dopo un determinato periodo di tempo. Ad esempio, se si vuole eseguire una funzione dopo 3 secondi, si può utilizzare il seguente codice:

```JS
setTimeout(function() {
  // codice da eseguire dopo 3 secondi
}, 3000);
```

**setInterval()**: questa funzione viene utilizzata per eseguire una funzione o un blocco di codice ripetutamente a intervalli di tempo specificati. Ad esempio, se si vuole eseguire una funzione ogni 3 secondi, si può utilizzare il seguente codice:

```JS
setInterval(function() {
  // codice da eseguire ogni 3 secondi
}, 3000);
```

**clearInterval()**: questa funzione viene utilizzata per interrompere l’esecuzione di una funzione che è stata programmata per essere eseguita ripetutamente con setInterval(). Ad esempio, se si vuole interrompere l’esecuzione di una funzione dopo 10 secondi, si può utilizzare il seguente codice:

```JS
const intervalId = setInterval(function() {
  // codice da eseguire ogni 3 secondi
}, 3000);

setTimeout(function() {
  clearInterval(intervalId);
}, 10000);
```
---

##OGGETTI

Gli oggetti in JavaScript sono contenitori per valori con nome chiamati proprietà. Le proprietà possono essere di qualsiasi tipo di dato, inclusi altri oggetti e funzioni. Quando una proprietà è una funzione, viene chiamata metodo1.

Gli oggetti possono essere creati utilizzando la sintassi letterale degli oggetti o il costruttore Object(). Ad esempio, puoi creare un oggetto con la sintassi letterale come segue:

```JS
const persona = {
  nome: "Mario",
  cognome: "Rossi",
  eta: 30
};
```
In questo esempio, abbiamo creato un oggetto chiamato persona con tre proprietà: `nome`, `cognome` e `eta`. Puoi accedere alle proprietà dell’oggetto utilizzando la notazione a punto o la notazione a parentesi quadre. Ad esempio:

```js
console.log(persona.nome); // "Mario"
console.log(persona["cognome"]); // "Rossi"
```

**Esempi**

```js
const palla = {
    colore: ['red', 'blue'],
    tipologia: "Palla da golf"
}
```
Richiesta informazione oggetto palla intero
```js
console.log( palla )
```
Richiesta informazione chiave "colore" con dot notation 
```js
console.log( palla['colore'] )
```
Richiesta informazione chiave "colore" con quadre notation
```js
console.log( palla.colore.includes('red') )
```
**Salvataggio in una variabile**

Salvataggio in una variabile del valore della chiave "colore"
```js
let arrayColore = palla.colore
```

Utilizzo della varibaile per le funzionni con gli array
```js
console.log( arrayColore.includes('red') )
```
**tipo stringa**

```js
console.log( `Ciao ${ datoUtente }, ecco per te una bellissima ${palla.tipologia}` )
```

**sovrascrivere informaizoni delle chiavi**

```js
palla.tipologia = "Palla da basket"

console.log( palla )
```
**arrray con oggetti**

```js
let classi = [
    {
       'nome' : 'Classe#1',
       'numeroStudenti' : 10,
       'nomeStudenti': [ 'Leonardo', "Edoardo", 'nome3' ]
    //    'nuovaChiave' : nuovoValore
    },
    {
       'nome' : 'Classe#2',
       'numeroStudenti' : 12,
       'nomeStudenti': [ 'Simone', 'francesca', 'nome4' ]
    },
];
```
### DESTRUTTURIZZAZIONE

La destrutturizzazione degli oggetti è una sintassi di assegnazione di JavaScript che consente di estrarre i valori dalle proprietà degli oggetti e assegnarli a variabili distinte. Ad esempio, supponiamo di avere un oggetto `persona` con due proprietà: `nome` e `cognome`:
```javascript
const persona = {
  nome: "Mario",
  cognome: "Rossi"
};
```
Senza la destrutturizzazione, per assegnare le proprietà dell'oggetto `persona` a due variabili distinte, dovresti fare qualcosa del genere:
```javascript
const nome = persona.nome;
const cognome = persona.cognome;
```
Con la destrutturizzazione degli oggetti, puoi fare la stessa cosa in modo più conciso:
```javascript
const { nome, cognome } = persona;
```
In questo esempio, abbiamo estratto le proprietà `nome` e `cognome` dall'oggetto `persona` e le abbiamo assegnate alle variabili `nome` e `cognome`.

Puoi anche assegnare valori predefiniti alle variabili durante la destrutturizzazione. Ad esempio:
```javascript
const { nome, cognome, eta = 30 } = persona;
console.log(eta); // 30
```
In questo esempio, abbiamo estratto le proprietà `nome`, `cognome` e `eta` dall'oggetto `persona`. Poiché l'oggetto `persona` non ha una proprietà `eta`, viene assegnato il valore predefinito di 30 alla variabile `eta`.

di esecuzione del ciclo.


### MAP & FILTER

`map` e `filter` sono due metodi degli array in JavaScript che consentono di trasformare e filtrare gli elementi di un array.

Il metodo `map` crea un nuovo array con i risultati della chiamata di una funzione fornita su ogni elemento dell'array chiamante. Ad esempio:
```javascript
const numeri = [1, 2, 3, 4];
const quadrati = numeri.map(numero => numero * numero);
console.log(quadrati); // [1, 4, 9, 16]
```
In questo esempio, abbiamo utilizzato il metodo `map` per creare un nuovo array `quadrati` contenente i quadrati degli elementi dell'array `numeri`.

Il metodo `filter`, invece, crea un nuovo array con tutti gli elementi dell'array chiamante che soddisfano una condizione specificata da una funzione fornita. Ad esempio:
```javascript
const numeri = [1, 2, 3, 4];
const pari = numeri.filter(numero => numero % 2 === 0);
console.log(pari); // [2, 4]
```
In questo esempio, abbiamo utilizzato il metodo `filter` per creare un nuovo array `pari` contenente solo gli elementi pari dell'array `numeri`.

### SPREAD

Lo spread operator (operatore di espansione) è una sintassi di JavaScript che consente di espandere un iterabile (come un array o una stringa) nei luoghi in cui sono previsti zero o più argomenti (per le chiamate di funzione) o elementi (per gli array letterali). Ad esempio:
```javascript
const numeri = [1, 2, 3];
const altriNumeri = [4, 5, 6];
const tuttiNumeri = [...numeri, ...altriNumeri];
console.log(tuttiNumeri); // [1, 2, 3, 4, 5, 6]
```
In questo esempio, abbiamo utilizzato lo spread operator per espandere gli array `numeri` e `altriNumeri` e creare un nuovo array `tuttiNumeri` contenente tutti gli elementi dei due array.

Lo spread operator può anche essere utilizzato per copiare un array:
```javascript
const numeri = [1, 2, 3];
const copiaNumeri = [...numeri];
console.log(copiaNumeri); // [1, 2, 3]
```
In questo esempio, abbiamo utilizzato lo spread operator per creare una copia superficiale dell'array `numeri`.

Lo spread operator può anche essere utilizzato con gli oggetti per copiare le proprietà di un oggetto in un altro oggetto:
```javascript
const persona = { nome: "Mario", cognome: "Rossi" };
const dettagli = { eta: 30, citta: "Milano" };
const personaDettagliata = { ...persona, ...dettagli };
console.log(personaDettagliata); // { nome: "Mario", cognome: "Rossi", eta: 30, citta: "Milano" }
```
In questo esempio, abbiamo utilizzato lo spread operator per copiare le proprietà degli oggetti `persona` e `dettagli` in un nuovo oggetto `personaDettagliata`.


---

## CICLO FOREACH

Il metodo `forEach` è un metodo iterativo degli array in JavaScript che esegue una funzione fornita per ogni elemento dell'array. Ad esempio:
```javascript
const numeri = [1, 2, 3, 4];
numeri.forEach(function(numero) {
  console.log(numero);
});
// Output: 1 2 3 4
```
In questo esempio, abbiamo utilizzato il metodo `forEach` per eseguire una funzione per ogni elemento dell'array `numeri`. La funzione fornita come argomento al metodo `forEach` viene chiamata con tre argomenti: l'elemento corrente dell'array, l'indice dell'elemento corrente e l'array stesso.

Il metodo `forEach` non restituisce alcun valore e non è concatenabile. Inoltre, non viene eseguito per gli elementi vuoti dell'array.

**Quando usare `forEach` e quando il `for`**


Il ciclo `forEach` e il ciclo `for` sono entrambi utilizzati per iterare sugli elementi di un array in JavaScript, ma ci sono alcune differenze tra i due.

Il ciclo `forEach` è un metodo degli array che esegue una funzione fornita per ogni elemento dell'array. La sintassi è più concisa rispetto al ciclo `for` e non richiede l'inizializzazione di una variabile contatore o l'aggiornamento del contatore ad ogni iterazione. Tuttavia, il ciclo `forEach` non può essere interrotto utilizzando le istruzioni `break` o `continue`.

Il ciclo `for`, d'altra parte, è una struttura di controllo del flusso che consente di eseguire un blocco di codice per un numero specificato di volte. La sintassi del ciclo `for` è più verbosa rispetto al ciclo `forEach`, ma offre maggiore flessibilità in termini di controllo del flusso. Ad esempio, puoi interrompere l'esecuzione del ciclo utilizzando le istruzioni `break` o `continue`.

In generale, il ciclo `forEach` è più adatto per iterare sugli elementi di un array quando non è necessario interrompere l'iterazione. Il ciclo `for`, invece, è più adatto quando hai bisogno di maggiore controllo sul flusso 


---

## CLASSI IN JAVASCRIPT

Le classi in JavaScript sono un modo per creare modelli per gli oggetti. Una classe definisce la forma di un oggetto e il comportamento che può avere. Le classi sono state introdotte in ECMAScript 2015 (ES6) e sono costruite su prototipi, ma hanno anche alcune sintassi e semantica uniche rispetto alle classi.

Per creare una classe in JavaScript, si utilizza la parola chiave `class` seguita dal nome della classe. Il corpo della classe è racchiuso tra parentesi graffe `{}` e contiene la definizione dei membri della classe, come metodi o costruttori. Ad esempio:
```javascript
class Rettangolo {
  constructor(altezza, larghezza) {
    this.altezza = altezza;
    this.larghezza = larghezza;
  }
}
```
In questo esempio, abbiamo creato una classe `Rettangolo` con un metodo costruttore che accetta due argomenti: `altezza` e `larghezza`. Il metodo costruttore viene chiamato automaticamente quando viene creato un nuovo oggetto utilizzando la classe `Rettangolo`.

Una volta definita una classe, puoi utilizzarla per creare nuovi oggetti utilizzando la parola chiave `new`:
```javascript
const rettangolo = new Rettangolo(10, 20);
console.log(rettangolo.altezza); // 10
console.log(rettangolo.larghezza); // 20
```
In questo esempio, abbiamo creato un nuovo oggetto `rettangolo` utilizzando la classe `Rettangolo`. Quando viene creato il nuovo oggetto, il metodo costruttore viene chiamato automaticamente con gli argomenti forniti.






---

---

# CODICE RICCORRENTE


#### ottenere il valore input
`.value`
```js
let km = document.getElementById('km').value;
```
#### arrotondare un numero a 2 decimali
`.toFixed(numero dei decimali)`

```js
document.getElementById('priceresult').innerHTML = (prckm * km).toFixed(2);
```

#### aggiungere una classe CSS ad un elemento HTML
`.classList.add('nome classe')`

```js
document.getElementById('DivOutput').classList.add('d-none');
```

#### aggiungere e togliere con toggle una classe un elemento HTML
`.classList.toggle('nome classe')`

```js
document.getElementById('DivOutput').classList.toggle('d-none');
```

#### selezionare il primo elemento HTML
`.querySelector('Elemento HTML')`

```js
const p = document.querySelector("p");
```
```js
const example = document.querySelector(".example");
```
#### creare un elemento HTML
`document.createElement('Elemento HTML')`
```js
let item = document.createElement('li');
```

#### aggiungere un elemento HTML all'interno di un'altro
`.append(child HTML)`
```js
const parent = document.querySelector("#parent");
const child = document.createElement("div");
child.textContent = "Sono un figlio";
parent.append(child);
```
#### prendere un numero divisibile per un altro, o i multipli di un certo numero
`num % numMultiplo == 0`

```js
for (let i = 1; i <= 100; i++) {
    //multiplo di 3 e 5
    if ((i % 3 == 0) && (i % 5 == 0)) {

    // multiplo di 3
    } else if (i % 3 == 0) {

    //multiplo di 5
    } else if (i % 5 == 0) {

    } else {

    }
}
```
#### inserire molte righe di testo o di contenuto HTML con il template litteral
.innerHTML = ``
inserire una variabile nel template litteral con `${nome variabile}`

#### generare un numero random
`Math.random()`

```js
const min = 1;
const max = 10;
const randomNumber = Math.floor(Math.random() * (max - min + 1)) + min;
console.log(randomNumber);
```

con una funzione per dare un range
```js
function generaNumeroCasuale(min, max) {
    return Math.floor(Math.random() * (max - min + 1)) + min;
    }
```

#### addEventListener di vari tipi

- **Eventi del mouse**: `click`, `dblclick`, `mousedown`, `mouseup`, `mousemove`, `mouseover`, `mouseout`
- **Eventi della tastiera**: `keydown`, `keyup`, `keypress`
- **Eventi del form**: `submit`, `change`, `input`, `focus`, `blur`
- **Eventi della finestra**: `resize`, `scroll`, `load`, `unload`

```js
const button = document.querySelector("button");
button.addEventListener("click", function() {
  console.log("Il pulsante è stato cliccato!");
});
```

#### aggiungere un valore ad un attributo HTML, può funzionare anche per aggingere classi
`.setAttribute()`

```js
const link = document.querySelector("a");
link.setAttribute("href", "https://www.example.com");
```
```js
img.setAttribute('src', images[index]);
```

#### rendere dei numeri come stringa in valori numerici interi o con virgola mobile
`parseInt()` e `parseFloat()`
```js 
const str = "123";
const num = parseInt(str, 10);
console.log(num); // 123
```
```js
const str = "123.45";
const num = parseFloat(str);
console.log(num); // 123.45
```

#### cambiare le proprietà di un valore CSS, con le variabili si possono fare grandi cose
`style.setProperty()`

```js
const element = document.querySelector("#my-element");
element.style.setProperty("color", "red");
```
esempio con delle varibili CSS
```js
if (difficoltà == 100) {
    document.documentElement.style.setProperty("--difficult", "10");
} else if (difficoltà == 81) {
    document.documentElement.style.setProperty("--difficult", "9");
} else if (difficoltà == 49) {
    document.documentElement.style.setProperty("--difficult", "7");
}
```
#### avere un array con numeri generati casualmente che NON SI RIPETONO
```js
const numbers = [];
while (numbers.length < 10) {
  const randomNumber = Math.floor(Math.random() * 101);
  if (!numbers.includes(randomNumber)) {
    numbers.push(randomNumber);
  }
}
console.log(numbers);
```
#### creare un timer countdown
```js
//timer
    let g = 23;
    let countdown = setInterval(function() {
        if (g >= 0) {
            document.getElementById('risultato').innerHTML = `<h2>${g}</h2>`;
            g--;
        } else {
        clearInterval(countdown);
        }
    }, 1000);
```

### Alcuni esempi di utilizzo del ciclo `forEach` in JavaScript:

#### 1. Calcolare la somma di tutti gli elementi di un array:
```javascript
const numeri = [1, 2, 3, 4];
let somma = 0;
numeri.forEach(function(numero) {
  somma += numero;
});
console.log(somma); // 10
```
In questo esempio, abbiamo utilizzato il ciclo `forEach` per calcolare la somma di tutti gli elementi dell'array `numeri`.

#### 2. Creare un nuovo array trasformando gli elementi di un array esistente:
```javascript
const numeri = [1, 2, 3, 4];
const quadrati = [];
numeri.forEach(function(numero) {
  quadrati.push(numero * numero);
});
console.log(quadrati); // [1, 4, 9, 16]
```
In questo esempio, abbiamo utilizzato il ciclo `forEach` per creare un nuovo array `quadrati` contenente i quadrati degli elementi dell'array `numeri`.

#### 3. Filtrare gli elementi di un array in base a una condizione:
```javascript
const numeri = [1, 2, 3, 4];
const pari = [];
numeri.forEach(function(numero) {
  if (numero % 2 === 0) {
    pari.push(numero);
  }
});
console.log(pari); // [2, 4]
```
In questo esempio, abbiamo utilizzato il ciclo `forEach` per creare un nuovo array `pari` contenente solo gli elementi pari dell'array `numeri`.


### forEach arrow function su un array di ogetti
Ecco un esempio che mostra come utilizzare il ciclo `forEach` per iterare su un array di oggetti e accedere all'elemento corrente, all'indice corrente e all'array stesso:

```javascript
const persone = [
  { nome: "Mario", cognome: "Rossi", eta: 30 },
  { nome: "Luigi", cognome: "Verdi", eta: 40 },
  { nome: "Anna", cognome: "Bianchi", eta: 50 }
];

persone.forEach((elemento, indice, array) => {
  console.log(`Elemento ${indice}:`, elemento);
});

// Output:
// Elemento 0: { nome: 'Mario', cognome: 'Rossi', eta: 30 }
// Elemento 1: { nome: 'Luigi', cognome: 'Verdi', eta: 40 }
// Elemento 2: { nome: 'Anna', cognome: 'Bianchi', eta: 50 }
```
In questo esempio, abbiamo un array `persone` che contiene tre oggetti. Ogni oggetto rappresenta una persona con le proprietà `nome`, `cognome` e `eta`.

Utilizziamo il ciclo `forEach` per iterare su ogni elemento dell'array `persone`. All'interno del ciclo `forEach`, la funzione fornita come argomento viene chiamata con tre argomenti: l'elemento corrente dell'array, l'indice dell'elemento corrente e l'array stesso.

In questo caso, utilizziamo i tre argomenti per stampare l'indice e l'elemento corrente ad ogni iterazione del ciclo.

### Esempio complesso di Class

Ecco un esempio più complesso che mostra come utilizzare le classi in JavaScript per creare un modello per un conto bancario:

```javascript
class ContoBancario {
  constructor(titolare, saldoIniziale) {
    this.titolare = titolare;
    this.saldo = saldoIniziale;
  }

  deposita(importo) {
    this.saldo += importo;
    console.log(`Deposito di ${importo} euro effettuato. Nuovo saldo: ${this.saldo} euro.`);
  }

  preleva(importo) {
    if (importo > this.saldo) {
      console.log(`Prelevamento non possibile: saldo insufficiente.`);
    } else {
      this.saldo -= importo;
      console.log(`Prelevamento di ${importo} euro effettuato. Nuovo saldo: ${this.saldo} euro.`);
    }
  }

  visualizzaSaldo() {
    console.log(`Il saldo del conto di ${this.titolare} è di ${this.saldo} euro.`);
  }
}

const contoMario = new ContoBancario("Mario Rossi", 100);
contoMario.visualizzaSaldo(); // Il saldo del conto di Mario Rossi è di 100 euro.
contoMario.deposita(50); // Deposito di 50 euro effettuato. Nuovo saldo: 150 euro.
contoMario.preleva(70); // Prelevamento di 70 euro effettuato. Nuovo saldo: 80 euro.
contoMario.preleva(200); // Prelevamento non possibile: saldo insufficiente.
```
In questo esempio, abbiamo creato una classe `ContoBancario` con un metodo costruttore che accetta due argomenti: il `titolare` del conto e il `saldoIniziale`. La classe ha anche tre metodi: `deposita`, `preleva` e `visualizzaSaldo`, che consentono di depositare denaro sul conto, prelevare denaro dal conto e visualizzare il saldo del conto.

Abbiamo quindi utilizzato la classe `ContoBancario` per creare un nuovo oggetto `contoMario` che rappresenta il conto bancario di Mario Rossi con un saldo iniziale di 100 euro. Abbiamo quindi utilizzato i metodi della classe per depositare denaro sul conto, prelevare denaro dal conto e visualizzare il saldo del conto.

