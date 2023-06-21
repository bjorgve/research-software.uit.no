+++
title = "Draft: Research software licensing guide"
description = ""
date = "2023-06-21"

[extra]
authors = "Radovan Bast"
+++

<div class="uk-alert-danger" uk-alert>

**This is an early draft**. We will share this draft with colleagues and
various stakeholders for review and comments and our hope is that this will
form the basis for a research software licensing guide at
[UiT](https://uit.no/).  Please send comments, suggestions, and corrections to
[radovan.bast@uit.no](mailto:radovan.bast@uit.no).

</div>

<!-- toc -->


## Scope: Is my code/script/notebook/file "research software"?

We consider any code or script or notebook or file, large or small, as
"research software" if it is needed to generate or visualize or reproduce data
or results that are part or will be part of a publication. You don't need to
be a "proper software engineer" to produce software. Most research software is
not written by "proper software engineers" (whatever that means).

Examples for what we consider in scope for this guide:
- Script to convert data from one format to another
- Script to read data and visualize it
- Program that generates data
- Analysis script
- Set of scripts that form an analysis pipeline
- Code that is compiled
- Code that is dynamically interpreted and not compiled
- Web app


## Why software licenses matter

In open research we strive towards reproducibility (results can be verified by
other researchers) and reusability (results can be reused in follow-up
research by you and/or others without starting over from scratch).

Without a license that allows reuse and redistribution and clarifies terms
under which code can be reused and redistributed:
- others may not be able to publish derivative work based on your code
- you may not be able to publish derivative work based on somebody else's code
  or even your own code (after changing jobs)

This means that **clarifying license terms is essential for derivative work
based on your research to be even publishable**. Choosing an open source
license can also be good insurance for you against being locked out of your
own code after changing affiliation/group or job.


## Which license to choose

### If your work is derivative work

Your code is derivative work if you have started from an existing code and
made changes to it or if you incorporated an existing code into your code.

If your code is derivative work, then you need to check the license of the
original code. Depending on the license, your choices might be limited. In
this case we recommend to use these two resources:
- [Joinup Licensing Assistant - Find and compare software licenses](https://joinup.ec.europa.eu/collection/eupl/solution/joinup-licensing-assistant/jla-find-and-compare-software-licenses)
- [Joinup Licensing Assistant - Compatibility Checker](https://joinup.ec.europa.eu/collection/eupl/solution/joinup-licensing-assistant/jla-compatibility-checker)

If the original code does not have a license, you may not distribute your
derivative code. You can try to contact the authors and ask them to clarify
the license of their code.


### If your work is not derivative work

If you have started "from scratch", not from an existing code, and not
incorporated existing code into your code. Note that if you only use (but not
incorporate or change) libraries, plug-ins, and packages, which are
distributed via platforms like PyPI, Conda, CRAN, Crates, ... is typically not
derivative work.

Before you choose a license, clarify (with your supervisor or principal
investigator):
- Does your work contract or grant or collaboration agreement dictate a
  specific license?
- Commercialization intent
- Whether there is unknown/mixed ownership: If there are multiple persons or
  organizations as owners, all must agree to the license.

Assuming that all the above is no problem and no overriding guidelines exist,
we recommend to choose one of these two licenses:
- **European Union Public Licence, Version 1.2 or later (EUPL)**
  (<https://data.europa.eu/doi/10.2799/77160>): this license is an official
  license of the European Union (EC Decision, part of European law), is
  interoperable, reciprocal (derivative work must publish and provide back the
  modified source code), and compatible with many standard licenses. It is a good choice
  if you want to make sure that you have access to changes and improvements applied
  to your code so that you can integrate them back and reuse them in your own work. This
  is the share-alike principle.
- **MIT License** if ease of reuse is more important for
  you than derivative work providing modifications back: Others will be able
  to do whatever they want as long as they include the original copyright and
  licence notice in any copy of the software/source. For small and short-lived projects
  this can be a good choice.


## Practical recommendations

- Choose a license early in the project, even before you publish it. Later in
  the project it may become complicated to change it.
- Add a `LICENSE` file to your repository containing the license text in plain text.
- Follow the checklist from https://reuse.software (good information about so-called SPDX identifiers).
- Do not invent your own license. Choose one of the standard licenses, otherwise compatibility is not clear:
  - [Joinup Licensing Assistant - Find and compare software licenses](https://joinup.ec.europa.eu/collection/eupl/solution/joinup-licensing-assistant/jla-find-and-compare-software-licenses)
  - [Joinup Licensing Assistant - Compatibility Checker](https://joinup.ec.europa.eu/collection/eupl/solution/joinup-licensing-assistant/jla-compatibility-checker)
- Keep track of where things come from.
  Before using and adapting somebody else's code, clarify their license. If
  their code does not have a license, contact the authors and ask them to
  clarify the license of their code.
- Work as if the repo is public even though it is still private:
  This is to avoid surprises about code in the history with incompatible
  license years later when we decide to open the project.
- Open core: You don't have to open source all your work. Core can be open
  and on a public branch. The unpublished stuff can be on a private repository.


## Make it persistent and citable

Choosing a license, adding a `LICENSE` file, and putting your code on GitHub or
GitLab is good but not enough to make your code findable, accessible,
interoperable, and reusable for the next 5-10 (or more) years, since nothing
will prevent the owner of the repository to delete it or move it and we have no
guarantee that these services will still be around in 5 or 10 years.

We recommend to go two steps further:
- Add a [CITATION.cff file](https://citation-file-format.github.io/)
- Get a [digital object identifier
  (DOI)](https://en.wikipedia.org/wiki/Digital_object_identifier) for your code
  on [DataverseNO](https://dataverse.no/) or [Zenodo](https://zenodo.org/)


## Questions and contact

Unsure which license to choose?  Unsure how to proceed with sharing your code
or reusing somebody else's code?  The [research software engineering (RSE)
group](https://research-software.uit.no/) at [UiT](https://uit.no/) is here to
help you. You can contact us at [rse@uit.no](mailto:rse@uit.no) or come to our
office hours.


## Great resources

- Guide from the Aalto University in Finland: ["Opening your Software at Aalto University"](https://www.aalto.fi/en/open-science-and-research/opening-your-software-at-aalto-university)
- [Joinup Licensing Assistant - Find and compare software licenses](https://joinup.ec.europa.eu/collection/eupl/solution/joinup-licensing-assistant/jla-find-and-compare-software-licenses)
- [Joinup Licensing Assistant - Compatibility Checker](https://joinup.ec.europa.eu/collection/eupl/solution/joinup-licensing-assistant/jla-compatibility-checker)
- [Citation File Format (CFF)](https://citation-file-format.github.io/)