# Italian language pack agent instructions

## Package contracts

- This repository ships language files and localized assets for DeltranslatePatch; it does not itself patch the game's `data.win`. Do not turn a translation change into a game-binary or patcher migration.
- Preserve `lang/` layout, chapter paths, JSON validity, string keys, placeholders, escape sequences, and runtime control markers. Change prose without accidentally changing executable string contracts.
- Preserve the Italian wording's intended meaning, character voice, and established terminology. Structural checks do not establish translation quality; review changed dialogue in context.
- Treat `lang/settings.json` update URLs/metadata and `lang/changes.json` as updater contracts. Do not alter release destinations or compatibility requirements during ordinary wording edits.
- Keep required localized assets and attribution intact. Do not add unlicensed material or copy original game files into the repository.

## Verification and completion

Use [README.md](README.md) for package layout and the distinction between language updates and manual DeltranslatePatch upgrades. Validate changed JSON and compare affected keys/control markers against the matching source or existing chapter contract. Check archive layout when packaging changes; avoid creating a nested `lang/lang/` payload.

Keep this guidance outside `lang/`, which is released as runtime content. Changes there can trigger automatic archive publication through the existing workflow. Do not run installation against a personal game directory as a test.

Finish with structural and contextual review recorded, release metadata synchronized only when required, and any missing game/runtime verification stated explicitly. Do not claim in-game validation from JSON parsing alone.
