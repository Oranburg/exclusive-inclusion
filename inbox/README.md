# Inbox

This directory is the **raw content drop zone** for the *Exclusive Inclusion* project.

## Purpose

Drop any of the following here for processing and incorporation into the site:

- **Raw images** (`.png`, `.jpg`, `.jpeg`, `.gif`, `.svg`, `.webp`)
- **HTML snippets** (`.html`)
- **Markdown drafts** (`.md`)
- **Plain text** (`.txt`)
- **PDF exports** (`.pdf`)
- **Word documents** (`.docx`)
- **Data files** (`.json`, `.csv`)

## Workflow

1. **Add** raw files to this `inbox/` directory
2. **Process** them (edit, convert, optimize) into the appropriate location:
   - Finished text → `paper/`
   - Blog posts → `blog/`
   - Activities → `activities/`
   - Teaching materials → `learning/`
   - Images/assets → `assets/`
3. **Move** processed files out of `inbox/` (or mark them with a `processed_` prefix)

## Notes

- Files in this directory are **not** linked from the public site by default
- Large binary files (PDFs, images &gt; 1 MB) should be added to `.gitignore` or tracked via Git LFS
- When in doubt, drop it here and process later
