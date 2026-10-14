# PERIGON

A retro arcade anti-aircraft shooter in the spirit of Atari / Intellivision. One cannon, 180 degrees of aim, and everything falling out of the sky wants your base dead.

Everything lives in a single self-contained `index.html` (embedded font, logo and sprites, no dependencies). Open it in a browser or load it on your phone and it just runs.

## Gameplay

- Your cannon sweeps **0 to 180 degrees**. Helicopters drop **parachute troopers**, bombers drop **physics-driven bombs**, and gunship-style **shooters** strafe your base.
- **Every bullet costs 10 points.** Kills pay, so spray-and-pray loses.
- Parachutes and troopers have **separate hitboxes**: popping the chute pays double.
- **Care drones** and **perk drones** carry power-ups. Don't shoot them (shooting one costs you points). Power-ups: Boost, Coins, Shockwave, Flower, Shunt (lock-on), Mines, Regen, Absorb, Reinforce.
- **Boss every 10 waves**: a V-22 Osprey-style tiltrotor. Bullets are absorbed by the hull and do no damage. Shoot down shooters so their wrecks fall onto the boss: fuselage hits deal 1/3 of its HP, engine hits 1/4.
- Optional ground turret.

## Controls

| Input | Action |
|---|---|
| Bottom slider + FIRE | Aim and shoot (mobile default) |
| Drag anywhere / tap | Aim / fire (touch-anywhere mode) |
| Mouse | Aim at cursor, click to fire |
| Arrow keys + Space | Aim and fire |
| Gamepad | Left stick aims, A fires, RT turbo, B ground turret, Start pauses |

## Display

Chunky 8-bit look from a low-resolution pixel buffer with nearest-neighbor upscaling. Three aspect-ratio presets (9:16, 1:1, 16:9), letterboxed. Wider windows reveal more world rather than stretching sprites.

## Run it

Open `index.html` directly, or serve the folder:

```
python3 -m http.server 8000
```

## Known issues / open questions

- **Shield Surge** (the boss's blue flash) no longer blocks anything now that bullets do zero chip damage. Decide: keep as a pure visual tell, give it a new job, or cut it.
- The name means a full 360-degree angle, but the cannon only sweeps 180. Intentional irony, or a rename? (Alternatives floated: PERIGRINE, PERIGEE.)
- Ideas not yet built: an Intellivision-flavored port.
