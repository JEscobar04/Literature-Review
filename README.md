# Week 3 Literature-Review
**Name:** Joel Escobar

**Questions to ChatGPT:** What is P vs NP, and what exactly makes this such an open problem in the field of computer science? Has there been attempts to prove P $\neq$ NP and if so can you go about the way it was done? What other developments have occurred after the most recent attempt was unsuccessful? Does the field of quantum computing offer any help in solving this problem?

**Goal:** The goal of this literature review was to get an understanding of complexity theory regarding the debate of P vs NP. This includes the different attempts and the recent developments. 
*** 
## What is P vs NP
"**P** vs **NP**" refers to the debate of Polynomial time vs Non-Deterministic Polynomial time for algorithms. **P** is the space of all decision problems that can be solved by a deterministic Turing machine in polynomial ($O(n^k)$ for $k \in \mathbb{R}$) time. **NP** refers to the space of all decision problems that can be verified in polynomial time by a deterministic Turing machine. 
### What are Turing Machines
Turing Machines are abstract machines that moves characters on a tape according to a set of rules. Turing machines are used instead of a computer model of today because it allows for a more universal approach to analyzing problems. Turing Machines are meant to be able to simulate any computer so this allows for a more formal approach. Additionally, this makes it easier to determine nondeterminism because Turing machines are automata so they can model deterministic and nondeterministic calculations. 
### Why it's Such an Open Problem
The debate of **P** vs **NP** is such an open problem because there has not been a definitive proof that **P = NP** or **P $\neq$ NP**. The way it is shown that **P = NP** is if there is a problem within **NP-complete** that can be solved in polynomial time. **NP-complete** is the subset of problems within **NP** that if solved in polynomial time, can solve all of **NP** in polynomial time because all problems in **NP** can be reduced to **NP-complete**. If **P = NP**, one implication means that cryptographic security systems are vulnerable because it's assumed it can only be solved in non-polynomial time. If **P $\neq$ NP**, then that means that some of the hardest problems can only be verified in polynomial time at best but are impossible to solve efficiently. Without a proof, there is no way to accurately conlcude that one claim is right. There have been attempts to prove both sides but there has been no success in either side. The general consensus is that **P $\neq$ NP** because the way the heirarchies are established suggest that some problems require more resources than others, implying that **P** and **NP** are different. For this literature review, only attempts at proving **P $\neq$ NP** will be looked at.

## Attempts to Prove P $\neq$ NP
### Diagonalization and Relativization
This proof was pioneered by Theodore Baker, John Gill, and Robert Solovay. The first step, diagonalization, involved creating a problem that lies outside the scope of algorithms already created. This ensured that the problem behaves differently from other problems. The second step, relativization, involved introducing Turing machines with an "oracle." This "oracle" can solve a problem instantly. However in the attempts that were made with multiple oracles, one oracle concluded **P = NP** while another oracle concluded **P $\neq$ NP**. Because of this, scientists concluded that these two techniques were insufficient to solve this problem. 
### Circuit Complexity
This proof was started by Alexander Razborov in the 1980s. This proof involved expressing computations as circuits composed of logical gates (AND, OR, NOT, etc.). The goal was to prove that circuits from **NP** required exponentially larger circuits while problems from **P** would only require polynomial-sized circuits. They were able show that restricted classes of circuits could not solve **NP-complete** efficiently. However when they tried extend it to general circuits, they were unsuccessful.
### Natural Proofs
This framework was developed by Razborov and Steven Rudich to characterize the techniques in circuit complexity. Rather than attempting to prove **P $\neq$ NP**, this framework attempted to categorize many techniques and their properties. This category was known as "natural" proofs. The outcome of this research argued that to prove that **P $\neq$ NP**, new non-natural techniques would be needed. 
### Algebrization
The most recent attempt was a technique called Algebrization introduced by Scott Aaronson and Avi Wigderson. This built upon the first proof of diagonalization and relativization, but modified the "oracle" such that instead of returning a yes or no, it would return a polynomial or algebraic value. This version of the "oracle" helped capture more sophisticated properties of computation. Aaronson and Wigderson's attempt at separating the different complexity classes was unsuccessful. However, this method set another technique that needs to be surpassed before **P $\neq$ NP** can be realized. 
### Geometric Complexity Theory
Before Algebrization, Ketan Mulmuley and Milind Sohoni introduced a different kind of proof called Geometric Complexity Theory (GCT). This proof aimed to use tools from algebraic geometry and representation theory to try and prove that **P $\neq$ NP**. The way this technique works is that it analyzes computational problems and looks at their symmetries to express their complexity in geometric terms. While no direct proof has been made, GCT showed promising results in solving matrix multiplication problems. As this is the only technique that just uses pure mathematical concepts, this approach has promise in the future. 

## Quantum Computing's Place in this Problem
When I asked ChatGPT what quantum computing has to offer in this problem, it revealed that qunatum computing has its own complexity class: **BQP** (Bounded-Error Quantum Polynomial time). While there have been a couple problems within **NP** that were able be solved in polynomial time (integer factorization), there has not been an **NP-complete** problem that has been solved in polynomial time with quantum computers. Since quantum computers have their own complexity class, it is difficult to prove that **P $\neq$ NP** with quantum computers. 

## Developments after Algebrization
Algebrization has shown computer scientists and mathematicians what kind of techniques **won't** work when trying to solve **P** vs **NP**. Researchers are look at more non-natural kinds of proofs to hopefully get one step closer to **P $\neq$ NP**. Besides **Geometric Complexity Theory**, there are **Interactive Proofs** and **Probabilistically Checkable Proofs (PCPs)**. These two techniques also go beyond the limits of relativization and algebrization but no proof for **P $\neq$ NP** has been found with any of those techniques.

## References
**<a href="https://epubs.siam.org/doi/10.1137/0204037">Baker, T., Gill, J., & Solovay, R. (1975). "Relativizations of the P=?NP Question." *SIAM Journal on Computing*.</a>**

**<a href="https://link.springer.com/chapter/10.1007/978-3-662-03927-4_4">Razborov, A. A. (1985). "Lower Bounds on the Size of Bounded Depth Networks Over a Complete Basis with Logical Addition." *Mathematical Notes*.</a>**

**<a href="https://www.sciencedirect.com/science/article/pii/S002200009791494X">Razborov, A. A., & Rudich, S. (1994). "Natural Proofs." *Journal of Computer and System Sciences*.</a>**

**<a href="https://dl.acm.org/doi/abs/10.1145/1374376.1374481">Aaronson, S., & Wigderson, A. (2008). "Algebrization: A New Barrier in Complexity Theory." *Proceedings of the 40th Annual ACM Symposium on Theory of Computing (STOC)*.</a>**

**<a href="https://epubs.siam.org/doi/10.1137/S009753970038715X">Mulmuley, K., & Sohoni, M. (2001). "Geometric Complexity Theory I: An Approach to the P vs NP and Related Problems." *SIAM Journal on Computing*.</a>**
