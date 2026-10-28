# Tuvalu: law history

**Paused, not yet law (on hold for permission).** Checked 2026-10-28. The official Tuvalu Legislation site (tuvalu-legislation.tv) has what a build needs: the 2008 and 2022 Revised Editions of every act and regulation as text PDFs with dates, and, in the 2022 edition, endnotes naming the amending act of each provision and its commencement. But its copyright notice says a user "may not transmit, distribute or commercialise the material without the permission of the Government of Tuvalu", and Tuvalu's Copyright Act (Cap. 40.24) has no exception for official texts. It will be built once the Government of Tuvalu gives permission.

This repository will hold the legislation of Tuvalu (TV) as a history: one file per provision and one commit per law taking effect, dated by the day it took force, with the law that made each change as the commit author. It follows the shared design of [lexifina/global-law](https://github.com/lexifina/global-law), which places it at `tv/` in the world tree.

**Status:** no law yet. This first commit records where the law of Tuvalu can be read and what a build would need.

**Can it be built?** Past versions by date are online, but with no API or bulk download, so a build has to read the site page by page.

**This commit is a placeholder.** The first real build must replace this history from scratch and force-push. It must never append law commits on top of it: they are dated by when each law took effect, often decades earlier, so dates in `main` would run backwards and break every on-date lookup. Builders should refuse to append when the root commit is this placeholder (its subject ends "sources, before any law").

**Official sources**

- [Tuvalu Legislation](https://www.tuvalu-legislation.tv)

All sources, with their status, are in [SOURCES.md](SOURCES.md). How these files were made is in [REPRODUCE.md](REPRODUCE.md).

This repository describes sources; it is not legal advice and holds no legal text yet.
