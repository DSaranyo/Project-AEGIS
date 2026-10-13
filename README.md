<div align="center">

# 🛰️ Project AEGIS
### Advanced Orbital Hazard Sandbox & Conjunction Risk Analytics Engine

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.10%2B-blue?style=for-the-badge&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/Astrodynamics-J2%20Perturbation-orange?style=for-the-badge&logo=esa&logoColor=white" />
  <img src="https://img.shields.io/badge/Status-Active%20Prototype-success?style=for-the-badge" />
  <img src="https://img.shields.io/badge/License-MIT-green?style=for-the-badge" />
</p>

*A high-performance simulation and situational awareness sandbox designed to track space debris, ingest live CelesTrak TLE data, and evaluate collision avoidance risks.*

</div>

---

## 🚀 Overview
**Project AEGIS** is a software-based orbital safety and collision-avoidance framework. Built to model realistic low-Earth orbit (LEO) dynamics, AEGIS processes thousands of tracked catalog objects, performs high-speed vector propagations, and runs a comprehensive validation suite to flag close-approach hazards.

---

## ✨ Key Architectural Features

| Module | Description | Technical Core |
| :--- | :--- | :--- |
| **J2 Vector Engine** | Propagates 3D Cartesian coordinates ($x, y, z$) incorporating Earth oblateness perturbations. | `NumPy`, `Skyfield`, `SGP4` |
| **Live TLE Ingestion** | Automatically pulls active satellite and debris catalogs from real-time orbital feeds. | CelesTrak API |
| **Proximity Screening** | Scans large object catalogs to filter, deduplicate, and flag high-risk conjunction warnings. | Vectorized Distance Matrices |
| **Mission Control UI** | Generates multi-graph analytics suites covering trajectory tracking and risk severity metrics. | `Matplotlib` / Analytics Suite |
| **Model Validation** | Evaluates hazard classification performance using precision, recall, and F1-score tracking. | Data Science Metrics |

---

## 📊 Core Physics & Math Model
AEGIS implements rigorous astrodynamics formulas to verify orbital behavior:
* **Orbital Radius ($r$):** Derived from input altitude and Earth's mean equatorial radius ($R_{\text{EARTH}} = 6,371 \text{ km}$).
* **Orbital Speed ($v$):** Computed via standard gravitational parameter ($\mu \approx 398,600 \text{ km}^3/\text{s}^2$):
  $$v = \sqrt{\frac{\mu}{r}}$$
* **$J_2$ Perturbation:** Accounts for secular variations in Right Ascension of the Ascending Node ($\text{RAAN}$) due to Earth's equatorial bulge.

---

## 🛠️ Quick Start & Installation

Clone the repository and install the required astrodynamics dependencies:

```bash
# Clone the repository
git clone [https://github.com/Dsaranyo/Project-AEGIS.git](https://github.com/DSaranyo/Project-AEGIS.git)
cd Project-AEGIS

# Install dependencies
pip install numpy skyfield sgp4 matplotlib pandas
