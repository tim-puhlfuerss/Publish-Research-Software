# 5. Make the Artifact Citable

## TL;DR

- Cite all relevant software packages as good as possible in your academic work.
- Make your artifact citable by adding citation metadata and archiving your artifact.
- Encourage citation of your software.
- Citable code != open source code

## Why is This Process Important?

- Software is a research product, just like a paper.
- Creating and maintaining research software is academic work, and should allow for academic credit and careers.
- Citing software enables reproducibility of research results and the assessment of the software.

## How to Cite Software?

- Cite all software packages (including your own) in the reference list of your academic work.
- Ideally try to cite:
  - The software itself.
  - The exact version of the software.
  - The software using its unique identifier.
  - The source code.
  - The software's authors.
  - The software's release date.

## Authorship and Contributorship in Software

When determining the authors, please consider the following recommendations:

- There are no universally accepted guidelines for software authorship.
- Different roles than programmers might be considered as authors.
For example, testers, reviewers, technical writers, maintainers, release engineers, software architects, UX designers, etc. may all qualify for authorship.
- Decisions about authorship are project-specific, but must follow good scientific practice.
Refer to the [ICMJE Uniform Requirements](https://www.icmje.org/recommendations/browse/roles-and-responsibilities/defining-the-role-of-authors-and-contributors.html) for papers, and translate the best practice to software, e.g.,
  - There may be no honorary authorship.
  - The contribution to the software must be substantial.
  - Final approval of the outcome may be covered by a CLA.
  - Agreement to be accountable for (at least own) changes may be factored into the decision.
- Contributors should be acknowledged, but are not always software authors, e.g., issue reporters, typo fixers, evangelists promoting the software, and managers/PIs with no substantial contribution to the software itself.
- Consider using automation to keep track of contributors, for example, with the help of the [All Contributors bot](https://allcontributors.org/).

## How to Make Your Software Citable?

- Provide citation metadata.
- Archive the software and obtain a persistent identifier (PID), e.g., a Document Object Identifier (DOI) via Zenodo.
- Provide a prominent citation hint as part of your documentation.

### Provide Citation Metadata

- You can directly manage citation metadata as part of your source code repository by providing one of the following options:
  - A [CITATION.cff](https://citation-file-format.github.io) file (human/machine-readable citation metadata).
  Use the [cffinit](https://citation-file-format.github.io/cff-initializer-javascript/#/) tool to create or update this file.
  - A [codemeta.json](https://codemeta.github.io) file (machine-readable information about your software including citation metadata).
  Use the [CodeMeta Generator](https://codemeta.github.io/codemeta-generator/) to create this file.
- Another option is to let digital object repositories such as [Zenodo](https://zenodo.org) manage your citation metadata.
Zenodo can also manage multiple software versions and provides one DOI per version.
- You can also combine the approaches.

### Archive the Software

- Archiving software in a publication repository is crucial to ensure long-term availability.
- Such a publication repository allows you to deposit your software and to obtain a PID (e.g., a DOI).
- The PID is a persistent reference to the software in a research publication.
In comparison, usual source code repository URLs break easily or the software may become unavailable at all.
- Example publication repositories:
  - Zenodo
  - [Figshare](https://figshare.com)
  - [Software Heritage](https://www.softwareheritage.org/) (Does not directly support citation metadata; you must add it explicitly to the repository.)

## Software Journals

- If your organization only "awards" peer-reviewed publications, software journals might be an option.
- See the [overview of software journals](https://www.software.ac.uk/which-journals-should-i-publish-my-software) by the _Software Sustainable Institute_.
- Recommendation: [Journal of Open Source Software (JOSS)](https://joss.theoj.org/)
  - Focus on research software tools
  - Developer-friendly
  - Ensures that the software itself is citable

## Further Reads

- Extensive guideline about [research software citations](https://cite.research-software.org)
- [Guidelines for archiving and referencing software artifacts](https://www.softwareheritage.org/save-and-reference-research-software/) by Software Heritage
