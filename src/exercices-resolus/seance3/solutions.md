# Solutions

## Exercice 3.7

1. Le groupe est de taille 12 et donc d'ordre 12. Une propriété des sous-groupes engendrés par $g \in G$ est que leur ordre divise l'ordre de $G$. Donc l'ordre de $g$ divise 12 (voir Sous-Groupe Engendré dans le chapitre sur les groupes). Les diviseurs de 12 sont 1, 2, 3, 4, 6 et 12. Donc les ordres possibles de $g$ sont 1, 2, 3, 4, 6 et 12.
2. $\braket{2}=\{2,4,8,3,6,12,11,9,5,10,7,1\}$, ordre $=12$
   
    $\braket{3}=\{3,9,1\}$, ordre $=3$
    
    $\braket{4}=\{4,3,12,9,10,1\}$, ordre $=6$
     
    $\braket{5}=\{5,12,8,1\}$, ordre $=4$

3. On remarque premièrement que $\braket{5}$ est un groupe (important). Comme les classes latérales forment une partition du groupe de départ et qu'elles sont de même taille, il faut qu'il y a 3 classes latérales modulo $\braket{5}$ pour arriver à une partition d'ordre $12$.
   Ces classes sont :
   
   $\braket{5}=\{5,12,8,1\}$
   
   $2\braket{5}=\{10,11,3,2\}$
   
   $4\braket{5}=\{7,9,6,4\}$
   
|               | $\braket{5}$  | $2\braket{5}$ | $4\braket{5}$ |
|---------------|---------------|---------------|---------------|
| $\braket{5}$  | $\braket{5}$  | $2\braket{5}$ | $4\braket{5}$ |
| $2\braket{5}$ | $2\braket{5}$ | $4\braket{5}$ | $\braket{5}$  |
| $4\braket{5}$ | $4\braket{5}$ | $\braket{5}$  | $2\braket{5}$ |

4. Comme tout élément de $\mathbb{Z}^{*}_{13}$ à la puissance $12$ donne $1$ (voir raisonnement de la sous-question $1$). On peut dire que $x^{2019}=5 \Leftrightarrow x^{2016}x^{3}=5\Leftrightarrow x^{3}=5$. Maintenant on peut essayer tous les éléments de $G$ pour voir lequel à la puissance $3$ donne $5$ ou on remarque que $2$ est un élément générateur et que donc tout élément de $G$ peut être exprimé comme une puissance de $2$ et donc :
   $$
  (2^{y})^{3}=2^{9} \Leftrightarrow 3y=9 \quad \text{mod}\,\,12
  $$

```admonish warning title="Pourquoi mod 12 ?"
Même si l'opérateur du groupe est définit avec mod $13$, il faut se rendre compte que chaque élément du groupe à la puissance $12$ donne le neutre et non pas $13$.
```

En ajoutant plusieurs fois $12$ à $9$ dans $3y=9$ et en regardant les valeurs possibles de $y$ on trouve $3, 7, 11$ ce qui donne des valeurs de $x$ : $8,11,7$ 
5. On a trouvé que $11=2^{7}$ donc $2^{7n}=2$ donne $7n=1\quad \text{mod\,\,12}$, ce qui donne $n=7$. Askip le fait que la solution est unique vient du fait que $\text{gcd}(7,12)=1$.


## Exercice 3.8

On calcule les puissance de $3$ dans $\mathbb{Z}^{*}_{7}$ ce qui donne : $3,2,6,4,5,1$. On en déduit que $x=2$ et $y=5$. Et donc $g^{10}=g^6 g^4=4$. Encore une fois faut bien faire gaffe de prendre le modulo $6$ et pas $7$.

