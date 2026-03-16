# QDMGRNSim - WIP 

## Claim
Classical models of gene regulatory networks (Boolean logic, differential equations, Markov processes) assume transitive logical structure and cannot capture context-dependent dominance relationships. A quantum-inspired Lindblad operator framework can model biological information networks as open dynamical systems and produce logical intransitivity that is provably impossible under classical Markov dynamics.
## Evidence
The evidence has three layers, each with varying degrees of completeness:
Mathematical. The Liouvillian superoperator ℒ is constructed explicitly in Kronecker form, its spectral structure is derived via the Hille–Yosida theorem and Jordan decomposition, uniqueness of the stationary state ρ* is proven under strong-connectivity conditions via the Evans–Frigerio theorem, and global asymptotic stability is proven via a Lyapunov function built from quantum relative entropy S(ρ‖ρ*) using the Spohn inequality.
Computational. A 5-node simulation using QuTiP computes expectation values ⟨O_ij⟩ = ⟨σ_z^i σ_z^j⟩ at stationarity and shows that the intransitivity index I(γ) peaks at intermediate decoherence strength γ before decaying — a non-monotone pattern. Four figures are generated.
Empirical. An RNA-seq dataset is described as being processed through alignment, quantification, normalization, partial correlation inference, and 1,000-iteration bootstrap resampling, yielding a significant intransitivity peak at intermediate γ (p < 0.01). However, the dataset is not named or cited with a GEO accession, making this evidence currently unverifiable.
## Result
Two results are reported:
The classical no-go theorem establishes that the variance of classical Markov correlations d I_{cl}/dγ ≤ 0 monotonically — classical mixing can only flatten correlations, never produce a dispersion peak. The operator framework violates this bound at intermediate γ, formally separating it from any classical Markov model over the same network topology.
The RNA-seq case study reports that a significant peak in the intransitivity index is observed at intermediate γ (p < 0.01 by permutation test), consistent with the theoretical prediction. The classical simulation shows monotonic decay for the same network, matching the no-go theorem.
