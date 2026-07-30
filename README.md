# Cools 3D Optical Matrix Engine

[한국어](README_KR.md) | [中文](README_ZH.md) | [Patent Portfolio](PATENT_PORTFOLIO.md) | [Public Notice](PUBLIC_NOTICE.md)

## Write the matrix into the volume. Rewrite it without rebuilding the device.

**Cools proposes a vertically integrated photonic-computing engine in which a two-dimensional light-source plane, a three-dimensional refractive-index weight volume, and a two-dimensional detector plane are integrated across a thermally stabilized optical host.**

Instead of stacking multiple planar masks, the target linear transformation is encoded as discrete refractive-index features distributed through the optical volume. The input optical field passes through the volume once and is mapped to the detector plane. Selected weight features can be locally rewritten, while differential and interferometric readout extend the architecture to signed and complex matrix operations.

![System architecture](assets/system_architecture.svg)

---

## 1. The conventional bottleneck

Conventional free-space optical computing commonly places one or more two-dimensional modulation planes between an emitter plane and a detector plane. This creates four structural limits:

- the number of independent weights is constrained by planar pixel count,
- multiple planes require layer-to-layer alignment,
- interfaces between stacked planes accumulate optical error,
- and fixed masks must be remade when the target transformation changes.

Intensity-only detection introduces an additional limitation: optical intensity is non-negative and does not directly retain the phase of the optical field. A practical matrix engine therefore needs not only a volumetric weight medium, but also signed and complex readout.

---

## 2. Cools architecture

```text
2D detector plane
(differential / interferometric readout)
────────────────────────────────────
Transparent optical path region
with discrete 3D refractive-index features
= volumetric weight medium
────────────────────────────────────
2D individually addressable light-source plane
────────────────────────────────────
Thermally conductive handle, vias and cooling path
```

The architecture divides system functions as follows:

| Element | Primary function |
|---|---|
| 2D light-source plane | Encodes the input vector as a spatial optical-field distribution |
| 3D refractive-index weight volume | Applies the target linear transformation during propagation |
| 2D detector plane | Reads the output distribution and converts it to electrical signals |
| Differential readout | Produces signed real-valued outputs |
| Interferometric readout | Recovers phase and complex-valued outputs |
| High-thermal-conductivity host | Provides optical propagation, mechanical support and thermal stabilization |
| Embedded vias / thermal paths | Provide vertical addressing and heat extraction |

---

## 3. From planar masks to volumetric weights

The weight medium contains discrete regions whose refractive index differs from that of the surrounding optical host. Their position, size, refractive-index contrast and state are selected from the target matrix or neural-network transfer function.

Representative weight features may include:

- high-index inclusions,
- low-index porous regions,
- locally doped regions,
- crystalline or amorphous regions,
- implanted or defect-engineered regions,
- phase-change material regions,
- and void or cavity voxels.

The decisive architectural shift is:

```text
Stacked 2D modulation planes
              ↓
A single optical host containing distributed 3D weight features
```

The optical field is transformed while propagating through the volume. No continuous target-weight modulation film is required between the emitter and detector planes.

---

## 4. One-pass optical matrix operation

The source array is driven according to an input vector. The emitted optical field propagates through the three-dimensional weight volume, where it undergoes controlled scattering and phase delay. The resulting field distribution reaches the detector plane as the matrix-operation output.

```text
Input vector
    ↓
2D source distribution
    ↓
Single pass through 3D weight volume
    ↓
Output optical-field or intensity distribution
    ↓
Electronic accumulation / normalization / activation
```

The propagation itself performs the linear mapping. System energy is concentrated in light generation, detection and required electronic post-processing rather than repeated electronic multiply-accumulate data movement.

---

## 5. Rewritable nonvolatile weight volume

Selected refractive-index features may contain a phase-change material that can reversibly transition between states with different refractive indices. A processing beam that passes through the host and is preferentially absorbed by the selected feature locally changes its phase state.

![Rewritable weight cycle](assets/rewrite_cycle.svg)

The rewriting concept provides:

- local update of selected weight voxels,
- nonvolatile retention without continuous bias power,
- binary or multilevel refractive-index states,
- repeated calibration against the measured transfer function,
- and update of the optical transformation without rebuilding the whole device.

A representative closed-loop procedure is:

1. apply a known optical input,
2. measure the actual detector response,
3. compare the measured and target transfer functions,
4. select the weight features to be changed,
5. locally rewrite those features,
6. repeat until the residual error meets the target.

The same class of sub-bandgap optical-processing equipment used for localized bonding can also serve as a weight-writing and recalibration tool.

---

## 6. Signed and complex matrix readout

A non-negative optical-intensity medium alone cannot directly represent arbitrary signed values. Cools separates a target matrix into positive and negative components and detects them with matched channels.

```text
W = W⁺ − W⁻
Output = detector(W⁺x) − detector(W⁻x)
```

Balanced detection can subtract the two photocurrents before digitization, suppressing common-mode source fluctuation and expanding usable dynamic range.

For complex-valued operations, the transformed optical field is combined with a phase-coherent reference beam. Homodyne, heterodyne, phase-stepped or optical-hybrid detection recovers the in-phase and quadrature components.

![Signed and complex readout](assets/signed_complex_readout.svg)

This makes the detector architecture independent of a single weight-medium implementation: the same readout concept can be coupled to volumetric, diffractive, waveguide-based or hybrid optical weight structures.

---

## 7. Thermal architecture is part of the computing architecture

Optical computation is highly sensitive to temperature because emitter wavelength, refractive index and optical phase drift with temperature. The Cools platform therefore treats heat flow as a primary system variable.

The platform may combine:

- a high-thermal-conductivity SiC, AlN, diamond, sapphire or transparent-ceramic optical host,
- a separate high-conductivity support and heat-spreading region,
- net-shape embedded vias for vertical heat and electrical paths,
- near-junction microchannels,
- a transparent upper heat-spreading slab,
- an isothermal multi-wavelength source island,
- and a thermal moat separating the source island from a hot processor or photonic integrated circuit.

The source array can thereby maintain channel-to-channel temperature uniformity and stabilize a wavelength grid without assigning a thermoelectric cooler or microheater to every channel.

---

## 8. Athermal source integration

Thin-film semiconductor light-source stacks can be joined to the thermally conductive host by interface-selective optical heating. The processing wavelength passes through the optical device body and is absorbed mainly at a dedicated interfacial absorber.

The intended structural result is:

- localized interfacial transformation,
- no corresponding thermal transformation in the optical active region,
- a short heat path from the active region to the handle,
- and preservation of wavelength and threshold-current characteristics during integration.

The source plane may include long-wavelength vertical-cavity surface-emitting lasers, distributed-feedback lasers, edge-emitting lasers, light-emitting diodes or other individually addressable thin-film optical sources.

---

## 9. Thermal-null optical bridge

Where a cold light-source island must couple to a hotter processor or photonic integrated circuit, the two regions can be separated by a thermal isolation gap and linked by a narrow optical bridge.

The optical coupling reference is positioned near the thermal null—the location at which the expansion references of the two regions meet. Thermal expansion then accumulates away from the coupling reference rather than across it.

This enables:

- optical continuity across a thermally isolated boundary,
- very small conductive heat leakage through the bridge,
- passive reduction of thermally induced coupling displacement,
- and close integration of cold emitters with hot electronic or photonic dies.

---

## 10. System scaling

The architecture scales in several dimensions:

### Spatial scaling

More source pixels, detector pixels and weight voxels increase the input dimension, output dimension and transformation complexity.

### Depth scaling

The optical host thickness provides additional independent weight locations beyond a single planar pixel count.

### Wavelength scaling

Multiple wavelengths can traverse the same volume or different depth regions to execute parallel transformations.

### Tiling

Multiple volumetric-weight tiles can be arranged laterally or vertically, with each tile executing a matrix sub-block.

### Layer scaling

The detector output can drive another source plane through electronic post-processing, or multiple optical stages can be optically interconnected to form successive neural-network layers.

---

## 11. Patent-backed technology stack

This repository consolidates a related portfolio covering the complete engine rather than a single optical component:

1. vertically integrated optical matrix computing with a volume-written refractive-index weight medium,
2. rewritable three-dimensional refractive-index weight media,
3. differential and interferometric detection for signed or complex optical matrix operations,
4. thermoelectric-cooler-independent high-density light-source arrays,
5. isothermal source arrays for wavelength-grid stabilization,
6. thermal-null-aligned optical bridges across thermally isolated regions,
7. athermally bonded InP optical engines on reaction-formed substrates,
8. long-wavelength vertical-cavity surface-emitting lasers with athermally bonded distributed Bragg reflectors,
9. and vertically integrated semiconductor light sources on high-thermal-conductivity handles.

See [PATENT_PORTFOLIO.md](PATENT_PORTFOLIO.md) for the portfolio map.

---

## 12. What is fundamentally different

| Conventional architecture | Cools architecture |
|---|---|
| Weight stored in one or more planes | Weight distributed through a 3D optical volume |
| Fixed optical mask | Locally rewritable nonvolatile weight features |
| Non-negative intensity result | Signed differential and complex interferometric readout |
| Layer-alignment accumulation | Single-host volume with no stacked target-weight planes |
| Thermal drift treated after design | Thermal path, isothermal source array and thermal isolation co-designed with computation |
| Separate bonding and tuning equipment | Local optical-processing platform can support bonding, rewriting and calibration |

This is not merely a new optical accelerator layout. It is an integrated material-device-system architecture in which the optical medium itself stores the transform, the detector reconstructs its mathematical sign and phase, and the thermal platform preserves the transform during operation.

---

## 13. Relationship to other Cools platforms

This repository covers the **complete three-dimensional optical matrix engine**. It can be combined with:

- [Cools Thin-Film III-V on SiC Platform](https://github.com/jhcho9494/Cools_ThinFilm_III-V_on_SiC_Platform) — thin active III-V optical layers on a permanent SiC thermal platform,
- [Cools CPO Zero Thermal Budget Bonding](https://github.com/jhcho9494/Cools_CPO_Zero_Thermal_Budget_Bonding) — interface-selective heterogeneous integration,
- [Cools Thermally Active Photonic Substrate](https://github.com/jhcho9494/Cools_Thermally_Active_Photonic_Substrate) — optical and thermal substrate engineering,
- [Cools Vertical Electro-Opto-Thermal Interconnect](https://github.com/jhcho9494/Cools_Vertical_Electro_Opto_Thermal_Interconnect) — vertically integrated electrical, optical and heat-flow paths,
- and [Cools 2D Optical Qubit Control Matrix](https://github.com/jhcho9494/Cools_2D_Optical_Qubit_Control_Matrix) — individually addressable optical control arrays.

---

## 14. Development and collaboration scope

Cools is open to technical evaluation and joint development in:

- inverse design of volumetric optical transfer functions,
- transparent host and embedded-weight material systems,
- phase-change optical voxels and multilevel programming,
- sub-bandgap localized writing and recalibration,
- high-density source and detector-plane integration,
- balanced and coherent optical readout,
- thermal-island and thermal-null optical packaging,
- wafer- and panel-level fabrication,
- and application-specific optical AI engines.

This repository provides a public architectural disclosure. Detailed material formulations, optical-writing conditions, voxel maps, process windows, device layouts, calibration algorithms and qualification data remain subject to separate technical and intellectual-property arrangements.

---

## Inventor and contact

**Jinhyun Cho**  
Cools  
Republic of Korea

For joint development, licensing discussion or technical evaluation, please contact Cools through the repository owner profile.

---

© 2026 Cools. Patent rights reserved. See [PUBLIC_NOTICE.md](PUBLIC_NOTICE.md).