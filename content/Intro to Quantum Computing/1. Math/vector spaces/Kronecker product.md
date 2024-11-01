$$A \otimes B = \begin{pmatrix}{a_{11}B}&{a_{12}B}&{\cdots}&{a_{1n}B}\\{a_{21}B}&{a_{22}B}&{\cdots}&{a_{1n}B}\\\vdots&{\ddots}&{\ddots}&{\vdots}\\{a_{m1}B}&{a_{m2}B}&{\cdots}&{a_{mn}B}\end{pmatrix} \in \mathbb{C}^{mp\times n1}$$for $A \in \mathbb{C}^{m\times n}$, $B \in \mathbb{C}^{p\times q}$

# Properties

- [x] TODO properties of kronecker product 📅 2024-11-03 ✅ 2024-10-30
##### Complex conjugation
is done elementwise:
$$(A \otimes B)^{*} = A^{*} \otimes B^{*}$$
##### Transposition
$$(A \otimes B)^{T} = A^{T} \otimes B^{T}$$
##### Conjugate transpose
$$(A \otimes B)^{\dagger} = {A}^{\dagger} \otimes {B}^{\dagger}$$
##### Associativity
$$(A\otimes B)\otimes C = A \otimes (B \otimes C)$$
##### Matrix-matrix multiplication
$$(A \otimes B) \cdot (C \otimes D)$$
##### Hermitian matrices

>[!conc] Kronecker product of Hermitian matrices is Hermitian

- see [[Hermitian matrix]]
##### Unitary matrices

>[!conc] Kronecker product of unitary matrices is unitary

- see [[unitary matrix]]

-----
# Python uwu

```python
np.kron(A, B)
```

----

[WIkipedia](https://en.wikipedia.org/wiki/Kronecker_product)