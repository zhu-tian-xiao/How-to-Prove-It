
Deductive reasoning: 演绎推理

Deductive reasoning in mathematics is usually presented in the form of a **proof**.

An integer larger than one is said to be **prime** if it can't be written as a product of two smaller positive integers. If it can be written as a product of two smaller positive integers, than it is **composite**.




| n   | Is n prime? | $2^n-1$ | Is $2^n-1$ prime?    |
| --- | ----------- | ------- | -------------------- |
| 2   | yes         | 3       | yes                  |
| 3   | yes         | 7       | yes                  |
| 4   | no          | 15      | no                   |
| 5   | yes         | 31      | yes                  |
| 6   | no          | 63      | no                   |
| 7   | yes         | 127     | yes                  |
| 8   | no          | 255     | no                   |
| 9   | no          | 511     | no: $255=15\cdot 17$ |
| 10  | no          | 1023    | no:$1023=31\cdot 33$ |

Conjecture 1:
Suppose $n$ is an integer larger than $1$ and $n$ is a prime. Then $2^n-1$ is prime.

Conjuecture 2:
Suppose $n$ is an integer larger than $1$ and $n$ is not prime. Then $2^n-1$ is not prime.


| n   | Is n prime? | $2^n-1$ | Is $2^n-1$ prime?     |
| --- | ----------- | ------- | --------------------- |
| 11  | yes         | 2047    | no: $2047=23\cdot 89$ |

Conjecture1 is incorrect. $11$ is a **counterexample** to Conjecture 1.

Proof of Conjecture 2: Since $n$ is not prime, there are positive integers a and b such that $a<n$, $b<n$, and $n=ab$. Let $x=2^b-1$, and $y=1+2^b+2^{2b}+\dots+2^{(a-1)b}$. Then 

$$
\begin{aligned}  
xy&=(2^b -1)\cdot (1+2^b+2^{2b}+\dots+2^{(a-1)b})\\
&=2^b\cdot(1+2^b+2^{2b}+\dots+2^{(a-1)b})-(1+2^b+2^{2b}+\dots+2^{(a-1)b})\\
&=(2^b+2^{2b}+\dots+2^{ab})-(1+2^b+2^{2b}+\dots+2^{(a-1)b})\\
&=2^{ab}-1\\
&=2^n-1
\end{aligned}
$$
Since $b<n$, we can conclude that $x=2^b-1<2^n-1$, Also, since $ab=n>a$, it follows that $b>1$. Therefore, $x=2^b-1>2^1-1=1$, so $y<xy=2^n-1$. Thus, we have shown that $2^n-1$ can be written as the product of two positive integers $x$ and $y$, both of which are smaller than $2^n-1$, so $2^n-1$ is not prime.

Now that the conjecture has been proven, we can call it a **theorem**.

If we continue checking prime number $n$ to see if $2^n-1$ is prime, will we continue to find counterexamples to the conjecture 1?

Theorem 3 There are infinitely many prime numbers.
Proof. Suppose there are only finitely may prime numbers. Let $p_{1}, p_{2}, \dots p_{n}$ be a list of all prime numbers. Let $m=p_{1}p_{2}\dots p_{n} +1$. Note that m  is not divisible by $p_{1}$, since dividing $m$ by $p_{1}$ gives a quotient of $p_{2}\dots p_{n}$ and a remainder of $1$, Similarly, $m$ is not divisible by any of $p_{2},p_{3},\dots p_{n}$.

Every integer larger than $1$ is either prime or can be written as a product of two or more primes. Clearly $m$ is larger than $1$, so $m$ is either prime or a product of primes. Suppose first that $m$ is prime. Note that $m$ is larger than all of the numbers in the list $p_{1}, p_{2}, \dots, p_{n}$, so we've found a prime number not in the list. But this contradicts our assumption that this was a list of all prime numbers.

Now suppose $m$ is a product of primes. Let $q$ be one of the primes in this product. Then $m$ is divisible by $q$, But we've already seen that m is not divisible by any of the numbers in the list $p_{1}, p_{2}, p_{n}$, so once again we have a contradiction with assumption that this list included all prime numbers.

Since the assumption that there are finitely many prime numbers that has led to a contradiction, there must be infinitely many prime numbers.

Prime numbers of the form $2^n -1$ are called Mersenne primes. It is still not known if there are infinitely many of them.

Mersenne primes are related to perfect numbers. A positive integer n is said to be perfect if n is equal to the sum of all positive integers smaller than n that divide n.

For any positive $n$, the product of all integers from $1$ to $n$ is called $n$ factorial and is denoted $n! =1\cdot 2 \cdot 3 \cdot n$. 

Theorem 4: For every positive integer $n$, there is a sequence of n consecutive positive integers containing no primes.

Proof: Suppose $n$ is a positive integer. Let $x=(n+1)!+2$. We will show that none of the numbers $x, x+ 1, x+2, \dots , x+(n-1)$ is prime. Since this is a sequence of n consecutive positive integers , this will prove this theorem.

$$
\begin{align}
x&=1 \cdot 2 \cdot 3 \cdot 4 \dots (n+1) +2 \\
&= 2 \cdot (1 \cdot 3 \cdot 4 \dots (n + 1) + 1).
\end{align}
$$
Thus, $x$ can be written as a product of two smaller positive integers, so $x$ is not prime.

In general, consider any number $x+i$, where $0\leq i\leq n-1$, Then we have
$$
\begin{align}
x+i&=1\cdot 2 \cdot 3 \cdot 4 \dots (n+1)+(i+2) \\
&=(i+2)\cdot(1 \cdot 2 \cdot 3\dots (i+1)\cdot(i+3)\dots(n+1)+1),
\end{align}
$$
so $x+i$ is not prime.

The only pair of consecutive positive integers that are both prime is $2$ and $3$. There are lots of pairs of primes that differ by only 2, such pairs are called **twin primes**. It is not known whether there are infinitely many twin primes.
# Exercise
1.(a) Factor $2^{15} -1=32767$ into a product of two smaller positive integers.
$32767=7\cdot 4681$

(b) Find an integer $x$ such that $1 < x < 2^{32767}-1$ and $2^{32767}-1$ is divisible by $x$.

Based on Proof of Conjecture 2, let $a=4681, b=7, n=ab=32767$, we find a $x=2^{b}-1=126, y=\frac{2^{32767}-1}{x}, xy=2^{32767}-1$, here we are sure $y$ is a positive integer.   Clearly $1<x<2^{32767}-1$.

2.Make some conjecture about the value of n for which $3^n-1$ is prime or the values of n for which $3^n-2^n$ is prime.

| n   | Is n prime? | $3^n-1$ | Is $3^n-1$ prime? | $3^n-2^n$ | Is $3^n-2^n$ prime? |
| --- | ----------- | ------- | ----------------- | --------- | ------------------- |
| 2   | yes         | 8       | no                | 5         | yes                 |
| 3   | yes         | 26      | no                | 19        | yes                 |
| 4   | no          | 80      | no                | 65        | no                  |
| 5   | yes         | 242     | no                | 211       | yes                 |

Conjecture 1: When $n$ is an integer larger than $1$, $3^n-1$ is not prime.

Conjecture 2: When $n$ is an integer larger than $1$ and $n$ is prime, $3^n-2^n$ is prime. 

Conjecture 3: $n$ is an integer larger than $1$ and $n$ is not prime, $3^n-2^n$ is not prime.

3.The proof of Theorem 3 gives a method for finding a prime number different from any in a given list of prime numbers.
(a) Use this method to find a prime different from $2, 3, 5,$ and $7$.
(b) Use this method to find a prime different from $2, 5, 11$

Suppose there is a list of prime numbers $p_{1}, p_{2}, \dots p_{n}$. Let $m =p_{1}p_{2}\dots p_{n}+1$. $m$ is prime or can be written as a product of primes. If $m$ is prime, then we find a new prime. If $m$ is not prime, let $q$ be one of the primes in this product, Because $m$ is not divisible by any of the numbers in the list $p_{1}p_{2}\dots p_{n}$, so $q\neq p_{i}( 1\leq i \leq n)$, again we find a new prime. So either $m$ is prime or not, we always find a new prime.

(a) $m=2\cdot 3 \cdot 5 \cdot 7+1=211$, and $211$ is prime.
(b) $m=2 \cdot 5 \cdot 11+1=111=3\cdot 37$, both $3$ and $37$ are prime.

4.Find 5 consecutive integers that are not prime.
Based on Theorem 4, Let $x=(n+1)!+2$. When $n = 5$, $x=6!+2=722$, so $722, 723, 724, 725, 726$ are not prime.

5.Use the table in Figure I.1 and the discussion on p5 to find two more perfect numbers.
$2^5-1=31$ is prime, so $2^4(2^5-1)=496$ is a perfect number.

$2^7-1=127$ is prime, so $2^6(2^7-1)=8128$ is a perfect number.

6.The sequence $3, 5, 7$ is a list of three prime numbers such that each pair of adjacement numbers in the list differ by two. Are there any more such "triplet primes"?

There are 2 types of sequence. Let sequence 1: $2+2i, 2+2\cdot(i+1), 2+2\cdot(i+2), i\geq0$.  Clearly $2+2\cdot(i+1)$ and $2+2\cdot(i+2)$ are divisible by $2$, so sequence 1 can't make triplet primes.

Let sequece 2: $3+2i, 3+2\cdot(i+1), 3+2\cdot(i+2), i\geq1$, there is exactly one element that is divisible by $3$ in $\{ i, i+1, i+2 \}$, so there is exactly one element in sequence 2 that is divisible by $3$.

So there are not more such triplet primes other than $3, 5, 7$.

7.A pair of distinct positive integers $(m, n)$ is called amicable if the
sum of all positive integers smaller than $n$ that divide $n$ is $m$, and the sum of all positive integers smaller than $m$ that divide $m$ is $n$.
Show that $(220, 284)$ is amicable.

All positive numbers smaller than $220$ that divide $220$ is $1, 2, 4, 5, 10, 11, 20, 22, 44, 55, 110$, sum is $284$.

All positive numbers smaller than $284$ that divide $284$ is $1, 2, 4, 71, 142$, sum is $220$.

So $(220, 284)$ is amicable.

# English
p1: give you a taste of: 初步感受

p2: try out:  to test or use somebody/something in order to see how good or effective they are 尝试

p2: conjecture: an opinion or idea that is not based on definite knowledge and is formed by guessing

p2: uncover: to discover something that was previously hidden or secret

p3: somewhat: to some degree

p3: admittedly: when you're accepting something is true.

p4: quotient: 商