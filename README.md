# 🌿 LeafCraft

> A modern, production-grade procedural foliage modeling studio built with C++20 and Qt 6. Designed from the ground up for cinematic asset generation and seamless Unreal Engine 5 integration (Nanite & Pivot Painter 2.0).

---

### ⚠️ Project Status: In Active Development (WIP)

LeafCraft is currently an early-access, active development preview. Source code, binary distributions, and pipeline toolsets will be published upon reaching the v0.1 milestone.

![LeafCraft Studio Overview](docs/images/studio_overview.png)
*Figure: The LeafCraft DCC interface featuring the 4-dock procedural studio layout.*

---

## ⚡ Highlights & Core Architecture

LeafCraft bridges the gap between procedural proceduralism and artist direct manipulation, providing fine-grained numerical control alongside interactive 3D viewport sculpting.

* **High-Performance Procedural Core:** Custom C++20 geometry pipeline with Bishop-frame parallel transport for smooth, twist-free spine skinning, dynamic Hermite curves, and procedural flare generation.
* **Manifold Branch Welding:** Seamless mesh boolean collar stitching that eliminates overlapping, disconnected tubes at parent-child junctions while averaging seam normals.
* **Modern Dark Glassmorphic DCC:** Custom Qt 6.8 interface utilizing tactile, scrubbable `TickSlider` inputs, instant keyboard overrides, and clean vector node graphs.
* **Production-Grade Vertex Pipeline:** Comprehensive multi-channel vertex layout tailored specifically for real-time engines:
  * **UV0:** Full-range PBR surface mapping and custom texture chart layouts.
  * **UV1:** Non-overlapping lightmap atlas coordinates.
  * **UV2:** Dynamic branch tangent flex vectors.
  * **UV3:** Native Epic Games Pivot Painter 2.0 hierarchy and pivot data.
  * **UV4.x:** Raycast ambient occlusion pre-bakes.
  * **UV5:** Welded collar continuous vertex motion clip (`LeafCraft_WeldWind.exr`).

---

## 📸 In-Progress Showcase

| Generation Node Graph | Tactile Property Inspector |
| :---: | :---: |
| ![Generation Graph](docs/images/node_graph.png) | ![Properties Inspector](docs/images/properties_panel.png) |
| *Typed node graph with real-time child instance counters and force badges.* | *Tactile pill sliders with continuous scrubbing and numeric precision typing.* |

| Topological Branch Welding | Material Studio & Cutouts |
| :---: | :---: |
| ![Branch Welding](docs/images/welded_junction.png) | ![Material Preview](docs/images/materials_dock.png) |
| *True manifold boolean branch junctions with continuous UV transitions.* | *Real-time OpenGL PBR preview sphere with multi-slot texture sets.* |

---

## 🛠️ Tech Stack & Prerequisites

* **Language:** C++20 (MSVC 2022 / Clang 18+)
* **Framework:** Qt 6.8.3 (Core, Gui, Widgets, OpenGLWidgets)
* **Graphics API:** Modern OpenGL (Core Profile 3.3+)
* **Build System:** CMake 3.28+
* **Target Platforms:** Windows x86-64 (Linux support planned)
* **Engine Targets:** Unreal Engine 5.2+ (Nanite, Lumen, Pivot Painter 2.0)

---

## 🗺️ Roadmap to v0.1

- [x] Typed Generation Graph (9 geometry classes, 10 placement modes)
- [x] Continuous bishop frame branch extrusion and split branching
- [x] Real-time Raycast Ambient Occlusion & Harmonic Wind Solver
- [x] Manifold branch junction welding with collar falloff
- [x] Full multi-channel vertex exporter (glTF 2.0 / FBX + EXR bundles)
- [ ] 3D Viewport direct Hermite knot manipulation and trimming gizmos
- [ ] Automated Unreal Engine 5 importer script and Master Material generator
- [ ] Public source release and pre-built binaries

---

## 📄 License & Notes

All rights reserved © 2026. Licensing terms, documentation, and source code will be updated with the initial public release.
