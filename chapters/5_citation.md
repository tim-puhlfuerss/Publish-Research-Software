# 5. Make the Artifact Citable

## TL;DR

- Cite all relevant software packages as good as possible in your academic work.
- Make your artifact citable by adding citation metadata and archiving your artifact.
- Encourage citation of your software.
- Citable code != open source

## Why is This Process Important?

- Software is a research product, just like a paper.
- Creating and maintaining research software is academic work, and should allow for academic credit and careers.
- Citing software is an important part of the provenance of research results and enables reproducibility.

## How to Cite Software?

- Cite all software packages (including your own) in the reference list of your academic work.
- Ideally try to:
  - Cite the software itself.
  - Cite the exact version of the software.
  - Cite the software using its unique identifier.
  - Cite the source code.
  - Cite the authors of the software.
  - Cite the release date of the software.

## Authorship and Contributorship in Software

When determining the authors, please consider the following recommendations:

- There are no universally accepted guidelines for software authorship.
- Different roles than programmers might be considered as the authors of a software.
For example, testers, reviewers, technical writers, maintainers, release engineers, software architects, UX designers, etc., may all qualify for authorship.
- Decisions about authorship are project-specific, but must follow good scientific practice.
Refer to the [ICMJE Uniform Requirements](https://www.icmje.org/recommendations/browse/roles-and-responsibilities/defining-the-role-of-authors-and-contributors.html) for papers, and translate the best practice to software, e.g.,
  - There may be no honorary authorship.
  - The contribution to the software must be substantial.
  - Final approval of the outcome may be covered by a CLA.
  - Agreement to be accountable for - at least the own - changes may be factored into the decision.
- Contributors should be acknowledged, but are not software authors.
Typical examples include issue reporters, typo fixers, evangelists promoting the software, and managers/PIs with no substantial contribution to the software itself.
Consider using automation to keep track of contributors, for example, with the help of the [All Contributors bot](https://allcontributors.org/).

## How to Make Your Software Citable?

- Provide citation metadata.
- Archive your software and obtain a persistent identifier (PID), e.g., a Document Object Identifier (DOI) via Zenodo.
- Provide a prominent citation hint as part of your documentation.

### Managing Citation Metadata

- You can directly manage citation metadata as part of your source code repository by providing one of the following options:
  - A [CITATION.cff](https://citation-file-format.github.io) file (human/machine-readable citation metadata).
  Use the [cffinit](https://citation-file-format.github.io/cff-initializer-javascript/#/) tool to create or update this file.
  - A [codemeta.json](https://codemeta.github.io) file (machine-readable information about your software including citation metadata).
  Use the [CodeMeta Generator](https://codemeta.github.io/codemeta-generator/) to create this file.
- Another option is to let digital object repositories such as [Zenodo](https://zenodo.org) manage your citation metadata.

### Archiving Software

- Archiving your software in a publication repository is crucial to ensure long-term availability.
- Such a publication repository allows you to deposit your software and to obtain a PID (e.g., a DOI).
- You can use the obtained PID to persistently reference your software in a research publication.
- Examples:
  - Zenodo
  - [Figshare](https://figshare.com)
  - [Software Heritage](https://www.softwareheritage.org/) (Does not directly support citation metadata; you must add it explicitly to the repository.)

## Software Journals

- If your organization only "awards" peer-reviewed publications, software journals might be an option.
- [Overview](https://www.software.ac.uk/which-journals-should-i-publish-my-software) of software journals by the _Software Sustainable Institute_
- Recommendation: [Journal of Open Source Software (JOSS)](https://joss.theoj.org/)
  - Focused on research software tools
  - Developer-friendly
  - Ensures that your software itself is citable
Overview of Software Journals

## Further Reads

- Extensive guideline [Research Software Citation](https://cite.research-software.org)
- [Guidelines for archiving and referencing software artifacts](https://www.softwareheritage.org/save-and-reference-research-software/) by Software Heritage
