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

### water-filling power allocation

it's an algorithm on power allocation, it allocates more power to client with better channel conditions

aim: allocate the power of client $P_i$ to obtain the max channel capacity 

$\sigma^2$: noise
$h_i$: channel gain of the client i, better the channel condition larger the value

$\underset{P} \max{C}\ = \ \sum\limits^{m}_{i=1}log_2(1+\frac{P_i}{\sigma^2}h_i) $

and the limiting condition:
$\sum\limits_{i=1}^{m}P_i\ =\ P_{\max} $

and the solution:

1.by Lagrange multiplier method
$$
\left\{ \begin{aligned} & u = \frac{P+\sum\limits_{i=1}^{m}{\frac{\sigma^2}{h_i}}}{m}  \\ &P_i = \max\begin{bmatrix}\begin{pmatrix}\mu-\frac{\sigma^2}{h_i}\end{pmatrix},0\end{bmatrix} \end{aligned}
\right. \ \ \Rightarrow better \ channel \ condition\ ,smaller\  \frac{\sigma^2}{h_i} \ larger \ allocated \ P_i 
$$
2.by geometric(GWF)

in GWF we don't have to solve water filling surface $\mu$ 

1. solve the worst client power(WCP)
2. add the water surface difference to WCP to obtain the power of each client

the water level difference :
$$
\delta_{3,2} = d_3 - d_2 = \frac{\sigma^2}{h_3}-\frac{\sigma^2}{h_2}
$$
 