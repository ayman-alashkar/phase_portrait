# Phase Portraits — Interactive Guide to Planar Systems

An interactive educational tool for visualizing and understanding phase portraits of 2×2 linear ODE systems **x′ = Ax**. Built for ODE courses, self-study, and anyone curious about dynamical systems.

🔗 **Live Demo:** [ayman-alashkar.github.io/phase_portrait](https://ayman-alashkar.github.io/phase_portrait/)

![Phase Portraits Interactive Guide](https://img.shields.io/badge/Interactive-Guide-blue?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)
![Made with](https://img.shields.io/badge/Made_with-HTML%2FJS%2FCanvas-orange?style=flat-square)

---

## Overview

Phase portraits reveal how **all** solutions of a 2D linear system behave at once. This tool pairs real-time simulations with step-by-step mathematical explanations, connecting the algebra (eigenvalues, eigenvectors, matrix exponentials) to the geometry you see on screen.

### Features

- **Six interactive tabs** covering the full theory of planar linear systems
- **Real-time RK4 integration** with animated particle trajectories
- **Click-to-add** trajectories on any phase plane
- **Parameter sliders** for smooth exploration of how eigenvalues affect dynamics
- **Time series** plots with synchronized playback
- **Trace-determinant diagram** in the Explorer tab
- **Step-by-step worked examples** from standard ODE textbooks
- **Fully responsive** — works on desktops, laptops, and tablets
- **Zero dependencies** — single HTML file, no build step, no frameworks

## Tabs

| Tab | Content |
|-----|---------|
| **Overview** | What is a phase portrait? The three canonical forms. Classification summary table. |
| **Case 1 · Real λ** | Diagonal matrices: nodes and saddles. Power-law trajectory equation. Sliders for α, β. |
| **Case 2 · Repeated λ** | Defective matrices: D+N decomposition, te^αt term, improper nodes. Slider for α. |
| **Case 3 · Complex λ** | Complex eigenvalues: rotation × exponential, foci and centers. Sliders for α, β. |
| **Examples** | Two fully worked textbook examples with step-by-step derivations. |
| **Explorer** | Free-form matrix input, parameter sliders, eigenvalue analysis, trace-det map. |

## Mathematical Content

Each case tab explains:

1. **Canonical form** — the matrix M that A is similar to
2. **Matrix exponential** — how e^{tM} is computed
3. **General solution** — explicit formulas for x₁(t) and x₂(t)
4. **Trajectory shape** — eliminating the parameter t
5. **Sub-cases** — how the sign of eigenvalues affects stability
6. **Physical analogies** — damped pendulums, overdamped doors, microphone feedback

### Classification covered

- **Stable/Unstable Nodes** — real eigenvalues, same sign
- **Saddle Points** — real eigenvalues, opposite sign
- **Star Nodes** — equal eigenvalues, diagonalizable
- **Improper Nodes** — repeated eigenvalue, defective matrix
- **Stable/Unstable Foci** — complex eigenvalues with nonzero real part
- **Centers** — pure imaginary eigenvalues

## Technical Details

- **Integration:** 4th-order Runge-Kutta (RK4) with adaptive termination
- **Rendering:** HTML5 Canvas with DPI-aware (retina) rendering
- **Eigenvalue computation:** Closed-form 2×2 eigenvalue/eigenvector solver
- **Animation:** `requestAnimationFrame` loop with time-based stepping
- **Design:** Dark academic theme with Fraunces serif + Outfit sans-serif typography

## Usage

### Quick Start

Just open `index.html` in any modern browser. No server, no build tools, no dependencies.

```bash
# Clone and open
git clone https://github.com/ayman-alashkar/phase_portrait.git
cd phase_portrait
open index.html
```

### Interaction

- **Click** on the phase plane to add a new trajectory
- **Click** near an existing trajectory to select it
- Use **Play/Pause** to animate the selected trajectory
- Use the **time slider** to scrub through the animation
- Use **parameter sliders** to change the matrix and see the portrait update live
- Use **preset pills** to jump to interesting examples

## Deployment

This is a single HTML file. To deploy on GitHub Pages:

1. Rename to `index.html` (or configure your repo accordingly)
2. Push to your repository
3. Enable GitHub Pages in repository settings

## Author

**Ayman Alashkar**
PhD Student, [Okinawa Institute of Science and Technology (OIST)](https://www.oist.jp)

## License

This project is open source and available under the [MIT License](LICENSE).

## Acknowledgments

- Mathematical content follows standard ODE textbook presentations (§2.2 — Phase Portraits and Planar Systems)
- Built as a teaching aid for ODE courses at OIST
