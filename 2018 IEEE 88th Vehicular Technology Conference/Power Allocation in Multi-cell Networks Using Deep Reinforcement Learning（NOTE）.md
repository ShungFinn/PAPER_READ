# Power Allocation in Multi-cell Networks Using Deep Reinforcement Learning（NOTE）

## Glossary

### NP-hard problem：

![img](https://img-blog.csdn.net/20151015164207766)

P,NP,NPC,NP-hard

definition:

They all based on the **time complexity (BIG-O)**

**polynomial time complexity**: 
like:
 $O(1),O[ln(n)],O(n^a)$
$\ n$ is appeared in the position of base

**non-polynomial time degree**:
like:
$O(a^n),O(n!)$ 
the complexity always can't be carried by computer

we always chose the former instead of latter avoiding time out, latter only applied in small scale calculation

P: can be solved in a period of time in the form of polynomial

NP: can't be solved  in a period of time in the form of polynomial
and it can be easily proved wrong if offers a wrong answer
(easy to verify but not easy to solve)

P and NP:
$P\subseteq NP$

NP-Complete:
requires to satisfy two conditions:

1. it' s a NP
2. all the NP can be translated(reduced) to it

NP-hard:
only has to satisfy point 2 of NPC
but it doesn't have to be a NP itself

That means a NPC is easier than a NPH, latter is sometimes more complex than former





