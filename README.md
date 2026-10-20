
VOIDRUNNER
"THE SECTOR WILL NOT SURVIVE YOU."
VOIDRUNNER is a fast-paced, top-down sci-fi action roguelite built for desktop and mobile browsers. Pilot customizable starfighters across hostile cosmic sectors, battle intelligent alien squadrons, draft synergistic combat upgrades in real time, and defeat multi-phase dreadnought bosses.
Built from the ground up using HTML5 Canvas 2D, TypeScript, React 19, Tailwind CSS, and a 100% procedural Web Audio API sound and music synthesizer—with zero external asset dependencies or backend requirements.
✨ Features
🚀 Responsive Flight & Combat Simulation
Custom 2D Vector Engine: High-contrast procedural spacecraft, multi-layered parallax starfields, cosmic nebulae, and dynamic particle effects running on a delta-time game loop.
Tactical Mobility: Smooth thruster acceleration, directional inertia damping, and a high-speed Thruster Boost / Dash with invulnerability frames.
Ultimate Ability — Void Burst: Charge your Ultimate gauge by dealing damage and eliminating enemies. Trigger Void Burst (F or mobile BURST button) to unleash an expanding cosmic EMP shockwave that vaporizes all enemy projectiles on screen, damages nearby threats, and grants temporary Hyperdrive fire rate and invulnerability.
Combo Killstreak System: Chain rapid kills to build multipliers (1.5x, 2.0x, 3.0x, up to 5.0x), boosting both score and Scrap yields.
Tactical HUD & Radar: Real-time mini-map radar, off-screen threat direction pointers, floating combat damage numbers, and boss phase telemetry.
🔫 4 Distinct Weapon Systems
Switch weapons on the fly (1–4, Q, or the mobile SWAP GUN button):
Pulse Cannon: Balanced, rapid-cycle plasma bolts with reliable range and accuracy.
Rapid Vector: High-cadence rotary particle accelerator designed to shred swarming targets.
Tri-Burst: Triple-barrel divergent shotgun wedge for devastating close-quarters impact.
Pierce Lance: High-velocity antimatter rail emitter that punches straight through multiple armored hulls.
👾 Hostile Fleet & 3 Multi-Phase Boss Encounters
5 Enemy Archetypes:
Void Scout: Fast vanguard fighter that closes distance rapidly.
Spectre Interceptor: Executes lateral flanking maneuvers and fires twin-burst volleys.
Iron Bruiser: Heavy armored cruiser firing 3-way plasma clusters.
Siege Drone: Long-range sniper platform that projects a visible red targeting laser before firing high-velocity rounds.
Elite Hunter: Aggressive apex pursuer with spiral projectile barrages and guaranteed Scrap drops.
3 Colossal Bosses:
Sector 01 — THE WARDEN: Heavy defensive fortress with rotating outer aegis shields and radial bullet rings.
Sector 02 — VOID REAPER: Fast scythe-wing predator with sweeping arc attacks and summoned support drone swarms.
Sector 03 — THE SINGULARITY: Final dimensional nexus core with rotating double-helix barrages and an Event Horizon collapse phase.
⚡ Rogue Upgrade Draft & Orbital Hangar
14 In-Run Rogue Upgrades: Draft 1 of 3 upgrades upon leveling up or clearing waves—including Overcharged Core, Quick Cycle, Plasma Split, Orbital Drones, Void Nova, Critical Systems, Phase Shield, Repair Nanites, and Singularity Drain.
3 Unlockable Starfighters:
STRIKER-X: Balanced vanguard interceptor.
PHANTOM-V: High-mobility, high-crit recon skirmisher.
BASTION-09: Heavy armored dreadnought with innate damage resistance.
Permanent Meta-Progression: Spend collected Scrap in the Hangar to permanently upgrade Hull Plating, Shield Capacitors, Sublight Injectors, Weapon Calibration, and Salvage Scanners.
🔊 Procedural Web Audio Synthesizer
Real-time synthesized sound effects for every weapon archetype, shield impact, hull hit, explosion, pickup chime, boost whoosh, and boss warning siren.
Generative ambient sci-fi synth soundtrack with sub-bass drones and cosmic arpeggios.
Independent Master, SFX, and Music volume sliders plus quick mute toggle.
🎮 Full Desktop & Mobile Customization
Interactive Keybind Remapping: Rebind every keyboard action (Move Up/Down/Left/Right, Primary Fire, Boost, Cycle Weapon, Void Burst Ultimate, Pause) directly in Settings.
Mobile Touch Controls: Dual-thumb virtual joystick with adjustable Sensitivity (50%–250%), Deadzone (2%–25%), Stick Size (Small/Medium/Large), and an Auto-Aim Assist toggle.
High-Performance / Anti-Lag Mode: Disables expensive canvas Gaussian shadow blurs for locked 60+ FPS performance on mobile devices and low-power laptops.
🛠️ Tech Stack
Runtime & UI: React 19, TypeScript, Tailwind CSS 4, Lucide Icons
Game Rendering: HTML5 Canvas 2D API (custom vector rendering & particle engine)
Audio Engine: Web Audio API (procedural oscillators, noise buffers, biquad filters)
Persistence: Versioned localStorage save schema (voidrunner_save_v1, voidrunner_settings_v1)
Build Tool: Vite
🚀 Getting Started
Prerequisites
Node.js (v18 or newer recommended)
npm (or pnpm / yarn)
Installation
Clone the repository and navigate into the project directory:
code
Bash
git clone <your-repo-url>
cd voidrunner
Install dependencies:
code
Bash
npm install
Start the development server:
code
Bash
npm run dev
Open your browser to http://localhost:3000.
Building for Production
To compile and bundle the application into static files for deployment:
code
Bash
npm run build
The optimized static bundle will be output to the dist/ directory. You can preview the production build locally with:
code
Bash
npm run preview
🎮 Controls Reference
Desktop (Default — Customizable in Settings)
Action	Default Binding
Move Ship	W, A, S, D or Arrow Keys
Aim	Mouse Cursor
Primary Fire	Spacebar or Left Mouse Button
Thruster Dash / Boost	Shift
Void Burst (Ultimate)	F
Cycle Weapon	Q
Select Weapon Directly	1, 2, 3, 4
Tactical Pause	Escape
Quick Restart (Post-Run)	R
Mobile / Touchscreen
Left Virtual Joystick: Drag to move in 360 degrees.
FIRE Button: Hold to fire active weapon continuously.
BOOST Button: Tap to trigger directional thruster dash.
BURST Button: Tap when glowing (100% charge) to unleash Void Burst.
SWAP GUN Button: Cycle through the 4 weapons.
AIM: AUTO / MANUAL Pill: Toggle automatic targeting of the nearest hostile.
📂 Project Structure
code
Text
├── index.html                    # Entry HTML with fonts & viewport configuration
├── package.json                  # Project scripts & dependencies
├── vite.config.ts                # Vite bundler configuration
└── src/
    ├── main.tsx                  # React DOM root entry
    ├── App.tsx                   # Application state machine & modal orchestrator
    ├── index.css                 # Tailwind CSS & sci-fi theme utilities
    ├── types/
    │   └── game.ts               # Core TypeScript interfaces & data models
    ├── config/
    │   ├── constants.ts          # Palette, world bounds, object caps & default settings
    │   ├── ships.ts              # Ship hulls (Striker-X, Phantom-V, Bastion-09)
    │   ├── weapons.ts            # Weapon stats, spread, velocity & pierce values
    │   ├── upgrades.ts           # 14 rogue draft upgrades & stack limits
    │   ├── enemies.ts            # Enemy archetype stats & drop rates
    │   ├── bosses.ts             # Multi-phase boss configurations
    │   └── metaUpgrades.ts       # Permanent Hangar upgrades
    ├── audio/
    │   └── soundEngine.ts        # Procedural Web Audio API SFX & synth music
    ├── utils/
    │   ├── math.ts               # Vector math, collision checks & interpolation
    │   └── storage.ts            # Versioned LocalStorage load/save/reset handlers
    ├── game/
    │   ├── GameEngine.ts         # Main loop, physics, camera, Ultimate & combo logic
    │   ├── Starfield.ts          # Parallax star layers & cosmic nebulae
    │   ├── Renderer.ts           # Canvas 2D vector drawing for ships, bosses & FX
    │   ├── CombatManager.ts      # Projectiles, pickups, particles & floating text
    │   ├── EncounterDirector.ts  # Wave pacing, enemy AI behaviors & boss patterns
    │   └── InputHandler.ts       # Keyboard, mouse & mobile touch input manager
    └── components/
        ├── HUD.tsx               # Tactical HUD, boss bar, radar & weapon hotbar
        ├── TouchControls.tsx     # Mobile virtual joystick & touch action buttons
        ├── MainMenu.tsx          # Animated title screen
        ├── HangarModal.tsx       # Ship selection & permanent Scrap upgrades
        ├── UpgradeDraftModal.tsx # 3-card rogue upgrade selection modal
        ├── PauseModal.tsx        # Pause menu with mission abandon confirmation
        ├── RunSummaryModal.tsx   # Victory / Defeat telemetry breakdown
        ├── ArchivesModal.tsx     # Lifetime career stats, boss codex & data reset
        └── SettingsModal.tsx     # Keybind remapper, mobile sensitivity & audio controls
⚙️ Balancing & Customization
All game balance parameters are modularized inside src/config/:
Tweak Ship Speeds or Health: Edit src/config/ships.ts.
Adjust Weapon Fire Rates or Damage: Edit src/config/weapons.ts.
Modify Enemy Health or Drops: Edit src/config/enemies.ts.
Change Boss Phases: Edit src/config/bosses.ts.
Add or Tune Rogue Perks: Edit src/config/upgrades.ts.
🌐 Deployment
Because VOIDRUNNER is a pure client-side web application with no external server dependencies, you can deploy the dist/ folder directly to any static hosting provider:
Vercel / Netlify / Cloudflare Pages: Set build command to npm run build and publish directory to dist.
GitHub Pages / itch.io: Run npm run build and upload the contents of dist/.
📄 License
SPDX-License-Identifier: Apache-2.0
