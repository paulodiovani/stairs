# Escada 3D

A simple static website for designing a straight residential staircase (escada reta) in 3D. The interface is in **Brazilian Portuguese**.

The 3D staircase model was created using the Claude Design tool.

## Purpose

Helps visualize and tune the geometry of a home staircase before building it. Adjusts step dimensions interactively and shows whether the proportions meet ergonomic guidelines (the `2h + b ≈ 63–64 cm` rule commonly used in Brazilian construction).

## Features

- Real-time 3D preview powered by [Three.js](https://threejs.org/) (loaded from CDN, no build step).
- Sliders for step depth, nosing overhang (bocel), person height, and position on the stairs.
- Preset buttons for common step depths (24–27 cm).
- Computed readouts: riser height, `2h + b` value, inclination angle, free headroom under the beam, step plate thickness, and gap between steps.
- Toggleable dimension labels rendered on top of the 3D view.
- Light/dark theme that follows the system preference.
- Responsive layout: sidebar collapses below the viewport on narrow screens.

## Design assumptions

The calculations are based on a specific project:

- 15 cm concrete slab
- 15 cm wide beam with its bottom face at 2.375 m
- 15 cm central spine, 5 cm step plates (no riser boards, except the last step closed by the wall)
- 2.55 m high × 2.80 m long wall, ending at the beam
- 90 cm wide opening in the slab

Free headroom is measured along the nosing line, under the inner face of the beam.

## Usage

Open `index.html` in any modern browser. No server, no dependencies to install.

Drag to orbit the camera, scroll to zoom.

## Files

- `index.html` — single-file application (HTML, CSS, and JavaScript all inline).
- Three.js and `OrbitControls` are fetched from the jsDelivr CDN at runtime.
