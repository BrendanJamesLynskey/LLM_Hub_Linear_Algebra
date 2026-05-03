# Linear Algebra for AI / ML

A twelve-deck presentation series that develops every piece of linear algebra a modern AI/ML engineer needs &mdash; from vectors and matrices to the SVD and tensor algebra &mdash; and lands each idea inside a transformer. The applied chapters cover up-projection and down-projection in MLPs, attention as a stochastic matrix product, LoRA / MLA / low-rank tricks, RoPE as 2D rotation, FlashAttention as a tiled GEMM, and the einsum / sharding view of large-model parallelism.

**Live index:** https://brendanjameslynskey.github.io/LLM_Hub_Linear_Algebra/

## Presentations in this series

| # | Title | Status | Description |
|---|-------|--------|-------------|
| 01 | [Vectors &amp; Vector Spaces](https://brendanjameslynskey.github.io/Linear_Algebra_AI_01_Vectors_and_Spaces/) | live | Vectors, span, basis, linear independence, dimension, coordinates &mdash; the geometric foundations behind every embedding. Interactive 2D vector playground. |
| 02 | [Matrices as Linear Maps](https://brendanjameslynskey.github.io/Linear_Algebra_AI_02_Matrices_as_Linear_Maps/) | live | A matrix is a linear map between coordinate spaces. Column picture, row picture, range &amp; null space, rank, MLP layer = matrix-vector. Interactive 2D map visualiser. |
| 03 | [Matrix Multiplication Deep-Dive](https://brendanjameslynskey.github.io/Linear_Algebra_AI_03_Matrix_Multiplication/) | live | Four equivalent views of matmul, block matrices, batched matmul, the arithmetic-intensity argument, why GEMM dominates LLM compute. Interactive matmul step-through. |
| 04 | [Inner Products, Norms &amp; Geometry](https://brendanjameslynskey.github.io/Linear_Algebra_AI_04_Inner_Products_and_Norms/) | live | Dot product, cosine similarity, L1/L2/L&infin; norms, orthogonality, Cauchy-Schwarz &mdash; the geometry behind embedding similarity and attention scores. Interactive cosine explorer. |
| 05 | [Projections &mdash; Up &amp; Down](https://brendanjameslynskey.github.io/Linear_Algebra_AI_05_Projections_Up_and_Down/) | live | Orthogonal projection, projection matrices, dimensionality lift &amp; collapse. Why transformer FFNs go up by 4&times; then back down. Interactive projection visualiser plus a working SwiGLU. |
| 06 | [Eigenvalues &amp; Eigenvectors](https://brendanjameslynskey.github.io/Linear_Algebra_AI_06_Eigenvalues_and_Eigenvectors/) | live | Eigendecomposition, the spectral theorem, power iteration, PCA, why eigenvalues control gradient flow and Jacobian conditioning. Interactive eigenvector animation. |
| 07 | [SVD, Low-Rank &amp; LoRA](https://brendanjameslynskey.github.io/Linear_Algebra_AI_07_SVD_Low_Rank_and_LoRA/) | live | Singular Value Decomposition, Eckart-Young, truncated SVD, LoRA / DoRA, DeepSeek MLA, low-rank KV-cache compression. Interactive image-rank slider. |
| 08 | [Orthogonality, QR &amp; RoPE](https://brendanjameslynskey.github.io/Linear_Algebra_AI_08_Orthogonality_QR_and_RoPE/) | live | Gram-Schmidt, QR factorisation, orthogonal matrices, condition number, weight initialisation, RoPE as a stack of 2&times;2 rotations. Interactive RoPE visualiser. |
| 09 | [Gradients, Jacobians &amp; Backprop](https://brendanjameslynskey.github.io/Linear_Algebra_AI_09_Gradients_Jacobians_Backprop/) | live | Derivative as the best linear approximation, the Jacobian, the chain rule as matrix product, JVP vs VJP, the linear-algebraic core of autograd. Interactive backprop walker. |
| 10 | [Attention as Linear Algebra](https://brendanjameslynskey.github.io/Linear_Algebra_AI_10_Attention_as_Linear_Algebra/) | live | Q, K, V as learned projections, softmax-row-stochastic attention matrix, multi-head as block-diagonal projection, masking, scale 1/&radic;d. Interactive attention playground. |
| 11 | [Transformer Block Anatomy](https://brendanjameslynskey.github.io/Linear_Algebra_AI_11_Transformer_Block_Anatomy/) | live | Walk a tensor through a full block: pre-norm, multi-head attention with all four projections, residual, FFN up-then-down with SwiGLU, residual. Every shape, every matmul. |
| 12 | [Tensors, Einsum &amp; Modern Tricks](https://brendanjameslynskey.github.io/Linear_Algebra_AI_12_Tensors_Einsum_and_Modern_Tricks/) | live | From matrices to tensors, einsum notation, batched / strided / sharded GEMMs, FlashAttention as block matmul, MoE as sparse projection, GQA as shared K/V, parameter / data / tensor parallelism. |

## Where this fits

Part of the [LLMs hub](https://github.com/BrendanJamesLynskey/LLMs) &mdash; an index of presentation series for AI/LLM engineers. This series is the mathematical foundation under the [Transformer Architecture](https://github.com/BrendanJamesLynskey/LLM_Hub_Transformer_Architecture) and [Modern Architectures](https://github.com/BrendanJamesLynskey/LLM_Hub_Modern_Architectures) sub-hubs, and the algorithmic motivation for the [NVIDIA GPU Architectures](https://github.com/BrendanJamesLynskey/LLM_Hub_NVIDIA_GPUs), [Google TPUs](https://github.com/BrendanJamesLynskey/LLM_Hub_Google_TPUs) and [CUDA Programming](https://github.com/BrendanJamesLynskey/LLM_Hub_CUDA) hubs.

## Pedagogical arc

Decks 01&ndash;04 build the language: vectors, matrices, matmul, inner products. Decks 05&ndash;09 develop the structure theorems &mdash; projection, eigendecomposition, SVD, QR, gradients &mdash; that explain *why* the transformer architecture is the shape it is. Decks 10&ndash;12 fold every piece back into a working transformer block and then scale it out across thousands of accelerators.

Every deck is a single-page interactive HTML presentation served on GitHub Pages, with KaTeX-rendered mathematics, dark-theme illustrations and at least one in-browser interactive widget. No build step; clone and open `index.html`.
