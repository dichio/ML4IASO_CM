# Notation Conventions — Foundations of Machine Learning

This course uses a **blended notation convention**, chosen because the course
spans classical statistical learning (ISL/ESL register) and probabilistic /
deep learning material (PRML/DL register), and no single reference's
notation serves both well on its own.

- **Vector boldness** follows PRML/DL (Bishop): every vector is bold,
  regardless of length. This is the more widely-used convention across the
  ML field generally, and avoids a length-dependent exception rule.
- **Random variable vs. realization** follows ISL/ESL: capital, non-bold
  letters denote random variables, distinct from their lowercase
  realizations. This distinction is load-bearing once the course moves
  between classical and probabilistic framings, even though Bishop's texts
  don't need it (they stay in one register throughout).
- **Counts of observations/features** stay lowercase ($n$, $p$), reserving
  capital letters exclusively for random variables — avoiding a collision
  between "capital = random" and "capital = fixed count."

Where a reading uses a different convention (e.g. ISL's non-bold feature
vectors, or Bishop's $N, D$), we translate on sight — flagged inline the
first time it comes up in a lecture.

## Comparison Table

| Item | ISL / ESL | PRML / DL (Bishop) | **This course** |
|---|---|---|---|
| Scalar | lowercase italic, $a$ | lowercase italic, $a$ | lowercase italic, $a$ |
| Vector | bold **only** if length = $n$; feature vectors ($p$-length) non-bold, $x_i$ | **always** bold, regardless of length, $\mathbf{x}$ | **always** bold — $\mathbf{x}$ |
| Matrix | bold uppercase, $\mathbf{X}$ | bold uppercase, $\mathbf{X}$ | bold uppercase, $\mathbf{X}$ |
| Random variable | capital, non-bold, $X$ — distinguished from its realization | not distinguished from realization; $x$ used for both, disambiguated by context | capital, non-bold, $X$ — kept from ISL/ESL |
| Realization of a random variable | lowercase, $x$ | same symbol as the RV, $x$ | lowercase, matching the vector-boldness rule above ($x$ or $\mathbf{x}$) |
| Number of observations | $n$ | $N$ | $n$ — note on slide that papers/Bishop write $N$ |
| Number of features / dimensionality | $p$ | $D$ | $p$ — note that papers/Bishop write $D$ |
| $i$-th observation (row) | $x_i$ (bold only if length $n$) | $\mathbf{x}_n$ | $\mathbf{x}_i$ — bold, subscript $i$ (not $n$, to avoid clashing with "$n$ = count") |
| $j$-th feature (column) | $x_j$, length-$n$ vector, so bold | $\mathbf{x}_d$ | $\mathbf{x}_j$ — bold, subscript $j$ |
| Data matrix | $\mathbf{X}$, $n \times p$ | $\mathbf{X}$, $N \times D$ | $\mathbf{X}$, $n \times p$ |
| Transpose | $x_i^T$ | $\mathbf{x}^T$ | $\mathbf{x}^T$ |
| Expectation | not formalized as standing notation | $\mathbb{E}_x[f(x,y)]$, subscript dropped when unambiguous | same as PRML/DL: $\mathbb{E}[\cdot]$, subscript only when needed for clarity |
| Variance / covariance | not formalized | $\mathrm{var}[\cdot]$, $\mathrm{cov}[\cdot,\cdot]$ | same as PRML/DL |
| i.i.d. sampling notation | not used | $x \sim p(x)$ | adopted from DL — used once probability/generative topics start |
| Identity matrix | not emphasized | $\mathbf{I}_M$, abbreviated $\mathbf{I}$ | $\mathbf{I}$, subscript only when dimension isn't obvious |
| Concatenation, floor, neighbor-set ($\oplus$, $\lfloor \cdot \rfloor$, $\mathcal{N}(i)$) | not used | used in DL for graph/sequence topics | adopted only in units that need them (e.g. GNNs), flagged as introduced |

## Open items (not yet decided)

- **Target/label notation** across regression vs. classification vs. DL
  framings (ISL/ESL use $Y$, $G$, $\hat{y}$; Bishop uses $t$). Not folded
  into this table yet — needs its own pass.
- **$n,p$ vs. $N,D$ in the DL unit specifically**: current default keeps
  $n,p$ throughout the course, with $N,D$ flagged as "what you'll see in
  papers." Revisit if the DL unit ends up large enough that constant
  translation becomes more disruptive than helpful.
- **Translation strategy for borrowed material**: decide, lecture by
  lecture, whether to rewrite ISL/ESL/PRML source notation to match this
  scheme, or leave it in its native form and rely on this document as a
  standing translation key.
