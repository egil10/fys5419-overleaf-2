# FYS5419 Project 2 — QAOA for Portfolio Optimization

*Can a quantum circuit find the minimum-volatility portfolio during a financial crisis?*

University of Oslo · Spring 2026 · Egil Furnes

<br>

## The idea

Portfolio selection under a cardinality constraint — pick exactly *k* assets to minimise volatility — is NP-hard. As the asset universe grows, classical solvers become intractable. The Quantum Approximate Optimization Algorithm treats the problem differently: encode the constraints into a cost Hamiltonian, prepare a parameterised quantum state through alternating layers of cost and mixer unitaries, and let a classical optimiser tune the angles until the circuit's output concentrates on low-cost bitstrings.

The QUBO formulation is structurally identical to finding the ground state of an Ising Hamiltonian. QAOA is, at its core, a variational ground-state search — the same idea as VQE, applied to combinatorial optimisation.

<br>

## Why crisis windows

Covariance matrices estimated during the 2008 crash, 2020 pandemic shock, and 2022 rate spike are not well-behaved. Correlations spike, eigenvalue spectra flatten, and the minimum-volatility portfolio shifts sharply. These are the conditions where classical assumptions break down and where a genuinely different approach has the most to prove.

<br>

## Layout

`00 MAIN.tex` — document root · `01 FRONTMATTER.tex` — abstract · `10 INTRO.tex` — introduction · `11 METHOD.tex` — QUBO formulation, QAOA circuit, optimization loop, dataset · `12 RESULT.tex` — results · `13 CONCLUSION.tex` — conclusion · `bib.bib` — references

<br>

## Build

```bash
pdflatex "00 MAIN" && biber "00 MAIN" && pdflatex "00 MAIN" && pdflatex "00 MAIN"
```

Or open on [Overleaf](https://www.overleaf.com) via the linked Git remote.

<br>

---

*Department of Physics · University of Oslo*
