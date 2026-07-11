# Nuclear Spin Model Simulation for Master's Thesis

[![DOI](https://zenodo.org/badge/1297505074.svg)](https://doi.org/10.5281/zenodo.21310949)
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/YOUR_USERNAME/master-thesis-nv-axion-simulation/blob/main/notebooks/thesis_simulation_main.ipynb)

---

## 📖 Overview

This repository contains the complete numerical simulation code used to generate the results for my Master's thesis:

**"Quantum Sensing Through a Particle Physicist’s Lens: From Lagrangian to Table-Top Detector"**

The code simulates a **14N nuclear spin** coupled to an **NV-center in diamond** for **axion dark matter detection**. The simulations reproduce **Figures 4 and 6** from the paper **Nuclear Spin Metrology with Nitrogen Vacancy Center in Diamond for Axion Dark Matter Detection**, showing the 95% exclusion limits for the axion-nucleon coupling parameter `1/ f̃_a`.

---

## 📂 Repository Structure
master-thesis-nv-axion-simulation/
│
├── notebooks/
│ └── thesis_simulation_main.ipynb # Main Jupyter notebook (all phases)
│
├── results/
│ └── figures/ # Generated figures (if saved)
│
├── README.md # This file
├── requirements.txt # Python dependencies
├── .gitignore # Git ignore rules
├── LICENSE # MIT License
└── CITATION.cff # Citation metadata

---

## 🔬 Notebook Structure (8 Phases)

The notebook is organized sequentially:

| Phase | Description | Output |
|-------|-------------|--------|
| **1** | 14N nuclear spin operators & full Hamiltonian | Spin operators, energy levels |
| **2** | Effective two-qubit Hamiltonian & quantum gates | CNOT, SWAP, Hadamard gates |
| **3** | DC Magnetometry (Ramsey sequence) | Ramsey fringes, F vs τ |
| **4** | AC Magnetometry (Hahn echo) | Hahn echo response |
| **5** | **Figure 4** (Analytical estimation) | Exclusion limit (analytical) |
| **6** | **Figure 4** (Full quantum dynamics) | Exclusion limit (QuTiP simulation) |
| **7** | **Figure 6** (Analytical estimation) | Hahn echo exclusion (analytical) |
| **8** | **Figure 6** (Full quantum dynamics) | Hahn echo exclusion (QuTiP simulation) |

**Phases 5-8** directly produce the figures shown in the thesis. Phases 1-4 define the theoretical framework and quantum gates.

---

## 🚀 How to Run the Code

### Option A: Run on Google Colab (Recommended – No Installation)

1. Click the **"Open In Colab"** badge at the top of this README.
2. Once the notebook opens in Colab, go to `Runtime` → `Run all`.
3. The notebook will automatically install QuTiP and all dependencies.
4. **Phases 5-8** will generate the exclusion limit plots.

### Option B: Run Locally

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Houshyar-jfr/master-thesis-nv-axion-simulation.git
   cd master-thesis-nv-axion-simulation
2. Create a virtual environment (recommended):
 python -m venv venv
 source venv/bin/activate   # On Windows: venv\Scripts\activate
3. Install dependencies:
 pip install -r requirements.txt
4. Launch Jupyter Notebook:
 jupyter notebook
5. Open and run:
 Navigate to notebooks/ and open thesis_simulation_main.ipynb, then click Run → Run All Cells.

## 📊 Expected Outputs

### Figure 4 (Ramsey sequence – 95% exclusion limits)
- **Analytical estimation** (Phase 5) – dashed curves
- **Full quantum dynamics** (Phase 6) – solid magenta curve matching the paper

The plot shows `1/f̃_a` [GeV⁻¹] vs axion mass `m_a` [eV] for three scenarios:
- `N = 10¹², t_obs = 1 s`
- `N = 10¹², t_obs = 1 yr`
- `N = 10²⁰, t_obs = 1 yr`

### Figure 6 (Hahn echo – 95% exclusion limits)
- **Room temperature** (T₂ = 10 ms) – top panel
- **Cryogenic** (T₂ = 1 s) – bottom panel

Both analytical and quantum simulation curves are generated and plotted for the same three scenarios.

---

## ⚙️ Key Physical Constants

| Constant | Value | Description |
|----------|-------|-------------|
| `γ_N` | `2π × 3.08 MHz/T` | ¹⁴N gyromagnetic ratio |
| `T₂*` | `7.25 ms` | Ramsey dephasing time |
| `T₂` | `10 ms` / `1 s` | Hahn echo coherence time |
| `ρ_a` | `0.4 GeV/cm³` | Local dark matter density |
| `v_a` | `10⁻³ c` | Axion virial velocity |
| `SNR threshold` | `8.48` | 95% confidence level |

---

## 📝 Citation

If you use this code for your research, please cite it using the DOI provided above.

### BibTeX entry:
```bibtex
@software{Jafari Asl_2026_Nuclear_Spin,
  author       = {Houshyar Jafari Asl},
  title        = {Quantum Sensing Through a Particle Physicist’s Lens: From Lagrangian to Table-Top Detector},
  year         = {2026},
  publisher    = {Zenodo},
  version      = {v1.0.1},
  doi          = {10.5281/zenodo.21310949}
}

### Plain text:

> Jafari Asl, Houshyar. (2026). *master-thesis-nv-axion-simulation*. Zenodo. doi:10.5281/zenodo.21310949

---

## 📄 License

This project is licensed under the MIT License – see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgments

- Supervisor: Hamed Bakhshiansohi
- Department of Physics, Isfahan University of Technology
- Based on the theoretical framework from the physics paper

---

## 📧 Contact

For questions or issues, please open a GitHub issue or contact:
**h.jafari@ph.iut.ac.ir**

---

**Last updated:** July 2026