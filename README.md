# 237 — 3D First-Person Maze Game

An immersive 3D first-person maze adventure game built with Next.js and React Three Fiber. Navigate a hedge maze in 3D with real physics, first-person controls, and an AI chaser.

## What It Does

- Renders a full 3D hedge maze (21×15 grid) in the browser using Three.js via React Three Fiber
- First-person player movement with pointer-lock mouse look and keyboard controls (WASD / arrow keys)
- Real-time physics powered by `@react-three/cannon` (player collision, ground plane, hedge walls)
- An AI enemy that chases the player through the maze
- GSAP-driven animations and realistic moss-textured hedge materials with PBR maps (color, normal, roughness, AO)
- Dynamic environment lighting and atmospheric effects
- Theme support (light/dark) via `next-themes` and a full Radix UI component set

## Features

- First-person maze navigation with pointer-lock controls
- Physics-based movement and collision detection
- AI chaser enemy with configurable speed and chase distance
- PBR moss textures on hedge walls with realistic lighting
- Responsive HUD built with Radix UI + Tailwind CSS
- Dark/light theme toggle
- Deployed on Vercel

## Tech Stack

- **Framework:** Next.js 15 (App Router), React 19, TypeScript
- **3D:** Three.js, `@react-three/fiber`, `@react-three/drei`, `@react-three/cannon` (physics)
- **Animation:** GSAP
- **UI:** Tailwind CSS, shadcn-style Radix UI primitives, lucide-react
- **Forms/Charts:** react-hook-form + zod, recharts
- **Analytics:** @vercel/analytics

## Quick Start

```bash
# install dependencies
pnpm install
# or: npm install

# run the dev server
pnpm dev
# open http://localhost:3000

# build for production
pnpm build

# start the production server
pnpm start
```

Controls: click to lock the pointer, move with **W A S D** / arrow keys, look with the mouse.

## Project Structure

```
237/
├── app/
│   ├── components/
│   │   └── 237.tsx        # game component: maze, player, AI chaser, physics
│   ├── layout.tsx         # root layout + theme provider
│   ├── page.tsx           # home page (renders the game)
│   └── globals.css        # global styles
├── components/
│   └── theme-provider.tsx # next-themes provider
├── lib/
│   └── utils.ts           # shared utilities (cn helper)
├── public/                # placeholder images / assets
├── styles/
│   └── globals.css        # additional global styles
├── components.json        # shadcn component config
├── next.config.mjs        # Next.js config
├── tailwind.config.ts     # Tailwind config
└── tsconfig.json
```

## Environment Variables

None required for local development.

## Deployment Notes

- The original v0 project deploys to Vercel (`next build && next start`).
- Static export is not enabled by default (dynamic server features aren't used by the game itself, but the App Router config targets a Node server).

## License

MIT

---

Built by Girish Lade — https://ladestack.in
