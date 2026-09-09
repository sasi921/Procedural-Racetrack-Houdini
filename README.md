# Procedural Racetrack Environment in Houdini

A procedural 3D environment project created in **SideFX Houdini Non-Commercial**. The scene builds a customizable racetrack integrated with generated terrain, barriers, lane details, and procedurally scattered trees.

## Project Overview

The goal of the project is to show how Houdini's node-based procedural workflow can create a reusable environment where the terrain, track layout, barriers, and vegetation can be adjusted without rebuilding the scene from scratch.

## Workflow

### 1. Terrain Generation

- A **Grid** node provides the base terrain surface.
- A **Mountain** node introduces hills and valleys.
- Height and frequency parameters control the terrain profile.

### 2. Racetrack Creation

- Curves define the track path and boundaries.
- A **Sweep** node creates the track geometry from the curves.
- UV preparation supports asphalt and marking materials.
- Auxiliary curves, Add, and Resample nodes generate repeating lane/boundary details.

### 3. Barrier Placement

- Reusable `.bgeo` barrier geometry is imported into the scene.
- Barriers are aligned procedurally along the racetrack edges.
- Group and color controls make sections easier to manage.

### 4. Procedural Forest

- Tree `.bgeo` assets are used as reusable geometry.
- **Scatter** nodes generate placement points across the terrain.
- **AttribTransfer** helps control forest density.
- **Copy to Points** instances trees efficiently.
- Transform variation randomizes scale and rotation for a more natural result.

### 5. Final Integration

- Terrain, racetrack, barriers, and trees are merged into the complete environment.
- Normals and smoothing improve shading.
- Cameras, lights, and materials prepare the scene for rendering.
- The project was designed with Karma or another compatible renderer in mind.

## Repository Contents

```text
Procedural-Racetrack-Houdini/
├── README.md
└── docs/
    └── PROJECT-REPORT.md
```

The original Houdini source package also contains `racetrack.hipnc` plus reusable geometry assets (`barrier.bgeo`, `firtreeA.bgeo`, `firtreeB.bgeo`, and `tire.bgeo`). Those are binary Houdini files and are kept separately from the GitHub-readable documentation currently in this repository.

## Skills Demonstrated

`Houdini` · `Procedural Modeling` · `Node-Based Workflows` · `Terrain Generation` · `Geometry Instancing` · `Point Scattering` · `UV Mapping` · `3D Environment Design`

## Author

**Sasidhar Reddy Velkuri**
