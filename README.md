# Curated Footage to 3D Reconstruction

**Shahram Shafiq | AI-Based 3D Reconstruction Track | PreserveMy.World x TechRealm 2026**

Live page: **[Add your GitHub Pages URL here after enabling Pages]**

---

## What this is

A single, self-contained web page that curates the strongest footage and reconstruction work from this internship into one narrative: real photos of two Pakistani heritage sites, the actual feature-detection and depth math behind reconstruction, and a genuine, live, drag-to-rotate 3D point cloud running in the browser via Three.js, not a screenshot or a mockup.

Everything shown is real work already built and verified in [`shahramshafiq/PMW-day1`](https://github.com/shahramshafiq/PMW-day1), pulled into this dedicated repo so it can be a clean, fully public, login-free web page.

---

## Structure

```
PMW-heritage-showcase/
├── index.html              <- the whole page, single file
└── assets/
    ├── badshahi/            <- 6 real, verified Badshahi Mosque photos
    ├── taxila/               <- Jaulian monastery ruins photo
    ├── pipeline/             <- ML feature map, AR overlay, capture-to-3D renders
    └── ply/
        └── jaulian_monastery_taxila.ply   <- the real point cloud, loaded live
```

---

## The live 3D viewer

Built with Three.js (loaded via CDN, no build step) and `PLYLoader`. It loads the actual `.ply` file, the same one hand-validated in the original build (13,375 points, vertex count and colors verified in-browser before shipping this page). Drag to rotate, scroll to zoom, matches the honest documentation already written for this reconstruction: a monocular depth heuristic, not multi-view Structure from Motion (that was tested first and ruled out on the curated Badshahi Mosque photos, only 12-17 geometrically consistent matches out of 2,000+ keypoints per photo pair, documented on the page itself).

---

## Why a separate repo

The portal's own review feedback flagged login-gated links as a real weakness elsewhere in this internship. A GitHub Pages site is the opposite of that: fully public, no account needed, loads directly. This repo exists specifically to be that kind of artifact.
