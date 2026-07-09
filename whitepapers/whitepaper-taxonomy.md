# OSCS: A 7-Layer Universal Education Taxonomy for Open, Competency-Based K-12 Curriculum Standards

**White Paper**  
**Version 1.2** — July 2026  

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

### 2.1 Foundational Learning Domains (Layer 1)

OSCS defines **nine** Foundational Learning Domains. Each domain has both a **Full Name** (used in documentation) and a **Short Name** (used for folders and metadata).

| # | Full Name | Short Name | Description |
|---|-----------|------------|-------------|
| 1 | Language, Literacy & Communication | `language-literacy` | Reading, writing, speaking, listening, and multilingual communication |
| 2 | Mathematical & Quantitative Reasoning | `mathematics` | Number sense, operations, algebra, geometry, data, financial literacy, and mathematical practices |
| 3 | Scientific Inquiry & Understanding the Natural World | `science` | Science practices, crosscutting concepts, and disciplinary core ideas |
| 4 | Human Societies, History, Geography & Civic Life | `human-societies` | History, civics, economics, geography, and evidence-based study of religion and culture |
| 5 | Creative Arts & Expressive Development | `creative-arts` | Visual arts, music, dance, theatre, and media arts |
| 6 | Health, Physical Development & Wellness | `health-wellness` | Physical education, health education, and personal wellness |
| 7 | Personal Agency, Social-Emotional Learning & Character | `personal-agency` | SEL, executive function, ethics, and character development |
| 8 | Technological Fluency, Computational Thinking & Innovation | `technology` | Computer science, digital literacy, and innovation |
| 9 | Theology, Philosophy, and Worldviews | `theology-philosophy` | Theology, faith traditions, philosophy, ethics, metaphysics, and systems of meaning (religious and secular) |

**Important Distinction**:

- **Domain 4 (`human-societies`)** contains the *evidence-based, historical, and sociological study of religion*.
- **Domain 9 (`theology-philosophy`)** contains *faith-based theology*, personal belief systems, and philosophical approaches to meaning and value.

---

### 3. Structural Implementation

OSCS is implemented as a **GitHub-based, Markdown-first repository** with rich YAML frontmatter for machine readability.

**Recommended Directory Structure** (using Short Names):

```
oscs/
├── language-literacy/
├── mathematics/
├── science/
├── human-societies/
├── creative-arts/
├── health-wellness/
├── personal-agency/
├── technology/
├── theology-philosophy/          ← New Domain
├── progression-maps/
├── cross-cutting/
└── alignments/
```

Each folder contains a `README.md` with the **Full Name** as the title.

---

### 3.1 Initial Layer 2 Strands under Theology, Philosophy, and Worldviews

The following Layer 2 strands are proposed for the new domain:

- `theology-and-faith-traditions`
- `philosophy-and-secular-worldviews`
- `ethics-and-moral-philosophy`
- `metaphysics-and-ultimate-questions`

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
- Publish full taxonomy documentation and example standards
- Build community contribution guidelines
- Develop reference implementations for AI tutor integration
- Create visual tools and progression map generators

We invite educators, curriculum designers, technologists, and families to collaborate on building the next generation of open curriculum infrastructure.

---

**About This Document**  
This white paper was developed as part of the initial OSCS project. Feedback and contributions are welcome via the project repository.

**Repository**: [github.com/WhisperForgeAI/oscs](https://github.com/WhisperForgeAI/oscs)
