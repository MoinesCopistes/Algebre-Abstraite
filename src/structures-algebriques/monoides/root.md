## Monoïdes :
Un ***monoïde*** est une structure $(A,*)$ telle que (rappel: comme un monoïde est une structure algébrique $*$ est une fonction $*:A\times A\rightarrow A$ et donc $x*y\in A$) :
- $*$ est ***associatif*** : $a*(b* c)=(a* b)* c=a* b * c$
- $*$ admet un ***neutre***, noté $1_{A}$ ou $\epsilon \in A$ tel que $\epsilon * a=a * \epsilon=a$ pour tout $\in A$


(On parle souvent du monoïde $A$, abrège $a * b$ en $ab$, et $1_{A}$ en $1$)

***Exemples :***

1. $(\mathbb{N},-)$ n'est pas un monoïde

2. $(A^{A},*)$ : l’ensemble des transformations de A muni de la composition est un monoïde (La notation $A^{A}$ signifie l'ensemble de toutes les applications (ou fonctions) qui prennent un élément de $A$ comme entrée et renvoient un élément de $A$ comme sortie.)

***Propriétés/Théorèmes :***
1. Le neutre d'un monoïde est unique 

	***Preuve*** : Soient $\epsilon, \epsilon'$ neutres pour ($A, *$). Alors :
   $$
  \epsilon * \epsilon '=\epsilon ' \quad \text{et} \quad\epsilon * \epsilon'=\epsilon       
  $$
	ce qui implique $\epsilon =\epsilon '$

2. Si un élément d'un monoïde ***fini*** est un inverse à gauche il est également un inverse à droite du même élément. Autrement dit, si un élément possède un inverse à gauche, alors cet élément est inversible.
   <details>
   <summary>
   <b><i>Preuve :</i></b>
   </summary>
	Soit $b$ un inverse à gauche de $a$ tel que $ba=1_{A}$ ($a$ est donc aussi l'inverse à droite de $b$), et l'application $f:A\rightarrow A:x\rightarrow ax$. 
	
	Soient $x_{1}$ et $x_{2}$ deux éléments de $A$, leur images par $f$ sont $ax_{1}$ et $ax_{2}$ respectivement, si $ax_{1}=ax_{2}$ alors $b(ax_{1})=b(ax_{2})$ et comme on est dans un monoïde $(ba)x_{1}=(ba)x_{2}\Leftrightarrow x_{1}=x_{2}$, ce qui prouve que l'application est injective. ***Il faut bien piger que si $a$ n'avait pas d'inverse à gauche on aurait pas pu prouver l'injectivité***. Comme l'application est injective et qu'on est dans un monoïde fini on en déduit qu'il existe une relation unique bidirectionnelle entre $x$ et $ax$ pour tout $x$. L'ensemble d'entrée est donc de même taille (et de même nature parce que l'opération est stable) que l'ensemble image. Ceci implique que l'idéntité se trouve dans l'ensemble image et donc qu'il existe un $c$ tel que $ac=1_{A}$ où $c$ est donc l'inverse à droite de $a$. Maintenant il suffit de multiplier à gauche par $b :$ $b(ac)=b$, encore une fois on applique l'associativité : $(ba)c=b$ et donc $c=b$. CQFD
   </details>



---

## Sous-Monoïdes :
Une structure $B \subseteq A$ est un ***sous-monoïde*** (qui est lui-même un monoïde) si :
- $\forall x,y \in B$ on a $x * y \in B$ (stabilité)
- $1_{A} \in B$

---

## Inverses :
Soit $(A,* )$ un monoïde et $(a,b) \in A$. $a$ est l'inverse de $b$ si $a* b=b* a=\epsilon$.

***Propriétés/Théorèmes :***
1. Si $b$ possède un inverse, alors cet inverse est unique.
	***Preuve*** : Soient $a_{1}, a_{2}$ tel que $a_{1}* b=b* a_{2}=1_{A}$. Alors :
   $$
  a_{1}=a_{1}* 1_{A}=a_{1}* (b* a_{2} )=(a_{1}* b )* a_{2}=1_{A}* a_{2}=a_{2}        
  $$