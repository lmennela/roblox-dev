# Changelog

All notable changes to this project will be documented in this file.
Format based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/);
versions follow [SemVer](https://semver.org/).

## [0.2.0] - 2026-11-01

Fork upgrade, verified against the Roblox creator docs (snapshot 2026-10-29),
release notes 690–745 and Studio 0.745. Code samples passed static analysis; they
have not been run inside Studio.

### Added

- Skills: `roblox-input`, `roblox-server-authority`, `roblox-studio-workflow`.
- `references/` files with limits, profiling tools, streaming, new solver types,
  platform gates, automation and more, loaded only when needed.
- A sources list and a last-verified date in every knowledge skill.
- Maturity labels (GA, Beta, Pending) for every recent feature.
- Reviewer lenses for platform currency and UI/input.

### Changed

- All seven original knowledge skills, `setup`, `new-system`, `review` and the
  reviewer rewritten or updated after checking each claim at the source.
- Toolchain pins: Rojo 7.7.1, Selene 0.32.0, StyLua 2.6.0, setup-rokit v0.2.1;
  luau-lsp 1.70.1 added to the CI template.
- `Validators.luau` uses `math.isfinite`.

### Fixed

- DataStore limit "one write per key per ~6 s" → 4 MB write and 25 MB read per
  key per minute.
- ProfileStore's Wally name → `lm-loleris/profilestore`.
- TestEZ no longer recommended for new suites (repository archived).
- Colon methods as the typed OOP idiom, `x :: any :: T`, `TextScaled` guidance,
  `IgnoreGuiInset` guidance and unsourced VFX claims.

## [0.1.0] - 2026-09-10

### Added

- Seven auto-activating skills: `roblox-security`, `roblox-datastores`,
  `roblox-performance`, `luau-strict-typing`, `roblox-architecture`,
  `roblox-ui`, `roblox-testing`.
- Three commands: `/roblox-dev:setup`, `/roblox-dev:new-system`,
  `/roblox-dev:review`.
- `roblox-reviewer` read-only audit agent.
- `SafeRemote` example module with TestEZ spec.
- Structural validation script and CI (plugin structure + Selene + StyLua on
  examples).
- Bilingual documentation (English/Spanish).
