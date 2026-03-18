# FYS5419 Project 2 — QAOA for Portfolio Optimization

**Course:** FYS5419 — Quantum Computing and Machine Learning, University of Oslo
**Author:** Egil Furnes (`egilsf@uio.no`) — [github.com/egil10](https://github.com/egil10)
**Due:** June 1, 2026

---

## Topic

Application of the **Quantum Approximate Optimization Algorithm (QAOA)** to
cardinality-constrained minimum-volatility portfolio selection. The optimization
problem is cast as a **QUBO** (Quadratic Unconstrained Binary Optimization) and solved
using a parameterized quantum circuit on Qiskit simulators. Covariance matrices are
estimated from historical crisis windows (2008, 2020, 2022) to evaluate performance
under stress conditions.

---

## Repository Layout

| File | Contents |
|------|----------|
| `00 MAIN.tex` | Document class, packages, and section imports |
| `01 FRONTMATTER.tex` | Title block and abstract |
| `10 INTRO.tex` | Introduction |
| `11 METHOD.tex` | Methods: QUBO formulation, QAOA circuit, optimization loop, dataset |
| `12 RESULT.tex` | Results *(in progress)* |
| `13 CONCLUSION.tex` | Conclusion *(in progress)* |
| `98 BIB.tex` | Bibliography printout |
| `99 APPENDIX.tex` | Notable figures in QC; QAOA circuit component table |
| `bib.bib` | BibTeX database |
| `article/` | Compiled PDF |

---

## Build

Compile with `pdflatex` + `biber` (standard LaTeX toolchain):

```bash
pdflatex "00 MAIN"
biber   "00 MAIN"
pdflatex "00 MAIN"
pdflatex "00 MAIN"
```

Or open on [Overleaf](https://www.overleaf.com) via the linked Git remote.

---

## Status

- [x] Introduction
- [x] Methods (QUBO formulation, QAOA circuit design, hybrid optimization loop, dataset)
- [ ] Results (benchmarks, approximation ratio vs. circuit depth, portfolio comparison)
- [ ] Conclusion
- [ ] Figures and tables (convergence plots, portfolio bar charts)
- [ ] Code listings (Qiskit circuit construction, COBYLA optimization loop)
