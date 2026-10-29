# Drop & Drift

A long-range ballistic solver that runs in the browser and installs to a phone or iPad home screen.

- Point-mass solver with standard G1 and G7 drag tables
- Air density from temperature, station pressure and humidity
- Shot angle, wind speed and clock direction
- Spin drift (Litz), Coriolis (horizontal and vertical) and aerodynamic jump
- Holds in MIL or MOA with turret clicks
- Bullet library with G1 and G7 BCs, plus your own bullets
- Muzzle velocity and BC truing
- Works offline after the first visit

## Files

| File | What it does |
|---|---|
| `index.html` | The whole app. The ballistics math is in the `<script id="solver">` block and has no page code mixed in. |
| `sw.js` | Saves the app on the device so it works with no signal. |
| `manifest.webmanifest` | Name and icons for installing to a home screen. |
| `*.png` | Home-screen icons. |

## Updating

When you upload a changed `index.html`, also change the version in the first lines of `sw.js`
(`dropdrift-v1` to `dropdrift-v2`, and so on). Installed copies pick up the new version the next
time they open with a connection.

## Caution

Library BCs and dimensions are starter values from published manufacturer data. Check them
against the manufacturer's current figures, and true the muzzle velocity and BC against real
impacts before relying on long-range holds.
