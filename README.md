# Thermodynamic Systems: Modeling in Python

A compact collection of aerospace models **rockets, engines, and flame physics**; implemented as reproducible Jupyter notebooks with **plots**. This repo is ideal for students and practitioners who want clear, minimal models they can run and extend.

> **Scope cutoff:** Analyses summarized here reflect work available as of **2025-09-24**.

---

## 📦 Contents

- Notebooks: `Ariane 6.ipynb`, `Boeing 777 300ER Engine.ipynb`, `Two Stage Rocket and Throttling.ipynb`, `Optimizing a Jet Engine.ipynb`
- External Mechanisms: `Mechanism1.yaml`, `C7H16.yaml`
- This README and a minimal `requirements.txt`

Contents Include:
```

├── Rocket Ariane 6 Staged Mass Loss.ipynb
├── Engine GE90 Residence Time.ipynb
├── Rocket Falcon Heavy Optimal Throttle Schedules.ipynb
├── Rocket Staged and Throttled.ipynb
├── Engine Optimizing for Pressure Ratio.ipynb
├── Mechanism1.yaml (n-dodecane)
├── C7H16.yaml
└── README.md
```

---

## 🚀 Quickstart

```bash
# (optional) create an isolated environment
python -m venv .venv
# macOS/Linux
source .venv/bin/activate
# Windows PowerShell
# .venv\Scripts\Activate.ps1

# install core packages
pip install -r requirements.txt

# launch Jupyter
jupyter lab  # or: jupyter notebook
```

> Some notebooks read mechanism files (`Mechanism1.yaml`, `C7H16.yaml`). If you move them, adjust paths in the notebooks.

---

## 📚 Model Catalog (at a glance)

> Replace any placeholders below with specifics if your notebooks print/annotate them.

### `Rocket Ariane 6 Staged Mass Loss.ipynb`
- **System:** Ariane 6 Rocket with Separation
- **Dimensions:** 0D 
- **Combustion:** Yes (Hydrogen)
- **Outputs:** Plot (total mass vs. time)
<img width="600" height="380" alt="image" src="https://github.com/user-attachments/assets/083b488a-6d74-46c6-b134-311d4991bdad" />


### `Engine GE90 Residence Time.ipynb`
- **System:** Boeing 777-300ER Engine
- **Dimensions:** 0D 
- **Combustion:** Yes (Heptane)
- **Outputs:** Plot (Temperature/Fuel Mass Fraction vs time), residence time
<img width="600" height="380" alt="image" src="https://github.com/user-attachments/assets/d21ff469-4dc9-4136-99a3-e3a79639efa1" />


### `Rocket Falcon Heavy Optimal Throttle Schedules.ipynb`
- **System:** Falcon Heavy
- **Dimensions:** 1D 
- **Combustion:** No
- **Outputs:** Plots (Thrust vs time, Propellant mass vs time, Velocity vs time, Altitude vs time
<img width="600" height="380" alt="image" src="https://github.com/user-attachments/assets/f46a74b9-c598-4b1c-a753-295c15c4db07" />
<img width="600" height="380" alt="image" src="https://github.com/user-attachments/assets/62b85b4b-0d95-4795-bb03-15398cd81bcd" />
<img width="600" height="380" alt="image" src="https://github.com/user-attachments/assets/e2021b44-3ce0-4b5f-ab19-0beef5657c93" />
<img width="600" height="380" alt="image" src="https://github.com/user-attachments/assets/12e05f52-5e04-4502-be8c-59fea0893d03" />


### `Rocket Staged and Throttled.ipynb`
- **System:** Falcon Heavy Boosters and Throttling
- **Dimensions:** 1D 
- **Combustion:** No
- **Outputs:** Plots (altitude vs time, dynamic pressure vs altitude, total mass vs time)
<img width="600" height="380" alt="image" src="https://github.com/user-attachments/assets/2f60f00e-2776-4b17-b8c5-331c6ca98a62" />
<img width="600" height="380" alt="image" src="https://github.com/user-attachments/assets/0434de96-f2e6-43b2-867f-b42342e8befc" />
<img width="600" height="380" alt="image" src="https://github.com/user-attachments/assets/ecfed296-c4fd-452a-b05f-e4fe01884b3c" />

### `Engine Optimizing for Pressure Ratio.ipynb`
- **System:** Optimizing Pressure Ratio
- **Dimensions:** 0D 
- **Combustion:** yes
- **Outputs:** Table of optimized outputs
**Ideal cycle + Cantera combustor**

| Metric                       | Value                 |
|-----------------------------|-----------------------|
| Optimization finished in    | 0.16 s                |
| Iterations                  | 10                    |
| Best overall pressure ratio | 14.76                 |
| Specific thrust *F*<sub>s</sub> | 1074.2 N·s/`kg_air`   |
| TSFC                        | 0.00002 kg/N/s        |
| Equivalence ratio φ         | 0.376                 |
| Fuel mass flow              | 0.022 kg/s            |
| Mass flow (compressor)      | 54.042 kg/s           |


---

## 🔁 Reproducibility notes

- Pin versions using `requirements.txt` (or add a conda `environment.yml`).
- For deterministic runs, set RNG seeds where applicable.
- Mechanism files are included to avoid external downloads.

---

## 🧪 Tested with

- Python 3.11
- `cantera`, `netCDF4`, `cftime`, `ruamel.yaml`, `matplotlib`, `jupyter`

---

## 🙌 Contributing

PRs are welcome! If you add a new model, please:
1. Follow the **Plot Style** defaults.
2. Add a short section to **Model Catalog**.
3. Include a small test cell or validation check.
