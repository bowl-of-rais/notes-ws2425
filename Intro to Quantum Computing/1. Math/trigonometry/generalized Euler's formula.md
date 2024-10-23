for self-inverse $A^{2}=I$ and $x \in \mathbb{R}$: $$e^{i A x} = \cos(x) I + i \sin(x) A$$

##### Proof
- from $A^{2}=I$, we have $A^{k} = \begin{cases}I & k \text{ even}\\A & k \text{ odd}\end{cases}$
- partition power series expansion of [[matrix exponential]]: $$\begin{align*}e^{iAx} &= I + iAx - \frac{1}{2!}I x^{2} - \frac{i}{3!} Ax^{3} + \cdots\\
  &= I \underbrace{\left(1 - \frac{1}{2!}x^{2} + \cdots\right)}_{\cos(x)}+ iA \underbrace{\left(x - \frac{1}{3!}x^{3} + \cdots\right)}_{\sin(x)}
  \end{align*}$$
##### <br>
---

see [[Euler's formula]]
