---
layout: post
author: Gregorio Baldi
title:  "Dal mondo delle simmetrie alla Teoria dei Gruppi "
description: "Un viaggio intergalattico tra rotazioni, Tori e il Gruppo Fondamentale"
date:   2014-05-23 15:00:00 +0200
categories: articles
---

Cosa hanno in comune un Sudoku, un Sudoku gigantesco, il cubo di Rubik, e i fenomeni di simmetria delle molecole chimiche? Tutti questi oggetti e fenomeni si basano su un oggetto matematico fondamentale: i gruppi!

Quadrati che rotolano
---

Prima di partire dobbiamo sapere qualcosa sui quadrati…
In apparenza lo studio delle simmetrie è un gioco da ragazzi, ma per ora preoccupiamoci solo delle rotazioni.

###Un quadrato è simmetrico

Possiamo farlo **ruotare** e ci apparirà sempre uguale.

<figure>
<img src="{{ site.url }}/images/grup/1.png"/>
</figure>

Lo stesso vale per un triangolo equilatero:

<figure>
<img src="{{ site.url }}/images/grup/2.png"/>
</figure>

Esagerando anche il cerchio, il cubo, la sfera e figure con i nomi sempre più complicati come l’ottaedro (che ha otto facce) o l’icosaedro (che ne ha venti) condividono tutti simili proprietà di simmetria.\\
Per ottenere delle informazioni matematiche da un semplice quadrato dobbiamo tenere un *diario*.\\
Se, ad esempio, volessimo tenere traccia delle quattro rotazioni sul quadrato potremmo disegnarle così:

<figure>
<img src="{{ site.url }}/images/grup/3.png"/>
</figure>

Un quadrato ha quattro lati e ci sono solo quattro modi diversi di farlo ruotare. Ruotando non può diventare rosso o verde, diventare un cerchio o un gatto; queste sono altre operazioni!\\
Se ruotiamo il quadrato di mezzo giro, la figura vista alla fine ci apparirà invariata:
<figure>
<img src="{{ site.url }}/images/grup/4.png"/>
</figure>

Ma noi sappiamo che è **cambiato qualcosa**, quindi sul nostro diario potremmo annotarlo così:

<figure>
<img src="{{ site.url }}/images/grup/6.png"/>
</figure> 

`Ma i matematici sono pigri!` e il nostro diario non ha molto spazio, quindi indichiamolo così:

<figure>
<img src="{{ site.url }}/images/grup/5.png"/>
</figure>

questo disegno indica l’ `azione` di far compiere al quadrato mezza rotazione.\\
Ovviamente se facciamo fare al quadrato un quarto di rotazione e poi ripetiamo l’operazione è come se avessimo fatto mezza rotazione: 

<figure>
<img src="{{ site.url }}/images/grup/7.png"/>
</figure> 

Allo stesso modo abbiamo che :

<figure>
<img src="{{ site.url }}/images/grup/8.png"/>
</figure>

L’importante è che il quadrato, dopo una combinazione di rotazioni, rimanga sempre un quadrato! \\
Le gambe e le braccia servono solo a tenere una traccia di cosa stiamo combinando!

Cosa succede se facciamo una rotazione di tre quarti e poi di mezzo giro? E’ come fargli fare un giro completo e poi un altro quarto. Ma, nella Teoria dei Gruppi, ci interessa solo il risultato finale: è come se avessimo fatto solo una rotazione di un quarto!

<figure>
<img src="{{ site.url }}/images/grup/9.png"/>
</figure>

perché le rotazione di un giro completo, in fondo, le possiamo ignorare: `sono fatica sprecata`.

>Le rotazioni del quadrato giocano un po’ come le lancette dell’orologio. Se sono le TRE e aspettiamo altre dodici ore, l’orologio indicherà sempre le TRE!

E possiamo continuare allo stesso modo con tutte le altre combinazioni; per fortuna abbiamo solo quattro tipi di rotazioni e finiamo in fretta! A questo punto è ora di salvare tutto sul diario nella **tavola di rotazione del quadrato**:

<figure>
<img src="{{ site.url }}/images/grup/10.png"/>
</figure>

### Le tavole sono la linfa vitale della teoria dei gruppi. Ogni mistero di questa materia enigmatica e sorniona risiede nelle tavole.


Riassumendo possiamo dire che un gruppo è un insieme di elementi con un’operazione che combina due di essi e ne restituisce un terzo, sempre dentro l’insieme da cui siamo partiti.\\
In più vogliamo che questa operazione soddisfi qualche proprietà aggiuntiva, simili a quelle dell’addizione o del prodotto che usiamo tutti i giorni.


Potevamo studiare un gruppo ancora più facile, ma non molto interessante: consideriamo il nostro quadrato e pensiamo di avere a disposizione solo la mossa corrispondente a nessuna rotazione:

<figure>
<img src="{{ site.url }}/images/grup/11.png"/>
</figure>

In questo caso la tavola di moltiplicazione si scrive in fretta: c’è solo un elemento e possiamo combinarlo quante volte vogliamo e il risultato sarà sempre lui!\\
Non ruotare più volte vuol dire non ruotare...

Su questo gruppo non c’è molto da dire, proprio per questo tutti lo chiamano **Gruppo Banale**.

Un bel gioco, ma a cosa serve?
---

Ora che abbiamo capito che la Teoria dei Gruppi si occupa di riempire delle tavole simili alle griglie del sudoku, come promesso, vediamo che non è, solo, un bel passatempo per i Matematici…\\
Il cubo di Rubik è un ottimo esempio per vedere **all’opera** la teoria dei gruppi. Tutte le mosse che possiamo fare col cubo *formano proprio un gruppo*.
<figure>
<img src="http://upload.wikimedia.org/wikipedia/commons/a/a6/Rubik%27s_cube.svg"/>
</figure>\\
Giocando con il cibo di Rubik non è mai capitato di vederlo trasformarsi in una piramide, o che diventasse tutto blu. Insomma muovendolo si può cambiare la disposizione dei colori ma rimane sempre un cubo!



Rispetto al quadrato abbiamo qualche mossa in più, ma i gruppi, anche se sono grossi, non ci spaventano! Armati di un po’ di pazienza possiamo scrivere la sua tavola. Perfetto, ma ne vale la pena?\\

### Certo!

Se vi cade dalle mani e lo ricomponete in maniera casuale possiamo dire se il cubo si potrà risolvere ancora oppure no: basta scrivere la tavola del nuovo cubo e vedere se combacia con quella iniziale.
Con la tavola a disposizione si può calcolare anche quante mosse mancano alla conclusione del cubo in fretta: invece che provare e vedere che succede basta un foglio e una matita e calcolare cosa succede combinando una sequenza di mosse!\\
Non avete mica buttato via il diario con i disegni dei quadrati??

##E’ nato prima il cubo di Rubik o la Teoria dei Gruppi?

>La Teoria dei Gruppi! E, i matematici, la usano per tante cose


Se vogliamo studiare un oggetto matematico una buona soluzione è associargli un gruppo e studiare quello…\\
Per studiare la natura dei ‘buchi’ di un oggetto, che in matematica si chiama [Spazio Topologico][link2], abbiamo a disposizione il **Gruppo Fondamentale**.

###Vediamolo all’opera

Fate parte di una spedizione di matematici-astronauti che vuole scoprire la forma di un Pianeta appena scoperto. Appena sbarcati sul pianeta, per cominciare, vi chiedete:

> Siamo finiti su una sfera o su una ciambella?

E’ tutto buio e avete a disposizione solo un filo e un chiodo. I fondi per spedizione erano proprio pochi, chi finanzia un gruppo di matematici nello spazio?\\
Non ci disperiamo: abbiamo a disposizione anche la *Teoria dei Gruppi*.\\
Con il chiodo e il filo possiamo considerare dei percorsi sul nostro Pianeta; ma abbiamo solo un chiodo a disposizione e quindi ci occupiamo solo di percorsi chiusi cioè che cominciano e finiscono nello stesso punto, detto punto *iniziale*. Il nostro chiodo in pratica.

<figure>
<img src="{{ site.url }}/images/fotoPNG-3.jpeg"/>
</figure>

Diciamo che due percorsi chiusi con lo stesso punto iniziale si *comportano allo stesso modo*, **omotopi** se vi piaciono i paroloni, se possono essere deformati uno nell’altro, senza muovere il punto iniziale e senza abbandonare il Pianeta.


Cerchiamo di capire come si comportano questi percorsi su una sfera.\\
Come prima cerchiamo di tenere un diario e, sempre per pigrizia, annotiamo in maniera uguale due percorsi che si comportano allo stesso modo.\\
Sulla sfera non c'è molta scelta...

<figure>
<img src="http://upload.wikimedia.org/wikipedia/commons/9/9e/P1S2all.jpg" />
</figure>

...tutti i percorsi si comportano allo stesso modo.\\
Quindi ci basta annotarne solamente uno.\\
Non dimentichiamoci che un insieme formato da un solo elemento è proprio un gruppo...



Per la ciambella, o *Toro* in matematichese, abbiamo più scelte. 
Un percorso potrebbe essere questo 

<figure>
<img src="http://upload.wikimedia.org/wikipedia/commons/thumb/2/25/Fundamental_group_torus1.png/440px-Fundamental_group_torus1.png" />
</figure>

ma i due percorsi più importanti sono loro:

<figure>
<img src="http://upload.wikimedia.org/wikipedia/commons/a/a4/Fundamental_group_torus2.png" />
</figure>


Sono i più importanti perché ogni altro percorso si comporta come una combinazione di questi due: magari fa due giri intorno al buco centrale, come il percorso **b** e poi 15 come il percorso **a**.\\
Comunque si comporti, per descriverlo, ci bastano i due percorsi principali (e i numeri ovviamente!).\\
Ad esempio il percorso che abbiamo appena descritto possiamo catalogarlo sul nostro diario scrivendo 2**b** + 15**a** che leggeremo così: fai 2 giri attorno al buco e poi 15 attorno al braccio.

> Disegnare i percorsi nello spazio può esser difficile, oltre che noioso.

Insomma *possiamo sommare i percorsi*


> Alla fine vogliamo trovare un gruppo, e un gruppo è un insieme con un’operazione…

<!-- <figure>
<img src="http://upload.wikimedia.org/wikipedia/commons/f/f7/Fundamental_group_torus3.png" />
</figure>-->


>Anche per la ciambella i percorsi formano un gruppo.

##A noi non piacciono solo la sfera e la ciambella…

L’insieme dei percorsi chiusi con lo stesso punto iniziale che si comportano allo stesso modo su un qualsiasi Spazio Topologico forma un gruppo e si chiama *Gruppo Fondamentale*.\\
Per essere più precisi è il Gruppo Fondamentale dello Spazio relativo a quel punto iniziale.

Ora che sappiamo come applicare le nostre conoscenze sui Gruppi possiamo finalmente capire se il Pianeta ha un buco come la ciambella oppure se è fatto come una Sfera!


Ci basterà piantare il nostro chiodo e cominciare a tracciare percorsi chiusi sul Pianeta.\\
Da qui in poi è un gioco da ragazzi: sarà sufficiente prendere entrambe le estremità dello spago e tirare, senza spostare il chiodo.\\
Se riusciamo, qualunque sia il percorso, a recuperare tutto il filo (mi raccomando, tirare **entrambe** le estremità contemporaneamente! se no non vale) allora la Matematica ci assicura che buchi non ci sono!\\
Nel toro, ad esempio, non riusciremo mai a tirare a noi il percorso **a** o il percorso **b**.

> Non possiamo mica rompere il nostro Pianeta!

###Ora siete pronti per la vostra spedizione alla scoperta di nuove forme!


---

[link2]: http://it.wikipedia.org/wiki/Spazio_topologico
