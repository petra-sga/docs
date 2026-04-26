# PeTRA — Performance Tracing Report Assistant

**An analytics engine for serious games, published as Open Documentation.**

[![DOI](https://zenodo.org/badge/1221296838.svg)](https://doi.org/10.5281/zenodo.19782551)

PeTRA is a research-grade analytics engine designed to read player behavior in serious games — not just outcomes (scores, completion), but the *information trails* players leave through the game environment over repeated play. Developed alongside *Nexus* (a serious game on social media risk awareness) as a paired example, PeTRA is intended to grow into a common analytics core that other serious-game researchers can adapt to their own games.

This repository hosts PeTRA's **Open Documentation**: the methodology, design rationale, and architecture. It does NOT host the implementation code.

> 🚧 **This repository is being actively populated.** Initial documentation is in the form of book chapter drafts (Loh, Sheng & Ifenthaler, in press, 2027). Source documents and dedicated documentation files will be added over the coming weeks.

---

## What is *Open Documentation*?

PeTRA's **Open Documentation** model means:

- **Methodology, design rationale, and architecture** are openly published here for inspection, replication, and scholarly reference.
- **Implementation code** is not openly licensed for unrestricted redistribution.

Academic methodology papers are, in effect, *blueprints* — they describe HOW to build something so that other researchers can implement it in their own context. Open Documentation extends this academic practice into a publication strategy: the blueprint is openly published; the implementation is one worked example.

This positioning fits within the broader *Curated Openness* discourse in the technology industry (Red Hat, Apple) and aligns with the OECD's framing of AI openness as a spectrum (OECD, 2025). On the Linux Foundation Model Openness Framework, PeTRA's Open Documentation tier sits below MOF Class III — a position the framework doesn't yet formally name.

The choice reflects two realities:

1. **Academic norms** of methodological transparency are met when design rationale and architecture are openly documented for reviewers, replicators, and other researchers.
2. **2026 security realities**: automated AI-assisted vulnerability scanning makes traditional open-source attack surfaces too costly to defend for a small research team.

---

## For researchers wanting to use PeTRA

PeTRA offers three paths, each suited to different research needs:

### Path 1 — Build your own implementation from the documentation

The PeTRA methodology is specifiable enough that you can implement an analytics engine for your own serious game in any tech stack. The documentation here is the blueprint; your implementation is the realization.

The architecture is three-layer:

1. **Adapter** — reads your game's data source and converts it into the format PeTRA expects
2. **Analytics modules** — process information trails and other behavioral indicators
3. **Reporting/visualization layer** — renders results for researchers

**Best for**: research teams with engineering capacity who want full independence over their analytics infrastructure.
**Cost**: free.
**Obligations**: standard academic citation when publishing.

### Path 2 — Hosted analytics with co-publication (active collaborators)

Use Loh's hosted PeTRA instance to analyze your data. Your game and database live on your own infrastructure (e.g., Vercel + Render); a custom adapter — which we'll create together — lets PeTRA read your database for analysis. PeTRA computes metrics in real-time; PeTRA is stateless and stores no data, so your data never leaves your infrastructure for storage purposes.

Because Path 2 is a genuine research collaboration — Loh contributes the engine and analytical expertise; you contribute the game, the data, and the research questions — **co-publication is part of the terms**. We discuss authorship, contribution roles, and publication targets at the start of the collaboration.

**Best for**: research collaborators who want to use PeTRA without engineering their own implementation, and who are open to genuine collaborative research.
**Cost**: free.
**Obligations**: co-publication agreement.

To inquire: email the author with your name, institutional affiliation, a brief description of your serious game and research project, your IRB approval status, and your willingness to co-publish.

### Path 3 — Snapshot license for self-hosting

For researchers who need to run PeTRA on their own infrastructure (typically due to IRB requirements, data residency rules, or institutional policies), a snapshot license is available. You receive a frozen version of PeTRA at the time of license; you run it on your infrastructure; you handle security and maintenance. PeTRA's continued development happens privately — newer versions are not provided as part of the snapshot license.

**Best for**: researchers with self-hosting requirements that prevent using Path 2.
**Cost**: token fee (covers administrative costs).
**Obligations**: non-redistribution agreement; you are responsible for the security and maintenance of your installation.

To inquire: email the author with your name, institutional affiliation, the reason a self-hosted version is required, and your IRB approval status.

---

## Related repositories

- **`petra-sga/adapters`** — Adapter SDK + worked examples for connecting other games (open-source-licensed; coming in Phase 2)
- **`petra-sga/papers`** — Methodology paper drafts (coming)

The implementation code (the *engine*) is not hosted in a public repository, in keeping with the Open Documentation model.

---

## Citation

If you use or build on PeTRA, please cite the forthcoming book:

> Loh, C. S., Sheng, Y., & Ifenthaler, D. (in press, 2027). *Serious Games Analytics in the Age of AI*. Springer.

A long-term archival identifier for this documentation repository will be assigned via [Software Heritage](https://www.softwareheritage.org/) once submitted: `swh:1:dir:[TBD]`.

---

## Mirror + archive

This repository is the canonical source. For resilience, mirrors are maintained on:

- GitLab: *(coming)*
- Codeberg: *(coming)*

For long-term preservation independent of any commercial Git platform, cite the Software Heritage SWHID (above) alongside this URL.

---

## Contact

**Christian Sebastian Loh, Ph.D.**
School of Education
Southern Illinois University Carbondale
csloh@siu.edu

For PeTRA-related inquiries — Path 2 collaboration proposals, Path 3 license inquiries, methodology questions, citation queries — please email above.

---

## References

- OECD (2025). *AI Openness: A Primer for Policymakers*. OECD Artificial Intelligence Papers No. 44. OECD Publishing.
- Linux Foundation (2024). *Model Openness Framework (MOF)*.
- Loh, C. S., Sheng, Y., & Ifenthaler, D. (in press, 2027). *Serious Games Analytics in the Age of AI*. Springer.
