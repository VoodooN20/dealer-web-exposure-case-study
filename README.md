# Dealer Web Exposure Case Study
An anonymized web security case study examining potential exposure of confidential dealer materials.

## Overview

While searching a company's website for discount codes, I accidentally discovered a publicly accessible, dealer facing webpage that appeared to contain confidential business materials.

The page provided download links to several documents, including a dealer merchandise price list marked confidential and not for public release under the dealer agreement, as well as a way to sign up for the dealer exclusive newsletter. I then checked Google search results and found that the page and associated document contents appeared to have been indexed.

I also reviewed the site's `robots.txt` file, which contained no disallow rules for web crawlers. I documented my observations, preserved screenshots as evidence, and contacted the company to report the potential exposure.

This case study documents the discovery, the evidence collected, the potential security implications, and the responsible disclosure process. The investigation was limited to passive observation; I did not download the documents or conduct further testing.

## Scope and Methodology

The investigation was limited to passive observation of publicly accessible website resources.

Activities performed:
- Discovered a dealer-facing webpage while searching for discount codes.
- Observed links to dealer materials, including a price list marked confidential.
- Checked Google search results for evidence that the webpage and associated document contents were indexed.
- Reviewed the website's `robots.txt` file.
- Captured screenshots documenting the observations.
- Contacted the company to report the potential exposure.

Activities not performed:
- Did not download the linked documents.
- Did not attempt to bypass authentication or access controls.
- Did not perform automated scanning or additional security testing.

## Security Analysis

### Potential Issue: Exposure of Confidential Business Resources

The publicly accessible dealer facing webpage displayed an explicit confidentiality notice stating that everything on the page should be considered confidential and was not intended for public dissemination under any circumstances. The notice also warned that public sharing could violate the dealer agreement.

The page included dealer specific resources, such as document download links and a dealer exclusive newsletter signup. Several linked documents were also marked confidential.

Because the page appeared accessible without dealer authentication, this raised concerns about potential unintended exposure of both the page itself and its associated resources.

If access to these materials was intended to be restricted to authorized dealers, their public accessibility could indicate an access control weakness.

### Search Engine Indexing

Google search results showed that the webpage and associated document contents appeared to have been indexed, potentially increasing their discoverability by unintended audiences.

The site's `robots.txt` file contained no disallow rules for web crawlers. This was recorded as contextual evidence, not as a vulnerability by itself: `robots.txt` is not an access control mechanism.

### Preliminary Framework Mapping

- **OWASP Top 10 — A01: Broken Access Control:** Potentially relevant if the page and its resources were intended to be restricted to authorized dealers.
- **OWASP Web Security Testing Guide — Information Gathering:** Relevant to the passive discovery of the page and its appearance in search engine results.

These mappings are preliminary. The intended access controls, underlying cause, and extent of exposure have not been independently verified.
