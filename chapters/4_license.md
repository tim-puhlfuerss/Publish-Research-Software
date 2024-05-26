# 4. Add a License

## Disclaimer

This is no legal advice.
Ask for legal advice if you are unsure about licensing (e.g., a lawyer or your organization's legal department).

## TL;DR

- The copyright holder must state a license to grant others rights to (re-)use the software.
- Check the compatibility of licences from third parties (libraries, data, etc.) from the very beginning.
- Prefer using [official, permissive FOSS licenses](https://opensource.org/licenses/alphabetical).
- Minimum: Add a `LICENSE` file and state the copyright holder.
- Recommended: Follow the [REUSE specification](https://reuse.software/specifications/).

## Why is This Process Important?

- An explicitly stated software license is required to (re-)use the artifacts legally.

## Copyright

### What is Copyright?

- Copyright gives the copyright holder exclusive rights on the protected artifact, such as the usage, creation of copies, distribution, and creation of derivative works.
- Copyright gives other persons no rights, unless the copyright holder explicitly grants them.
The copyright holder can decide in what way their work is used or not used at all.
- Copyright law works differently per country.
In the following, we orientate on [German copyright law](https://www.gesetze-im-internet.de/urhg/).
- In accordance to German Copyright law, some of the exclusive rights (e.g., attribution) cannot be waived or transferred to a third party.

### What is Protected by Copyright?

- Copyright protects the expression of an idea but not the idea itself.
- In context of software, copyright protects software as source code, object code, or integrated with hardware, including documentation and accompanying material.
- In which case is the software protected by copyright?
  - A certain threshold of originality is required.
  - If two developers independently create the same source code, the required threshold of originality might be not achieved.

### Who is the Copyright Holder?

- The copyright holder of a software is the person or organization who has the exclusive rights with regard to this software.
- Everyone who contributed to the creation of the software ("authors") is considered a copyright holder.
- The quality and size of the contribution do not matter.
- Usually, authors and copyright holders are the same.
- __However, if an author is paid by an employer__:
  - The employer is often the copyright holder instead of the author and is entitled to exercise all economic rights in the software ("Verwertungsrechte"), unless otherwise agreed.
  - The developers are still authors and keep certain rights, such as attribution.
- If your private initiative is the reason for the development of the software and you have developed the software off work, you are the sole copyright holder.
This is also the case if you have been inspired by your work experiences and knowledge.
- All copyright holders jointly exercise the rights granted by copyright.
For example, if you want to re-license a software, all copyright holders must agree on the license change.

## Software Licenses

- A copyright holder can grant rights to other persons or legal entities with licenses.
- Parts of a software license:
  - Grant specific rights (e.g., use, copy, distribute)
  - Demand obligations (e.g., disclosure of source code under a certain license, constraints concerning the distribution, attribution)
- Every software you use must be covered by a license.
- Users are covered by whatever license you place on your software.

## Software License Types

### Proprietary

- Non-standardized licenses with specific licensing
- Examples: Commercial License, Shareware License, Freeware License

### Free and Open Source

- Defined by the Free Software Foundation (FSF) and the Open Source Initiative (OSI).
Both essentially refer to the same set of licenses but favor different values (development methodology vs. social movement).
- These licenses imply the public availability of the source code and allow open code distribution, modification, and re-use.

#### "Copyleft" Licenses

- “The world is evil.”
- Requires to use the same or compatible license for distributed derivative work.
- Results in a "viral effect" as all distributed derivative code must also be publicly available.
- The definition of a "derivative work" differs per license.
- There are strong ("No exceptions!") and weak ("exceptions possible") copyleft licenses.
- Examples: GNU General Public License (GPL-2.0, GPL-3.0), Eclipse Public License (EPL)

#### "Permissive" Licenses

- “The world is good.”
- Generally, these licenses are compatible and interoperable with most other licenses due to only few obligations.
- These licenses permit using the code in non-free and proprietary derivative works.
- Hence, they place very few restrictions on what can be done with the code.
- Examples: MIT, BSD-3, Apache License 2.0
- __Prefer Apache over MIT for collaborative projects.__

### Public Domain

- Copyright holders waive all their exclusive rights.
- Not possible in accordance to German copyright law ("Urheberpersönlichkeitsrechte").
- Effectively "no copyright" in accordance to US-American copyright law.
- Example: CC0

## Combining Modules under Different Licences

### License Incompatibility

- Exists when a software is a derivative work of components licensed under conflicting licensing terms.
- Typical problem with copyleft licenses
- Modules under conflicting licenses cannot be legally combined and distributed.

### Derivative Work or Combined Work?

- Important questions when dealing with copyleft licenses
- Type of your work depends on:
  - The concrete license and its definition of a derivative work.
  Strong copyleft licenses (e.g., GPL) are quite strict and make it hard to "achieve" a combined work.
  - The usage mechanism (copying, static linking, dynamic linking)

![](https://upload.wikimedia.org/wikipedia/commons/6/6b/Software-license-compatiblity-graph.svg)

## Minimal Checklist

1. Choose a license.

   - Decision depends on different factors, e.g.:
     - Your publication strategy
     - Restrictions from third-party dependencies (requires a list of dependencies, their version, their license, and the way you use them)
     - Restrictions in the working group/organization
     - Typically used licenses in your community of practice.
   - Only use Open Source Initiative (OSI)-approved licenses for own code.
   - ["Choose a License"](https://choosealicense.com/) by GitHub helps to get started.
   - Prefer permissive licenses because they make it easier to re-use code.
     - Small works: MIT or BSD (3-clause, 2-clause) license. They are short and quite understandable.
     - Larger works: Apache License 2.0. A bit more complicated but allows to practice __patent claims__ of contributors to the code.
  
2. Ask your supervisor for permission.

   - Your organization holds the rights on software that you produce during your work ("Verwertungsrechte").
   The organization must explicitly permit sharing the software under the selected license.

3. Prepare your code:

   - Minimum: Add a `LICENSE` file that contains the license text and states the copyright holder.
   - Recommended:
     - Document the license and copyright holders for each file.
     - Document third-party dependencies, including their licenses and the way they are used (e.g., statically linked, dynamically linked, run as command).
     - Document this information in a `LICENSE` file and the license texts in a `LICENSE` folder.
     - Add a brief "License" section to the `README` file summarizing the main license(s), indicating the copyright holder, and linking to the license-related files.
     - Use and follow the [REUSE tool](https://reuse.software/tutorial/) to lint the project for missing licence statements and add them automatically.

## Further Reads

- Open Source definition and approved licenses by the [_Open Source Initiative_](https://opensource.org)
- [SPDX License List](https://spdx.org/licenses/) to download license texts
- [Software Licenses in Plain English](https://www.tldrlegal.com) by _tl;drLegal_
- [Free Software definition](https://www.gnu.org/philosophy/free-sw.html) by _GNU_
- [Paper](https://doi.org/10.1371/journal.pcbi.1002598) "A Quick Guide to Software Licensing for the Scientist-Programmer"
