# Prompt Library Registry

This registry lists the canonical template families and built-in modes.

## Prompt families

| Family | Folder | Purpose | Default template |
|---|---|---|---|
| analysis | `prompt_library/analysis/` | Break down existing material | `template_v1.md` |
| product_spec | `prompt_library/product_spec/` | Define products, MVPs, architecture | `template_v1.md` |
| research_brief | `prompt_library/research_brief/` | Create research briefs | `template_v1.md` |
| execution_plan | `prompt_library/execution_plan/` | Create step-by-step plans | `template_v1.md` |
| writing_content | `prompt_library/writing_content/` | Draft, rewrite, edit, tone-shift | `template_v1.md` |
| outreach_persuasion | `prompt_library/outreach_persuasion/` | Messages, pitches, proposals | `template_v1.md` |
| debugging_troubleshooting | `prompt_library/debugging_troubleshooting/` | Diagnose and fix issues | `template_v1.md` |
| critique_loop | `prompt_library/critique_loop/` | Review and improve work | `template_v1.md` |
| circumstantial | `prompt_library/circumstantial/` | Situation-specific prompts | `template_v1.md` |

## Built-in modes

| Mode | Folder | Mutable | Copyable | Purpose |
|---|---|---:|---:|---|
| one_night_ai_stack_builder | `prompt_library/modes/one_night_ai_stack_builder/` | no | yes | Build scoped one-night MVPs |
| minimal_token_efficiency | `prompt_library/modes/minimal_token_efficiency/` | no | yes | Reduce tokens and rate-limit pressure |

## Import policy

When importing files from another prompt repo:

1. Identify whether the file is a prompt template, mode, workflow, doc, or config.
2. Move prompt templates into the closest family folder.
3. Move modes into `prompt_library/modes/`.
4. Move repo-level docs into `docs/` if they are not reusable templates.
5. Leave repo configuration files at the repo root.
6. Remove any duplicate `prompt-library/` staging folder after migration.
