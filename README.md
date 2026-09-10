```
astra-void
· · · · · · · · · · · ·
nothing out here but tools
```

I build developer tooling and the web apps that end up needing it — compilers,
type checkers, and the awkward layer between a language and whatever it ends up
compiling down to. Usually a Rust core with a TypeScript surface, on the theory
that the compiler should be doing the work instead of the runtime.

### Compilers & type systems

- **[surge-ts](https://github.com/astra-void/surge-ts)** — a TypeScript type checker written in Rust, aiming for `tsc --noEmit`-compatible diagnostics, with compatibility measured per feature and per project against `tsc` itself. Ships as an embeddable library and a CLI. Still experimental; the parity bar is the whole difficulty.

### Roblox toolchain

A modern web toolchain, rebuilt one layer at a time for [roblox-ts](https://roblox-ts.com).

| Layer | Project | What it does |
| --- | --- | --- |
| framework | **[aruna](https://github.com/astra-void/aruna)** | Compiler-first framework for server-authoritative games. Server actions are discovered at compile time, with an inspectable action contract and boundary-aware diagnostics. |
| behavior | **[lattice-ui](https://github.com/astra-void/lattice-ui)** | Headless UI primitives for `@rbxts/react` that own focus flow, layering, portals, and presence, and leave the styling to you. |
| styling | **[vela-rbxts](https://github.com/astra-void/vela-rbxts)** | Tailwind-style `className` for React and Vide UI, lowered to Roblox props at compile time. Comes with a Rust LSP and a VS Code extension. |
| composition | **[facet](https://github.com/astra-void/facet)** | Copy-in components built on Lattice and Vela. You don't install a `Button`; a `button.tsx` lands in your project and it's yours. |
| assets | **[rbxts-svg](https://github.com/astra-void/rbxts-svg)** | SVG compiled at build time by a Rust compiler into a compact vector IR, drawn at runtime through `EditableImage`. The entire Lucide icon set ships precompiled. |
| preview | **[loom](https://github.com/astra-void/loom)** | Roblox UI rendered as a live web DOM, with Roblox-accurate layout from a Rust/WASM engine. A Vite plugin, so HMR comes free. |

Docs live at **[docs.astra-void.xyz](https://docs.astra-void.xyz)** ([source](https://github.com/astra-void/astra-void-docs)).

### Web

Mostly Next.js App Router on React 19 and Tailwind 4, with Cloudflare Workers and Hono when it belongs at the edge. The source is mostly private, so the links here go to the products.

- **[Project RowCat](https://project-rowcat.com)** — local-first AI character and story chat. Conversations live in the browser, LLM keys never leave it, and sync between devices is end-to-end encrypted so the server only ever holds ciphertext. A Next.js monorepo with an Expo app, an importer extension, payments, and its own [status page](https://status.project-rowcat.com).
- **[astra-void.xyz](https://astra-void.xyz)** — the personal site.
- **[fastify-svg-renderer-template](https://github.com/astra-void/fastify-svg-renderer-template)** — Fastify + Preact SVG renderer, Lambda-first, with a plain Node entry if you'd rather run it as a server.

### Elsewhere

- **[skills](https://github.com/astra-void/skills)** — Claude Code skills for Conventional Commits and Keep a Changelog.

### Not here

A standing habit of reimplementing things I use — a package manager, a shell,
an IPC layer, editor and linter plugins — in whatever language makes the
problem interesting that week. Usually the point is finding out how it works,
not shipping it.

### Stack

`TypeScript` · `Rust` · `React` · `Next.js` · `Expo` · `roblox-ts` · `Luau` · `WebAssembly`
<br><sub>plus regular detours through C, C++, C#, Python, and Lua</sub>

<sub>South Korea · most of this is unfinished on purpose — the interesting part is the compile step</sub>
