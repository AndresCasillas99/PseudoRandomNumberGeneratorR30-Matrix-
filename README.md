# PseudoRandomNumberGeneratorR30-Matrix-
We present a pseudo-random number generator using the values of the central column of Wolfram's Rule 30 automata arranged as a matrix.

We can arrange the first $1$ million values of Wolfram's Rule 30's central column in a $1,000$ by $1,000$ square matrix. We can then, given $k>0$,
generate a random number  between $0$ and $2^{k}$ as follows:

1. Choose a random point $(x,y)$ from the matrix.
2. Choose a random direction (right, diagonal right up, up, diagonal left up, left, diagonal left down, down, diagonal right down).
3. Read $k$ bits starting from $(x,y)$ and in the chosen direction.
4. Interpret the resulting string as a base $2$ number and return its representation in base $10$.


We've done some benchmarking and, given a uniform random seed (x,y), the output of the algorithm shows a uniform distribution. 


![R30CentralColumn_1000x1000](https://github.com/user-attachments/assets/68ca3295-5c72-44f0-aaa9-fad11b62639d)
Picture of the first $1$ million values of Wolfram's Rule 30's central column in a $1,000$ by $1,000$ square matrix.
0 => white
1 => black
