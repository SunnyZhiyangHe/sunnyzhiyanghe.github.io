---
title: "Round-Robin CCZ Is All You Need"
permalink: /round_robin_ccz/
author_profile: true
robots: index,follow
scholar:
  title: "Round-Robin CCZ Is All You Need"
  authors:
    - "He, Zhiyang"
    - "Menon, Varun"
    - "Yoder, Theodore J."
  date: "2026/06/17"
  pdf_url: "https://sunnyzhiyanghe.github.io/files/Notes/Round-robin-CCZ.pdf"
  language: en
  keywords: "quantum error correction; CSS codes; logical CCZ gates; round-robin circuits; stabilizer codes; fault tolerance"
  # institution: "Massachusetts Institute of Technology"
---

Zhiyang He, Varun Menon, Theodore J. Yoder &mdash; June 17, 2026.
[[PDF]](https://sunnyzhiyanghe.github.io/files/Notes/Round-robin-CCZ.pdf) [[blog post]](/blog/round-robin-ccz/)

<!-- 
## Abstract

Round-robin entangling gates are a primitive for implementing logical gates on
stabilizer codes non-transversally. For qubit sets $$A, B, C$$, the round-robin gate
$$\text{CCZ}(A, B, C)$$ applies a physical CCZ to every triple
$$(a, b, c) \in A \times B \times C$$. When $$A, B, C$$ are the supports of three $$Z$$
logical operators, $$\text{CCZ}(A, B, C)$$ enacts a logical CCZ. When any one of them is
the support of a $$Z$$ stabilizer, it preserves the code space and acts trivially. In this
note, we prove that on any CSS code, round-robin CCZ is all you need: every
code-space-preserving CCZ circuit factors into a product of round-robin CCZ circuits, in
each of which either all three sets are $$Z$$ logical operators or at least one is a $$Z$$
stabilizer. The proof is elementary and constructive: it yields a polynomial-time
algorithm that returns the decomposition. The same argument carries over verbatim from
CCZ to general $$\text{C}^r\text{Z}$$. This characterization offers a combinatorial
perspective on the design of codes with low-depth logical CCZ gates: existing frameworks,
such as algebraic code families and topological properties, can be re-examined as
conditions that enable effective cancellation within products of simple round-robin
circuits. The proof of this observation was derived by Claude Opus 4.8 and verified in
Lean by an auto-formalization model MerLean. -->

<iframe
  src="https://sunnyzhiyanghe.github.io/files/Notes/Round-robin-CCZ.pdf"
  width="100%"
  height="800px"
  style="border: none;">
</iframe>
