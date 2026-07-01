# Mode Templates

Modes define how the assistant or app behaves while using prompt templates.

A prompt family answers: what kind of artifact is being created?

A mode answers: how should the system behave while creating it?

## Built-in mode behavior

Built-in modes should be non-editable but copyable.

```yaml
status: built_in
mutable: false
copyable: true
```

## Custom mode behavior

Custom modes are editable copies of built-in modes or user-created modes.

```yaml
status: custom
mutable: true
copyable: true
parent_mode_id: original_mode_id
```

## UI requirements

The future app should provide:

1. Built-in modes tab.
2. Custom modes tab.
3. Active mode selector.
4. Duplicate to Custom button.
5. Custom mode editor.
6. Version history.
7. Import/export as Markdown with frontmatter.
