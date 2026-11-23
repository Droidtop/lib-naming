# mytop-naming

Shared code for droidtop, Pythia, Enginehost and droidtop-agent: titles, parts and versions from folder and file names, `compareLoose`, and version detection from a game's files (Ren'Py `config.version`, `package.json`).

One of the shared libraries of mytop-project/tracker#867, in the split the owner approved on 2026-11-21
(mytop-project/tracker#960, step 1.0). Where its code comes from: new; seeded from droidtop's GameNaming and GameTitleParser, the agent's folder rules and Pythia's onboarding and reconciliation rules.

**Shared code with versions, not releases** (owner, 2026-11-21: "these libraries aren't standalone… They're shared
code", then "we still make pinned versions, we just don't make releases. We can build them for testing and stuff, we
wanna be able to use versioning"). Programs pin a version tag (vX.Y.Z). CI here builds and tests the library and
builds the programs that pin it against each change; it publishes no releases or release builds.

- **Platform-neutral:** no Android-only code; an Android adapter, where one is needed, is a separate, marked module.
  The programs also target mobile Linux.
- **Replace in place:** code moves here in the change that deletes the copy it replaces in a program.
- Licence: GPL-3.0 (see `LICENSE`).
