# Electric Field Visualization (Point Charges)

Simulation of field lines and equipotential surfaces for a system of point charges arranged at the vertices of a regular polygon, with equal-magnitude but varying-sign configurations.

## Physics background

Starting from Maxwell's equations in the static case (`∇·E = ρ/ε₀`, `∇×E = 0`), the field and potential of a single point charge are derived using Gauss's theorem in spherical symmetry:

- `E(r) = kq / r²`
- `φ(r) = kq / r`

The total field and potential of a multi-charge system are obtained via the superposition principle:

- `E(r) = Σ kqₙ/rₙ³ · rₙ`
- `φ(r) = Σ kqₙ/rₙ`

## What the code does

- Builds a 2D coordinate grid and computes the scalar potential `φ` and field components `(Eₓ, E_y)` for an arbitrary list of `(x, y, q)` point charges via superposition
- Visualizes field lines with `matplotlib.pyplot.streamplot` and equipotential contours with `plt.contour`
- Compares three configurations of 5 charges with different sign combinations, and configurations of 4/5/6 equal-magnitude charges at the vertices of a square/pentagon/hexagon with alternating signs

## Files

| File | Description |
|---|---|
| `field_visualization.py` | Full simulation and plotting script |
| `figures/` | Output plots for the charge configurations described in the report |
| `report.pdf` | Full write-up: derivation, methodology, and results (in Russian) |

## Example result

Field lines (blue) and equipotential lines (red, solid = positive charge, dashed = negative) for `q = (2, -3, 5, -4, 1)`:


## Running it

```bash
pip install numpy matplotlib
python field_visualization.py
```

## Contributors

- Anastasiia Latysheva
- Yulia Kriventsova

Reviewed by A. Chaikovskaya (course project, Dec 2024).


