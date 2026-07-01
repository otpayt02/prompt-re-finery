# Prompt Library

`prompt_library/` is the canonical home for all reusable prompt templates, modes, workflow patterns, and prompt engineering assets in this repo.

## Folder map

```txt
prompt_library/
├── README.md
├── registry.md
├── analysis/
├── product_spec/
├── research_brief/
├── execution_plan/
├── writing_content/
├── outreach_persuasion/
├── debugging_troubleshooting/
├── critique_loop/
├── circumstantial/
└── modes/
```

## Placement map

| Asset type | Folder |
|---|---|
| Analysis / breakdown prompts | `analysis/` |
| Product spec / MVP planning prompts | `product_spec/` |
| Research prompts | `research_brief/` |
| Step-by-step execution prompts | `execution_plan/` |
| Writing, rewriting, tone prompts | `writing_content/` |
| Outreach, proposal, persuasion prompts | `outreach_persuasion/` |
| Debugging and troubleshooting prompts | `debugging_troubleshooting/` |
| Critique and review prompts | `critique_loop/` |
| One-off situation prompts | `circumstantial/` |
| Operating modes | `modes/` |

## Template metadata

Prompt templates should use this frontmatter shape when possible:

```yaml
template_id: product_spec_v1
family: product_spec
display_name: Product Spec Template
version: 1
status: active
recommended_mode: default
```

Mode templates should use this frontmatter shape:

```yaml
mode_id: minimal_token_efficiency
display_name: Minimal Token Efficiency
version: 1
status: built_in
mutable: false
copyable: true
default_prompt_family: circumstantial
token_policy: minimal
scope_policy: smallest_next_action
```

## Migration rule

If a `prompt-library/` folder exists, treat it as import staging. Move useful files into this folder by category, then remove the duplicate staging folder.