# ichatsdk-evolution

## Overview

An [Architectural Decision (AD)](https://en.wikipedia.org/wiki/Architectural_decision) is a software design choice that addresses a functional or non-functional requirement that is architecturally significant. 
This might, for instance, be a technology choice (e.g., Java vs. JavaScript), a choice of the IDE (e.g., IntelliJ vs. Eclipse IDE), a choice between a library (e.g., [SLF4J](https://www.slf4j.org/) vs [java.util.logging](https://docs.oracle.com/javase/8/docs/api/java/util/logging/package-summary.html)), or a decision on features (e.g., infinite undo vs. limited undo).
Do not take the term "architecture" too seriously or interpret it too strongly.
As the examples illustrate, any decisions that might have an impact on the architecture somehow are architectural decisions.

It should be as easy as possible to
a) write down the decisions and
b) to version the decisions.

This repository records architectural decisions.
It provides files to document Architectural Decisions using **M**arkdown and **A**rchitectural **D**ecision **R**ecords.

The decisions are placed in the folder `docs/adr` to
1) Enable [GitHub pages](https://pages.github.com/) to render it using the web.
   See <https://help.github.com/articles/configuring-a-publishing-source-for-github-pages/> for more information.
2) Separate the architectural decisions from other documentation.

The filenames are following the pattern `NNNN-title-with-dashes.md` ([ADR-0005](docs/adr/0005-use-dashes-in-filenames.md)), where

- `NNNN` is a consecutive number and we assume that there won't be more than 9,999 ADRs in one repository.
- the title is stored using dashes and lowercase, because [adr-tools] also does that.
- the suffix is `.md`, because it is a [Markdown](https://github.github.com/gfm/) file.

### Create a new ADR

Manual approach:

1. Copy `template.md` to `NNNN-title-with-dashes.md`, where `NNNN` indicates the next number in sequence.
2. Edit `NNNN-title-with-dashes.md`.
3. Update `index.md`, e.g., by executing `adr-log -d .`
   You can get [adr-log](https://github.com/adr/adr-log) by executing `npm install -g adr-log`.

Note you can also use [other patterns for the directory format](https://github.com/joelparkerhenderson/architecture_decision_record#adr-file-name-conventions), but then the tools cannot be applied.
