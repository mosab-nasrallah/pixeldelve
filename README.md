# Pixeldelve

A small pixel-art mining and crafting game. A flat 2D sprite miner explores a 3D voxel island: punch trees, craft tools, dig into caves, fight slimes and work your way up to a diamond pickaxe.

**Play it:** https://mosab-nasrallah.github.io/pixeldelve/

![Pixeldelve](https://img.shields.io/badge/runs%20in-the%20browser-f2b33d)

## Features

- A new random island every game, with hills, beaches, caves, trees, coal, iron and diamonds
- Hold-to-mine blocks with a tool tier system (wood → stone → iron → diamond)
- Compact crafting list with Workbench and Furnace stations
- Underground cutaway view so you never lose sight of your miner
- Slimes to fight, swords to craft, lanterns to light caves
- A goal tracker that walks you through the progression
- Autosaves in your browser; touch controls on phones and tablets

## Controls

| Action | Keys |
| --- | --- |
| Walk | `W` `A` `S` `D` |
| Jump | `Space` |
| Mine / attack | Hold left mouse button |
| Place block | Right mouse button |
| Pack & crafting | `E` or `Tab` |
| Pick hotbar slot | `1`–`9` or mouse wheel |
| Turn camera | `←` `→` or middle-drag |
| Zoom | `↑` `↓` or Shift + wheel |

## Run it yourself

It is a single HTML file with no build step. Clone the repo and open `index.html` in a browser, or serve the folder:

```bash
python -m http.server 8000
```

Then visit http://localhost:8000. It needs an internet connection the first time to load [three.js](https://threejs.org/) and the pixel fonts from CDNs.

## Tech

- [three.js r128](https://threejs.org/) for rendering, drawn at 1/3 resolution and upscaled for crisp pixels
- All textures, sprites and icons are generated in code at startup, so there are no image files
- Chunked voxel meshing with face culling, ambient occlusion and simple sky and lantern lighting

## License

MIT
