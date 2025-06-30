## Overview[​](https://leetcodethehardway.com/tutorials/math/number-theory/sieve-of-eratosthenes#overview "Direct link to Overview")

The Sieve of Eratosthenes is an algorithm used to find all prime numbers up to a given limit. It works by iteratively marking as composite (i.e., not prime) the multiples of each prime, starting with 2. The algorithm starts by creating a list of all integers from 2 to the limit. It then marks the first number, 2, as prime and removes all multiples of 2 from the list. The next unmarked number in the list is 3, which is also prime, so it marks it and removes all multiples of 3 from the list. This process continues until all numbers in the list have been marked as prime or composite. The remaining unmarked numbers are the prime numbers up to the given limit.

#### General rule
If a number `x > √n` is composite, then `x = a × b`, and **at least one of `a` or `b` is ≤ √n**. That smaller factor would have already marked `x` as non-prime.
- Similar rule to calculating if a number is prime or not