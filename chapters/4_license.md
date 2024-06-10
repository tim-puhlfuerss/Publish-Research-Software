# 4. Add a License

## Disclaimer

This is not legal advice.
Consult a lawyer or your organization's legal department for legal guidance on licensing.

## TL;DR

- The copyright holder must state a license to grant others rights to (re-)use the software.
- Check the compatibility of licenses from third parties (libraries, data, etc.) from the beginning.
- Prefer using [official, permissive FOSS licenses](https://opensource.org/licenses/alphabetical).
- Minimum: Add a `LICENSE` file and state the copyright holder.
- Recommended: Follow the [REUSE specification](https://reuse.software/specifications/).

## Why is This Process Important?

- An explicitly stated software license is required to (re-)use the artifacts legally.

## Copyright

### What is Copyright?

- Copyright grants the holder exclusive rights to the protected artifact, such as use, copying, distribution, and creating derivative works.
- Others have no rights regarding the artifact unless explicitly granted by the copyright holder.
- Copyright law varies by country.
This guide is based on [German copyright law](https://www.gesetze-im-internet.de/urhg/).
- Some rights (e.g., attribution) cannot be waived or transferred to a third party according to German law.

### What is Protected by Copyright?

- Copyright protects the expression of an idea but not the idea itself.
- In the context of software, it covers source code, object code, software integrated in hardware, documentation, and accompanying material.
- Copyright protection requires a threshold of originality.
If two developers independently create the same source code, the required threshold of originality might be not achieved.

### Who is the Copyright Holder?

- The copyright holder is the person or organization with exclusive rights to the software.
- All contributors are considered as artifact author and, therefore, copyright holders.
- Quality and size of contribution do not matter.
- If developed as part of employment, the employer is usually the copyright holder and entitled to exercise all economic rights with the software ("Verwertungsrechte").
Developers still retain attribution rights.
- For privately developed software, the developer is the sole copyright holder.
This is also the case if the developer has been inspired by work experiences and knowledge.
- All copyright holders jointly exercise the rights granted by copyright.
For example, if one wants to re-license a software, all copyright holders must agree on the license change.

## Software Licenses

- Copyright holders can grant rights through licenses.
- Licenses specify granted rights (e.g., use, copy, distribute) and obligations (e.g., source code disclosure, attribution).
- Every software you use must be covered by a license.
- Users are covered by whatever license you place on your software.

## Software License Types

### Proprietary

- Non-standardized licenses with specific terms
- Examples: Commercial License, Shareware License, Freeware License

### Free and Open Source

- Defined by the Free Software Foundation (FSF) and the Open Source Initiative (OSI).
Both refer to the same set of licenses but favor different values (reusability vs. social movement).
- These licenses imply public availability of source code, and allow open distribution, modification, and reuse.

#### "Copyleft" Licenses

- “The world is evil.”
- Require derivative work to use the same or compatible licenses
- Ensure distributed derivative code is publicly available
- The definition of a "derivative work" differs per license.
- There are strong ("No exceptions!") and weak ("exceptions possible") copyleft licenses.
- Examples: GNU General Public License (GPL-2.0, GPL-3.0), Eclipse Public License (EPL)

#### "Permissive" Licenses

- “The world is good.”
- Place minimal restrictions on code use, allowing inclusion in projects with most other licenses, incl. non-free and proprietary works.
- Examples: MIT, BSD-3, Apache License 2.0

### Public Domain

- Copyright holders waive all exclusive rights.
- Not possible under German law ("Urheberpersönlichkeitsrechte").
- Effectively "no copyright" under US-American law.
- Example: CC0

## Combining Modules under Different Licenses

### License Incompatibility

- Occurs when software combines components with conflicting licenses.
- Common with copyleft licenses
- Incompatible modules cannot be legally combined and distributed.

### Derivative Work or Combined Work?

- Important when dealing with copyleft licenses
- Depends on:
  - The specific license's definition of derivative work.
  Strong copyleft licenses (e.g., GPL) are strict and make it hard to "achieve" a combined work.
  - The usage mechanism (e.g., copying, static linking, dynamic linking)

![Overview when code is considered as combined and derivative work](https://upload.wikimedia.org/wikipedia/commons/6/6b/Software-license-compatiblity-graph.svg)

## Minimal Checklist

1. **Choose a License**:
   - Consider your publication strategy, third-party dependencies, organizational restrictions, and community norms.
   - Use OSI-approved licenses for your own code.
   - Refer to [Choose a License](https://choosealicense.com/) by GitHub for guidance.
   - Prefer permissive licenses as they make it easier to reuse code:
     - For small, more static projects: MIT or BSD (3-clause, 2-clause).
     - For larger, evolving projects: Apache License 2.0 (allows to practice **patent claims** of contributors to the code).

2. **Seek Permission from Supervisor**:
   - Ensure your organization permits sharing the software under the selected license.

3. **Prepare Your Code**:
   - Minimum: Add a `LICENSE` file with the license text and copyright holder.
   - Recommended:
     - Document license and copyright holders for each file.
     - Document third-party dependencies, including their licenses and usage method.
     - Include this information in the `LICENSE` file and create a `LICENSES` folder for license texts.
     - Add a "License" section to the `README` file summarizing the main licenses and linking to related files.
     - Use the [REUSE tool](https://reuse.software/tutorial/) to ensure comprehensive license statements.

## Further Reading

- Open Source definition and approved licenses by the [Open Source Initiative](https://opensource.org)
- [SPDX License List](https://spdx.org/licenses/) for license texts
- [Software Licenses in Plain English](https://www.tldrlegal.com) by tl;drLegal
- [Free Software definition](https://www.gnu.org/philosophy/free-sw.html) by GNU
- Paper ["A Quick Guide to Software Licensing for the Scientist-Programmer"](https://doi.org/10.1371/journal.pcbi.1002598)
