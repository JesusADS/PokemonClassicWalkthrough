# Repository instructions

## Project scope

This repository contains a bilingual, chronological walkthrough for **Pokémon Classic v1.5**. It is a Markdown documentation project, not an application.

- Spanish edition: `es/`
- English edition: `en/`
- Shared images: `images/`
- Root landing page and legal notice: English

Before changing content, read `README.md`, `NOTICE.md`, and the relevant files in both language editions.

## Sources and factual accuracy

The primary source is *Pokémon Classic v1.5 Player Help*. *Pokémon Yellow* is used only when the hack documentation does not specify a Gym Leader team or level.

- Prefer documented Pokémon Classic data over inherited Pokémon Yellow data.
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
- search English files for malformed list markers with `rg -n "^-[^-\\s]" en --glob "*.md"`;
- search for accidental local paths and untranslated Spanish terminology where relevant.

Do not apply unreviewed bulk formatting fixes.

## Git safety

- Preserve unrelated user changes.
- Do not commit or push unless the user explicitly asks.
- Do not rewrite history, force-push, change repository visibility, or perform another destructive Git operation without explicit authorization.
- Keep changes small and reviewable, and use non-interactive Git commands.
