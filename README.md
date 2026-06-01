# FlightSimulatorProject1

A single-file JavaScript flight simulator built with Three.js. It creates a huge procedural world, a flyable airliner, airports, AI traffic, collision detection, audio, smoke effects, maps, and a HUD.

## Run It

Open `gemini-code-1780309344786.html` in a browser. The project currently loads Three.js from a CDN, so the page needs internet access the first time it runs.

## Controls

- `Shift` / `Ctrl`: throttle up / down
- Drag the throttle lever with the mouse
- `W` / `S`: pitch down / up
- `A` / `D`: roll left / right
- `Q` / `E`: yaw left / right
- `G`: landing gear
- `F`: flaps
- `B`: airbrake
- `M`: large map

## Code Map

- HTML and CSS: cockpit HUD, gauges, throttle, maps, crash screen
- Setup: Three.js scene, camera, renderer, sun, fog
- World: terrain height function, ocean, airport runways, terminals, trees
- Aircraft: procedural airliner model made from Three.js geometry
- AI traffic: other planes fly between airports
- Effects: exhaust smoke, engine audio, touchdown and crash sounds
- Controls: keyboard and throttle lever input
- Physics loop: speed, thrust, drag, lift, landing, crashes, camera, HUD updates
- Flight assist: co-pilot style advisory text for takeoff, approach, overspeed, sink rate, and arrival

## Good Next Missions

1. Add a pause button and reset key.
2. Add a simple waypoint mission: fly from one named airport to another.
3. Improve mobile support with touch controls for pitch, roll, and throttle.
4. Split the large HTML file into `index.html`, `style.css`, and `simulator.js`.
5. Add a proper autopilot mode for heading, altitude, or approach hold.
6. Save best landings: touchdown speed, descent rate, and airport name.

## Notes For Learning

The most important function is `animate()`. It runs every frame and connects the whole simulator together: input, physics, AI traffic, collisions, camera, HUD, and rendering.

The best way to experiment is to change one small number at a time, refresh the browser, and write down what changed. Flight physics can get wild fast, which is part of the fun.
