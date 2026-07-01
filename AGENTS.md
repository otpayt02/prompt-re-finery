# AGENTS.md

## Repo purpose

This repository stores reusable prompt engineering systems: prompt families, modes, refinement loops, context patterns, workflow templates, and operating instructions.

## Organization rules

- Use `prompt_library/` as the canonical folder.
- Do not add a duplicate `prompt-library/` folder.
- If files arrive inside `prompt-library/`, migrate them into `prompt_library/` by category, then delete the duplicate source folder.
- Keep prompt templates as Markdown files.
- Use YAML frontmatter for templates and modes when possible.
- Keep built-in modes immutable and copyable.
- Save custom copied modes under `prompt_library/modes/custom/`.

## Naming rules

- Family default templates: `template_v1.md`, `template_v2.md`.
- Special workflow templates: `{clear_slug}_v1.md`.
- Mode templates: `prompt_library/modes/{mode_id}/template_v1.md`.
- Documentation: `docs/{clear_topic}.md`.

## Definition of done

A repo organization change is done when:

1. Files are in the correct canonical folder.
2. Duplicate folders are removed or documented as staging only.
3. README and registry are updated.
4. New modes/templates include frontmatter.
5. No unrelated files are changed.
