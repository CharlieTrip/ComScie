---
layout: post
author: Brunetta Carlo
title:  "Numeri Primi e Crittografia"
description: "Come si comunica in maniera sicura?"
date:   2014-05-21 18:00:00 +0200
categories: ocma
---

Nella vita di tutti i giorni vogliamo rendere sicure le nostre informazioni.\\
Ma *come* fare? 

## Ci servono i Numeri Primi
> Un numero naturale, diverso da 1, si dice **primo** se è divisibile unicamente da 1 e da se stesso.


Ma cosa vuol dire esser *divisibili*?

> Un numero naturale $$a$$ è **divisibile** da un numero naturale $$b$$ se esiste un numero naturale $$c$$ in modo che $$a = bc$$.\\
> Equivalentemente diciamo che $$b$$ **divide** $$a$$

Quindi 1 divide 2, 1 divide 3, 1 divide 4...

> 1 divide tutti i numeri naturali perché per ogni $$a$$ numero naturale abbiamo che $$1 \cdot a = a$$

3 non divide 5 e 2 non divide 1 anche se $$1/2 = 0,5$$.\\
Però $$0,5$$ **non** è un naturale!

###Quindi quali sono i primi?

+ 1 non è primo perché deve esser diverso da 1 !
+ 2 è primo perché 2 può esser diviso solo da 2 e 1.
+ 5 è primo.  $$ 5 = 5 \cdot 1$$
+ 10 non è primo. 2 e 5 dividono 10. $$10 = 5 \cdot 2$$
+ 101 è primo. 2 non lo divide, 3 non lo divide, ... , 100 non lo divide. Quindi 101 è primo!
+ 16603 ? Per verificarlo dobbiamo dividerlo per 2, per 3, per 4, per 5, per 6, ... , per ogni numero più piccolo di 16603.
+ ...e 19134702400093278081449423917 è primo? O non lo è?

### È difficle dire se un numero è primo, specialmente se è molto grande.

I computer possono darci una mano a fare i conti ma quando vogliamo sapere se un numero con miliardi di cifre sia primo, anche i computer impiegano molto tempo per poterci rispondere.

### Ma i non primi?
Quando moltiplichiamo due numeri primi, diciamo $$p$$ e $$q$$, otteniamo un nuovo numero $$n$$.\\
$$n = p \cdot q$$ cioé $$n$$ viene diviso da 1 e se stesso ma anche da $$p$$ e $$q$$. $$n$$ non è quindi primo!\\
Ma possiamo fare il procedimento inverso. Prendiamo un numero e iniziamo a dividerlo per i suoi divisori, tipo:

+ Ad esempio $$6 = 3 \cdot 2$$
+ Oppure $$9 = 3 \cdot 3$$
+ $$30 = 3 \cdot 10$$ ma $$10 = 5 \cdot 2$$. Quindi $$30 = 3 \cdot 5 \cdot 2$$
+ $$16603$$, con un po' di pazienza, possiamo verificare che è un primo.

### È difficile trovare i divisori di un numero, specialmente se è molto grande.

Come sfruttare questi numeri?

## Orologi

Tutti conoscono gli orologi!\\
Ci permettono di conoscere in *quale momento* della giornata ci troviamo.\\
Ma come facciamo le **operazioni** sull'orologio?

Sono le **11 della mattina** e ci arriva un messaggio da un nostro amico:

> Ehi! Tra 5 ore passo a trovarti a casa. Ho una bella sorpresa per te!

Visto che ci piaciono le sorprese (specialmente se belle) vogliamo sapere a che ora dobbiamo essere a casa. Prendiamo un orologio e iniziamo a girare le lancette. Un ora... due ore... tre... finché non arriviamo a segnare le 4 del pomeriggio.\\
Cioè abbiam fatto $$11+5 = 16$$ e poi diciamo che le 16 sono le 4, per convenienza psicologica. Abbiamo fatto la somma e poi abbiamo tolto 12.\\
E se il numero ottenuto fosse ancora più grande di 12?\\
Gli avremmo tolto tante volte 12 fino ad ottenere un numero tra 0 e 11.


Con lo stesso criterio possiamo usare un orologio con quante ore vogliamo. Diciamo $$p$$ un qualsiasi numero naturale.

> Un numero $$n$$ si dice congruo ad un numero $$m$$ modulo $$p$$, scritto $$ n \equiv m \bmod p$$, se $$n = k \cdot p + m$$ per un qualche $$k$$ intero\\
> cioé $$n$$ è un multiplo di $$p$$ a meno di $$m$$\\
> in altro modo, $$p$$ divide $$n-m$$

Cosa vuol dire questo?\\
Prendiamo $$p = 16.603$$. Un gran bel numero per un orologio!

Ora, diciamo di voler fare $$3.015 \cdot 4.756$$ in questo orologio. Sappiamo (dopo aver fatto i conti) che vale $$14.339.340$$.

### Ma a quale numero è congruo modulo $$p$$?

Possiamo fare la divisione usuale : $$ 14.339.340 : 16.603 = 863,659579594\cdots$$.\\
Consideriamo la parte intera di questo numero, $$863$$ è il numero di volte che $$p$$ divide il nostro numero in maniera intera.

$$16.603 \cdot 863 = 14.328.389$$ e ora $$ 14.339.340 - 14.328.389  = 10.951$$ che è minore di $$ p $$.\\
Quindi $$3.015 \cdot 4.756 = 14.339.340 \equiv 10.951 \bmod 16.603$$

Abbiamo ottenuto un metodo abbastanza veloce per fare le congruenze in modulo $$p$$.


Allora costruiamo una comunicazione sicura!

## Metodo RSA

Per prima cosa, scegliamo due primi $$p$$ e $$q$$. Possibilmente grandi! D'ora in poi $$n = p \cdot q$$ sarà il nostro numero rispetto al quale faremo le nostre congruenze!\\
Allo stesso modo consideriamo $$s$$ come $$s =(p-1)\cdot (q-1)$$.

> Un numero naturale $$a$$ si dice coprimo con il numero naturale $$b$$ se non esiste alcun numero naturale $$c$$ diverso da 1 che divide entrambi.

Scegliamo ora un numero $$e$$ coprimo con $$s$$, diverso da 1 e più piccolo di $$s$$.\\
Utilizzando l'[Algoritmo di Euclide][algeuc] possiamo sempre calcolare il numero $$d$$ tale che $$ ed \equiv 1 \bmod s$$.

Adesso abbiamo tutto quello che ci serve per poter comunicare in maniera sicura!

Come?\\
Vediamolo con un esempio pratico:

+ Alice e Billy si mettono d'accordo su un vocabolario dove ogni parola o carattere corrisponde a un numero naturale.
+ Alice vuole comunicare con Billy. Sceglie due primi $$p,q$$, calcola $$n = p\cdot q$$ e $$s = (p-1)\cdot(q-1)$$. Trova $$e$$ e $$d$$ come sopra.\\
Alice comunica a Billy $$n$$ ed $$e$$ mentre tiene nascosto $$d$$.
+ Billy riceve $$n$$ ed $$e$$.\\
Prende il suo messaggio $$M$$ (che è un numero naturale) ed esegue il conto $$M^e $$ che sarà congruo ad $$m$$ modulo $$n$$. Billy comunica $$m$$ ad Alice
+ Alice calcola $$m^d \bmod n$$ e ottiene *proprio $$M$$*.

Perché ottiene $$M$$ ?

### Teorema di Fermat - Eulero
> Se $$n = p \cdot q$$ è un intero positivo con $$p,q$$ primi ed $$a$$ è coprimo con $$n$$\\
allora $$a^{(p-1)(q-1)}\equiv 1 \bmod n$$

Quindi Alice, mentre calcola $$m^d$$ in realtà sta facendo $$m^d = M^{e\cdot d}$$. Il fatto che $$ed \equiv 1 \bmod (p-1)(q-1)$$ vuol dire che esiste un valore $$k$$ intero tale che $$ed = 1 + k (p-1)(q-1)$$

Se sostituiamo, otteniamo
$$M^{ed} = M^{ 1 + k(p-1)(q-1) } = M \cdot M^{k(p-1)(q-1)} = M \cdot (M^{(p-1)(q-1)})^k \equiv M \cdot 1^k \bmod n \equiv M \bmod n$$\\
Cioé abbiamo ricostruito il messaggio!



##Perché questo metodo è sicuro?

Rivediamo *cosa* viene reso publico e se può rendere insicuro il nostro sistema di comunicazione.

### Alice rende publico $$n$$ ed $$e$$

Ora, immaginiamo che Charlie voglia leggere i messaggi che Alice e Billy si comunicano.\\
Quel che può fare è eseguire i passi che fa Alice.

Ma Charlie non conosce $$p$$ e $$q$$. Però potrebbe ottenerli da $$n$$ se riesce a fattorizzarlo cioé a trovare i due numeri che moltiplicati tra loro danno $$n$$.

###Fattorizzare è difficile. Costa tempo e fatica.

Quindi a Charlie non conviene fattorizzare $$n$$. Cosa può fare?

Può cercare di indovinare il numero $$d$$ custodito da Alice. In che modo?

### Ogni numero che viene comunicato tra Alice e Billy è pubblico e chiunque può vederlo.

Charlie può simulare l'invio di un messaggio ad Alice ottenendo però un messaggio cifrato che è incapace di leggere fintanto che non conosce $$d$$.\\
Inizia a *provare* tanti numeri al posto di $$d$$, capisce che si tratta proprio di $$d$$ quando ritrova il proprio messaggio.\\
Charlie **trova** il numero $$d$$ custodito da Alice ed è così in grado di rubare i messaggi che le arrivano.\\
Unico difetto: l'enorme numero di conti da fare per poter ottenere $$d$$. Tutto questo richiede molto tempo. 


>Più grandi sono i numeri scelti all'inizio, più tempo sarà necessario.


Ci rimangono poche alternative.

###O si fattorizzano i numeri o si fanno tanti conti!








<script type="text/javascript"
  src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML">
</script>

[algeuc]: http://it.wikipedia.org/wiki/Algoritmo_di_Euclide