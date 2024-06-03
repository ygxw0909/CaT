# CaT

Github page for paper \textbf{Context-Aware Tracking and Dynamic Introduction for Incomplete Utterance Rewriting in Extended Multi-Turn Dialogues} accepted by Findings of ACL 2024

# Data

\begin{table}
% \vspace{-4mm}
		\begin{center}
            \scalebox{0.68}{
				\begin{tabular}{lccccc}
					\toprule
					Dataset & Train & Dev & Test & $avg_c$ & $avg_t$ \\
					\hline
					\\[-6pt]

                    \small\textbf{ReWriter}~\cite{DBLP:conf/acl/SuSZSHNZ19} & 18000 & 2000 & - & 3.0 & 24.2\\
                    
					\small\textbf{Restoration}~\cite{DBLP:conf/emnlp/PanBWZL19} & 116360 & 3024 & 2999 & 4.9 & 34.4\\

                    % \textbf{Task} & - & - & - & - & - \\

                    \small\textbf{MuDoCo}~\cite{DBLP:conf/lrec/MartinPU20} & 5901 & 691 & 749 & 5.4 & 41.1 \\
                    
                    \small\textbf{CQR}~\cite{2019arXiv190311783R} & 2131 & 271 & 276 & 5.7 & 46.2 \\
                    
					\small\textbf{CANARD}~\cite{DBLP:conf/emnlp/ElgoharyPB19} & 31526 & 3430 & 5571 & 9.8 & 92.9 \\
                    
				\small\textbf{INSQR} & 4733 & 591 & 593 & \textbf{30.1} & \textbf{600.5} \\
					\bottomrule
			\end{tabular}
			}
		\caption{The comparison of INSQR with the existing benchmarks. Here, "$avg_c$" and "$avg_t$" denote the average of turns and length of context, separately. We use the three with the longest context for experiments.}\label{dataset}
        \vspace{-3mm}
	\end{center}
\end{table}

Our experiments are concstructed on 
