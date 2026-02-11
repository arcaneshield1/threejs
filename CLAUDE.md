# Three.js Playground

A static Three.js playground for testing and iterating on 3D elements. Deployed via Vercel.

## Structure

- `index.html` — Single-page app with all demos, controls, and Three.js loaded via CDN import map
- `vercel.json` — Vercel deployment config (static site, no build step)

## How it works

- Three.js v0.170 loaded from jsDelivr CDN via ES module import map
- OrbitControls for camera interaction (drag to orbit, scroll to zoom)
- 6 built-in demos: Rotating Cube, Sphere Grid, Particles, Torus Knot, Shader Plane, Bouncing Boxes
- Sidebar controls: speed, color, scale, wireframe toggle, animation pause

## Development

This is a zero-build static site. Edit `index.html` and push — Vercel deploys automatically.

To add a new demo:
1. Add a `<li>` entry in the `#demo-list` section of `index.html`
2. Add a corresponding function in the `demos` object in the `<script>` block
3. The demo function should create Three.js objects, add them to `scene`, set `demoObjects` array, and define `demoUpdate(t)` callback

## Deployment

- Connected to Vercel for continuous deployment
- Every push to the main branch triggers a new deployment
- No build step required — serves static files directly
