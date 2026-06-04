# Impateca
> Interactive educational content for undergraduate mathematics.

Impateca is an educational initiative being developed at IMPA Tech with the goal of producing interactive university-level mathematics content for undergraduates. 

The project combines mathematical writing, web technologies, and interactive visualizations to transform traditional static notes into dynamic educational experiences.

At its core, Impateca is built around an ecosystem composed of a custom language, authoring tools, interactive frameworks, and educational content.

---

# Vision

Mathematics is often taught through static textbooks, lecture notes, and PDF documents. While these formats are excellent for presenting rigorous content, they offer limited opportunities for exploration, experimentation, and visual intuition. Many of the objects mathematicians study—functions, transformations, limits, dynamical systems, and abstract structures—exist vividly in their imagination, yet remain invisible on the page. Impateca aims to bridge this gap by transforming mathematical ideas into interactive experiences, making visible what mathematicians see when they read, think, and discover.

The long-term objective is to create a platform where students can:

- Read mathematical content;
- Interact with visual demonstrations;
- Manipulate parameters;
- Develop intuition alongside formal theory.

---

# Ecosystem

The Impateca ecosystem is organized into five major components.

```text
Impateca
│
├── DELTA (Language)
├── DELTA Editor
├── Canvas Framework
├── Books
└── Web Platform
```

---

# DELTA 

The production of this interactive mathematical learning materials was are powered by DELTA, a lightweight markup language for mathematical writing. The original language has been extended to support interactive components, dynamic visualizations, and other features required for modern web-based educational materials.

Check out the DELTA repository here: [DELTA](https://github.com/rbribeiro/delta)

DELTA is a lightweight markup language designed for mathematical writing.

The language was created to reduce the verbosity of LaTeX while preserving a structured and expressive way of producing mathematical documents.

Instead of writing large amounts of HTML, CSS, or LaTeX boilerplate, authors write content using DELTA syntax.

Example:

```delta
# Definition

A sequence converges to L if...
```

The DELTA compiler transforms the source file into a responsive HTML document.

The goal is to allow authors to focus on mathematics rather than document formatting.

The DELTA Editor is the authoring environment of the ecosystem. The objective is using this software allow we writing educational materials as simple as writing plain text.

---

# Canvas Framework

One of the main innovations of Impateca is the integration of interactive visualizations through HTML5 Canvas.

Traditional mathematical documents are static. The Canvas Framework introduces dynamic content directly into educational materials.

Authors will be able to embed simulations and animations through DELTA commands.

Example:

```delta
canvas(HTML5): animations/riemann_sum.js
name: "riemann-sum"
```

The compiler will automatically:

- Create the canvas element;
- Connect the JavaScript source;
- Handle responsive layouts;
- Integrate the visualization into the page.

Authors only need to implement the mathematical behavior in JavaScript.

### Example Applications

- Compacts Sets
- Taylor approximations
- Linear transformations

---

# Books

Impateca introduces a book-oriented workflow for educational content.

A DELTA document may define metadata describing a mathematical work.

Example:

```delta
dlt type == "book"
area="analysisI"
name="real-analysis"

author: "Author Name"

chapter: 0.1
title: Preface
```

The metadata defines:

- Document type;
- Subject area;
- Book identifier;
- Author information;
- Chapter organization.

---

## Chapter Structure

Regular chapters:

```delta
chapter: 1
chapter: 2
chapter: 3
```

Front matter sections:

```delta
chapter: 0.1
chapter: 0.2
chapter: 0.3
```

Examples include:

- Preface
- Introduction
- Acknowledgements
- Notation

---

## Generated Files

The chapter number determines the generated source file.

| Chapter | Generated File |
|----------|----------|
| 0.1 | cap0-1.txt |
| 0.2 | cap0-2.txt |
| 1 | cap1.txt |
| 2 | cap2.txt |

This structure allows books to be automatically assembled while preserving a logical organization of content.

---

# Web Platform

The Web Platform is the final layer of the ecosystem.

Its purpose is to provide access to educational materials compiler by DELTA and enhanced by the Canvas Framework.

The platform will serve as a public repository of mathematical content.

### Long-Term Goals

- Interactive textbooks
- Course notes
- Educational visualizations
- Searchable content
- Community contributions

The platform is intended to become a central hub for university-level mathematical learning resources.

---

# Development Roadmap

## Phase 1 — DELTA Foundation

- [ ] Extend DELTA syntax
- [ ] Improve compiler architecture
- [ ] Define project structure
- [ ] Book metadata support

---

## Phase 2 — Interactive Components

- [ ] HTML5 Canvas integration
- [ ] Responsive visualization system
- [ ] Animation framework
- [ ] Interactive mathematical objects

---

## Phase 3 — Educational Content

- [ ] Real Analysis I
- [ ] Real Analysis II
- [ ] Complex Analysis
- [ ] Measure Theory and Integration
- [ ] Differential Equations

---

## Phase 4 — Authoring Environment

- [ ] Dedicated DELTA editor
- [ ] Live preview
- [ ] Project management tools
- [ ] Export utilities

---

## Phase 5 — Public Platform

- [ ] Content repository
- [ ] Search system
- [ ] Community contributions
- [ ] Open educational library

---

# Current Status

🚧 Active development.

The project is currently focused on integrating DELTA with interactive web technologies and defining the architecture required for the future Impateca platform.

---

# About

Impateca is being developed as part of an undergraduate extension initiative at IMPA Tech.

The project seeks to combine mathematical rigor, interactive visualization, and modern web technologies to create a new generation of educational resources for higher mathematics.