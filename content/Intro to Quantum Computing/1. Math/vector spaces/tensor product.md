>[!info] combination $V \otimes W$ of two (arbitrary) vector spaces $V$ and $W$ containing linear combinations of tensor products $v \otimes w$ with $v\in V, w \in W$

examples for our purposes:
- usually $V = \mathbb{C}^{2}, W = \mathbb{C}^{2}, V\otimes W = \mathbb{C}^{2} \otimes \mathbb{C}^{2}$
- $\vert 0\rangle \otimes \vert 0\rangle = \vert 00\rangle$

>[!goal] See this [blog post](https://www.math3ma.com/blog/the-tensor-product-demystified) for a bit of an intuition. 
>TL;DR: tensor products are kinda like doing cartesian-style products with vectors (aka multiplying each entry of one vector with each entry of the others) or a vector version of the [[Kronecker product]].
>
>This is similar to the [outer product](https://en.wikipedia.org/wiki/Outer_product), but the outer product results a matrix, and we really like our vectors (e.g. two-qubit states should still be vectors) - so we define this operation that gives us a vector (in typical mathematician "ich mach mir die Welt wie sie mir gefällt" fashion).

# Basis

for $V\otimes W$, we have a basis $$\{\vert{i}\rangle_{V} \otimes \vert{j}\rangle_{W}:i=1, \dots, m, j=1, \dots, n\}$$where
- $\{\vert{i}\rangle_{V} : i = 1,\dots, m\}$ is a basis of $V$
- $\{\vert{j}\rangle_{W} : j = 1,\dots, n\}$ is a basis of $W$

it holds that $$\dim(V \otimes W) = \dim(V) \cdot \dim(W)$$

NOTE: $\vert{i}\rangle_{V} \otimes \vert{j}\rangle_{W}$ is generally also written as $\vert{i}\rangle \vert{j}\rangle$ or $\vert{ij}\rangle$ -> this is where the $\vert 00\rangle$ comes from!

# Properties
-> these are just properties of any [bilinear map](https://en.wikipedia.org/wiki/Bilinear_map), which $\otimes$ should be

#### "Multiply a scalar wherever"

for $\vert{v}\rangle\in V, \vert{w}\rangle\in W, \alpha \in \mathbb{C}$: $$\alpha(\vert{v}\rangle\otimes \vert{w}\rangle) = (\alpha \vert{v}\rangle)\otimes \vert{w}\rangle = \vert{v}\rangle \otimes (\alpha \vert{w}\rangle)$$
#### Additivity

for $\vert{v_1}\rangle, \vert{v_2}\rangle \in V$ and $\vert{w}\rangle \in W$: $$(\vert{v_{1}}\rangle + \vert{v_{2}}\rangle) \otimes \vert{w}\rangle = \vert{v_{1}\rangle}\otimes \vert{w}\rangle + \vert{v_2}\rangle \otimes \vert{2}\rangle$$
and for $\vert{v}\rangle\in V$ and $\vert{w_{1}}\rangle, \vert{w_{2}}\rangle \in W$: $$\vert{v}\rangle \otimes (\vert{w_{1}}\rangle + \vert{w_{2}}\rangle) = \vert{v\rangle}\otimes \vert{w_{1}}\rangle + \vert{v}\rangle \otimes \vert{w_{2}}\rangle $$

# Vector notation

for $$\begin{align*}
\vert{v}\rangle &= v_{1} \vert 0\rangle + v_{2} \vert 1\rangle = \begin{pmatrix}{v_{1}}\\{v_{2}}\end{pmatrix}\\
\vert{w}\rangle &= w_{1} \vert 0\rangle + w_{2} \vert 1\rangle = \begin{pmatrix}{w_{1}}\\{w_{2}}\end{pmatrix}
\end{align*} $$we have $$\begin{align*}
\vert{v}\rangle \otimes \vert{w}\rangle &= (v_{1} \vert 0\rangle + v_{2}\ \vert 1\rangle) \otimes (w_{1} \vert 0\rangle + w_{2}\vert 1\rangle )\\
&= v_{1}w_{1} \vert 00\rangle + v_{1}w_{2} \vert 01\rangle + v_{2}w_{1} \vert 10\rangle + v_{2}w_{2} \vert 11\rangle 
\end{align*}$$
and using $$\vert 00\rangle = \begin{pmatrix}1\\0\\0\\0\end{pmatrix}, \vert 01\rangle = \begin{pmatrix}0\\1\\0\\0\end{pmatrix} , \vert 10\rangle = \begin{pmatrix}0\\0\\1\\0\end{pmatrix}, \vert 11\rangle = \begin{pmatrix}0\\0\\0\\1\end{pmatrix}$$we get $$\begin{pmatrix}{v_{1}}\\{v_{2}}\end{pmatrix} \otimes \begin{pmatrix}{w_{1}}\\{w_{2}}\end{pmatrix} = \begin{pmatrix}{v_{1}w_{1}}\\{v_{1}w_{2}}\\{v_{2}w_{1}}\\{v_{2}w_{2}}\end{pmatrix} $$
##### General version
$$\begin{pmatrix}{v_{1}}\\{\vdots}\\{v_{m}}\end{pmatrix} \otimes \begin{pmatrix}{w_{1}}\\{\vdots}\\{w_{n}}\end{pmatrix} = \begin{pmatrix}{v_{1}w_{1}}\\{\vdots}\\{v_{1}w_{n}}\\\vdots\\{v_{m}w_{1}}\\{\vdots}\\{v_{m}w_{n}}\end{pmatrix}$$

# Inner product

if $V, W$ have inner products $\langle{\cdot}\vert \cdot \rangle$, an inner product on $V \otimes W$ can be defined by $$\left\langle \sum\limits_{j} \alpha_{j} \vert{v_{j}}\rangle \vert{w_{j}}\rangle \middle\vert \sum\limits_{k}\beta_{k} \vert{\tilde{v}_{k}}\rangle \vert{\tilde{w}_k}\rangle \right\rangle := \sum\limits_{j} \sum\limits_{k} \alpha^{*}_{j} \beta_{k} \langle{v_{j}}\vert{\tilde{v}_{k}}\rangle \langle{w_{j}}\vert{\tilde{w}_{k}}\rangle $$
-> combine inner products in $V$ and $W$ spaces


----

see [Wikipedia](https://en.wikipedia.org/wiki/Tensor_product)