# Corpus repository rules

- Read README.md and corpus.json before changing sources or publication configuration.
- Preserve enacted project files unchanged. Record changes through separate enacted amendment instruments; never invent enactment authority or dates.
- Keep drafts out of corpus.json. Do not add test fixtures as real publications.
- Keep generated files and the engine checkout untracked. Pin the engine workflow checkout to a reviewed commit.
- Validate with the engine publication build before a focused commit. Review staged changes and run git diff --cached --check. Push only when authorised.
- Report source changes, validation, commit and deployment status accurately.
