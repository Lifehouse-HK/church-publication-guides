# Lifehouse Hong Kong Publication Guides

The source and publication history for Lifehouse Hong Kong’s 夢幻團隊翻譯團隊. The editor and rendering engine live in [Style Guide Studio](https://github.com/Lifehouse-HK/style-guide-studio).

This repository starts empty. No specimen is an enacted church document. The static website and API will list Guides after genuine enacted projects are added.

## Editing and publication

1. Use [the editor](https://lifehouse-hk.github.io/style-guide-studio/). Keep downloaded portable project JSON in `documents/drafts/` while drafting. XML is an interchange projection; project JSON is the publication source of truth.
2. After the Translation Team’s actual enactment decision, record enactment in the editor and save the resulting immutable project in `documents/enacted/`.
3. Add that path to `corpus.json` → `documents`. Include the original and every enacted amendment in its timeline. Each amendment project retains its verified principal source snapshot.
4. Commit and push. GitHub Actions validates the timeline and generates HTML, PDFs, historical views and static API snapshots as one Pages deployment. Invalid references or amendment preconditions fail the build.
5. To create a later amendment, enter `https://lifehouse-hk.github.io/church-publication-guides/` in the editor’s Create amendment dialog. The editor resolves current revised text automatically.

Never overwrite an enacted source to apply an amendment. Add a separate enacted amendment project. Dated website expressions are generated; Git tracks the instruments. Drafts are not included in publication configuration, although files committed to this public repository are publicly readable.

## Building

The workflow pins the independent engine to an exact commit. Update that pin deliberately after reviewing and testing a new engine release. It rebuilds daily so whole-instrument effective dates take effect without source edits; GitHub scheduled runs may be delayed. Manually dispatch the workflow when publication timing matters.

With the engine checked out beside this repository and its dependencies installed:

```sh
cd ../style-guide-studio
npm run publish:corpus -- ../church-publication-guides/corpus.json ../church-publication-guides/generated
```

Deploy only `generated/`. No server, paid renderer or paid hosting service is required. The engine is MIT licensed; this repository does not grant an additional licence to church publication content or branding.
