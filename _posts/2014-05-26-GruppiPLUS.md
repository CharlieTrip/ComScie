---
layout: post
author: Baldi Gregorio
title:  "Gruppi: dalla prima definizione di Galois al teorema di Cayley"
description: "La scrivo dopo..."
date:   2014-05-26 09:00:00 +0200
categories: ocma
---

Riprendiamo le fila del discorso ricordando la definizione di Gruppo.\\
Prima proviamo a capire cosa sia un'operazione: somma, prodotto vanno bene, ma ce ne possono essere altre?\\
Certo, per noi un'operazione binaria su un insieme $$G$$, che indichiamo con $$\ast$$, è semplicemente un modo di associare a due elementi di $$G$$, diciamo $$a$$ e $$b$$, un terzo elemento di $$G$$ che indichiamo con $$a \ast b$$.


##Un *gruppo*

è un insieme $$G$$ con un'operazione binaria $$\ast$$
che soddisfa i seguenti:

+ Associatività : per ogni $$a,b,c \in G$$, si ha 

$$(a \ast b) \ast c = a \ast (b \ast c)$$


+ Esistenza di un elemento neutro : esiste un elemento $$e \in G$$ tale che 

$$a \ast e = a = e \ast a $$

+ Esistenza di un inverso : per ogni $$a \in G$$ esiste un $$a^\prime \in G$$ tale che 

$$a \ast a^\prime = e= a^\prime \ast a $$



Leggendo la definizione sembra molto complicata! Ma vediamo che abbiamo già incontrato alcuni esempi di gruppi.

+ Uno dei primi gruppi che si studia a scuola (senza dire che è un gruppo) è l'insieme degli interi, che indichiamo con $$\mathbb{Z}$$, ovvero l'insieme dei numeri che usiamo per contare: $$\dots, -3 , -2, -1, 0, 1, 2,3, \dots$$\
...con l'addizione! Per verificare che si tratta davvero di un gruppo basta notare che $$0$$ è il elemento neutro, l'inverso di un numero $$a \in \mathbb{Z}$$ è $$-a$$ (naturalmente abbiamo $$a+(-a)=0=(-a)+a$$) e l'associatività segue dal fatto che la somma di due interi è ancora un intero (non sarà mai, ad esempio, una frazione).
+ Abbiamo giù studiato il gruppo delle rotazioni del quadrato, più in generale possiamo considerare il gruppo delle sue simmetrie (cioè le rotazioni e le riflessioni), che indichiamo con $$D_4$$: se chiamiamo $$1$$ la mossa che non fa nulla, $$r$$ la rotazione di un quarto di giro, $$f$$ la riflessione abbiamo che $$D_4= \lbrace  1, r,r^2, r^3,f,fr,fr^2,fr^3   \rbrace$$.\\
Scritto in questo modo è molto semplice ricavare la tavola di moltiplicazione: basta notare le seguenti relazioni:
 - $$r^4=1$$ che è come dire che ruotare quattro volte il quadrato è equivalente a non ruotarlo
 - $$f^2=1$$ cioè se riflettiamo due volte il quadrato è come se non avessimo fatto nulla
 - $$rf=fr^3$$ cioè se ruotiamo di un quarto verso destra e poi riflettiamo è come riflettere e poi ruotare di un quarto verso sinistra.
+ L'ultimo protagonista è il *gruppo delle permutazioni di un insieme finito*. Immaginiamo di avere un sacchetto che contiene due lettere: A,B. Estraendo, senza rimettere la lettera estratta nel sacchetto, possiamo scrivere solo due *"parole"*: AB o BA. Se avessimo a disposizione le tre lettere A,B e C abbiamo $$6=3 \cdot 2 \cdot 1$$ modi diversi di comporle: ABC, ACB, BAC, BCA, CAB, CBA. È semplice convincersene: visto che non vogliamo ripetizioni abbiamo tre scelte per la prima lettera, due per la seconda e solo una per la terza: $$6=3 \cdot 2 \cdot 1$$. Più in generale $$n$$ oggetti possono essere scritti in $$n \cdot (n-1) \cdot (n-2) \cdot \dots 2 \cdot \cdot 1$$ modi diversi.\\ 
Occupiamoci delle parole ABC, ACB, BAC, BCA, CAB, CBA. Una permutazione tra due parole è **l'azione** di scambiare tutte le lettere necessarie per trasformare la prima parola nella seconda. Ad esempio per passare dalla parola CAB a CBA dobbiamo fare l'azione di "scambiare la seconda lettera con la terza". Per passare da CBA a ABC dobbiamo "scambiare la prima lettera con la terza". E per passare da CAB a ABC? Basta *comporre* le due azioni di prima: cominciamo scambiamo la seconda con la terza lettera e poi la prima con la terza; abbiamo ottenuto ancora una permutazione! Con tre lettere possiamo formare, senza ripetizioni, sei parole diverse e abbiamo proprio sei permutazioni.\\
Insomma l'insieme delle permutazioni, con la composizione, forma un gruppo. Con un po' di pazienza possiamo considerare le permutazioni su $$n$$ lettere, formano un gruppo che indichiamo con $$S_n$$ e sono in tutto $$n \cdot (n-1) \cdot (n-2) \cdot \dots 2 \cdot \cdot 1$$. Ad esempio se avessimo a disposizione 6 lettere abbiamo $$6 \cdot 5 \cdot 4 \cdot 3 \cdot 2 \cdot 1 =720$$ permutazioni diverse.



Gli assiomi di Gruppo sono brevi e naturali ma per essere formulati così come li abbiamo appena letti ci è voluto un secolo di lavoro. Vediamo la loro evoluzione.


##Chi ha inventato i Gruppi?

Il concetto, e la parola "gruppo", compaiono per la prima volta nel 1831 in un'opera di Galois. 
La sua storia è molto interessante. Evariste Galois è nato vicino a Parigi nel 1811 ed è morto, per una ferita ricevuta in un duello, nel 1832 (se state facendo i conti non vi siete sbagliati, aveva proprio ventun anni). Nella sua famiglia non c'erano matematici e, dopo essere stato educato dalla madre, ha cominciato la scuola solo nel 1827.\\
La sua carriera scolastica è tutto tranne che convenzionale: concentrato solo sulla matematica provò ad entrare nella prestigiosa Ècole Polytechnique ma fallì il test per due volte. Riusci poi ad entrare nella meno prestigiosa Ècole Normale e, all'inizio del 1830, pubblico una sua teoria riguardo alle equazioni (teoria che oggi porta il suo nome).\\
Si arruolò nell'Artiglieria della Guardia Nazionale e nel maggio del 1831 venne arrestato due volte, una delle quali per aver brindato al Re con un coltello in mano, gesto che lasciava intendere un attentato alla vita del Re. Un mese dopo essere stato rilasciato morì in duello.\\
La tragedia per i matematici fu l'incompletezza del lavoro di Galois. I suoi lavori vennero poi studiati e pubblicati da Liouville nel 1846, ma nei lavori originali c'era molto di più. 

<figure>
<img src="{{ site.url }}/images/grup/galoisfoto.jpg"/>
<figcaption>Evariste Galois</figcaption>
</figure>


Vediamo meglio che idea aveva Galois all'inizio della teoria dei gruppi. Per lui erano dei *gruppi di permutazioni di un insieme finto*, quindi la sua definizione di gruppo richiedeva solo che il prodotto di due permutazioni del gruppo fosse ancora un elemento del gruppo. Associatività, esistenza di un elemento neutro e inverso erano una conseguenza e quindi troppo ovvie per essere considerate importanti dal suo punto di vista.\\
La teoria delle permutazioni di un insieme finito fu sistemata da Cauchy nel 1844 che sottolineò l'importanza dell'elemento neutro, che indicava con $$1$$, e dell'inverso, l'inverso di $$g$$ veniva indicato con $$g^{-1}$$.\\
Il primo a considerare la possibilità di gruppi più astratti, e di conseguenza la necessita di postulare l'associatività, fu Cayley nel 1854. Per Cayley gli elementi di un gruppo erano semplicemente "simboli" con un prodotto simbolico tra $$A$$ e $$B$$ indicato con $$A\cdot B$$, soggetto alla legge

$$A \cdot \left( B \cdot C \right) = \left( A \cdot B \right) \cdot C$$
e con un unico elemento $1$ tale che $$A \cdot 1= A = 1 \cdot A $$.
Ma si limitava a considerare i gruppi **finiti** (noi all'inizio abbiamo visto due esempi: gli interi che sono finiti e i le simmetrie di un quadrato che rappresentano un gruppo finito).


##Galois non si sbagliava di molto.

Un teorema di Cayley del 1878 mostra che l'astrazione del concetto di gruppo è, in un certo senso, vuota, perché ogni gruppo è essenzialmente un gruppo di permutazioni.


###E poi?

Un grande contributo fu dato, nel 1872 da Ludwig Sylow che studiò i gruppi $$2,3,5,7,11,13,17…$$ elementi. E tutti gli altri? Scrivere, sapendo il numero di elementi, la tavola di un gruppo non è facile. Questo è stato l'obiettivo percorso durante tutto il Novecento, ma di recente sono state scritte tutte le tavole! 

<figure>
<img src="{{ site.url }}/images/grup/atlasoffinitegroups.jpg"/>
</figure>

Uno dei gruppi che ha messo a dura prova i matematici è stato il **gruppo mostro**, un gruppo con ben $$808.017.424.794.512.875.886.459.904.961.710.757.005.754.368.000.000.000$$ elementi! Pensate a come riempire un Sudoku così grande $$\dots$$

> ###Ma questa è un'altra storia.




<script type="text/javascript"
  src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML">
</script>