# Repository instructions

## Project scope

This repository contains a bilingual, chronological walkthrough for **Pokémon Classic v1.5**. It is a Markdown documentation project, not an application.

- Spanish edition: `es/`
- English edition: `en/`
- Shared images: `images/`
- Root landing page and legal notice: English

Before changing content, read `README.md`, `NOTICE.md`, and the relevant files in both language editions.

## Sources and factual accuracy

The primary source is *Pokémon Classic v1.5 Player Help*. For exact Trainer teams, levels, and moves omitted by that document, use the matching Pokémon Classic v1.5 internal trainer data from `DaniRainbow/pokeclassic`, especially `src/data/trainer_parties.h`. Use *Pokémon Yellow* only when neither Classic source provides the data.

- Prefer documented Pokémon Classic data over inherited Pokémon Yellow data.
- Treat Pokémon Classic v1.5 internal trainer data as authoritative over Pokémon Yellow for Trainer rosters, levels, and moves.
- Clearly distinguish confirmed hack data, inherited reference data, and editorial recommendations.
- Do not invent teams, levels, moves, items, encounters, events, or rewards.
- Mark undocumented information as pending in-game verification.
- Do not add a complete Pokédex or full learnsets; keep the project focused on the walkthrough.

## Bilingual maintenance

Content changes must normally be applied to both editions in the same change:

- preserve equivalent sections, tables, images, warnings, and navigation;
- use official or established Spanish terminology in `es/`;
- use official English names for locations, Badges, items, moves, Trainer classes, and game mechanics in `en/`;
- never translate Pokémon species names as ordinary words;
- avoid literal machine translations such as `MO`, `Silph S.A.`, or unofficial location names in the English edition;
- keep language-switch links between equivalent volumes valid.

If a change intentionally affects only one language, state why in the handoff.

## Volume structure

Keep the existing twelve-volume organization and one Gym Leader per volume. Preserve, where applicable:

1. title and coverage summary;
2. previous/index/next navigation and language switch;
3. sections by location;
4. maps and captions;
5. objectives and numbered walkthrough;
6. encounter, item, and Trainer tables;
7. important notices and boss information;
8. departure checklist;
9. final navigation.

## Gym and boss consistency

- Keep the Gym Leader's exact team in the main boss table.
- Keep the Gym Trainer table limited to the other Trainers; do not duplicate the leader there.
- When a leader team or level cap changes, update both language volumes, the combat advice and source note, `es/INDICES-DE-CONSULTA.md`, and `en/REFERENCE-INDEXES.md`.
- Search the repository for the previous team members and cap values so stale references do not survive elsewhere.

## Markdown conventions

- Keep Markdown compatible with GitHub rendering.
- Use simple Markdown tables unless existing HTML is necessary.
- Keep GitHub alerts in their native form: `> [!IMPORTANT]`, `> [!WARNING]`, `> [!TIP]`, and `> [!NOTE]`.
- Every unordered-list marker must be followed by a space: use `- Hiker`, never `-Hiker`.
- Preserve relative links and do not introduce `C:\`, `/mnt/data/`, or `file://` paths.

## Images

Images are shared by both editions and come from the original documentation.

- Do not delete, regenerate, rename, or replace maps without checking every reference.
- Do not duplicate images between language folders.
- Volume files normally reference images through `../../images/volumen-NN/media/...`.
- Preserve the number and order of images between equivalent Spanish and English volumes.

## Required validation

Before handing off a change:

- run `git diff --check`;
- inspect `git status --short` and the relevant diff;
- verify local Markdown links and image paths in `README.md`, `NOTICE.md`, `es/`, and `en/`;
- check previous/index/next and language-switch navigation;
- compare image and table counts between equivalent volumes when structure changes;
- when Gym data changes, verify that the leader appears once, the secondary Trainer tables remain bilingual, and both reference indexes use the same cap;
- search English files for malformed list markers with `rg -n "^-[^-\\s]" en --glob "*.md"`;
- search for accidental local paths and untranslated Spanish terminology where relevant.

Do not apply unreviewed bulk formatting fixes.

## Git safety

- Preserve unrelated user changes.
- Do not commit or push unless the user explicitly asks.
- Do not rewrite history, force-push, change repository visibility, or perform another destructive Git operation without explicit authorization.
- Keep changes small and reviewable, and use non-interactive Git commands.
