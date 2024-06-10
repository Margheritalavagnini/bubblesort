SUPSI 2023-24  
Corso d’interaction design, CV427.01  
Docenti: A. Gysin, G. Profeta  

Elaborato 1: Bubble Sort 

# MOODY
Autore: Margherita Lavagnini  
[MediaPipe demo-ES6](https://margheritalavagnini.github.io/moody/index.html)


## Introduzione e tema
Il sito web che ho realizzato è sviluppato per poter spiegare l'agoritmo del Bubble sort in maniera semplice e intuitiva. Il Bubble Sort è un semplice algoritmo di ordinamento che opera confrontando ripetutamente gli elementi adiacenti e scambiandoli se sono disposti nell'ordine sbagliato. Questo processo continua finché l'intero array non è ordinato. È uno degli algoritmi di ordinamento più semplici da capire e implementare, anche se non è efficiente per grandi insiemi di dati. Tuttavia, è utile per scopi didattici e può essere un punto di partenza per comprendere i concetti di base dell'ordinamento. La sua logica è simile a quella di ordinare carte da gioco tenendole in mano e spostando le carte più grandi verso l'alto mano a mano che si scorre attraverso il mazzo.

## Riferimenti progettuali


## Design dell’interfraccia e modalià di interazione
il sito web presenta un’interfaccia grafica che illustra l’algoritmo di ordinamento “Bubble Sort”. L’interfaccia è caratterizzata da un tema scuro, che può essere particolarmente utile per ridurre l’affaticamento visivo durante l’uso prolungato.
Sul lato destro dell’interfaccia, ci sono diverse etichette che fungono da collegamento ai diveri capitoli che spiegano come funziona l'algoritmo.
Sul lato destro è sempre presente il titolo dell'argomento trattato, con un sottotitolo e un testo di spegazione differente a seconda del tema trattato.

L'interfaccia presenta un designe semplice e intuitivo che permette all'utente di orientarsi in maniera intuitiva all'interno del sito.
[<img src="doc/cards.gif" width="500" alt="Magic trick">]()


## Tecnologia usata
A livello di codice si tratta molto semplicemente di implimentazione css e js che permettono un pieno controllo dell'impaginazione e delle illustrazioni presenti all'interno del sito. Nella pagina dell'esempio e presente un codice di ordinamento visualizzato in un canvas usando l'algoritmo di ordinamento a bolle (bubble sort) con un'animazione. setup(): Inizializza l'ambiente di disegno. Viene creato un canvas di dimensioni 650x600 pixel e il frame rate viene impostato a 10 frame al secondo. Viene inoltre creato un array chiamato "values" della lunghezza della larghezza del canvas (650). Ogni elemento dell'array viene inizializzato con un valore casuale compreso tra 0 e l'altezza del canvas. draw(): Questa funzione viene chiamata ripetutamente dal programma per disegnare i frame dell'animazione. Il background viene impostato a nero. Vengono quindi visualizzati i valori dell'array "values" come linee verticali sul canvas. L'animazione consiste nell'ordinare gli elementi dell'array utilizzando l'algoritmo di ordinamento a bolle. swap(arr, a, b): Questa funzione scambia gli elementi di un array alle posizioni "a" e "b". Nel ciclo "draw()", viene iterato su tutti gli elementi dell'array "values" e ogni coppia di valori viene confrontata. Se il valore precedente è maggiore di quello successivo, i due valori vengono scambiati utilizzando la funzione "swap()". Questo processo viene ripetuto finché l'array non è completamente ordinato. Quando il ciclo di ordinamento è completato, viene stampato "finished" nella console e l'animazione si ferma usando la funzione "noLoop()".


let values = [];

let i = 0;
let j = 0;

function setup() {
  createCanvas(windowWidth, windowHeight);
  values = new Array(width);
  for (let i = 0; i < values.length; i++) {
    values[i] = random(height);
    //values[i] = noise(i/100.0)*height;
  }
}

function draw() {
  background(0);

  if (i < values.length) {
    for (j = 0; j < values.length - i - 1; j++) {
      let a = values[j];
      let b = values[j + 1];
      if (a > b) {
        swap(values, j, j + 1);
      }
    }
  } else {
    console.log("finished");
    noLoop();
  }
  i++;

  for (let k = 0; k < values.length; k++) {
    stroke(100);
    line(k, height, k, height - values[k]);
  }
}


function swap(arr, a, b) {
  let temp = arr[a];
  arr[a] = arr[b];
  arr[b] = temp;
}


## Target e contesto d’uso


Il sito web è principalmente rivolto a un pubblico che desidera comprendere i principi di base dell'algoritmo di ordinamento. In particolare, si indirizza a diversi gruppi di utenti:

Studenti di informatica, sia delle scuole superiori che universitari, che stanno esplorando algoritmi di base o corsi introduttivi di programmazione, trovano utile una spiegazione chiara del Bubble Sort per assimilare concetti fondamentali e imparare a implementare algoritmi semplici.

Coloro che si avvicinano alla programmazione per la prima volta, come principianti o autodidatti, possono trarre vantaggio da una guida accessibile al Bubble Sort, che li aiuta a comprendere i meccanismi dell'ordinamento e a sviluppare le loro competenze di programmazione.

Gli appassionati di tecnologia che non necessariamente hanno un background accademico in informatica ma sono interessati a esplorare concetti di base come gli algoritmi di ordinamento possono trovare stimolante esplorare il Bubble Sort come uno degli algoritmi più semplici e comprenderne il funzionamento attraverso una spiegazione dettagliata.

Insegnanti e educatori di informatica, matematica o scienze della computazione possono utilizzare risorse online che spiegano il Bubble Sort per arricchire i materiali didattici e offrire ai propri studenti un'ulteriore comprensione degli algoritmi di ordinamento, sia a livello concettuale che pratico.

Il sito web si rivolge a chiunque sia interessato a comprendere i fondamenti dell'informatica e degli algoritmi di ordinamento, fornendo spiegazioni accessibili e risorse utili per diversi livelli di conoscenza e esperienza.


[<img src="doc/munari.jpg" width="300" alt="Supplemento al dizionario italiano">]()
