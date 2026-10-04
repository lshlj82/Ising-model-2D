# The two-dimensional Ising model

An interactive, single-file web demo of the Ising model on the square lattice: Onsager's exact solution, simulations, Peierls' argument, Widom's scaling ansatz, the scaling relations, and the Ginzburg criterion. It is based on lecture notes by Sang Hoon Lee for Chapter 2, which follow K. Christensen and N. R. Moloney, *Complexity and Criticality* (2005). It is a companion to the other Ising and percolation demos.

Everything runs in the browser. There is no build step, no server and no dependencies beyond an optional web font. Units are k<sub>B</sub> = 1 and J = 1.

## Running it

Open `index.html` in any modern browser (Chrome, Edge, Firefox or Safari).

To publish it with GitHub Pages, push this repository, then go to **Settings → Pages**, choose **Deploy from a branch**, and select the branch and the root folder. The page will be served at `https://<user>.github.io/<repository>/`.

## What the page contains

**Live lattice.** A two-dimensional Ising model from 8 × 8 to 256 × 256 with Metropolis or Wolff updates, temperature presets, a field H, and charts of m over time, its distribution, and the spin–spin correlation function.

**Onsager's exact solution.**

- Z(T, 0), m<sub>0</sub>(T), ε(T) and c(T), using complete elliptic integrals computed with the arithmetic–geometric mean
- Wolff simulations of 16 × 16, 32 × 32 and 64 × 64 lattices compared with the exact curves
- β = 1/8 on log–log axes, with the finite-size flattening near T<sub>c</sub>
- χ against |t| with Γ<sup>±</sup>|t|<sup>−7/4</sup> (Γ<sup>+</sup>/Γ<sup>−</sup> ≈ 37.69)
- the logarithmic divergence of c (α = 0)

**Peierls' argument.** A random droplet of flipped spins on a clickable 16 × 16 lattice, with its interface length n, energy 2Jn and entropy bound ln(N3<sup>n</sup>). A chart shows the bound k<sub>B</sub>T<sub>c</sub> &gt; 2J/[ln 3 + (ln N)/√N] approaching 2/ln 3 ≈ 1.820, compared with one dimension, where a droplet always costs only 4J.

**Widom's scaling ansatz.** Metropolis simulations of a 64 × 64 lattice in a field at 10 reduced temperatures and 4 reduced fields. They are plotted raw as m against h and collapsed as m/|t|<sup>β</sup> against h/|t|<sup>Δ</sup> onto the two scaling functions 𝓜<sub>±</sub>, with sliders for β and Δ and presets for the 2D and mean-field values. The text derives the scaling forms for χ, c and g(r).

**Scaling relations.** A calculator that takes ν, η and d and returns α, β, γ, δ and Δ from hyperscaling, Fisher's relation and the Widom relation, and checks Rushbrooke's relation and the Ginzburg dimension (γ + 2β)/ν. Presets cover 2D exact, 3D numerical, mean field at d = 4, and d = 1 with the reduced temperature t = e<sup>−kJ/k<sub>B</sub>T</sup> and a slider for k.

**Non-universal T<sub>c</sub>, universal exponents.** Tables of critical temperatures for different lattices and of exponents for d = 1, 2, 3 and ≥ 4 and for mean field.

**The Ginzburg criterion.** The derivation of d &gt; (γ + 2β)/ν and the upper critical dimension d<sub>u</sub> = 4, with a chart of the relative fluctuations (−t)<sup>d/2 − 2</sup> for d = 2 to 5.

## Methods

| Topic | Approach |
| --- | --- |
| Exact curves | Onsager's ε and c with complete elliptic integrals F and E (arithmetic–geometric mean); Yang's m<sub>0</sub>; χ amplitudes Γ<sup>+</sup> ≈ 0.42420 and Γ<sup>−</sup> ≈ 0.011254 |
| H = 0 sweep | Wolff cluster updates, 200 equilibration and 1 500 measurement sweeps per temperature; k<sub>B</sub>Tχ = (⟨M²⟩ − ⟨\|M\|⟩²)/N, k<sub>B</sub>T²c = (⟨E²⟩ − ⟨E⟩²)/N |
| Field runs for the collapse | Checkerboard Metropolis on 64 × 64, 400 equilibration and 1 200 measurement sweeps per (t, h), starting from all spins up |
| Peierls droplet | Random cluster growth from the center; interface length counted as broken bonds |

## Files

```
index.html   the complete demo (HTML, CSS and JavaScript in one file)
README.md    this file
```

## References

**Key reference.** K. Christensen and N. R. Moloney, *Complexity and Criticality*, Imperial College Press, London (2005), Chapter 2.

1. L. Onsager, "Crystal statistics. I. A two-dimensional model with an order-disorder transition," *Phys. Rev.* **65**, 117 (1944).
2. C. N. Yang, "The spontaneous magnetization of a two-dimensional Ising model," *Phys. Rev.* **85**, 808 (1952).
3. H. A. Kramers and G. H. Wannier, "Statistics of the two-dimensional ferromagnet. Part I," *Phys. Rev.* **60**, 252 (1941).
4. R. Peierls, "On Ising's model of ferromagnetism," *Proc. Cambridge Philos. Soc.* **32**, 477 (1936).
5. B. Widom, "Equation of state in the neighborhood of the critical point," *J. Chem. Phys.* **43**, 3898 (1965).
6. K. Huang, *Statistical Mechanics*, 2nd ed., Wiley (1987), Chapters 14 and 15.
7. N. Metropolis, A. W. Rosenbluth, M. N. Rosenbluth, A. H. Teller and E. Teller, "Equation of state calculations by fast computing machines," *J. Chem. Phys.* **21**, 1087 (1953).
8. U. Wolff, "Collective Monte Carlo updating for spin systems," *Phys. Rev. Lett.* **62**, 361 (1989).
9. R. J. Baxter, *Exactly Solved Models in Statistical Mechanics*, Academic Press (1982).

## Credits

Lecture notes: Sang Hoon Lee.

Created by Claude Opus 5.5.
