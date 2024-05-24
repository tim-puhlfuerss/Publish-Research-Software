# 4. Add a License

## TL;DR

- Minimum: Add a license file and state the copyright holder.
- Recommended: Follow the REUSE Specification, version 3.0.0.
- Consider licences from third parties (libraries, data, etc.) from the very beginning.

## Why is This Process Important?

- Otherwise, potential users cannot (re-)use your artifacts legally.

## Copyright

- Software is protected by a copyright.
- Copyright law works differently depending on a country. In the following, we orientate on German copyright law.
- Copyright protects the expression of an idea but not the idea itself.
In context of software, it includes source code, object code, and design material (§ 69a UrhG, German copyright law).
- Copyright gives the copyright holder certain exclusive rights such as usage, creation of copies, distribution, creation of derivative works (§ 69c UrhG, German copyright law).
- In accordance to German Copyright law, some of the exclusive rights (e.g., attribution) cannot be waived or transferred to a third-party.
- Copyright gives other persons no rights, unless the copyright holder explicitly grants them. 
The copyright holder can decide in what way their work is used or not used at all.

## Software Licenses

- A copyright holder can grant rights to other persons or legal entities with licenses.
- Parts of a software license:
  - Grant rights (e.g., use, copy, distribute)
  - Demand obligations (e.g., disclosure of source code under a certain license, constraints concerning the distribution, attribution)
- Every software you use must be covered by a license.
- Your users are covered by whatever license you place on software that you write.
- License incompatibility exists when a program is a derivative work of components licensed under conflicting licensing terms.

## Software License Types

### Proprietary

- Non-standardized licenses with specific licensing

### Public Domain

- Copyright holders waive all their exclusive rights.

### Free and Open Source

- Imply the availability of the source code and allow open distribution, modification, and re-use
- "Copyleft" licenses:
  - “The world is evil.”
  - Distributed derivative work must also disclose all source code (viral effect)
  - E.g., GPL-2.0, GPL-3.0
- "Permissive" licenses:
  - “The world is good.”
  - Have only a few obligations. Licenses are compatible and interoperable with most other licenses.
  - E.g., MIT, BSD-3, Apache License 2.0

## Combining Modules under Different Licences

### License Incompatibility

- Exists when a program is a derivative work of components licensed under conflicting licensing terms.
- Typical problem with copyleft licenses
- Modules under conflicting licenses cannot be legally combined and distributed.
- Make sure to check the license of libraries that you use!
- Prefer using [official, permissive FOSS licenses](https://opensource.org/licenses/alphabetical).
- __Prefer Apache over MIT for collaborative projects.__

### Derivative Work or Combined Work?

- Important questions when dealing with copyleft licenses
- "Type" of work depends on:
  - The concrete license and its definition of a derivative work. Strong copyleft licenses (e.g., GPL) are quite strict and make it hard to "achieve" a combined work.
  - The usage mechanism (copying, static linking, dynamic linking)

![](https://upload.wikimedia.org/wikipedia/commons/6/6b/Software-license-compatiblity-graph.svg)

## Minimal Checklist

1. Choose a license.

   - ["Choose a License"](https://choosealicense.com/) by GitHub helps to get started.
   - Analyze / comply with licenses of third-party dependencies.
   This requires a list of dependencies, their version, their license, the way you use them.
  
2. Ask your boss for permission.

   - Your organization holds the rights on software that you produce during your work ("Verwertungsrechte").
   For that reason, your organization has to explicitly permit sharing the software under the selected license.

3. Prepare your code:

   - Minimum: Add a `LICENSE` file that contains the license text and states the copyright holder.
   - Recommended:
     - Make it easy to determine the license and copyright holders for each file.
     - Document your third-party dependencies, including their licenses.
     - Use and follow the [REUSE tool](https://reuse.software/tutorial/) to lint your project for and add missing licences automatically.

Ask for legal advice if you are unsure!

## Further Reads

- Open Source definition and approved licenses by the [_Open Source Initiative_](https://opensource.org)
- [SPDX License List](https://spdx.org/licenses/) to download license texts
- [Software Licenses in Plain English](https://www.tldrlegal.com) by _tl;drLegal_
- [Free Software](https://www.gnu.org/philosophy/free-sw.html) definition by _GNU_
- [Paper](https://doi.org/10.1371/journal.pcbi.1002598) "A Quick Guide to Software Licensing for the Scientist-Programmer"
