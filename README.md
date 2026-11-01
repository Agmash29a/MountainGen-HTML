# MountainGen — standalone HTML edition

Open `index.html` in a modern web browser. No installation, server, framework, build, or internet connection is required.

This is a browser-only adaptation of [MountainGen-Web](https://github.com/Agmash29a/MountainGen-Web), itself inspired by Riley T. Perry's original [MountainGen](https://github.com/Agmash29a/MountainGen) from 2002.

## Porting notes

- `TerrainGenerator.Generate()` uses the same triangular base and subdivision falloff as the C# generator.
- `DivideLine()`, `Make_Sides()` and `MakeTriangle()` deliberately preserve the original VB6 terminology.
- Each edge midpoint is cached so adjacent triangles share vertices.
- A seeded JavaScript PRNG replaces C# `System.Random`, so meshes will not match the C# version bit-for-bit for identical seeds.
- Flat-shaded material classification uses the same snowline/vegetation/rock rules.
- 3D display is implemented in software using Canvas 2D, camera transforms and depth sorting rather than Three.js/WebGL. This can produce minor water/terrain occlusion artefacts and can be slower at 16,384 triangles.
- OBJ and PNG downloads work locally.

No files in the original GitHub repository have been altered.