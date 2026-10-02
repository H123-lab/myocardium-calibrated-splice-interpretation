# Reduced-order LV Digital-Twin Framework Provenance Record

## Model Specification
- **Model type:** Zero-dimensional (0D) / low-dimensional lumped-parameter left-ventricular mechanics model integrated with circulatory Windkessel afterload.
- **Biophysical Architecture:** Modified time-varying elastance framework cross-linked to multi-isoform myofilament passive material curves.

## Inputs
- **Molecular Spring Ratio:** `TTN` N2BA:N2B isoform expression ratio (modulating global matrix baseline \(C_1\) scale factor).
- **Exon Inclusion Percentages:** `TTN` PEVK region exon-level Percent Spliced-In (PSI) metrics (governing structural spring rest-length transformations).
- **Contractile Features:** `MYH7` head-domain splicing configuration features (linearly scaling maximum active isometric tension generation \(T_{max}\)).

## Outputs
- **Diastolic Function:** Directional estimates of passive myocardial stiffness changes (normalized curves of \(E_{passive}\) and filling pressure surrogates).
- **Systolic Function:** Directional estimates of contractile/function performance changes (Action Potential Duration, Conduction Velocity, and Peak \(Ca^{2+}\) Transient amplitudes).

## Recovered Framework Dependencies
- **Original model file:** NOT RECOVERED (Reconstructed via canonical forward-differential equations)
- **Geometry file:** Idealized thin/thick-walled truncated ellipsoid geometry coordinates (No personalized finite element meshes recovered)
- **Parameter file:** Integrated via a centralized array profile mapping: \(\Delta C_1 \propto - \Delta \text{Ratio}_{N2BA}\) and \(\Delta T_{max} \propto \Delta \text{PSI}_{Head}\).
- **Solver:** Python SciPy core ODE suite (`scipy.integrate.solve_ivp`) / Runge-Kutta 4th-order method.
- **Boundary conditions:** Closed-loop lumped systemic vascular impedance values (Windkessel model afterload resistance parameters).
- **Material parameters:** Hyperelastic passive framework modeling (calibrated to mimic native non-failing myocardium pressure-volume benchmarks under baseline conditions).
- **Mesh:** Non-applicable (0D/axisymmetric low-dimensional lumped system configuration).
- **Calibration procedure:** Normalized global response tracking aligning simulated trends against external cardiac validation arrays (No patient-specific individual records recovered).
