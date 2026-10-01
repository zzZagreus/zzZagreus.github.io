# 1 GTM 53 interpretation 定义重写

Suppose $L$ is a language in $\mathfrak L_1$. An interpretation of $L$ is denoted by a binary tuple $(M,\phi)$. $M$ is a nonempty set from where all the 'meanings' comes from.

$\phi$ is a class of functions, turning meaningless symbols in $L$ into elements in $M$, or structure related to it.

Why can such tuples called a 'interpretation'?

Let's recall what decides a language: variables, constants and operations. More specifically, symbols prepared for them. Suppose they're respectively denoted by $V_L, C_L, O_L$.

Imagine we're in a course of solving equations, we all know that $x, y$ on paper are variables, as textbook has told us.

Mathematical logic demands u to forget these 'variables' for now, and imagine an object 'without meaning': not a numbers, a set, a tuple nor any structure u can tell. What it calls 'variables' in a language $L$, also denoted by $x$ in most logic textbooks, actually means 'something hasn't but finally will become some mathematics object'.

All u should know it is that: They're waiting, and it has the possibility, like superhero before awakening.

Waiting for what? Possibility to what?

Can we just be simple and clean and drop out this fucking redundant description? Actually, that's textbook has done. While they're gaining generality and 'being clean', readers pay for it. QAQ

Back to the point, interpretation $(M,\phi)$ is exactly what 'variables' are waiting.

Suppose $V_L$ consists of all variables in $L$. Consider a function $f: V_L \longrightarrow M$. Functions like $f$ assign meanings to variables. In this way, its waiting ends.

If $M$ represents nature numbers, then variables become corresponding numbers. If a class of set, then they become sets.

Hence, $F = \{f_V \mid f_V: V_L \longrightarrow M\}$ seems like interpreters for $L$. But is this enough?

Don't forget that constants and operations are still 'waiting', eager for functions to give them meaning, point them precisely to elements in $M$.

Consider functions $f_c: C_L \longrightarrow M$ and $f_O: O_L \longrightarrow \mathrm O(M)$.

$\mathrm O(M)$ refers to the set of operations on $M$.

Hence, with such $f_V, f_C, f_O$ fixed, every terms can be translated into elements in $M$.

Consider $f: L \longrightarrow M$:

$$f(m) = \begin{cases} f_V(m), & \text{if } m \in V_L \\ f_C(m), & \text{if } m \in C_L \\ f_O(m), & \text{if } m \in O_L \end{cases}$$

Remember that formulas are what we finally need to deal with. As rules for generating formulas are known. They are fixed by choice of terms.

Consider atomic formula $\mathrm P = r(t_1, t_2, \ldots t_n)$. With function $f$ above, we're able to turn all $t_1, t_2, \ldots t_n$ into elements in $M$, gaining a tuple $t^f = (f(t_1), f(t_2), \ldots f(t_n))$. Also, symbols $r$ is also correlated to a relation on $M$: $f(r) \subseteq M^n$. Now we can exactly tell whether $t^f$ is in $f(r)$, otherwise, 'true or false' of formula $\mathrm P$.

然后，用上一点代数技巧，所有的 formulas 都能判断'真伪'了。

书 P25 懒得拍。

Hence, to make all formulas 'meaningful', all we need are just $f$ compounded by $f_V, f_C, f_O$. A interpretation of $L$ in $M$ is actually decided by tuple $(f_V, f_C, f_O)$, which provides a corresponding function $\mathrm J: F_L \longrightarrow \{0,1\}$, telling the 'true or false' for every formulas of $L$.

So u can say 'an interpretation is a triple like $(f_V, f_C, f_O)$ ...' or 'an interpretation is binary tuple $(f_C, f_O)$ where process for variables keep unfixed temporarily for its specialty', the latter is what GTM53 does.

While the boundary of a concept differs a little from text to text, the key takeaway is that this construction enables us to give meaning to formulas and make them not just syntactically decidable, but also truth-evaluable semantically.

In this book, an interpretation of $L = (V_L, C_L, O_L)$ is denoted by a binary tuple $(M, \phi)$.

$M$ is a nonempty set and $\phi = \{f_c: C_L \longrightarrow M, f_O: O_L \longrightarrow M\}$. Let $\overline{M} = (M,\phi)$. $\phi$ is called the primary mappings of $\overline M$.
