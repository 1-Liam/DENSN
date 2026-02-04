# DENSN: Dynamic Energy-Based Neuro-Symbolic Network

**Dual-Pathway Neuro-Symbolic Optimization via Spectral Structure Learning**

[![License: CC BY-NC-ND 4.0](https://img.shields.io/badge/License-CC%20BY--NC--ND%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-nd/4.0/)
[![Status: Research Preview](https://img.shields.io/badge/Status-Research%20Preview-blue)](https://github.com/1-Liam/DENSN)

> **Abstract:** Conventional neuro-symbolic systems operate on fixed graphs, failing when faced with "out-of-distribution" logical paradoxes. **DENSN** treats logical frustration not as a terminal error, but as a generative signal for topological expansion. It introduces a **Dual-Pathway** architecture: minimizing tension via spectral diffusion in low-conflict regimes, and triggering **Topological Structure Learning (TSL)** to synthesize new Meta-Symbols in high-conflict regimes.

---

## 📄 The Paper
**[Read the Full Whitepaper (PDF)](paper/DENSN_Whitepaper.pdf)**

*Note: This repository serves as the reference implementation for the theory described in the paper. The core engine code will be released in the upcoming Alpha phase.*

---

## 🗝️ Core Innovations

### 1. Dual-Pathway Optimization
Optimization is not a monolithic process; it is a thermodynamic response to tension. DENSN splits this into two distinct pathways:
* **Pathway A (Coherence):** Triggered when $\Psi < \Psi_{crit}$. The system optimizes for modularity and consistency within the existing ontology, minimizing free energy via diffusion.
* **Pathway B (Frustration):** Triggered when $\Psi \ge \Psi_{crit}$ (Persistent Singularity). The system recognizes the ontology is insufficient and forces **Topological Structure Learning (TSL)** to synthesize a new Meta-Symbol that resolves the paradox.

### 2. The Spectral-MCM Engine
DENSN replaces heuristic solvers with a physics-based hybrid engine:
* **Spectral Diffusion:** Utilizes the **Graph Laplacian** ($\Phi_{t+1} = (I - \kappa \mathcal{L})\Phi_t$) to diffuse "logical potential" across the graph structure. This allows the system to "feel" global topology before committing to discrete decisions.
* **Stochastic Collapse:** A modified WalkSAT operator projects the continuous potential field back into discrete truth values, using the spectral gradient to avoid local minima.

### 3. Energetic Verification Protocol (Solving Hallucination)
To address the Symbol Grounding Problem, DENSN mathematically decouples **Structural Truth** from **Semantic Meaning**:
1.  The system learns a structure ($f_{meta}$) to resolve a paradox.
2.  It queries an Oracle (LLM) for a semantic label ($L_{meta}$).
3.  It injects a verification constraint ($L_{meta} \leftrightarrow f_{meta}$) and measures the **Global Tension Response** ($\Delta \Psi$).
4.  If $\Delta \Psi$ spikes, the label is rejected as a hallucination. The semantic map must respect the structural territory.

---

## 📊 Benchmarks & Validation

The framework has been validated on both synthetic and real-world datasets:

* **Biomedical Case Study (Ovarian Cancer):** Ingested 579 atomic symbols from conflicting PubMed literature. The system successfully isolated the specific "Singular Contradiction" regarding Cisplatin vs. Carboplatin efficacy, separating it from the high-consensus background knowledge.
* **Synthetic XOR Paradox:** Demonstrated the ability to autonomously "invent" a Meta-Symbol to resolve an irreducible 3-constraint loop. The Conflict Cache escalated weights until TSL was triggered, reducing global tension from $\Psi=16.0$ to $\Psi=0.0$.

---

## 📜 Citation

If you use this theory in your research, please cite the whitepaper:

```bibtex
@article{oboyle2025densn,
  title={DENSN: Dual-Pathway Neuro-Symbolic Optimization via Spectral Structure Learning},
  author={O'Boyle, Liam},
  year={2025},
  journal={Open Research Archive},
  url={https://github.com/1-Liam/DENSN}
}
```

## ⚖️ License
This work is licensed under a **Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International License**.

* **You are free to:** Share, copy, and redistribute the material in any medium or format.
* **Under the following terms:**
    * **Attribution:** You must give appropriate credit, provide a link to the license, and indicate if changes were made.
    * **NonCommercial:** You may not use the material for commercial purposes.
    * **NoDerivatives:** If you remix, transform, or build upon the material, you may not distribute the modified material.

**Commercial Inquiries:** For commercial licensing, collaboration, or access to the production engine, please contact the author.

---
*Author: Liam O'Boyle | Contact: liamoboyle0@gmail.com*
