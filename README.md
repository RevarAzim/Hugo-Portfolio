# Revar Azim Muhammed

Personal site, built with Hugo and no theme. Pages, data files, and the rules for editing them are in [AGENTS.md](AGENTS.md). Open questions are in [OPEN-QUESTIONS.md](OPEN-QUESTIONS.md).

Preview, including drafts:

```bash
hugo server --buildDrafts
```

Check the production build. Output goes to `public/`:

```bash
hugo --minify --panicOnWarning
```

Content pages are drafts until `draft: true` is removed, so that command currently writes a site with no CV pages.
