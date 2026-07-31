# Essential DICOM Metadata for Reproducible Imaging AI

A multi-phase development-and-validation study that builds a **modality-specific,
high-value DICOM tag list** (an *essential DICOM metadata checkpoint*) for CT,
MR, and mammography (MG). The checkpoint identifies the imaging-protocol items,
expressed as internationally standardized DICOM attributes, that should be
prioritized when developing, validating, and deploying medical imaging AI.

**Now recruiting experts for Phase 4** 

> **Status:** Pre-registration deposited; expert consultation (Phase 4) opening.
> The data-driven candidate checkpoint (Phases 1–3) is built and internally
> validated; the rating and analysis rules for Phase 4 are fixed in advance.

---

## Why this study

Imaging AI models often behave differently once they leave the setting they were
built in. A large and *controllable* part of that shift comes not from the
patients but from **how images are produced**, such as acquisition, reconstruction,
display, and post-processing. Those parameters are already captured as
machine-readable DICOM tag–value pairs, yet a single image carries hundreds of
them, only a fraction of which shape any given model, and completeness varies by
site and vendor. Existing reporting guidance (STARD-AI, CLAIM, TRIPOD+AI) asks
that the acquisition protocol be described but does not say *which* elements
matter.

This study answers that question: **which imaging-protocol items, expressed as
DICOM metadata, are most important to identify in advance so that a model
performs consistently wherever it is deployed.** The framing is *adoption and
verification*, not obligation: a practical reference developers and sites can
use to check whether the context needed to reproduce a model's reported
performance is documented.

---

## At a glance

| | |
|---|---|
| **Design** | Four-phase development-and-validation; single pre-registered round of expert consultation |
| **Modalities** | CT, MR, mammography (MG) |
| **Output** | Modality-specific *essential DICOM metadata checkpoint* (a prioritized tag list) |
| **Candidate items rated** | CT 30 / MR 37 / MG 13 |
| **Phase 4 instrument** | Single online form (Google Forms), one page set per modality |
| **Rating** | 5-point Likert importance; bands fixed in advance (4–5 high / 3 uncertain / 1–2 low) |
| **Retention rule** | Median 4–5 **and** ≥ 70% of scoring respondents rate 4–5 |
| **Pre-registration** | GitHub deposit before consultation opens · OSF [link TBD] |
| **Contact** | Kyulee Jeon (kyulee.jeon@gmail.com), Yonsei University College of Medicine |

---

## The four phases

| Phase | What happens | Question it answers |
|---|---|---|
| **1. Extraction** | Mine acquisition parameters from open-access imaging-AI literature (PubMed Central, Jul 2024–Jun 2025; 1,010 CT / 1,089 MR / 56 MG papers) with a few-shot LLM | What does the community report? |
| **2. Alignment** | Map extracted parameters to standardized DICOM attributes (PS3.3); organize under FAIR principles | How do these map to the standard? |
| **3. Threshold & validation** | Retain tags reported by > 5% of papers; test whether reporting frequency tracks model behavior via AI-model replication (FDR-adjusted) | Does reporting frequency carry a performance signal? |
| **4. Expert consultation** | Single structured round; experts rate each candidate's importance for real-world AI; steering committee revises | How important do experts judge each attribute to be? |

Phases 1–3 construct and internally validate a **data-driven candidate
checkpoint**; Phase 4 refines it. The two evidence streams — what the community
*reports* and what experts *judge important* — are reported side by side and
interpreted jointly, each with its own biases (publication/extraction bias vs.
self-selection bias).

In Phase 3, the highly-reported sets were markedly enriched for
performance-associated (FDR-significant) tags relative to rarely-reported ones
(enrichment: CT 8.7×, MR 7.8×, MG 3.0×), and a small set of infrequently
reported but performance-associated tags was carried forward.

---
## Versioning

The protocol is deposited on GitHub before the consultation begins. Substantive
amendments after deposition are logged with date and rationale in a versioned
amendment record; minor edits (typography, formatting, clarification) are tracked
in a change log without a new version number.

| Version | Summary |
|---|---|
| v0.13 | Pre-registration protocol: four-phase design, candidate checkpoint, and fixed Phase 4 rating/analysis rules |

---

## How to cite

> Jeon K, Park WY, Sippel Schmidt TM, Dewey B, Nagy PG, Yoon SH, You SC.
> *Essential DICOM Metadata for Reproducible Imaging AI: A Multi-Phase
> Development and Expert Validation Study* (Pre-registration Protocol, v0.13).
> 2026. [OSF/repo link]

The full data-driven analysis (Phases 1–3) is reported separately:
Jeon K, et al. *Essential DICOM metadata for transparent reporting in radiology
AI: A data-driven approach* (in preparation).

---

## Authors

Kyulee Jeon¹˒², Woo Yeon Park³, Teri M. Sippel Schmidt³, Blake Dewey³,
Paul G. Nagy³, Soon Ho Yoon⁴, Seng Chan You¹˒²

1. Department of Biomedical Systems Informatics, Yonsei University College of Medicine, Seoul, Republic of Korea
2. Yonsei Institute for Digital Health, Yonsei University, Seoul, Republic of Korea
3. Department of Biomedical Informatics and Data Science, Johns Hopkins University School of Medicine, Baltimore, MD, USA
4. Department of Radiology, National Jewish Health, Denver, CO, USA

Experts who complete the consultation receive an advisory honorarium on study
completion. The authors declare no financial conflicts of interest related to
this work.

---

## License

- Protocol, instrument, and documentation: [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)
- Any analysis code (added later): [MIT](https://opensource.org/licenses/MIT)

---

## Acknowledgements

We thank the medical imaging AI, radiology, medical physics, and imaging
informatics communities whose expertise makes this checkpoint possible. 
