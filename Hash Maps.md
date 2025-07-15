---
tags:
  - COMP250
---
# Hash Maps

A map is a set of:: (key, value) pairs. For each key, there is at most one value. Note that it is possible for two keys to map to the same value.

Some map methods are:: `put(key, value), get(key), remove(key)`

`string.hashCode()` function $\equiv$::$\sum\limits_{i=0}^{\text{string.length}-1}\text{string}[i]\cdot 31^{\text{string.length}-1-i}$

If `s1.hashCode() == s2.hashCode()` then what can we conclude about `s1.equals(s2)` ?:: `s1` may or may not be the same string as `s2`.
If `s1.hashCode() != s2.hashCode()` then what can we conclude about `s1.equals(s2)` ?:: `s1` is a different string then `s2`.

"hash function"$\equiv$::compression(`hashCode`) = |`hashCode`| % `m` where `m` called the number of buckets can be the number of `hashCode`s or more

A `hashCode` maps keys to:: `int` (index).
A "hash function" maps keys to:: "hash values"

Diagram of `hashCode()`, compression and hash values:
?
![[image-20241127221133553.png|500]]


Load factor formula $\equiv$::$\frac{\text{number of (key, value) pairs in map}}{\text{number of buckets,}~m}$

One typically keeps the load factor below 1. In the Java `HashMap class`, the default MAXIMUM load factor is:: 0.75.

