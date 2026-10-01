## GTM 6.7 2

### 01.  Definition Raised  by A Toy Model 

Consider a language $\mathcal L$ **with only one  constant** and no function symbols with the simplest alphabet $\mathcal A = \{\mathcal V,\mathcal C,\mathcal O,\mathcal R\}$ = $\{\{x_n\},\{c\},\empty,\{r^i_j\}\}$.

Suppose $\mathcal M = \{a,b\}$ serves as a domain of $\mathcal L$. 
Consider interpretation $\phi_L(\mathcal M)$:
$c\longmapsto a$
$r\longmapsto \{(b)\}$ 

Let $\mathrm P(x)$ denote $r(x)$.
Obviously, $\exists x\mathrm P(x)$ is true **but there's no constant $c$ to make $\mathrm P(c)$ true**. 
Otherwise, we cannot talk about $b$ directly because we cannot name it.

In other words, there's no constant make $\exists x\mathrm P(x)\Rightarrow \mathrm P(c)$ true under $\phi_\mathcal L(\mathcal{M})$

Let:
$r_1\longmapsto \{(a)\}$ 
$r_2\longmapsto \{(b)\}$ 

Let $\mathrm P_1(x),\mathrm P_2(x)$ denote $r_1(x),r_2(x)$.
Consider $\mathcal E = \{\exists x\mathrm P_1(x)\Rightarrow \mathrm P_1(c_1),\exists x\mathrm P_2(x)\Rightarrow \mathrm P_2(c_2)\}$
As there's only one constant in $\mathcal A$, **$c_1$ and $c_2$ are necessarily equivalent**, breaking the expressive strength of $\mathcal E$.

Let us observe the structure of $\phi_L(\mathcal M)$ and **try to translate its contradictory into syntactic property**.
The dilemma above actually comes from that there's no element satisfies $\mathrm P_1,\mathrm P_2$ both, which can be described as $\forall x\neg(\mathrm P_1(x)\and \mathrm P_2(x))$.

To be simple, let $\mathrm R_{\mathrm P_1} = \exists x\mathrm P_1(x)\Rightarrow \mathrm P_1(c_1)$，$\mathrm R_{\mathrm P_2} = \exists x\mathrm P_2(x)\Rightarrow \mathrm P_2(c_2)$
Let us reconsider $\mathcal E = \{\forall x\neg(\mathrm P_1(x)\and \mathrm P_2(x)),\exists x\mathrm P_1(x),\exists x\mathrm P_2(x)\}$ 
Expand $\mathcal E$ to $\mathcal E' = \mathcal E\cup \{\mathrm{R_{P_1}},\mathrm{R_{P_2}}\}$. If $c_1$ is equivalent to $c_2$, $\mathcal E'$ is not consistent. 

Otherwise, the consistency of $\mathcal E'$ requires more constants in $\mathcal A$. 
From this point on, **the argument becomes purely syntactic**.

> **Definition 1: 'sufficient':**^1^
> Suppose $\mathcal L$ is a language and $\mathcal E$ is a formulas set on it.
> $\mathcal E$ is sufficient iff 
> 1 ) For every closed formula $\exists x\mathrm P (x)\in \mathcal E$ with $\mathrm P$ having at most one free variable, there exists a constant $c$, $\exists x\mathrm P(x)\Rightarrow \mathrm P(c) \in \mathcal E$.
> 2 ) $\mathcal E$ is consistent 

Risk in the toy model is processed into a requirement on the pair (formula set, alphabet):
Every asserted existential statement must have its witness formula present without breaking consistency, implying the numbers of constants sometimes.

### 02 Expansion of $\mathcal L$

It can be seen that the lack of constant leads to loss of 'expressive strength'.
Naturally, we wonder whether we can **add enough constant to $\mathcal A$ in a proper way** without loss of 'good property' like consistency and completeness. 
( According to 6.6, a consistent formulas set can be expanded to a complete set, so we only concern about consistency here. )

Know that $\mathcal E$ is a consistent formula in $\mathcal L$. 
( Self-evidently, $\mathcal E\cup\mathrm {Ax}\mathcal  L$ is also consistent. Hence, we need not to require $\mathrm {Ax}\mathcal L\subseteq\mathcal E$ )

Fortunately, 'adding constant' does not break the consistency^2^ of $\mathcal E$: 

> **Lemma 1** :
> Consider a language $\mathcal L$ with alphabet $\mathcal A$. $\mathcal E$ is a consistent set on it.
> $\mathrm C = \{\mathrm c_i\}$ consists of arbitrary numbers of constants. 
>
>  In language $\mathcal L'$ represented by $\mathcal A' = \mathcal {A}\cup \mathrm C$, 
> $\mathcal E' = \mathcal E\cup \mathrm {Ax}\mathrm L'$ is also consistent.

Therefore, we may adjoint as many constants as possible until every formula with single variable like $\mathrm P(x)$ gains an unique constant $c_\mathrm P$.

As $\{\mathrm P(x)\}$ is a subset of $\mathrm{Formula }(\mathcal  L')$, a family of finite subsets of $\mathcal A$, $\mathrm {card}(\{\mathrm P(x)\}) \leq \mathrm {card}(\mathcal A ) +\aleph _0$.^3^

Let us 'add' $\mathrm {card}(\mathcal A ) +\aleph _0$ constants to $\mathcal A$:
Suppose $\mathrm C$ consists of $\mathrm {card}(\mathcal A ) +\aleph _0$ constants. Consider $\mathcal L'$ represented by $\mathcal A' = \mathcal {A}\cup \mathrm C$.
As for **Lemma 1**, $\mathcal E' = \mathcal E\cup\mathrm {Ax}\mathcal L'$ is consistent.

### 03 Sufficiency In New Language $\mathcal L'$

We know construct a sufficient set based on $\mathcal E'$.
The first problem we meet is that without knowing the exact member of $\mathcal E'$, we cannot judge how much 'witness formulas' should be adjoined into $\mathcal E'$. 
As for a trivial example,to be processed to a sufficient set, $\mathcal E_1 = \{\exists x\mathrm P_1(x)\}$ only needs one more witness formula. But obviously we could not repeat this operation to other consistent set.

We solve this problem by a proof sufficient for the purpose.
We assign a constant $c_\mathrm P$ for every formula with at most one free variable like $\mathrm P(x)$.
Consider $\mathrm R = \{\exists x\mathrm P(x)\Rightarrow \mathrm P(c_\mathrm P)| \ \ \mathrm P(x)\in \mathrm{Formula}(\mathcal L')\}$.
Notice that the assignment $\mathrm P \longmapsto c_\mathrm P$ is **injective**, so each constant occurs in exactly one member of R  (its own witness formula).

Now we prove $\mathcal  E'\cup \mathrm R$ is consistent and sufficient by induction.
As all witness formulas added, sufficiency would be automatically satisfied when consistency is proved.

Let $\mathcal W_i := \exists x\mathrm{P}_i(x)\Rightarrow \mathrm P_i(c_i)$.
Suppose witness formulas are all listed in $(\mathcal W_1, \mathcal W_2,...\mathcal W_n,...)$ (possible since $|\mathrm R|\leq \mathrm{card} \mathcal A+\aleph_0$, well-ordered if uncountable). 
Let $\mathcal E_0 =\mathcal E',\mathcal E_1 = \mathcal E'\cup\{\mathcal W_1\},\mathcal E_2 = \mathcal E_1\cup\{\mathcal W_2\}$ and so on. 

Now we prove that: $\mathcal E_n$ is consistent $\Longrightarrow$  $\mathcal{E}_{n+1}$ is consistent

​	Assume that $\mathcal E_n$ is consistent and $\mathcal E_{n+1}$ is not.
​	$\mathcal E_{n}\cup \{\mathcal W_{n+1}\}\vdash \mathcal W_{n+1}$, $\mathcal E_{n}\cup \{\mathcal W_{n+1}\}\vdash \neg\mathcal  W_{n+1}$

> Lemma 2:
> Suppose $A,B$ are formulas in a language.
> $A\Rightarrow B \vdash \neg A\or B$
> $\neg(A\Rightarrow B )\vdash  A\and \neg B$

​	Hence, $\mathcal E_{n}\vdash \neg\mathcal  W_{n+1}$ means $\mathcal E_{n}\vdash \exists x\mathrm P_{n+1}(x)$ and $\mathcal E_{n}\vdash \neg \mathrm P_{n+1}(c_{n+1})$

> Lemma 3: Constant Lemma
> Suppose $\Gamma$ is a formulas set of a language, and constant $c$ has never happened in any member of $\Gamma$.
> If $\Gamma \vdash \mathrm P(c)$, then $\Gamma \vdash \forall x \mathrm P(x)$

​	According to $\mathcal E_{n}\vdash \neg\mathrm P_{n+1}(c_{n+1})$, we know that $\mathcal E_{n}\vdash \forall x\neg\mathrm P_{n+1}(x)$. 
​	Assumption fails. $\mathcal{E}_{n+1}$ is consistent

As $\mathcal E_0$ is consistent, we may say, by induction, $\mathcal E_1,\mathcal E_2,...$ are consistent.
Let $\mathcal E^* =\bigcup \limits_n \mathcal E_n$.
As consistent set is not closed under union, we need to a further proof of $\mathcal E^*$'s consistency:
	Assume $\mathcal E^* =\bigcup \limits_n \mathcal E_n$ is inconsistent, then there exists two deductions leading to contradiction.
	Following the proof of 6.6, there exists a $\mathcal E_k$ that includes all formulas in two contradictory deductions. 	
	Hence $\mathcal E_k$ is inconsistent. Assumption fails.

Obviously, $\mathcal E^*$ is also sufficient by **Definition 1**.

In this way, we gain the method to construct a sufficient set based in a language with harmless operation on alphabet.
