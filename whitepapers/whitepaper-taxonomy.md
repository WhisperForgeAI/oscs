# OSCS: A 7-Layer Universal Education Taxonomy for Open, Competency-Based K-12 Curriculum Standards

**White Paper**  
**Version 1.0** — July 2026  

---

### Executive Summary

The **Open Source Curriculum Standard (OSCS)** introduces a flexible, layered taxonomical framework designed to organize, share, and evolve K-12 curriculum standards in an open, collaborative, and AI-ready way.

Traditional standards (CCSS, NGSS, state frameworks) are valuable but often rigid, grade-bound, and difficult to adapt for competency-based learning, neurodiverse students, homeschooling, or personalized AI tutoring. OSCS addresses these limitations by providing a **7-layer universal taxonomy** that:

- Separates **content** (what to learn) from **progression** (at what level of mastery)
- Supports **rank/competency-based** progression instead of (or alongside) traditional grades
- Enables deep **integration** across subjects while maintaining clear standards alignment
- Is fully **open source** and machine-readable for AI systems and modern tooling

This white paper outlines the taxonomy, its structural implementation, benefits, and roadmap for community adoption.

---

### 1. Introduction: The Challenge with Current Standards

Existing K-12 standards frameworks have served education well but face growing limitations in 2026:

- **Grade-centric rigidity** — Most systems assume students progress uniformly by age/grade, which does not reflect real learning variability (especially for neurodivergent students).
- **Siloed subjects** — Strong vertical alignment within subjects, but weak support for integrated, project-based, or cross-domain learning.
- **Limited machine readability** — Standards are often published as PDFs or static documents, making them difficult to use in adaptive learning platforms or AI tutors.
- **Slow evolution** — Updating or extending standards at scale is cumbersome for districts and open communities.

The **Open Source Curriculum Standard (OSCS)** proposes a modern, layered alternative that preserves the strengths of existing frameworks while adding flexibility, openness, and AI compatibility.

---

### 2. The OSCS 7-Layer Universal Education Taxonomy

OSCS organizes curriculum through seven distinct but interconnected layers. This separation of concerns creates clarity, reusability, and powerful composability.

| Layer | Name | Primary Focus | Role in the System |
|-------|------|---------------|--------------------|
| **1** | Foundational Learning Domains | Broad pillars of human knowledge and development | Highest-level organization (e.g., Mathematical & Quantitative Reasoning, Language/Literacy & Communication) |
| **2** | Core Strands / Competency Clusters | Major organizing categories within a domain | Provides structure within domains (e.g., Number & Operations – Fractions) |
| **3** | Specific Learning Standards / Performance Expectations | Granular, assessable learning targets | The core atomic unit — precise “what students should know and be able to do” statements |
| **4** | Developmental Progressions & Mastery Levels (Ranks) | How mastery develops over time | Enables competency-based progression (Emerging → Developing → Proficient → Advanced) independent of age/grade |
| **5** | Cognitive Processes, Depth & Practices | How deeply and in what ways students think | Bloom’s/DOK levels + disciplinary practices (modeling, justifying, etc.) |
| **6** | Application Contexts & Real-World Transfer | Where and how learning is applied | Personal, local, global, career, and authentic problem contexts |
| **7** | Dispositions, Mindsets & Cross-Domain Integration | Holistic growth and connections | Growth mindset, SEL, ethical reasoning, and integration across domains |

**Key Design Principle**:  
**Layer 3 (Standards)** is the primary organizational unit.  
**Layer 4 (Rank)** is a property of standards, not a container. This allows one standard to be taught at multiple levels of mastery without duplication.

---

### 3. Structural Implementation

OSCS is implemented as a **GitHub-based, Markdown-first repository** with rich YAML frontmatter for machine readability.

**Recommended Directory Structure** (Domain-first):

```
oscs/
├── mathematical-quantitative-reasoning/
│   └── number-and-operations-fractions/
│       └── standard-fractions-classification-equivalence.md
├── progression-maps/
├── cross-cutting/
│   ├── cognitive-depth/
│   ├── application-contexts/
│   └── dispositions-mindsets/
├── alignments/
└── LICENSE, README, TAXONOMY.md
```

Each standard file contains:
- Clear **Layer 3** content (the actual standard)
- **YAML frontmatter** encoding Layers 4–7
- Sections for different ranks when needed
- Links to progression maps for vertical alignment

This structure is human-editable, version-controllable, searchable, and directly consumable by AI systems via retrieval-augmented generation (RAG).

---

### 4. Alignment with Existing Standards

OSCS does **not** replace CCSS, NGSS, C3, or state frameworks. Instead, it provides an organizing layer on top of them.

Every OSCS standard includes explicit mappings in its frontmatter (e.g., “maps to MCCRS 4.NF.A.1 and CCSS 4.NF.A.1”). This enables:
- Seamless use in existing school systems and portfolios
- Easy transition and hybrid adoption
- Clear lineage and credibility

---

### 5. Benefits and Use Cases

**For Schools & Districts**
- Clearer vertical alignment and cross-curricular integration
- Support for competency-based education and mastery tracking

**For Homeschooling & Portfolios**
- Flexible rank-based progression that still maps to state expectations (e.g., MCPS reviews)

**For AI-Powered Personalized Learning**
- Rich, structured context windows for tutors and adaptive platforms
- Precise targeting of standards + rank + depth + context + dispositions

**For Open Collaboration**
- Anyone can contribute, fork, or extend standards while maintaining clear attribution and compatibility

---

### 6. Licensing and Openness

OSCS is released under the **Creative Commons Attribution 4.0 International (CC BY 4.0)** license. This choice maximizes adoption while requiring proper credit. The taxonomy structure, Markdown files, and frontmatter schemas are freely usable, adaptable, and remixable.

---

### 7. Conclusion and Next Steps

The OSCS 7-layer taxonomy offers a practical, forward-looking framework that balances rigor with flexibility. By separating standards from progression levels and embedding rich metadata, it supports both traditional schooling and emerging models of personalized, competency-based, and AI-augmented learning.

**Immediate Roadmap**
- Publish full taxonomy documentation and example standards (including detailed fractions progression)
- Build community contribution guidelines
- Develop reference implementations for AI tutor integration
- Create visual tools and progression map generators

We invite educators, curriculum designers, technologists, and families to collaborate on building the next generation of open curriculum infrastructure.

---

**About This Document**  
This white paper was developed as part of the initial OSCS project. Feedback and contributions are welcome via the project repository.

**Repository**: [github.com/WhisperForgeAI/oscs](https://github.com/WhisperForgeAI/oscs)
