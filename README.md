# Asymptotic Equivalences

In the lectures, we said that logarithms with different bases don't affect the
asymptotic complexity of an algorithm. Prove that $O(\log_{2} n)$ is the same as
$O(\log_{5} n)$. Use the mathematical definition of $O$ -- do a formal proof,
not just the intuition.

I have started with the formal definition of $O$ below. Add your answer to this
markdown file. [This
page](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
might help with the notation for mathematical expressions.

If $T(n) \in O(f(n)) \land T(n) \in O(g(n))$ then $O(f(n)), O(g(n))$ are the same.


$(T(n) \in O(\log_{2} n) \implies (T(n) \in O(\log_{5} n)$

$(\exists (c, n_0)>0:T(n) \le c \cdot \log_2 n, \forall n \ge n_0) \implies (\exists ((x, z_0)>0): T(z) \le x \cdot \log_5 z, \forall z \ge z_0)$

$(\forall c, n_0)(\exists x, z_0)(\forall z \ge z_0)(\exists n \ge n_0) [(T(n) \le c \cdot \log_2 n) \implies (T(z) \le x \cdot \log_5 z)]$ {migrate quantifiers}

Remove quantifiers: $\forall$ s are just replaced with their variable name. For $\exists$ everything but x will be choice of a for all variable written of the form for x choice of y = $y_c$

$x= c \cdot \log_2 5$

$(T(z_c) \le c \cdot \log_2 z_c) \implies (T(z) \le c \cdot \log_2 5 \cdot \log_5 z)$

$(T(z_c) \le c \cdot \log_2 z_c) \implies (T(z)) \le c \cdot \log_2 z)$ {right hand simplifies due to property of logs}

$True$ { $z_c = z$ therefore true by propositional reasoning}

Sources:
https://www.youtube.com/watch?v=MY-VCrQCaVw 
 Video that helped me better grasp why they are equivalent.

 I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice.
