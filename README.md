# JRR Matterport mesh (reference)

The Julis Romo Rabinowitz Building (JRR) at Princeton, from its Matterport MatterPak (model `R1FX6EmdcDt`), pulled
through the Matterport Model API. This branch holds only these files, so `main` stays light. Fetch it when you need it:

```bash
git fetch origin jrr-mesh
git checkout jrr-mesh
```

What's in `jrr/`:

- `049aa8a684d24e138f82dd08cf435757.obj`: the textured mesh (37 MB). Opens in Blender, MeshLab or any OBJ viewer.
- `049aa8a684d24e138f82dd08cf435757.mtl` and the `049aa8a684d24e138f82dd08cf435757_NNN.jpg` files: its material and
  236 texture images. Keep them next to the `.obj`.
- `colorplan.pdf` and `colorplan_00N.jpg`: coloured floor plans; `ceilingcolorplan.*`: the same seen from below.
- `readme.pdf`: Matterport's notes on the MatterPak formats and units.

Not included: the raw point cloud (`cloud.xyz`, 2.9 GB, too big for GitHub). Isaac keeps a thinned copy for hazard
detection under `cache/clouds/` (see `nudge/perceive.py`), and can pull the full MatterPak again from the API.

The mesh is in Matterport's model frame, the same frame as the scan positions and walls Isaac routes on, in metres.
