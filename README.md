# BATTLEZONE FPS

An original, browser-playable first-person survival shooter prototype. It is a learning project and a foundation for a later native Unity/C# PC and Android build.

## Run locally

1. Install [Visual Studio Code](https://code.visualstudio.com/) if you do not already have an editor.
2. Clone this repository and open its folder in VS Code.
3. Install the free **Live Server** extension in VS Code.
4. Right-click `index.html` and choose **Open with Live Server**.
5. Open the local address shown by VS Code in a modern browser with WebGL support.

Alternative: if Python is installed, run `python -m http.server 5173` in the project folder and open `http://localhost:5173`.

This is a static, single-file prototype: no `npm install` or build step is required. Internet access is required to load Three.js from the CDN.

## Controls

- PC: WASD move, mouse look, Shift sprint, C crouch, left-click fire, right-click aim, R reload, E collect, G throw grenade, 1/2 switch weapon.
- Touch: left joystick to move, drag the right side to look, FIRE, AIM and R buttons.
- Match: eliminate all hostile bots before the five-minute clock expires and stay inside the contracting safe area.

## Dependencies and licenses

- [Three.js 0.160.0](https://threejs.org/) is loaded as an ES module from [jsDelivr](https://cdn.jsdelivr.net/npm/three@0.160.0/build/three.module.js). Three.js is distributed under the [MIT License](https://github.com/mrdoob/three.js/blob/dev/LICENSE). The CDN is an external runtime dependency; no API key or paid service is used.
- The arena geometry, prototype code, HUD and generated Web Audio tones in this repository are original project work. No third-party game characters, maps, music, sound recordings or proprietary assets are included.
- Browser audio is generated at runtime using the Web Audio API; there are no audio-file dependencies.

## Current milestone

Prototype 08 adds cover-aware combat. Building structures block the player's hitscan shots and prevent enemy bots from firing through walls. The game remains single-player and browser-based.

## Known limitations

- Enemy navigation is still lightweight steering, not full pathfinding; bots can occasionally hesitate around obstacles.
- Cover checks currently use the main building meshes. Smaller crates, barrels and trees are not full ballistic cover.
- This is not online multiplayer. A future multiplayer version needs a dedicated authoritative server or a separate networking backend for movement, hit validation, matchmaking and anti-cheat.
- Browser performance and touch controls vary by device. Test on target Android phones and desktop browsers before treating a milestone as stable.
