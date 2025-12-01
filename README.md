# Electrodynamics II - TDGL Simulations

Time-Dependent Ginzburg-Landau (TDGL) simulations for superconducting thin films with multiple terminal configurations. This project explores current-voltage characteristics and dynamics in mesoscopic superconducting devices under applied magnetic fields.

## 📋 Overview

This repository contains numerical simulations using the [py-tdgl](https://github.com/loganbvh/py-tdgl) library to study:
- **Two-terminal superconducting devices** with varying junction configurations (0-gap, 1-gap, 2-gap)
- **Current-voltage (I-V) characteristics** under magnetic field bias
- **Vortex dynamics** and current streamlines in superconducting films
- **Time-resolved voltage evolution** during current sweeps

## 🗂️ Project Structure

```
Electrodynamics_II/
├── notebooks/           # Jupyter notebooks with simulations
│   ├── 2sources_clean.ipynb      # Two-terminal 0-gap configuration
│   ├── 2sources_1gap_clean.ipynb # Two-terminal 1-gap configuration
│   └── 2sources_2gap_clean.ipynb # Two-terminal 2-gap configuration
├── datasets/            # Simulation output data
│   ├── series/          # I-V data for 0-gap
│   ├── series2/         # I-V data for 1-gap
│   ├── series4/         # I-V data for 2-gap
│   ├── two_terminal_sweep/       # Current sweep data (0-gap)
│   ├── two_terminal_1gap_sweep/  # Current sweep data (1-gap)
│   └── two_terminal_2gap_sweep/  # Current sweep data (2-gap)
├── src/                 # Source code
│   └── electrodynamics_ii/
└── pyproject.toml       # Project dependencies and configuration
```

## 🚀 Installation

This project uses [pixi](https://pixi.sh/) for environment management:

```bash
# Clone the repository
git clone https://github.com/A-guacate/Electrodynamics_II.git
cd Electrodynamics_II

# Create and activate the environment
pixi shell
```

### Requirements
- Python 3.11
- CUDA-compatible GPU (optional, for CuPy acceleration)
- Key dependencies: numpy, scipy, matplotlib, h5py, tdgl, cupy

## 📊 Usage

Open any notebook in the `notebooks/` directory to run simulations:

1. **2sources_clean.ipynb** - Base configuration without junction gaps
2. **2sources_1gap_clean.ipynb** - Single gap junction configuration
3. **2sources_2gap_clean.ipynb** - Double gap junction configuration

Each notebook includes:
- Device geometry setup and mesh generation
- Current sweep simulations (0-12 μA)
- I-V curve extraction
- Voltage time-trace analysis
- Current streamline visualization

## 🔬 Physics

The simulations solve the time-dependent Ginzburg-Landau equations for superconducting thin films with:
- **Coherence length** (ξ): 0.1 μm
- **London penetration depth** (λ): 2 μm
- **Film thickness**: 0.1 μm
- **Applied magnetic field**: 30 mT
- **Temperature regime**: Close to critical temperature (γ = 1)

## 📈 Output

Simulation results are saved in the `datasets/` directory:
- `.npz` files containing voltage and time traces for each current bias point
- `.npy` files with I-V characteristic data
- Figures showing current streamlines, vortex patterns, and voltage dynamics

## 👨‍🔬 Author

**William Alexander Pacheco Valderrama**  
wpachecov@unal.edu.co

## 🙏 Acknowledgments

This project builds upon  [py-tdgl](https://github.com/loganbvh/py-tdgl) library developed by [Logan Bishop-Van Horn](https://github.com/loganbvh). 

The simulation parameters were suggested by [nick0413](https://github.com/nick0413) to ensure numerical stability and physical accuracy.

## 📝 License
This project is part of academic research in computational superconductivity.
