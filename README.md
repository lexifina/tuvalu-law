# Tuvalu: law history in git

The law of Tuvalu as a git history, once it can be built: one file per provision, one commit per version on the day it took effect, and the act that made each change as the commit's author. `git blame` will name the act behind every line; `git log` will list every change to a provision; picking a date will give the text in force that day.

Part of [lexifina/global-law](https://github.com/lexifina/global-law), one git history for every country's law: this is Tuvalu's national law, which global-law reads at `tuvalu/national/acts/`.

**What is in it now:** no law text. [`SOURCES.md`](SOURCES.md) records the official source, from Lexifina's register of world law sources (28 October 2026), and [`REPRODUCE.md`](REPRODUCE.md) says how these files were made. There is nothing yet to run git commands on, and global-law, which already lists Tuvalu, has no Tuvaluan text to search.

**Why there is none.** The copyright notice of Tuvalu Legislation Online, the official site, says: "A user may download, store in cache, display, print and copy the material in unaltered form only. A user may not transmit, distribute or commercialise the material without the permission of the Government of Tuvalu." Building is paused until the Government of Tuvalu gives that permission.

**What is planned:** the Constitution and every act and regulation, with the versions the site keeps for each: the Revised Editions of the laws in force at 31 December 2008 and at 31 December 2022, as PDFs with a text layer, and the acts made since. The 2022 edition's endnotes name the act that amended each provision and the day it commenced, so each change can be credited to that act on that day.

The laws are in English, as the site publishes them.

## Sources

| Source | Kind | Past versions | Notes |
| --- | --- | --- | --- |
| [Tuvalu Legislation Online](https://www.tuvalu-legislation.tv) (Government of Tuvalu) | Official legislation site: the Revised Editions of 2008 and 2022 and later acts | yes, a version history per act and regulation | No API or bulk download; copyright is retained by the Government of Tuvalu, and the material may not be redistributed without its permission |

## Licence

See [`LICENSE`](LICENSE). There is no legal text here; it will be added only with the Government of Tuvalu's permission. Lexifina's own contributions (the documentation and the tables) are CC0 1.0.

No AI wrote legal text. The sources register was compiled by Claude Code running Claude Opus 5.5, with research sub-agents on the same model; no AI model runs when these files are built (see [`REPRODUCE.md`](REPRODUCE.md)).

## How it is checked

- [vulnerabilities/](vulnerabilities/): possible drafting mistakes in this law, found by global-law's detectors and checked by hand. Not run yet.

## Visualisations

- [visualisations/](visualisations/): charts drawn from this repository. Not drawn yet.

## More

From [lexifina/global-law](https://github.com/lexifina/global-law):

- [FEATURES.md](https://github.com/lexifina/global-law/blob/main/FEATURES.md): every feature, and what every corpus must support (`git blame`, `law.py`, the MCP tools)
- [FAQ.md](https://github.com/lexifina/global-law/blob/main/FAQ.md): questions and answers · [CONTRIBUTING.md](https://github.com/lexifina/global-law/blob/main/CONTRIBUTING.md): proposing changes · [MCP.md](https://github.com/lexifina/global-law/blob/main/MCP.md): the MCP server · [REPRODUCE.md](https://github.com/lexifina/global-law/blob/main/REPRODUCE.md): how it was built · [CHANGELOG.md](https://github.com/lexifina/global-law/blob/main/CHANGELOG.md)
- [FRESHNESS.md](https://github.com/lexifina/global-law/blob/main/FRESHNESS.md): how current each corpus is · [Monitoring](https://github.com/lexifina/global-law/tree/main/monitoring): whether updates are running · [WATCHING.md](https://github.com/lexifina/global-law/blob/main/WATCHING.md): how each official source is watched for changes
- [performance/](https://github.com/lexifina/global-law/tree/main/performance): how fast the tools are, measured
- [visualisations/](https://github.com/lexifina/global-law/tree/main/visualisations): charts and bridges across the world's law
- [Vulnerabilities](https://github.com/lexifina/global-law/tree/main/vulnerabilities): mistakes in legislation as published
