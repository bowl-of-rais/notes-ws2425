- [x] TODO spectral decomposition ✅ 2024-10-19

any [[normal matrix]] $A \in \mathbb{C}^{n \times n}$ is **unitarily diagonalizable**, meaning there is a [[unitary matrix]] $U = (u_{1} \vert \cdots \vert u_{n})\in \mathbb{C}^{n \times n}$ of eigenvectors as columns and corresponding [eigenvalues](eigenvalues%20and%20eigenvectors.md) $\lambda_{1}, \dots, \lambda_{n}\in \mathbb{C}$ s.t. $$A = U \begin{pmatrix}\lambda_{1} & & \\ & \ddots & \\ & & \lambda_n\end{pmatrix}U^{\dagger}$$aka $$A u_{i} = \lambda_{i} u_{i} \forall i = 1, \dots, n$$
- every matrix representable like this is normal
- eigenvalues do not need to be distinct
- rewrite: $Av = \sum\limits_{i=1}^{n} \lambda_{i}u_{i} \langle {u_{i}} \vert {v} \rangle$
- generalized decomposition: [Jordan normal form](https://en.wikipedia.org/wiki/Jordan_normal_form)
