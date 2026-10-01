# 2.3 Subgroup

## 2.3.1 Definition and its equivalences

Definition 1.1:

Suppose $(G,*)$ is a group. $e$ is $G$'s identity. $\forall x \in H$. $x^{-1}$ refers to $x$'s inverse element under $*$.
 $H\subseteq G \and H\neq \empty$. $(H,*)$ is a group iff:

1. $\forall x,y \in H, xy\in H$
2. $e\in H$
3. $\forall x \in H, x^{-1}\in H$ 

$(H,*)$ is called a subgroup of $(G,*)$.



Theorem 1.2:

Suppose $(G,*)$ is a group. $e$ is $G$'s identity. $\forall x \in H$. $x^{-1}$ refers to $x$'s inverse element under $*$.$H\subseteq G \and H\neq \empty$. 

$(H,*)$ is a subgroup of $(G,*)$ iff $\forall a,b \in H, a*b^{-1}\in H$.

Proof:

($\longrightarrow$) 

$(H,*)$ is a subgroup,  $b\in H\rightarrow b^{-1}\in H$

Hence, $\forall a,b \in H$, $(a\in H\and b\in H) \rightarrow (a*b^{-1}\in H)$.

($\longleftarrow$) 

$H$ is not empty. $\exists a \in H, a*a^{-1} = e$. Hence $e\in H$.

$\forall a (a\in H)\rightarrow  (e*a^{-1} \in H)\rightarrow (a^{-1}\in H)$

$\forall a,b \ \ (a\in H)\and (b\in H) \rightarrow (a\in H)\and (b^{-1}\in H)\rightarrow a*(b^{-1})^{-1}\in H\rightarrow a*b \in H$

Therefore, $(H,*)$ is a subgroup subgroup of $(G,*)$.





