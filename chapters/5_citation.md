# 5. Make the Artifact Citable

## TL;DR

- Open source code != citable code.
- Cite all relevant software packages accurately in your academic work.
- Make your artifact citable by adding citation metadata and archiving your artifact.
- Encourage the citation of your software.

## Why is This Process Important?

- Software is a research product, like a paper.
- Creating and maintaining research software is academic work deserving credit.
- Citable software enhances research reproducibility and software assessment.

## How to Cite Software?

- Cite all software packages (including your own) in the reference list of your academic work.
- Ideally, cite:
  - The software using its unique identifier.
  - The exact version of the software.
  - The source code.
  - The software's authors.
  - The software's release date.

## Authorship and Contributorship in Software

When determining authors, consider the following:

- There are no universally accepted guidelines for software authorship.
- Roles beyond programmers might qualify as authors (e.g., UX designers, testers, reviewers, technical writers).
- Decisions about authorship are project-specific but must follow good scientific practice.
Refer to the [ICMJE Uniform Requirements](https://www.icmje.org/recommendations/browse/roles-and-responsibilities/defining-the-role-of-authors-and-contributors.html) for papers, translating best practices to software:
  - Contributions must be substantial.
  There may be no honorary authorship.
  - Final approval of the outcome might be covered by a CLA.
  - An agreement to be accountable for (at least own) changes may be factored into the decision.
- Contributors should be acknowledged, but are not always authors (e.g., issue reporters, typo fixers, evangelists promoting the software).
- Consider using automation to track contributors, e.g., with the [All Contributors bot](https://allcontributors.org/).

## How to Make Your Software Citable?

- Provide citation metadata.
- Archive the software and obtain a persistent identifier (PID), e.g., a Document Object Identifier (DOI) via Zenodo.
- Include a prominent citation hint in your documentation.

### Provide Citation Metadata

- Manage citation metadata directly in your repository by providing:
  - A [CITATION.cff](https://citation-file-format.github.io) file (human/machine-readable citation metadata).
  Use the [cffinit](https://citation-file-format.github.io/cff-initializer-javascript/#/) tool to create or update this file.
  - A [codemeta.json](https://codemeta.github.io) file (machine-readable information including citation metadata).
  Use the [CodeMeta Generator](https://codemeta.github.io/codemeta-generator/) to create this file.
- Alternatively, use digital object repositories like [Zenodo](https://zenodo.org) to manage your citation metadata.
Zenodo supports multiple software versions and provides one DOI per version.
- Combining both approaches is also an option.

### Archive the Software

- Archiving software in a publication repository ensures long-term availability.
- A publication repository provides a PID (e.g., DOI) for persistent reference in research publications.
Normal repository URLs might break or become unavailable.
- Example publication repositories:
  - Zenodo
  - [Figshare](https://figshare.com)
  - [Software Heritage](https://www.softwareheritage.org/) (Does not directly support citation metadata; you must add it explicitly to the repository.)

## Software Journals

- If your organization only values peer-reviewed publications, consider software journals.
- See the [overview of software journals](https://www.software.ac.uk/which-journals-should-i-publish-my-software) by the Software Sustainability Institute.
- Recommended: [Journal of Open Source Software (JOSS)](https://joss.theoj.org/), which focuses on research software tools, is developer-friendly, and ensures software is citable.

## Further Reading

- Extensive guidelines on [research software citations](https://cite.research-software.org)
- [Guidelines for archiving and referencing software artifacts](https://www.softwareheritage.org/save-and-reference-research-software/) by Software Heritage
