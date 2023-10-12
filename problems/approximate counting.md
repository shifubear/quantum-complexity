---
alias: amplitude estimation
---

# Statement
In the $\sc{Apx}\sc{Count}_{N,w}$ problem, the goal is to decide whether a nonempty set $S \subseteq [N]$ satisfies $|S| \geq 2w$ (YES) or $|S| \leq w$ (NO), promised that one of these is the case. 

# Comments 
- Classical randomized algorithms
	- $\Theta(N/|S|)$ membership queries are necessary and sufficient
- Quantum algorithms that allow membership queries in superposition
	- Optimal (by Grover lower bound/BBBV Theorem) $O(\sqrt{N / |S|})$ algorithm
- QMA setting with an $m$-qubit quantum witness, then
	- either $m = \Omega(|S|)$ or $T = \Omega(\sqrt{N/|S|})$ 
- This problem is complete for the class [[SBP]] [BGM06]

# References
- BHT98
- BHMT
- BBBV
- [[@AKKT20]]


\documentclass{llncs}
\usepackage{cite}
\usepackage{amsmath}
\usepackage{amssymb}
\usepackage{graphicx}
\usepackage{subcaption}
\usepackage{listings}

\usepackage{braket}
\usepackage{tikz}
\usetikzlibrary{quantikz}

\newif\ifAnon
\Anonfalse  % Set to \Anonfalse to get the non-anonymous version
%algochapter
\usepackage[linesnumbered,ruled,vlined,nosemicolon]{algorithm2e}
\usepackage{color}
\usepackage[pdfencoding=auto]{hyperref}
\newcommand{\todo}[1]{\textbf{\textcolor{blue}{#1}}}
\renewcommand{\emph}[1]{\textit{\textbf{#1}}}
% \newtheorem{theorem}[section]{Theorem}
% \newtheorem{lemma}[theorem]{Lemma}
% \newtheorem{corollary}[theorem]{Corollary}
% Operators and functions:
%
\DeclareMathOperator{\rank}{rank}
%
% Discourage hyphenation
%
\clubpenalty=1000
\widowpenalty=1000
\hyphenpenalty=2000
\tolerance=1000

\let\epsilon\varepsilon

\begin{document}
\title{Quantum Tutte Embeddings}
\ifAnon
\author{Anonymous Author List}
\else
\author{
Shion Fukuzawa
\and
Michael T. Goodrich
\and
Sandy Irani
}
\institute{Dept. of Computer Science, Univ.~of California, Irvine, USA}
\fi
% \date{}   % Uncomment to remove the date if you see it

\maketitle
\begin{abstract}
Using the framework of Tutte embeddings, we begin an exploration
of \emph{quantum graph drawing}, which uses quantum computers to
visualize graphs. We discuss how a graph-drawing quantum circuit from a given graph, and
show how to calculate a Tutte embedding as a quantum state that can then be sampled to extract the embedding.
To evaluate the complexity of our quantum Tutte embedding circuits,
we compare them to theoretical bounds established in the classical
computing setting derived from a well-known classical algorithm for
solving the types of linear systems that arise from Tutte embeddings.
We also present empirical results obtained from experimental quantum
simulations.

\keywords{Tutte embeddings; quantum computing; linear systems.}
\end{abstract}

\pagestyle{plain}

% \nolinenumbers
% \clearpage
\section{Introduction}

In this work, we begin an exploration of
\emph{quantum graph drawing},
which studies how to use quantum computers to visualize graphs.
As a first step in this exploration, 
we focus on quantum circuits for what is 
arguably
the first graph 
drawing algorithm---\emph{Tutte embeddings}~\cite{tutte1963draw}.
A Tutte embedding of a graph $G$ is a crossing-free straight-line embedding
of $G$ such that the outer face, $f$, is a convex polygon and such that each interior
vertex (not on $f$) is at the average (or barycenter) of its neighbors’ positions; 
see, e.g.,~\cite{battista1999graph,kobourov2013}..
It is well known now due to Tutte that such a configuration can be found by minimizing the energy of a physical system in which edges are 
represented as springs connecting massless particles representing the vertices.
This system of vertices is described by a linear system defined by combining the following pair of equations for every vertex $u$:
\begin{align}\label{eq:short-tutte}
    &\sum_{v \in N(u)} (x_v - x_u) = 0, 
    &\sum_{v \in N(u)} (y_v - y_u) = 0
\end{align}
Thus the Tutte embedding problem is reduced to solving the above set of linear equations. 

A quantum linear systems solver \cite{harrow2009} computes a vector unit vector $x$ that 
satisfies $A x  = b$ for input matrix, $A$, and unit vector, $b$. 
The leading classical linear systems solver is due to Spielman and Teng \cite{spielman2004nearly} and can solve a system of $N$ equations in $\Tilde{O}(N \log (\kappa/\epsilon))$ where the $\Tilde{O}$ suppresses sublinear terms in $N$. 

There are three challenges that must be handled to port the linear system in equation \ref{eq:short-tutte} into a quantum linear systems solver. First, the input and output vectors must be unit vectors, so the graph drawing problem must be scaled accordingly. Second, we combine techniques from 
The spring-optimization of a Tutte embedding can be represented as a linear system where the matrix $A$ corresponds to the graph Laplacian of the spring system, where edges of a graph encode the spring constraints.  
We explore how to translate the input matrix into a quantum circuit. Explicit constructions are limited, so we provide a way for encoding graph Laplacians into Harrow et al.'s linear systems solver. 
Another challenge of using quantum computers for this application is that the output embedding is encoded in the vector $x$ as a quantum state.
Sampling an exact and precise description for the full embedding is expensive, but this can largely be avoided if the focus is only on a subset of the embedding. 


\section{Summary of Results}



% \input{tutte}
% % \input{np}
% \input{algs}
% \input{experiments}

\subsection*{Acknowledgements}
We would like to thank David Eppstein for helpful discussions regarding
the topics of this paper.
This work was supported in part by NSF grant 2212129.

\clearpage
%    \bibliographystyle{abbrv}
    \bibliographystyle{splncs03}
    \bibliography{refs}

\clearpage
\begin{appendix}
\input{appendix}
\end{appendix}
\end{document}
