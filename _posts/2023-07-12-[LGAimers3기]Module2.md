---
layout: single
title: "[LG Aimers 3기] Module 2. Mathematics for ML"
categories: LGAimers
tag: [AI, MachineLearning]
use_math: true
author_profile: false
---

## 1. Matrix Decompositions
### 1) Determinant and Trace

<span style="font-size:95%">**Determinant**</span>  
<span style="font-size:80%">
For a matrix $A\in \mathbb{R}$, for all $j = 1, \cdots ,n$,  
&nbsp;&nbsp;1. Expansion along column $j$ : <span style="font-size:90%"> $det(A) = \displaystyle\sum_{k=1}^{n} (-1)^{k+j}\,a_{kj}\,det(A_{k,j})$</span><br>
&nbsp;&nbsp;2. Expansion along row $j$ : <span style="font-size:90%"> $det(A) = \displaystyle\sum_{k=1}^{n} (-1)^{k+j}\,a_{jk}\,det(A_{j,k})$</span></span>

<span style="font-size:80%">
&nbsp;&nbsp;<span style="color:red">Theorem</span>. <span style="font-size:90%"> $det(A) \neq 0 \iff rk(A) = n \iff A$  is invertible</span></span>

<span style="font-size:78%">
&nbsp;&nbsp;(1) $det(AB) = det(A)\,det(B)$  
&nbsp;&nbsp;(2) $det(a) = det(A^T)$  
&nbsp;&nbsp;(3) For a regular $A$, $det(A)^{-1} = 1/det(A)$  
&nbsp;&nbsp;(4) For two similar matrices $A$, $A'$ ( i.e., $A' = S^{-1}AS$ for some $S$ ),  $det(A) = det(A')$  
&nbsp;&nbsp;(5) For a triangular matrix $T$, $det(T) = \prod_{i=1}^{n}T_{ii}$  
&nbsp;&nbsp;(6) Adding a multiple of a column/row to another one does not change $det(A)$  
&nbsp;&nbsp;(7) Multiplication of a column/row with $\lambda$ scales $det(A)$ : $det(\lambda A) = \lambda^nA$  
&nbsp;&nbsp;(8) Swapping two rows/columns changes the sign of $det(A)$</span>


<span style="font-size:95%">**Trace**</span>  
<span style="font-size:80%">
The trace of a square matrix $A\in \mathbb{R}^{n \times n}$ is defined as  
<span style="font-size:90%">$tr(A) := \displaystyle\sum_{i=1}^{n} a_{ii}$</span></span>

<span style="font-size:78%">
&nbsp;&nbsp;(1) $tr(A + B) = tr(A) + tr(B)$  
&nbsp;&nbsp;(2) $tr(\alpha A) = \alpha tr(A)$  
&nbsp;&nbsp;(3) $tr(I_n) = n$  </span>

---
### 2) Eigenvalues and Eigenvectors
<span style="font-size:95%">**Definition**</span>  
<span style="font-size:80%">
Consider a square matrix $A \in \mathbb{R}^{n \times n}$. Then, $\lambda \in \mathbb{R}$ is an **eigenvalue** of $A$ and $x \in \mathbb{R}^n\setminus\begin{Bmatrix}0\end{Bmatrix}$ is the corresponding **eigenvector** of $A$ if</span>  
<span style="font-size:80%">$Ax = \lambda x$</span>

<span style="font-size:80%">
&nbsp;&nbsp;<span style="color:red">Determinant</span>. For (possibly repeated) eigenvalues $\lambda_i$ of $A \in \mathbb{R}^{n \times n}$, $det(A) = \prod_{i=1}^{n}\lambda_i$  
&nbsp;&nbsp;<span style="color:red">Trace</span>. For (possibly repeated) eigenvalues $\lambda_i$ of $A \in \mathbb{R}^{n \times n}$, $tr(A) = \sum_{i=1}^{n}\lambda_i$</span>  

---
### 3) Cholesky Decomposition
<span style="font-size:95%; color:red">**Theorem**</span>  
<span style="font-size:80%">
For a symmetric, positive definite matrix $A$, $A = LL^T$, where<br>
&nbsp;&nbsp;- $L$ is a lower-triangular matrix with positive diagonals  
&nbsp;&nbsp;- Such a $L$ is unique, called <span style="color:blue">Cholesky factor</span> of $A$</span>  

---
### 4) Eigendecomposition and Diagonalization
<span style="font-size:95%; color:red">**Diagonal matrix**</span>  
<span style="font-size:80%">
zero on all off-diagonal elements,
$D = \begin{pmatrix} d_1 & \cdots & 0 \\\ \vdots &  & \vdots \\\ 0 & \cdots & d_n \end{pmatrix}$  
<br>
&nbsp;&nbsp;$D^k = \begin{pmatrix} d_1^k & \cdots & 0 \\\ \vdots &  & \vdots \\\ 0 & \cdots & d_n^k \end{pmatrix}$,
   $D^{-1} = \begin{pmatrix} 1/d_1 & \cdots & 0 \\\ \vdots &  & \vdots \\\ 0 & \cdots & 1/d_n \end{pmatrix}$,
   $det(D) = d_1d_2 \cdots d_n$</span>

<span style="font-size:95%; color:red">**Diagonalization**</span>  
<span style="font-size:80%">
$A \in \mathbb{R}^{n \times n}$ is **diagonalizable** if it is imilar to a diagonal matrix $D$, i.e., $\exists$ an **invertible** $P \in \mathbb{R}^{n \times n}$, such that $D = P^{-1}AP$.  
$A \in \mathbb{R}^{n \times n}$ is **orthogonally diagonalizable** if it is imilar to a diagonal matrix $D$, i.e., $\exists$ an **orthogonal** $P \in \mathbb{R}^{n \times n}$, such that $D = P^{-1}AP = P^TAP$.  ( orthogonal $P$ : $PP^T = I$ )</span>  

<span style="font-size:95%; color:red">**Theorem**</span>  
<span style="font-size:80%">
$A \in \mathbb{R}^{n \times n}$ is **orthogonally diagonalizable** $\iff$ $A$ if symmetric.</span>  

<span style="font-size:95%; color:red">**Spectral Theorem**</span>  
<span style="font-size:80%">
If $A \in \mathbb{R}^{n \times n}$ is symmetric,  
&nbsp;&nbsp;(a) the eigenvalues are all real.  
&nbsp;&nbsp;(b) the eigenvectors to different eigenvalues are perpendicular.  
&nbsp;&nbsp;(c) there exists an orthogonal eigenbasis.</span>  

---
### 5) Singular Value Decomposition
<span style="font-size:95%; color:red">**Theorem**</span>  
<span style="font-size:80%">
$A \in \mathbb{R}^{m \times n}$ with rank $r \in [0, min(m,n)]$. The SVD of $A$ is a decomposition of the form  
$A = U \Sigma V^T$  
with and orthogonal matrix $U = (u_1, \cdots, u_m) \in \mathbb{R}^{m \times m}$ and an orthogonal matrix $V = (v_1, \cdots, v_n) \in \mathbb{R}^{n \times n}$. Moreover, $\Sigma$ is an $m \times n$ matrix with $\Sigma_{ii} = \sigma_i \geq 0$ and $\Sigma_{ij} = 0, i \neq j$, which is uniquely determined for $A$.</span>

<span style="font-size:78%">
**Note**  
&nbsp;&nbsp;- The diagonal entires $\sigma_i, i = 1, \cdots, r$ are called <span style="color:blue">singular values</span>.  
&nbsp;&nbsp;- $u_i$ and $v_j$ are called left and right singular vectors, respectively.</span>

<br>
<br>

## 2. Convex Optimization
### 1) Optimization Using Gradient Descent