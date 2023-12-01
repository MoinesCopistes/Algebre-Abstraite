## Groupes
Un groupe est un ***monoïde*** $(G,*)$ tel que :
- tous les éléments de $G$ possèdent un inverse par rapport à l'opérateur $*$. ***(Cet inverse peut être et est souvent unique à l'élément en question, il ne faut pas savoir trouver de forme générale pour l'inverse comme $1/a$ pour que tous les éléments soient inversibles)*** 

***Exemple(s) :***
1. $(\mathbb{Z},+)$ est un groupe, mais pas $(\mathbb{N}, +)$
2. $(\mathbb{R}^{*},\times)$ et $(\mathbb{R}^{\gt0},\times)$ sont des groupes
3. $S(A)$ est un groupe
4. $\mathbb{T}=\{e^{i\alpha}|\alpha \in \mathbb{R} \}$ muni de la multiplication est un groupe
5. L’ensemble des matrices orthogonales muni de la multiplication est un groupe
6. L’ensemble $A^{A}$ des transformations de $A$ muni de la composition n’est pas un groupe

***Propriétés/Théorèmes :***

1. L'ordre d'un groupe est le nombre d'éléments qu'il contient.

2. Si $a,b,c$ sont membres d'un groupe alors :
   $$
ac=bc \quad \text{ou}  \quad ca=cb \quad \text{alors} \quad a=b 

$$
    ***(Note : $ab$ est une façon plus courte d'écrire $a*b$)***

	***Preuve*** : Soit $d=c^{-1}$. Alors :
	$$
ac=bc\Rightarrow a=a\epsilon =acd=bcd=b\epsilon =b  
$$
3. Les inverses sont symétriques. Si $ab=\epsilon$ alors $a=b^{-1}$ et $b=a^{-1}$
   
	***Preuve*** : 
	$$
ab=\epsilon \Rightarrow bab=b \Rightarrow babb^{-1}=bb^{-1}\Rightarrow ba=\epsilon       
$$

4. Si tous les éléments d'un monoïde possèdent un inverse à gauche, alors le monoïde est un groupe.

   <details>
   <summary>
   <b><i>Preuve :</i></b>
   </summary>
	Soit $a$ un élément de $A$, $b$ son inverse à gauche et $c$ l'inverse à gauche de $b$. On commence avec $ab=1_{A$ et on multiplie à gauche par $c$ : $cab=c$ et on applique l'associativité : $c(ab)=c$ et donc $(ca)b=c$. On sait que $ca=1_{A}$ et donc $b=c$. $a$ est donc inversible et $A$ est un groupe.
   </details>

---

## Groupes commutatifs/abéliens
Un groupe $G$ est commutatif si :
- $a*b=b*a$ $\forall a,b\in G$

***Exemple(s) :***

---

## Sous-Groupes
$H \subseteq G$ est un sous-groupe de $(G,*)$ si :
- $\forall x,y\in H$ on a $x*y \in H$ (stabilité)
- $1_{A} \in H$
- Si $x\in H$ alors $x^{-1} \in H$\

***Exemple(s) :***

***Propriétés/Théorèmes :***

1. Si $H$ est un sous-groupe de $(\mathbb{Z,+)}$ alors $H=n\mathbb{Z}$ pour un certain $n\in \mathbb{N}$ 
   
   ***Preuve :*** Si $H=\{0\}$, alors $H=0\mathbb{Z}$
   Soit $H\neq\{0\}$ et $n$ le plus petit entier $>0$ de $H$
    - Vu que $H$ est un groupe, $\{0,n,-n,2n,-2n,\dots\}=n\mathbb{Z}\in H$
    - Soit $a\in H$. On peut écrire $a=qn+r$ avec $r\in \{0,\dots,n-1\}$.
      On a $r=0$ car sinon $a-qn=r\in H$ est un entier positif $\leq n$
    Donc $H=\{0,n,-n,2n,-2n,\dots\}=n\mathbb{Z}$
$$
 ac=bc\Rightarrow a=a\epsilon =acd=bcd=b\epsilon =b  
$$
2. Les inverses sont symétriques. Si $ab=\epsilon$ alors $a=b^{-1}$ et $b=a^{-1}$
   
	***Preuve*** : 
	$$
ab=\epsilon \Rightarrow bab=b \Rightarrow babb^{-1}=bb^{-1}\Rightarrow ba=\epsilon       
$$
3. Soit $H$ un sous-ensemble fini non-vide d'un groupe $G$. Si $H$ est stable, alors $H$ est un sous-groupe de $G$.
   
    ***Preuve :***
    Soit $a\in H$ et $f:H\rightarrow H:x\rightarrow ax$

    On observe que $f$ est bijective

    **Présence du neutre** : Comme $f$ est bijective, $\exists b\in H:f(b)=a=ab$. Donc $b=\epsilon$

    **Présence de l'inverse** :  $\exists b\in H:f(b)=\epsilon$. Donc $b=a^{-1}$

4. ***Théorème de Lagrange*** Soient $G$ un groupe fini et $H$ un sous-groupe de $G$ tels que $|G|=n$ et $|H|=m$, alors $m$ divise $n$
   
    ***Preuve :*** Les classes latérales de $H$ sont toutes de taille $m$ et forment une partition de $G$
    Donc $|G|=k|H|$ où $k$ est le nombre de classes latérales de $H$
    On a donc : $|G/H|=|G|/|H|$
---

## Classes Latérales/Suivant un Sous-Groupe $H$ 
Soit $H$ un sous-groupe de $G$. La classe latérale de $a\in G$ modulo $H$ est :
$$
aH=\{ax|x\in H\}
$$

(ici, $ab$ signifie $a*b$ où $*$ est l'opérateur du groupe)

```admonish warning title="Attention"
Les classes latérales de $a\in G$ modulo $H$ avec $H$ un sous-groupe ne sont pas forcément des groupes.
```

***Exemple(s) :***
1. $\mathbb{Z}$ est un sous-groupe de $(\mathbb{R},+)$ : les classes latérales sont $\{x+a|x \in \mathbb{Z}\}$ avec $a\in[0,1]$
2. $\{(x, ax) | x \in \mathbb{R}\}$ est un sous-groupe de $(\mathbb{R}^2, +)$ (addition par composants) 
   Les classes latérales sont ${(x, ax + b) , | , x \in \mathbb{R}}$ avec $b \in \mathbb{R}$
3. $n\mathbb{Z} = \{nx | x \in \mathbb{Z}\}$ avec $n \in \mathbb{N}^{\geq 1}$ est un sous-groupe de $(\mathbb{Z}, +)$ 
   Les classes latérales sont $\{nx + b , | , x \in \mathbb{Z}\}$ avec $b \in \{0, \ldots, n-1\}$
4. $\{2^i | i \in \mathbb{Z}\}$ est un sous-groupe de $(\mathbb{R}^{\gt 0}, *)$ 
   Les classes latérales sont $\{a *2^i , | , i \in \mathbb{Z}\}$ avec $a \in [1, 2)$

***Propriétés/Théorèmes :***
1. Il existe une bijection entre $aH$ et $H$.
   
   ***Preuve*** : Soit $f:G\rightarrow aH$ tel que $f(x)=ax$
   - $f$ est injective :
     Vu que $a$ est inversible, $ax_{1}=ax_{2}\Rightarrow x_{1}=x_{2}$
   - $f$ est surjective :
     Par définition de $aH$, tout $y \in aH$ est dans l'image de $f$
	Donc $f$ est bijective
2. Les classes latérales distinctes modulo $H$ forment une partition de $G$. Une partition est un ensemble de        sous-ensembles non-vides et disjoints dont l'union est l'ensemble de départ.
   
   ***Preuve*** : Soient $a_{1}H,a_{2}H,\dots$ les classes latérales modulo $H$ 
   - Tout élément de $G$ est dans une classe latérale 
     Si $g\in G$ alors $g \in gH$ puisque $\epsilon \in H$
   - Les classes latérales $aH$ et $bH$ sont disjointes ou identiques.
     Soient $a,b\in G$ et $x \in bH$. On montre que $x \in aH \Leftrightarrow b^{-1}a\in H$
     (Ainsi, $aH=bH$ si $b^{-1}a\in H$ et $aH  \cap bH=\emptyset$ sinon)		
 
	 $\Rightarrow$ Soit $x=ah_{1}=bh_{2}$ avec $h_{1},h_{2}\in H$. On a :
	           $ah_{1}=bh_{2}\Rightarrow a=bh_{2}h_{1}^{-1}\Rightarrow b^{-1}a=h_{2}h_{1}^{-1} \in H$
	     
	 $\Leftarrow$ Soit $b^{-1}a\in H \Rightarrow a^{-1}b \in H$ et 
	           $x=bh_{1}=(aa^{-1})bh_{1}=a((a^{-1}b)h_{1})\in aH$ 
3. Si $G$ est commutatif, alors $(ax)(bx)=(ab)(xy)$. En supposant que $x,y\in H$, $a'=ax$ et $b'=by$ cela implique que :
   $$
a'\in  aH \quad \text{et} \quad b'\in  bH\Rightarrow (a'b')\in  (ab)H 
$$
	(Quand $H$ est clair dans le contexte, on écrit $[a]$ pour $aH$)

4. Soient $aH$ et $bH$, si il n'existe aucun $c \in G$ tel que $a \in cH$ ***et*** $b \in cH$ (dit autrement : si $a$ et $b$ ne partagent pas une même classe latérale) alors $aH\cap bH=\emptyset$. (Enfaite il s'agit en quelque sorte d'une reformulation de la propriété 2 mais je trouve que ça illustre mieux son utilité).
   
   <details>
   <summary>
   <b><i>Preuve : (ma preuve, pas encore vérifié par une autre personne mais, encore une fois, assez semblable à celle de la propriété 2)</i></b>
   </summary>
	Par l'absurde, admettons qu'il existe un $c\in G$ tel que $c\in aH$ et $c\in bH$ alors que $a$ et $b$ ne sont trouvent pas dans une même classe, on en déduit les relations suivantes :
	$$
	c=ah_{1} \quad \text{et} \quad c=bh_{2} \quad \Leftrightarrow \quad h_{1}h_{2}^{-1}=a^{-1}b\in  H
	$$
	Or, si $a^{-1}b$ est dans $H$ on a $b$ dans $aH$ or $a$ est également dans $aH$ par la présence du neutre dans $H$ ce qui contredit le fait que $a$ et $b$ ne se trouvent pas dans une même classe.
   </details>

```admonish warning title="Attention"
Cette 4e propriété est utile pour trouver l'ensemble des classes latérale modulo $H$ disjointes qui forment une partition de $G$, il suffit de prendre comme $a$ un élément qui ne se trouve pas encore dans les classes latérales déjà trouves et on obtiendra une classe disjointe de celle déjà trouvées. Voir exercice 3.7.3 de la séance 3.
```

$$

$$

---


## Groupe Quotient
Le groupe quotient $G/H$ est le groupe commutatif formé de : 
- l’ensemble des classes latérales de $G$ modulo $H$ 
- l’opérateur défini par $[a][b]=[ab]$ *(Rappel : [a]=aH)*
- le neutre défini par $[\epsilon ]=H$

```admonish warning title="Attention"
Les éléments d'un groupe quotient sont des ***ensembles***.
```

Autre façon de le dire : 
- Relation d’équivalence sur $G$ commutatif créée par le sous-groupe $H$ : $a\sim b$ ssi $a^{-1}b\in H$.
- Les classes d’équivalences sont précisément les classes latérales de $H$
- Le groupe quotient $G$ est le groupe $G$ quotienté par la relation d’équivalence

***Exemple(s) :***

---

## *a mod n*
Soient $a\in \mathbb{Z}$ et $n\in \mathbb{N}^{>1}$ **$a$ mod $n$** est le reste de la division de $a$ par $n$

--- 

## Addition modulo
On dit que $\mathbb{Z}_{n}=\{0,\dots,n-1\}$ est muni de l'addition modulo $n$ si $a+b=r$ mod $n$ 

***Exemples :***
1. $2+4=1$ dans $\mathbb{Z}_{5}$
2. $1+3=0$ dans $\mathbb{Z}_{4}$

***Propriétés/Théorèmes :***
1. $\mathbb{Z}_{n}$ est isomorphe à $\mathbb{Z}/n\mathbb{Z}$
    ***Preuve :*** Considérer $f:\mathbb{Z}_{n} \rightarrow\mathbb{Z}/n\mathbb{Z}$ telle que $f(a)=[a]$

---

## Sous-Groupe Engendré
Soit $G$ un groupe fini et $g \in G$.

Le sous-groupe $\langle g \rangle$ engendré par $g$ est $\langle g \rangle = \{g, g^2, g^3, \dots \}$. (On peut vérifier que l'ensemble $\large \{g, g^2, g^3, \dots \}$ est effectivement un sous-groupe et donc un groupe en vérifiant toutes les propriétés des groupes)

***Exemples :*** soit $G = \mathbb{Z}_6$
1. $\langle 1 \rangle = \{1, 2, 3, 4, 5, 0, 1, \dots \} = \mathbb{Z}_6$
2. $\langle 2 \rangle = \{2, 4, 0, \dots \} \subsetneq \mathbb{Z}_6$
3. $\langle 3 \rangle = \{3, 0, \dots \} \subsetneq \mathbb{Z}_6$

***Propriétés/Théorèmes :*** 
1. Il existe $m$ tel que $g^m = \epsilon$, vu que $\langle g \rangle$ est un sous-groupe de $G$. L’ordre de $g$ est la plus petite valeur de $m$ telle que $g^m = \epsilon$, c’est-à-dire $|\langle g \rangle|$
2. Pour tout $g \in G$, l’ordre de $g$ divise $|G|$. (Résultat issu du théorème de Lagrange et du fait que $\langle g \rangle$ est un sous-groupe de $\large G$)

--- 

## Groupes cycliques

On dit que le groupe $G$ est cyclique si il existe $g$ tel que $\langle g \rangle = G$

***Propriétés/Théorèmes :*** 
1. Si $G = \langle g \rangle$ est d’ordre fini $n=|G|$, alors $g^n = \epsilon$
   
    ***Preuve :*** 
    Il doit exister $i$ tel que $g^i = \epsilon$. Vu que les éléments de $G$ se répètent pour $j > i$, il faut que $i = n$ pour que $|\langle g \rangle| = n$
    
2. ***Théorème [Euler-Fermat] :*** Si $G$ est d’ordre fini $n$, alors $g^n = \epsilon$
   
    ***Preuve :*** 
	Si $|\langle g \rangle| = m$ alors $m$ divise $n$ vu que $\langle g \rangle$ est un sous-groupe de $G$. Or, si $g^{m}=\epsilon$, on a $g^{km}=\epsilon$ pour tout $k\in \mathbb{N}$ et donc $g^{n}=\epsilon$
	
3. On dit que $G$ est cyclique si $|G| = n$. $G$ possède un unique sous-groupe $H$ d’ordre $m$ pour tout $m$ divisant $n$, et $H$ est cyclique. 
   
    ***Preuve :*** Soit $⟨g⟩ = G$. 
    
    Alors $⟨g^{n/m}⟩ = \{g^{n/m}, g^{2n/m}, g^{3n/m}, \dots , g^{(m−1)n/m}, \epsilon\}$ est un sous-groupe cyclique d’ordre $m$ de $G$. 3. 
    
    Pour vérifier l’unicité, s’intéresser à $⟨h⟩$ où $h = g^i$ et $i$ est le plus petit entier $> 0$ tel que $g^i \in H$. 

   <details>
   <summary>
   <b><i>Notation Ordre d'un élément</i></b>
   </summary>
    Dans le contexte des groupes multiplicatifs, l'ordre d'un élément $ a $ d'un groupe $ G $ est le plus petit entier positif $ n $ tel que $ a^n = 1 $, où 1 est l'élément neutre du groupe. Autrement dit, c'est le plus petit $ n $ pour lequel, effectue l'operation $ a $ par lui-même $ n $ fois, on obtient l'élément neutre.

    Plus spécifiquement, dans le groupe multiplicatif $ \mathbb{Z}^*_{13} $, l'ordre d'un élément $ a $ est le plus petit nombre entier positif $ n $ tel que $ a^n \equiv 1 \mod 13 $.

    Par exemple, si on veut trouver l'ordre de 2 dans $ \mathbb{Z}^*_{13} $, on cherche le plus petit $ n $ tel que $ 2^n \equiv 1 \mod 13 $.
   </details>


---

## Le groupe multiplicatif $\mathbb{Z}^*_p$

Soit $\mathbb{Z}^*_p = \{1, . . . , p − 1\}$ avec $p$ premier, muni de la multiplication modulo $p$

***Exemple(s) :*** $\mathbb{Z}^*_7 = \{1, 2, 3, 4, 5, 6\}$
1. $3 \times 4 = 5$
2. $3 \times 5 = 1$

***Propriétés/Théorèmes :*** 
1. $\mathbb{Z}^{*}_{p}$ est un groupe
   
    ***Preuve :***
    
    Stable : Si $p$ est premier, le produit $ij$ avec $1\leq i,j<p$ ne sera jamais un multiple de $p$. Donc $ij\neq 0$ mod $p$ et $ij\in \mathbb{Z}^{*}_{p}$
    
    Neutre : $1$ est le neutre
    
    Inverse : Soit $a\in \mathbb{Z}^{*}_{p}$, et considérons la fonction
	$f:\mathbb{Z}^{*}_{p}\rightarrow\mathbb{Z}^{*}_{p}:f(x)\rightarrow ax$, $f$ est injective : si $f(i)=f(j)$ alors $ai=aj$ mod $p$ et $ai-aj=kp$ pour $k\in \mathbb{Z}$. Or, $a,i$ et $j$ ne sont pas multiples de $p$, donc $k=0$ et $i=j$. Donc $f$ est bijective, et $\exists b:ab=1$.

---



