# prompt-re-finery

Prompt engineering practices, loops, modes, templates, families, refinements, context, and reusable AI workflow systems.

## Canonical structure

This repo uses `prompt_library/` as the source of truth for reusable prompt assets.

Do **not** use a duplicate `prompt-library/` folder. If a `prompt-library/` folder is imported or created temporarily, move its useful contents into `prompt_library/` using the category map below.

```txt
prompt-re-finery/
├── README.md
├── AGENTS.md
├── docs/
│   ├── repo_organization.md
│   ├── mode_customization_plan.md
│   └── migration_notes.md
├── prompt_library/
│   ├── README.md
│   ├── registry.md
│   ├── analysis/
│   ├── product_spec/
│   ├── research_brief/
│   ├── execution_plan/
│   ├── writing_content/
│   ├── outreach_persuasion/
│   ├── debugging_troubleshooting/
│   ├── critique_loop/
│   ├── circumstantial/
│   └── modes/
└── workflows/
    └── one_night_ai_stack.md
```

## Prompt families

- `analysis` — break down existing material
- `product_spec` — define product, MVP, architecture
- `research_brief` — structured research question
- `execution_plan` — step-by-step build or action sequence
- `writing_content` — drafting, editing, tone
- `outreach_persuasion` — pitch, message, proposal
- `debugging_troubleshooting` — isolate and resolve failure
- `critique_loop` — evaluate and improve existing work
- `circumstantial` — situation-specific prompts that do not fit a standard family

## Modes

Modes control how the app or AI assistant behaves while using prompt templates.

Built-in modes live under:

```txt
prompt_library/modes/{mode_id}/template_v1.md
```

Custom copied modes should live under:

```txt
prompt_library/modes/custom/{custom_mode_id}/template_v1.md
```

## Current status

Organized starter structure is ready. Add or migrate prompt files into `prompt_library/` by family.