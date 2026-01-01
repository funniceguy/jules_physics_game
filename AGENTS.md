# AGENTS.md for Antigravity Client

## 🧠 Context Knowledge
Before planning or coding, ingest the context from the `docs/` directory in this order:
1. `docs/01_Requirements/PRD.md`: **[Core]** Product requirements, Target Audience, and Roadmap.
2. `docs/02_Architecture/TechSpec_Antigravity.md`: **[Critical]** Definition of Physics World, Gravity Logic, and Object Interactions.
3. `docs/04_Planning/TaskList.md`: Priority tasks (Sprint Backlog).
4. `docs/06_UI/01_UI_Design_System.md`: UI Assets, HUD layout, and responsive design rules.

## 🕹️ Tech Stack & Environment
- **Language:** TypeScript (Strict Mode is Mandatory).
- **Game Engine:** Phaser 3.80+ (Use `Phaser.Game`).
- **Physics Engine:** Matter.js (via Phaser's generic `matter` physics). **Do NOT use Arcade Physics.**
- **Bundler:** Vite (for fast HMR).
- **Package Manager:** npm or pnpm.

## 🛡️ Coding Standards
- **Type Safety:** Define explicit Interfaces for all Game Objects (e.g., `interface Player extends Phaser.Physics.Matter.Sprite`).
- **Scene Management:** Separate Logic into distinct Scenes (`BootScene`, `PreloadScene`, `MainGameScene`, `UIScene`).
- **Component Pattern:** Use Composition over Inheritance where possible. Logic should be in separate Managers (e.g., `GravityManager.ts`).
- **Comments:** Use JSDoc for all public methods and interfaces.

## 🚫 Constraints
- **No 'any':** Do NOT use the `any` type. Use `unknown` or define a proper type.
- **Performance:** Avoid creating new Vector objects inside the `update()` loop (60fps). Reuse existing objects to prevent Garbage Collection stutter.
- **Physics Authority:** While currently client-side, structure the physics code (Gravity logic) in a pure TypeScript module so it can be moved to a Server later.
- **Assets:** Do not use placeholder assets without defining them in `Constants.ts`.
