# Repo Organization Guide

## Canonical rule

Use `prompt_library/`, not `prompt-library/`.

`prompt-library/` is allowed only as a temporary import staging folder. After import, move useful files into `prompt_library/` and remove the staging folder.

## Root folders

| Folder | Purpose |
|---|---|
| `prompt_library/` | Reusable prompt templates and modes |
| `docs/` | Documentation about organization, migration, architecture, and UI plans |
| `workflows/` | Larger multi-step workflow guides |

## File placement decision tree

1. Is it a reusable prompt template?
   - Put it in the closest `prompt_library/{family}/` folder.
2. Is it an operating mode?
   - Put it under `prompt_library/modes/{mode_id}/template_v1.md`.
3. Is it a custom mode?
   - Put it under `prompt_library/modes/custom/{custom_mode_id}/template_v1.md`.
4. Is it a long process or playbook?
   - Put it under `workflows/`.
5. Is it documentation about the repo or app?
   - Put it under `docs/`.
6. Is it repo config?
   - Keep it at root.

## Large migration process

For 1000+ files:

1. Do not move everything blindly.
2. Generate a file inventory grouped by extension and top-level folder.
3. Classify files into prompts, modes, docs, workflows, code, assets, and config.
4. Move files in batches by category.
5. Commit each batch separately.
6. Update `prompt_library/registry.md` after each batch.
7. Delete duplicate source folders only after verifying files moved correctly.
