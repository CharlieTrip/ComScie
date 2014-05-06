---
layout: post
author: Gregorio Baldi
title:  “Dal mondo delle simmetrie alla Teoria dei Gruppi "
description: “ci sto pensando”
date:   2014-05-02 15:00:00 +0200
categories: articles
---


Cosa hanno in comune un sudoku, il cubo di Rubik, la teoria della relatività, il numero delle particelle subatomiche e i fenomeni di simmetria delle molecole chimiche? Tutto questo si bassa sullo studio dei gruppi!\\

Quadrati che rotolano
---

Prima di partire dobbiamo sapere qualcosa sui quadrati…
In apparenza lo studio delle simmetrie è un gioco da ragazzi. Un quadrato è simmetrico:possiamo farlo **ruotare** è ci apparirà sempre uguale.

<figure>
<img src="{{ site.url }}/images/grup/1.png"/>
</figure>

Lo stesso vale per un triangolo equilatero:

<figure>
<img src="{{ site.url }}/images/grup/2.png"/>
</figure>

Esagerando anche il cerchio, il cubo, la sfera e figure con nomi sempre più complicati come ottaedro (che ha otto facce) o l’icosaedro (che ne ha venti) condividono tutti simili proprietà di simmetria.\\
Per ottenere informazioni matematiche da un semplice quadrato dobbiamo tenere un **diario**.\\
Se, ad esempio, volessimo tenere traccia delle quattro rotazioni sul quadrato potremmo disegnarle così:

<figure>
<img src="{{ site.url }}/images/grup/3.png"/>
</figure>

Un quadrato ha quattro quattro lati e ci sono solo quattro modi diversi di farlo ruotare. Ruotando non può diventare rosso o verde, diventare un cerchio o un gatto; queste sono altre operazioni!\\
Se ruotiamo il quadrato, ad esempio, di mezzo giro la figura, vista alla fine, rimarrà invariata:

<figure>
<img src="{{ site.url }}/images/grup/4.png"/>
</figure>

Ma non sappiamo che è **cambiato qualcosa**, quindi sul nostro diario potremmo annotare così:

<figure>
<img src="{{ site.url }}/images/grup/6.png"/>
</figure> 

`Ma i matematici sono pigri!` e il nostro diario non ha molto spazio, quindi indichiamolo così:

<figure>
<img src="{{ site.url }}/images/grup/5.png"/>
</figure>

questo disegno indica l’ `azione` di far compiere al quadrato mezza rotazione.\\
Ovviamente se facciamo fare al quadrato un quarto di rotazione e poi ripetiamo l’operazione, abbiamo ottenuto l’equivalente di una rotazione di mezza rotazione: 

<figure>
<img src="{{ site.url }}/images/grup/7.png"/>
</figure> 

Allo stesso modo abbiamo che :

<figure>
<img src="{{ site.url }}/images/grup/8.png"/>
</figure>

L’importante è che il quadrato, dopo una combinazione di rotazioni, rimanga sempre un quadrato! Le gambe e le braccia servono solo a ricordarci cosa abbiamo combinato giocando col quadrato.\\
Cosa succede se facciamo una rotazione di tre quarti e poi di mezzo giro? E’ come fargli fare un giro completo e poi un altro quarto. Ma, nella Teoria dei Gruppi, ci interessa solo il risultato finale, quindi è come se avessimo fatto solo una rotazione da un quarto:

<figure>
<img src="{{ site.url }}/images/grup/9.png"/>
</figure>

perché le rotazione di un giro completo, in fondo, le possiamo ignorare: `sono fatica sprecata`.

>Le rotazioni del quadrato giocano un po’ come le lancetta dell’orologio. Se sono le TRE e aspettiamo dodici ore, l’orologio indicherà sempre le TRE!

E così avanti per tutte le altre combinazioni. A questo punto è ora di salvare tutto sul diario nella **tavola di rotazione del quadrato**:

<figure>
<img src="{{ site.url }}/images/grup/10.png"/>
</figure>

### Le tavole sono la linfa vitale della teoria dei gruppi. Ogni mistero di questa materia enigmatica e sorniona risiede nelle tavole.


Un bel gioco, ma a cosa serve?
---

Ora che abbiamo capito che la teoria dei gruppi si occupa di riempire delle tavole simili alle griglie del sudoku, come promesso, vediamo che non è, solo, un bel passatempo per i Matematici…\\
QUALCOSA SU COME FUNZIONA IL CUBO DI RUBIK…
Il cubo di Rubik è un ottimo esempio per vedere **all’opera** la teoria dei gruppi. Tutte le mosse che possiamo fare col cubo ‘formano proprio un gruppo’.
<figure>
<img src="http://upload.wikimedia.org/wikipedia/commons/a/a6/Rubik%27s_cube.svg"/>
</figure>\\
Rispetto al quadrato abbiamo qualche mossa in più, ma i gruppi (e i matematici che li studiano), anche se non grossi, non si spaventano!
Se, ad esempio, vi cade dalle mani il cubo e lo ricomponete in modo casuale, grazie allle tavole del gruppo saprete se si potrà ancora risolvere o meno..


I gruppi sono molto usati: se vogliamo studiare un oggetto matematico una buona soluzione è associargli un gruppo e studiare quello…\\
In particolare è il caso del **gruppo fondamentale** associato a un insieme `topologico: è un modo per capire se due cammini, che cominciano e finiscono nello stesso punto, si possono deformare “”senza strappi” uno nell’altro; intuitivamente raccogli informazioni sui ‘buchi’ dell’insieme. Ad esempio prendiamo una ciambella 

<figure>
<img src="http://upload.wikimedia.org/wikipedia/commons/a/a4/Fundamental_group_torus2.png"/>
</figure>
e una sfera.

Il gruppo fondamentale vuole raccoglierne la forma e quindi assoceremo due gruppi fondamentali diversi a questi oggetti perché il primo ha un buco nel mezzo, mentre il secondo no. In termini di cammini la sfera ha la proprietà che ogni cammino chiuso può essere portato in un punto, mentre la ciambella no.

<figure>
<img src="{{ site.url }}/images/fotoPNG-3.jpeg"/>
</figure>

Questo è uno strumento molto utile per la teoria dei Nodi che è di fondamentale importanza per lo studio del DNA, di come si uniscono i fluidi e anche per la struttura della corona del Sole.


Mi hai convinto! Ma come è nata?
---

I primi passi, all’inizio dell’Ottocento, sono stati compiuti da [Cauchy][link].Poco più tardi, nel 1832, Galois notò che, a volte, nelle tavole si formavano delle **sottotavole** speciali con le quali riuscì a capire come si comportano le equazioni, da quelle che si studiano alle medie: x^2+3, fino a equazioni complicate a piacere.

La vita di Galois è molto particolare: provò, e fallì, due volte l’esame di ammissione al Politecnico di Parigi perché si rifiutava di eseguire gli esercizi di matematica: erano banali. E morì ventunenne in un duello per salvare l’onore della donna amata.

I suoi contributi nella teoria dei gruppi ci mostrano quanto può essere lontana la teoria dalla applicazioni.\\
Un grande contributo fu dato da Ludwig Sylow nel 1872 sui gruppi di elementi 2,3,5,7,11,13,17… E tutti gli altri? Scrivere, sapendo il numero di elementi, la tavola di un gruppo non è facile. Questo è stato l’obiettivo percorso duranti tutto il Novecento dai matematici, ma di recente sono state scritte tutte le tavole! Uno dei gruppi che ha messo a dura prova i matematici è stato il ‘gruppo mostro’, un gruppo con ben 808.017.424.794.512.875.886.459.904.961.710.757.005.754.368.000.000.000 elementi! E’ un po’ come riempire la griglia di un super Sudoku! 

<figure>
<img src="{{ site.url }}/images/atlasoffinitegroups.jpg"/>
</figure>

Questo libro, del 1985, contiene quasi tutte le tavole dei gruppi!\\
Ma questa è un’altra storia…




[link]: http://it.wikipedia.org/wiki/Augustin-Louis_Cauchy
