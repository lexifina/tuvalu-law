# How this repository was made (Tuvalu)

This file is written by the build on 2026-10-28, the day the source data was retrieved. Everything below is enough to rebuild this repository hash for hash.

## Sources

| Source | Address | Retrieved | Requests | Licence |
| --- | --- | --- | ---: | --- |
| Tuvalu Legislation Online | <https://tuvalu-legislation.tv/cms/> | 2026-10-28 | 8 | see the site copyright page |

Every response is cached by the sha256 of its URL, and the table above lists every source with its retrieval date. Lexifina keeps its fetch scripts privately; `tools/parse.py` reads only the cache and writes `corpus.json`, so the same cache always gives the same corpus.

## What is in it

| Act | Title | Versions | Span |
| --- | --- | ---: | --- |
| `constitution` | The Constitution of Tuvalu | 2 | 2007-08-03 to 2023-10-01 |

The build made 2 commits:

| Commits | Kind |
| ---: | --- |
| 1 | first version of an act |
| 1 | one law on its in-force day |
| 0 | changes no amendment note explains, credited to the publisher |

Other counts:
- 0 commits on the branch `future`: laws not yet in force on 2026-10-28.
- 0 commits dated 1 January 1970: in force before 1970, with the real day in their `In-force` trailer.
- 7 laws in the record.
- 3 tags.

## Dates

Each commit is dated at noon (Pacific/Funafuti) on the day the change took effect. The other dates, enacted and published, are trailers.

When a law gives no date of its own, the default rule applies: Dates are the commencement dates printed by the publisher (endnotes and "Commencement [...]" lines). https://tuvalu-legislation.tv/cms/

## Commands, in order

```sh
# fill the cache from the sources listed above (network; Lexifina's fetch scripts are kept privately)
python -X utf8 tools/parse.py                  # cache -> corpus.json (no network)
python -X utf8 tools/build.py <folder> --repo <empty folder> --docs-date 2026-10-28
python -X utf8 tools/check_repo.py <repo> --corpus <folder>/corpus.json --write
python -X utf8 tools/build.py <folder> --repo <another empty folder> --docs-date 2026-10-28 --compare <repo>
```

In the main Lexifina repository these files live as follows:
- `fetch.py`, `parse.py` and `repo/`: in `scripts/tuvalu-law/`.
- `build.py`, `check_repo.py` (`check.py` there) and `on.py`: in `scripts/gitlaw_common/`, with the corpus format in `SCHEMA.md`.

## Exact inputs

- `corpus.json` sha256 `0636fc7214a79057c6311478a05baae85404b48f4f74164faf26a60fac90f7e7` (506388 bytes)
- Script blob hashes (`git hash-object`):

| Script | Blob |
| --- | --- |
| build.py | `42aa8d2a7c12fbca91f57c90d6554960ccca0795` |
| check.py | `cd346c7ff9996d450240e3bab52bcae03b2bc865` |
| on.py | `644a6c0857fbcc72562032b58d57aa113fee0641` |
| fetch.py | `09f22378eacc85525dc9b196ea75597e7c01c871` |
| parse.py | `fe94b569da0a4a4720fbdfada0df59569d699578` |

- Tools:
  - Python 3.14.0
  - git version 2.52.0.windows.1
  - curl 8.21.0 (Windows) libcurl/8.21.0 Schannel zlib/1.3.2 WinIDN WinLDAP

## Checks

2 versions of 1 acts read back from git on the day each took effect and on the day before: 0 mismatches. Trailers: 0 commits whose trailers git cannot parse. Health: 0 merge commits on main, 0 commit dates that go backwards, 0 commits dated after the build.

Not yet run for this build.

These results are from the check run on the build before this one, from the same corpus.

## Decisions made by hand

- Constitution version 1 is the 2008 Revised Edition PDF (version 1 on the site); its endnote 1 lists amendments up to Act 4 of 2007 (commences 3 August 2007), so it is dated 2007-08-03 as the oldest version available. The site dates this file 1986-10-01, the original commencement, which is not the date of this text.
- Constitution version 2 is the Constitution of Tuvalu Act 2023 (Act 7 of 2023), commencement 1 October 2023 per its own endnote and Commencement line; every changed unit is credited to it. The site lists it as versions 2 and 3 dated 2022-12-30; both files parse to identical units, so the current file (version 3) is used.
- Part and Division headings are their own units (part-NN, part-NN-div-MM); footnote reference numerals are dropped from the text.

## What AI did and did not do

The fetch, parse and check scripts were written by Claude Code running Claude Opus 5.5 (`claude-opus-5-5`) under Lexifina's direction.

No model wrote, translated or corrected legal text. No model runs at build time. Every word of law in this repository comes from the official sources above, through code that anyone can rerun.

The commit messages are written by `build.py` from the source data.

Model use at data-build time:
- none: text is extracted from the PDFs text layer by layout.py rules; no model wrote or edited legal text.
