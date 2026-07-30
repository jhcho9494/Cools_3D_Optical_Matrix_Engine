# Patent Portfolio Map — Cools 3D Optical Matrix Engine

[English Overview](README.md) | [한국어 개요](README_KR.md) | [中文概述](README_ZH.md) | [Public Notice](PUBLIC_NOTICE.md)

## Portfolio logic

The Cools 3D Optical Matrix Engine is protected as a layered technology stack rather than as a single optical component.

```text
SYSTEM ARCHITECTURE
Vertically integrated source / 3D weight volume / detector engine
                         │
        ┌────────────────┼────────────────┐
        │                │                │
 WEIGHT MEDIUM      MATHEMATICAL      SOURCE / THERMAL
 AND REWRITING      READOUT           INFRASTRUCTURE
        │                │                │
 Rewritable 3D      Signed output     TEC-free source array
 index features     Complex output    Isothermal wavelength grid
                                      Thermal-null optical bridge
                                      Athermal InP integration
                                      Long-wave VCSEL / DBR
                                      High-conductivity handle
```

The portfolio separates the system claim, the weight-storage claim, the readout claim and the enabling thermal-photonic device claims. Each family can be implemented independently and can also be combined into the complete engine.

---

## 1. System-level architecture

### Vertically-Integrated Optical Matrix-Computing Structure Having a Volume-Written Refractive-Index Weight Medium and Method for Manufacturing the Same

**Korean title**  
부피 기입 굴절률 가중치 매체를 구비하는 수직통합 광 행렬 연산 구조 및 그 제조 방법

**Portfolio role**

This is the system-level architecture linking:

- a two-dimensional light-source plane,
- a three-dimensional refractive-index weight volume inside a transparent host,
- a two-dimensional detector plane,
- one-pass optical linear transformation,
- optional rewriting of selected weight features,
- signed or complex readout,
- and the thermal architecture required to preserve the optical transfer function.

**Primary strategic position**

The matrix is not stored in a stack of target-weight planes. It is distributed through a three-dimensional optical volume integrated between source and detector planes.

---

## 2. Rewritable volumetric weight medium

### Rewritable Three-Dimensional Refractive-Index Weight Medium and Method for Rewriting the Same

**Korean title**  
재기록 가능한 3차원 굴절률 가중치 매체 및 그 재기록 방법

**Portfolio role**

This family protects the weight medium itself, independently of a particular emitter or detector implementation.

The medium includes discrete phase-change refractive-index features distributed through an optical path region. Selected features can be reversibly switched between different refractive-index states by localized optical processing.

**Core claim axis**

- three-dimensional discrete weight features,
- no continuous target-weight modulation plane,
- nonvolatile phase states,
- binary or multilevel weight programming,
- selected-feature rewriting through the host,
- and closed-loop transfer-function calibration.

**Strategic value**

The optical transform can be changed without manufacturing a new optical element.

---

## 3. Signed and complex mathematical readout

### Differential and Interferometric Detection Optical Computing Apparatus for Signed or Complex Optical Matrix Operation and Operation Method Thereof

**Korean title**  
부호 있는 또는 복소 광 행렬 연산을 위한 차동·간섭 검출 광 연산 장치 및 그 연산 방법

**Portfolio role**

This family solves the mathematical limitations of intensity-only detection and is independent of one specific weight-medium construction.

**Signed-output axis**

- decomposition of a target matrix into non-negative positive and negative components,
- matched positive and negative detector channels,
- balanced photocurrent subtraction,
- common-mode noise suppression,
- and signed real-valued matrix output.

**Complex-output axis**

- combination of the transformed field with a coherent reference beam,
- homodyne, heterodyne, phase-stepped or optical-hybrid detection,
- recovery of in-phase and quadrature components,
- and complex-valued matrix output.

**Strategic value**

The optical engine is not limited to non-negative intensity weights. It can represent the signed and phase-bearing quantities required by general matrix operations.

---

## 4. TEC-independent two-dimensional source plane

### Thermoelectric-Cooler-Free Semiconductor Light-Source Array on a High-Thermal-Conductivity Handle and Method for Manufacturing the Same

**Korean title**  
고열전도성 핸들 기반 열전냉각기 비의존 반도체 광원 어레이 및 그 제조 방법

**Portfolio role**

This family protects a dense, individually addressable two-dimensional optical input plane in which:

- thin-film semiconductor source stacks are integrated on a high-conductivity handle,
- embedded vias provide electrical and/or thermal paths,
- near-junction microchannels and an upper heat-spreading slab can provide double-sided cooling,
- and the array operates without depending on a channel-level thermoelectric cooler.

**Strategic value**

The input dimension scales with area rather than with the perimeter of an edge-coupled source arrangement.

---

## 5. Isothermal multi-wavelength source array

### Isothermal Light-Source Array for Wavelength-Grid Stabilization and Method for Manufacturing the Same

**Korean title**  
파장 그리드 안정화를 위한 등온 광원 어레이 및 그 제조 방법

**Portfolio role**

This family protects the thermal uniformity of a multi-wavelength source plane.

The in-plane thermal conductivity of a common source island and the pitch of vertical thermal vias are selected so that wavelength shift caused by channel-to-channel temperature difference remains below the wavelength-grid spacing.

**Core claim axis**

- common high-conductivity optical-source island,
- vertical via pitch as a local-temperature-control variable,
- wavelength-grid stability without channel-by-channel TEC or microheater correction,
- and optional thermal-moat isolation from a hot processor or photonic integrated circuit.

**Strategic value**

Thermal uniformity becomes a passive physical property of the source platform rather than a control burden multiplied by channel count.

---

## 6. Thermal-null optical bridge

### Thermal-Isolation Optical Coupling Structure Having a Thermal-Null-Aligned Optical Bridge and Method for Manufacturing the Same

**Korean title**  
열영점 정렬 광 브리지를 구비하는 열적 격리 광 결합 구조 및 그 제조 방법

**Portfolio role**

This family protects optical coupling between two regions maintained at different temperatures.

A narrow optical bridge crosses a thermal isolation region. The optical coupling reference is aligned near the thermal null where the expansion references of the two regions meet.

**Core claim axis**

- thermal isolation between hot and cold regions,
- low-conductance optical bridge,
- coupling reference inside the isolation region,
- thermal expansion accumulating away from the reference,
- and passive suppression of thermally induced optical misalignment.

**Strategic value**

A cold emitter island can remain optically coupled to a hot processor or photonic die without sacrificing the thermal isolation that protects wavelength and efficiency.

---

## 7. Athermally bonded InP optical engine

### Optical Engine Having an InP Photonic Device Athermally Bonded to a Reaction-Formed Substrate and Method of Manufacturing the Same

**Korean title**  
무열 접합된 InP 광소자를 구비하는 반응성형 기판 광엔진 및 그 제조방법

**Portfolio role**

This family protects the integration of an InP optical device on a reaction-formed high-conductivity substrate having separate electrical and thermal inserts.

**Core claim axis**

- reaction-bonded silicon-carbide substrate body,
- insulated electrical inserts,
- thermally coupled heat-transfer inserts,
- localized interfacial optical heating through the InP device,
- and an athermal integration fingerprint in which the active region is not subjected to the interface transformation.

**Strategic value**

Electrical drive, heat removal and low-thermal-budget optical-device attachment are integrated into one optical-engine substrate.

---

## 8. Long-wavelength VCSEL with athermally bonded DBR

### Long-Wavelength Vertical-Cavity Surface-Emitting Laser with Athermally-Bonded Distributed Bragg Reflector and Method for Manufacturing the Same

**Korean title**  
무열 접합 분포 브래그 반사기를 구비하는 장파장 수직공진 표면방출 레이저 및 그 제조 방법

**Portfolio role**

This family protects the long-wavelength vertical-cavity source used in dense source arrays.

A high-conductivity handle supports and spreads heat from a distributed Bragg reflector while optional bypass current and thermal paths avoid the electrical and thermal penalties of a thick dielectric reflector stack.

**Core claim axis**

- athermally bonded lower distributed Bragg reflector,
- high-conductivity handle as reflector support and heat spreader,
- stop-band-aware or backside/side optical bonding,
- bypass current paths around a non-conductive reflector,
- thermal bypass structures around the optical aperture,
- and two-dimensional individually addressable long-wavelength VCSEL arrays.

**Strategic value**

The reflector is no longer an unsupported thermal bottleneck placed between the active region and the package.

---

## 9. High-thermal-conductivity vertically integrated light-source platform

### Vertically-Integrated Semiconductor Light Source on a High-Thermal-Conductivity Handle and Method for Manufacturing the Same

**Korean title**  
고방열 핸들 기반 수직통합 반도체 광원 구조 및 그 제조 방법

**Portfolio role**

This is the common semiconductor-source platform underlying multiple optical-engine variants.

**Core claim axis**

- thin-film semiconductor light-source stack,
- high-conductivity handle,
- net-shape embedded vertical vias,
- interface-selective athermal bonding,
- optional near-junction microchannels,
- optional transparent upper heat spreader,
- and two-dimensional individually addressable source matrices.

**Strategic value**

The bulk III-V substrate is removed from the permanent heat path, while the handle becomes the combined thermal, mechanical, electrical-routing and optional optical platform.

---

## Combined coverage matrix

| Engine function | Primary family | Supporting families |
|---|---|---|
| Complete source-to-detector optical matrix engine | Vertically integrated optical matrix structure | All families |
| Three-dimensional weight storage | Rewritable 3D refractive-index weight medium | System architecture |
| Weight update and recalibration | Rewritable 3D refractive-index weight medium | Sub-bandgap optical integration platform |
| Signed real-number output | Differential detection | System architecture |
| Complex-number output | Interferometric detection | System architecture |
| Dense input source plane | TEC-independent source array | High-conductivity light-source platform |
| Multi-wavelength stability | Isothermal wavelength-grid array | Thermal-null optical bridge |
| Hot/cold optical co-integration | Thermal-null optical bridge | Isothermal source island |
| Low-thermal-budget InP attachment | Athermally bonded InP optical engine | High-conductivity light-source platform |
| Long-wavelength surface-emitting source | Athermally bonded DBR VCSEL | TEC-independent source array |
| Vertical electrical and thermal routing | High-conductivity light-source platform | InP optical engine / VCSEL families |

---

## Public-disclosure boundary

This repository discloses the system architecture and the relationship among the invention families. It does not publish the complete manufacturing package.

Retained implementation know-how may include:

- material formulations and precursor chemistry,
- detailed voxel coordinates and inverse-designed weight maps,
- optical writing pulse conditions and depth-control methods,
- absorber construction and interface preparation,
- source-to-volume and volume-to-detector alignment tolerances,
- phase-change endurance and drift-compensation methods,
- thermal-island dimensions and cooling conditions,
- detector balancing and coherent-reference stabilization,
- calibration algorithms,
- process-control limits,
- and reliability and qualification data.

No license is granted by this public portfolio map. See [PUBLIC_NOTICE.md](PUBLIC_NOTICE.md).

---

© 2026 Cools. Patent rights reserved.