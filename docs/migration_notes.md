# Migration Notes

## Current connector-visible state

At the time this organization branch was created, GitHub showed only the initial root files on `main`:

- `.gitattributes`
- `README.md`

If more than 1000 files were added locally, they need to be committed and pushed before this connector can move or reorganize them.

## Target migration

Move any useful content from a hyphenated `prompt-library/` staging folder into the canonical underscore folder:

```txt
prompt-library/   ->   prompt_library/
```

## Safe migration policy

For a large file set:

1. Inventory first.
2. Classify by file type and content.
3. Move in batches.
4. Keep commit messages specific.
5. Verify after each batch.
6. Remove the source staging folder only after all useful files are moved.

## Suggested local inventory commands

Run these locally from the repo root if files are not pushed yet:

```powershell
git status --short
Get-ChildItem -Recurse -File | Select-Object FullName, Extension, Length | Export-Csv .\file_inventory.csv -NoTypeInformation
Get-ChildItem -Recurse -Directory | Select-Object FullName | Export-Csv .\folder_inventory.csv -NoTypeInformation
```

Then commit and push:

```powershell
git add .
git commit -m "Add imported prompt library files"
git push origin main
```
