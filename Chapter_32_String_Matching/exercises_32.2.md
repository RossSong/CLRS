## 32.2 The Rabin-Karp algorithm

### 32.2-1

> Working modulo $q = 11$, how many spurious hits does the Rabin-Karp matcher encounter in the text $T = 3141592653589793$ when looking for the pattern $P = 26$?

$|\\{15, 59, 92, 26\\}| = 4$.

### 32.2-2

> How would you extend the Rabin-Karp method to the problem of searching a text string for an occurrence of any one of a given set of $k$ patterns? Start by assuming that all $k$ patterns have the same length. Then generalize your solution to allow the patterns to have different lengths.

Truncation.

### 32.2-3

> Show how to extend the Rabin-Karp method to handle the problem of looking for a given $m \times m$ pattern in an $n \times n$ array of characters. (The pattern may be shifted vertically and horizontally, but it may not be rotated.)

Calculate the hashes in each column just like the Rabin-Karp in one-dimension, then treat the hashes in each row as the characters and hashing again.

### 32.2-4

> Alice has a copy of a long $n$-bit file $A = \langle a\_{n-1}, a\_{n-2}, \dots, a\_0 \rangle$, and Bob similarly has an $n$-bit file $B = \langle b\_{n-1}, b\_{n-2}, \dots, b\_0 \rangle$. Alice and Bob wish to know if their files are identical. To avoid transmitting all of $A$ or $B$, they use the following fast probabilistic check. Together, they select a prime $q > 1000n$ and randomly select an integer $x$ from $\\{ 0, 1, \dots, q - 1 \\}$. Then, Alice evaluates

> $\displaystyle A(x) = \left ( \sum\_{i=0}^{n-1} a\_i x^i \right ) \~\text{mod}\~ q$

> and Bob similarly evaluates $B(x)$. Prove that if $A \ne B$, there is at most one chance in $1000$ that $A(x) = B(x)$, whereas if the two files are the same, $A(x)$ is necessarily the same as $B(x)$. (Hint: See Exercise 31.4-4.)
