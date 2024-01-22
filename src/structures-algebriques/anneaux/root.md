## Anneau
Un **anneau** est une structure $(A, +, \cdot)$ telle que :
- $(A, +)$ est un ***groupe commutatif*** — on écrit $0$ pour son neutre.
- $(A, \cdot)$ est un ***monoïde*** — on écrit $1$ pour son neutre.
- La multiplication se distribue sur l'addition, à gauche et à droite :
   $$
   x \cdot (y + z) = x \cdot y + x \cdot z \quad \forall x, y, z \in A
   $$
   $$
   (x + y) \cdot z = x \cdot z + y \cdot z \quad \forall x, y, z \in A
   $$

Un anneau est ***commutatif*** si la multiplication est commutative.

***Exemple(s) :***
1. $\mathbb{Z}, \mathbb{R}, \mathbb{Q}, \mathbb{C}$ munis des opérations habituelles.
2. $\mathbb{R}[X]$, l’ensemble des polynômes à coefficients réels.
3. $\mathbb{R}^{n \times n}$ — non commutatif quand $n \geq 2$.

***Propriété(s) :***
1. $0$ est absorbant : $\forall r,0\cdot r=r\cdot0=0$
     On voit : $r=r\cdot 1=r\cdot(1+0)=r+0\cdot r\Rightarrow0=0\cdot r$
2. Si $A$ est un anneau et $0=1$ alors $A=\{0\}$
     On voit : $r=r\cdot1=r\cdot0=0$ pour tout $r\in A$
3. Si $(A,+,\cdot)$ est un anneau tel que $0\neq 1$, alors $(A,\cdot)$ n'est pas un groupe. On voit : $0$ n'est pas inversible, vu qu'il est absorbant

## L'anneau $Z_n$
L'anneau $Z_n$ est défini comme:
$$
Z_n = \{0, 1, \ldots, n-1\}
$$
muni de l'addition modulaire et de la multiplication modulaire forme un anneau commutatif.

***Proposition(s) :***

1. Si $n$ est premier, alors $Z_n$ est un corps, souvent noté $F_n$.
2. Si $n$ est composé, alors $Z_n$ n'est pas un corps.

***Preuve :***

Soit $a \neq 1$ divisant $n$ et $b = \frac{n}{a}$. 
$$
Alors \quad ab \equiv 0 \mod n
$$
ce qui veut dire que $a$ est un diviseur de 0 et n'est donc pas inversible.

***Corollaire :***

Un élément $a \in Z_n$ est inversible si et seulement si:
$$
gcd(a, n) = 1
$$

***Preuve :***

Si $gcd(a, n) \neq 1$, alors 
$$
a \cdot \frac{n}{gcd(a,n)} \equiv 0 \mod n
$$
Si $gcd(a, n) = 1$ alors $an$ est le premier multiple de $a$ qui est un multiple de $n$, et $a$ ne divise donc pas 0.