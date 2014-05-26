---
layout: post
author: Brunetta Carlo
title:  "Primi, gruppi e crittografia"
description: "Come si comunica in maniera sicura?"
date:   2014-05-21 18:00:00 +0200
categories: ocma
---

Nella nostra vita quotidiana vogliamo rendere sicure le nostre informazioni.\\
Ma *come* fare? Per poterlo fare dobbiamo usare 

## i numeri primi

Ma quali sono?

> Un numero intero, diverso da 1, si dice **primo** se è divisibile unicamente per se stesso ed 1.

Ma cosa vuol dire esser *divisibili*?

> Un numero intero $$a$$ è **divisibile** per $$b$$ intero se esiste un valore $$c$$ intero in modo che $$a = bc$$.\\ Allo stesso modo si dice che $$b$$ **divide** $$a$$

Quindi 1 divide 2. 2 divide 4. 3 non divide 5! 2 non divide 1 anche se $$1/2 = 0,5$$.\\
Però $$0,5$$ **non** è intero!

###Quindi quali sono i primi?

+ 1 non è primo perché deve esser diverso da 1 !
+ 2 è primo perché 2 può esser diviso solo da 2 e 1.
+ 5 è primo : $$ 5 = 5 \cdot 1$$
+ 10 non è primo. 2 divide 10 e anche 5. $$10 = 5 \cdot 2$$
+ 101 è primo. 2 non lo divide, 3 non lo divide, ... , 100 non lo divide. Quindi 101 è primo!
+ 16603 è ... primo? O no?
+ ...e 19134702400093278081449423917 ?

### È difficle dire se un numero è primo, specialmente se è molto grande.

Certo, i computer possono darci una mano per fare i conti ma quando parliamo di numeri con miliardi di cifre, persino i computer impiegano molto tempo per poterci rispondere. Ma i non primi?\\
Quando moltiplichiamo due numeri primi, diciamo $$p$$ e $$q$$, otteniamo un nuovo numero $$n$$.\\
$$n = p \cdot q$$ cioé $$n$$ viene diviso da 1 e se stesso ma anche da $$p$$ e $$q$$.\\
Ma possiamo fare il procedimento inverso. Prendiamo un numero e iniziamo a dividerlo per i suoi divisori, tipo:

+ Ad esempio $$6 = 3 \cdot 2$$
+ Oppure $$9 = 3 \cdot 3$$
+ $$30 = 3 \cdot 10$$ ma $$10 = 5 \cdot 2$$. Quindi $$30 = 3 \cdot 5 \cdot 2$$
+ $$16603 = ?$$ Vediamo se 2 lo divide... no... 3 nemmeno... uhm... quindi non abbiamo numeri che dividono 16603. Quindi 16603 è primo.

### È difficile conoscere i divisori di un numero, specialmente se è molto grande.

Come sfruttare questi numeri?

## Orologi

Tutti conoscono gli orologi!\\
Ci permettono di conoscere in *quale momento* della giornata ci troviamo.\\
Ma come facciamo le operazioni sull'orologio?

Sono le 11 della mattina.\\
Ci arriva un messaggio da un nostro amico:

> Ehi! Tra 5 ore passo a trovarti a casa. Ho una bella sorpresa per te!

Visto che ci piaciono le sorprese (specialmente se belle) vogliamo sapere a che ora dobbiamo esser a casa. Prendiamo un orologio e iniziamo a girare le lancette. Un ora... due ore... tre... finché non arriviamo a segnare le 4 del pomeriggio.\\
Cioè abbiam fatto $$11+5 = 16$$ e poi diciamo che le 16 sono le 4, per convenienza psicologica. Abbiamo fatto le somme negli interi e poi gli abbiamo tolto 12.\\
E se il numero ottenuto fosse ancora più grande di 12?\\
Gli avremmo tolto tante volte 12 fino ad ottenere un numero tra 0 e 11.\\
Con lo stesso criterio possiamo usare un orologio con quante ore vogliamo. Diciamo $$p$$.

> Diremo che un numero $$ n $$ sarà congruo $$m$$ modulo $$p$$, scritto $$ n \equiv m \bmod p$$, se $$n = k \cdot p + m$$ per un qualche $$k$$ intero cioé $$n$$ è un multiplo di $$p$$ a meno di $$m$$.

Cosa vuol dire questo?\\
Prendiamo $$p = 16.603$$. Un gran bel numero per un orologio!

Ora, diciamo di voler fare $$3.015 \cdot 4.756$$ in questo orologio. Sappiamo (dopo aver fatto i conti) che vale $$14.339.340$$. Ma quanto vale modulo $$p$$?

Possiamo fare la divisione usuale : $$ 14.339.340 : 16.603 = 863,659579594\cdots$$. Consideriamo la parte intera di questo numero, $$863$$ è il numero di volte che $$p$$ divide il nostro numero in maniera intera. Il resto dopo la virgola è un numero più piccolo di $$p$$ e sarà quindi il nostro resto modulo $$p$$!

$$16.603 \cdot 863 = 14.328.389$$ e ora $$ 14.339.340 - 14.328.389  = 10.951$$ che è minore di $$ p $$.\\
Quindi $$3.015 \cdot 4.756 = 14.339.340 \equiv 10.951 \bmod 16.603$$

Abbiamo così un metodo piuttosto veloce per fare le divisioni in modulo.


Allora proviamo a costruire una comunicazione sicura!

## Metodo RSA

Per prima cosa, scegliamo due primi $$p$$ e $$q$$. Possibilmente grandi! D'ora in poi $$n = p \cdot q$$ sarà il nostro modulo!\\
Allo stesso modo $$(p-1)\cdot (q-1) = s$$ un numero che utilizzeremo presto.

Scegliamo ora un numero $$e$$ che **NON** ha divisori in comune con $$s$$ (tranne 1!. Questo numero si dice **coprimo**) e sia più piccolo.\\
Facciamo dei conti e troviamo il numero $$d$$ tale che $$ ed \equiv 1 \bmod s$$.

Adesso abbiamo tutto quello che ci serve per poter comunicare in maniera sicura!

Come?\\
Vediamolo con un esempio pratico:

+ Alice vuole comunicare con Billy. Sceglie i due primi $$p,q$$, calcola $$n = p\cdot q$$ e $$s = (p-1)\cdot(q-1)$$. Trova $$e$$ e $$d$$ come sopra.\\
Alice comunica a Billy $$n$$ e $$e$$ mentre tiene nascosto $$d$$.
+ Billy riceve $$n$$ e $$e$$ e prende il suo messaggio $$M$$ ed esegue il conto $$M^e \bmod n$$ che sarà congruo a $$m$$. Billy comunica $$m$$ ad Alice
+ Alice calcola $$m^d \bmod n$$ e ottiene $$M$$.

Perché ottiene $$M$$ ?

### Teorema di Fermat - Eulero
> Se $$n = p \cdot q$$ è un intero positivo con $$p,q$$ primi ed $$a$$ è coprimo (non ha divisori comuni tranne 1) rispetto ad $$n$$\\
allora $$a^{(p-1)(q-1)}\equiv 1 \bmod n$$

Quindi Alice, mentre fa $$m^d$$ in realtà sta facendo $$m^d = M^{e\cdot d}$$. Il fatto che $$ed \equiv 1 \bmod (p-1)(q-1)$$ vuol dire che esiste un valore $$k$$ intero tale che $$ed = 1 + k (p-1)(q-1)$$

Se sostituiamo, otteniamo
$$M^{ed} = M^{ 1 + k(p-1)(q-1) } = M \cdot M^{k(p-1)(q-1)} = M \cdot (M^{(p-1)(q-1)})^k \equiv M \cdot 1^k \bmod n \equiv M \bmod n$$\\
Cioé abbiamo ricostruito il messaggio!



##Perché questo metodo è sicuro?

Rivediamo *cosa* viene reso publico e se può esser utile per rompere il nostro sistema.

### Alice rende publico $$n$$ ed $$e$$

Ora, immaginiamo che Charlie voglia leggere i messaggi che Alice e Billy si comunicano.\\
Quel che può fare è eseguire i passi che fa Alice.

Ma Charlie non conosce $$p$$ e $$q$$. Però potrebbe ottenerli da $$n$$ se riesce a fattorizzarlo cioé a trovare i due numeri che moltiplicati tra loro danno $$n$$.

###Fattorizzare è difficile. Costa tempo e fatica.

Quindi a Charlie non conviene fattorizzare $$n$$. Cosa può fare?

Può cercare di indovinare la chiave privata di Alice. In che modo?

### Il nostro sistema è completamente conosciuto.

Charlie può criptare un messaggio con i valori di Alice e poi inizia a provare tanti numeri per $$d$$ fino a ritrovare il proprio messaggio.\\
Il metodo richiede un sacco di conti da fare però dopo un adeguato tempo, Charlie ottiene la chiave privata $$d$$ con cui può decifrare i messaggi di Alice e Billy.

Quindi ci sono poche alternative. O si fattorizzano i numeri o si fanno tanti conti!\\
O si rubano gli altri valori in qualche modo!









<script type="text/javascript"
  src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML">
</script>