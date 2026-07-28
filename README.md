```
astra-void
· · · · · · · · · · · ·
nothing out here but tools
```

I build developer tooling — compilers, type checkers, and the awkward layer
between a language and whatever it ends up compiling down to. Usually a Rust
core with a TypeScript surface, on the theory that the compiler should be doing
the work instead of the runtime.

### Compilers & type systems

- **[surge-ts](https://github.com/astra-void/surge-ts)** — a high-performance TypeScript type checker written in Rust, targeting `tsc --noEmit` compatibility. Still experimental; the compatibility bar is the whole difficulty.

### Roblox toolchain

Making Roblox development feel like modern web development, end to end.

- **[aruna](https://github.com/astra-void/aruna)** — compiler-first framework for server-authoritative games. Server actions are discovered at compile time, with an inspectable action contract and boundary-aware diagnostics.
- **[loom](https://github.com/astra-void/loom)** — live web DOM preview of Roblox UI, with Roblox-accurate layout from a Rust/WASM engine.
- **[lattice-ui](https://github.com/astra-void/lattice-ui)** — headless-first UI toolkit built with roblox-ts and `@rbxts/react`.
- **[vela-rbxts](https://github.com/astra-void/vela-rbxts)** — Tailwind-style `className` support for roblox-ts React UI.

Docs for most of the above: **[astra-void-docs](https://github.com/astra-void/astra-void-docs)**

### Elsewhere

- **[skills](https://github.com/astra-void/skills)** — Claude Code skills for Conventional Commits and Keep a Changelog.

### Not here

Most of what I build never lands on this profile: web apps in Next.js, editor
and linter plugins, and a standing habit of reimplementing things I use — a
package manager, a shell, an IPC layer — in whatever language makes the problem
interesting that week. Usually the point is finding out how it works, not
shipping it.

### Stack

`TypeScript` · `Rust` · `React` · `Next.js` · `roblox-ts` · `Luau`
<br><sub>plus regular detours through C, C++, C#, Python, and Lua</sub>

<sub>South Korea · most of this is unfinished on purpose — the interesting part is the compile step</sub>
