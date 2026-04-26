# PeTRA — Performance Tracing Report Assistant

**An analytics engine for serious games, published as Open Documentation.**

PeTRA is a research-grade analytics engine designed to read player behavior in serious games — not just outcomes (scores, completion), but the *information trails* players leave through the game environment over repeated play. Developed alongside *Nexus* (a serious game on social media risk awareness) as a paired example, PeTRA is intended to grow into a common analytics core that other serious-game researchers can adapt to their own games.

This repository hosts PeTRA's **Open Documentation**: the methodology, design rationale, and architecture. It does NOT host the implementation code.

> 🚧 **This repository is being actively populated.** Initial documentation is in the form of book chapter drafts (Loh, Sheng & Ifenthaler, in press, 2027). Source documents and dedicated documentation files will be added over the coming weeks.

---

## What is *Open Documentation*?

PeTRA's **Open Documentation** model means:

- **Methodology, design rationale, and architecture** are openly published here for inspection, replication, and scholarly reference.
- **Implementation code** is not openly licensed for unrestricted redistribution. Researchers wanting to use PeTRA can either (a) build their own implementation from the documentation, or (b) request access to a Docker image as a vetted collaborator.

Academic methodology papers are, in effect, *blueprints* — they describe HOW to build something so that other researchers can implement it in their own context. Open Documentation extends this academic practice into a publication strategy: the blueprint is openly published; the implementation is one worked example.

This positioning fits within the broader *Curated Openness* discourse in the technology industry (Red Hat, Apple) and aligns with the OECD's framing of AI openness as a spectrum (OECD, 2025). On the Linux Foundation Model Openness Framework, PeTRA's Open Documentation tier sits below MOF Class III — a position the framework doesn't yet formally name.

The choice reflects two realities:

1. **Academic norms** of methodological transparency are met when design rationale and architecture are openly documented for reviewers, replicators, and other researchers.
2. **2026 security realities**: automated AI-assisted vulnerability scanning makes traditional open-source attack surfaces too costly to defend for a small research team.

---

## For researchers wanting to use PeTRA

Two paths:

**Path 1 — Build your own implementation from the documentation.**

The PeTRA methodology is specifiable enough that you can implement an analytics engine for your own serious game in any tech stack. The documentation here is the blueprint; your implementation is the realization. Cite PeTRA as the methodological source.

The architecture is three-layer:

1. **Adapter** — reads your game's data source and converts it into the format PeTRA expects
2. **Analytics modules** — process information trails and other behavioral indicators
3. **Reporting/visualization layer** — renders results for researchers

**Path 2 — Request access to the Docker image as a vetted collaborator.**

A Dockerized version of PeTRA is available to vetted academic researchers on request. Email the author with:

- Your name, institutional affiliation, and role
- A brief description of your research project and intended use
- Your IRB approval status, if applicable
- Acknowledgement that the Docker image will not be redistributed

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

For PeTRA-related inquiries — Docker access requests, collaboration proposals, methodology questions, citation queries — please email above.

---

## References

- OECD (2025). *AI Openness: A Primer for Policymakers*. OECD Artificial Intelligence Papers No. 44. OECD Publishing.
- Linux Foundation (2024). *Model Openness Framework (MOF)*.
- Loh, C. S., Sheng, Y., & Ifenthaler, D. (in press, 2027). *Serious Games Analytics in the Age of AI*. Springer.
