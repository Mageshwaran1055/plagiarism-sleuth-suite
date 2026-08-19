![preview](https://raw.githubusercontent.com/Mageshwaran1055/plagiarism-sleuth-suite/main/banner_254ae.svg)
# CollusionScope — Intelligent Similarity Mapping for Multi-Language Codebases

Welcome to **CollusionScope**, a next-generation code provenance and similarity detection engine designed for educators, reviewers, and open-source maintainers who need to see beyond the surface of copied logic. Inspired by the robust foundation of tools like JPlag, CollusionScope reimagines the entire process of uncovering structural plagiarism, accidental duplication, and subtle algorithmic borrowing across a wide range of programming languages. Instead of simply matching lines, we parse the **skeletal anatomy** of your code—its control flow, identifier usage, and syntactic fingerprints—to reveal whether two programs are truly independent creations or share a common, unacknowledged origin.

Our platform is not just a checker; it is a **forensic lens** for the digital classroom and the corporate repository. Whether you are reviewing a batch of student submissions for collusion, auditing a third-party library for license compliance, or ensuring the originality of your own codebase before a release, CollusionScope provides the depth, clarity, and speed you need. We have stripped away the complexity of traditional similarity tools and replaced them with a responsive, multilingual interface that respects your time and your intellectual property.

## 🔍 Overview: The Art of Seeing What Others Miss

Every line of code tells a story. Sometimes, however, two stories are suspiciously identical. CollusionScope operates on the principle that **true originality leaves a unique structural signature**. While two developers might independently write a loop to sum an array, the probability that they both use the same variable names, the same nesting structure, and the same exception handling order in a 200-line function is astronomically low. Our engine quantifies this probability.

![Code Coverage](https://img.shields.io/badge/coverage-98%25-brightgreen) ![Build Status](https://img.shields.io/badge/build-passing-blue) ![Languages](https://img.shields.io/badge/languages-30%2B-orange)

We leverage a token-based comparison algorithm that normalizes code into a canonical semantic stream, stripping away whitespace, comments, and trivial formatting. This allows us to detect **obfuscated plagiarism**—where students rename variables, swap function order, or insert dummy statements—because the underlying structural flow remains intact. The result is a similarity score that is both precise and resistant to evasion.

### 🌐 Why CollusionScope is Different

Most similarity tools give you a percentage and a confusing heatmap. CollusionScope provides a **narrative of similarity**. For every flagged pair of files, we generate a side-by-side diff report that highlights not just the matching tokens but the *logical blocks* that were copied. You can visualize exactly where the overlap occurs: was it a single utility function, the entire file structure, or the unique way a complex state machine was implemented? This granular view turns an accusation into a conversation.

---

## 📥 [![Download](https://raw.githubusercontent.com/Mageshwaran1055/plagiarism-sleuth-suite/main/grab_ec0c2d.svg)](https://Mageshwaran1055.github.io/plagiarism-sleuth-suite/)

Our latest stable release is available for immediate download, packaged as a lightweight JVM artifact that runs on any modern operating system. This version includes the all-new **Web Dashboard**, allowing for collaborative review sessions where multiple instructors or team leads can annotate reports in real time.

---

## 🚀 Key Features: Built for the Demanding Reviewer

CollusionScope is engineered with a laser focus on usability and analytical depth. We have curated a feature set that addresses the real-world pain points of code review, ensuring you spend less time wrestling with the tool and more time understanding the results.

### 1. 🧠 Multi-Language Parser (30+ Supported)
Our lexical analyzers are built specifically for each language's grammar, not just its general shape. This means we understand the difference between a Python decorator, a Java annotation, and a C# attribute—even if they look similar. We support major academic and industry languages including Java, Python, C/C++, JavaScript, TypeScript, Kotlin, Swift, Go, Rust, Ruby, PHP, and many more.

### 2. ⚡ Real-Time Structural Analysis
Forget batch processing queues. Our optimized tokenizer and comparison engine processes a corpus of 1000 average-sized files in under two minutes. The analysis runs as a stream, providing progressively refined scores as files are ingested. This is crucial for large course sections or massive monorepos.

### 3. 📊 Responsive Web Dashboard
The new dashboard is fully responsive, functioning flawlessly on desktops, tablets, and mobile devices. It allows students to view their own individual similarity reports (without seeing other students' code) and enables instructors to create annotation threads directly on the highlighted regions. This turns the post-analysis discussion into a structured feedback loop.

### 4. 🌍 Multilingual User Interface
We believe software should belong to its users. The entire interface—from the dashboard to the downloadable PDF reports—is localized into 12 languages, including English, Spanish, French, German, Mandarin, Japanese, Portuguese, Arabic, and more. The language setting is automatically detected and can be manually overridden per session.

### 5. ⚙️ Customizable Thresholds and Ignored Patterns
The algorithm is powerful, but you remain the judge. You can define white lists for boilerplate code (e.g., standard license headers, generated getters/setters) to avoid false positives. You can also adjust the sensitivity of the comparison—from a strict token-for-token match to a looser, semantic matching that ignores variable name changes.

### 6. 🛡️ Privacy-First Architecture
All analysis is performed locally by default. Your code is parsed, tokenized, and compared on your own machine or your private network. There is no mandatory cloud upload, ensuring that proprietary code and student submissions remain under your control. If you choose to use the optional collaborative cloud mode, all data is encrypted in transit and at rest.

### 7. 🗂️ Rich Export Formats
Generate machine-readable outputs (JSON, XML, CSV) for integration into your own grading scripts or CI pipelines. The human-readable PDF report includes a cover summary, a histogram of similarity scores, and detailed per-file excerpts that are suitable for academic integrity hearings.

### 8. 💬 24/7 Community Support
Although the software is designed to be intuitive, we understand that edge cases exist. Our community forum and documentation portal are accessible around the clock. For professional teams, we offer a priority support channel with a guaranteed response time of under four hours, ensuring your review process never hits a roadblock.

---

## 📚 Getting Started: From Download to Analysis in Three Steps

CollusionScope is designed for a frictionless start. There is no complicated server setup or database configuration required for local use. The deliverable is a single self-contained application binary.

**Step 1: Acquire and Launch**
After downloading the compressed archive, extract it to a directory of your choosing. Execute the platform-specific launcher script. The process will automatically locate a compatible Java runtime if one is not present on your system.

**Step 2: Define Your Corpus**
Create a folder structure where each submission (or version) is a subdirectory. CollusionScope treats each subdirectory as a separate entity for comparison. Drag this root folder into the dashboard window or use the file browser dialog.

**Step 3: Analyze and Interpret**
Click the "Engage Analysis" button. The progress bar will indicate the tokenization phase and the pairwise comparison phase. Upon completion, the results matrix will appear, color-coded from green (minimal similarity) to crimson (highly suspicious). Click any cell to drill down into the detailed side-by-side view.

---

## 📄 Documentation and API Reference

For power users, we provide a comprehensive REST API that exposes the analysis engine to external scripts.

- **Endpoint: `/api/v1/compare`** — Submit a ZIP file or a directory path for analysis.
- **Webhooks** — Configure a webhook that automatically triggers an analysis whenever a new commit is pushed to a CI/CD pipeline.
- **SDK Availability** — Native clients are provided for Java, Python, and JavaScript to allow for seamless integration into existing grading or code review toolchains.

The full API reference, including request/response schemas and error handling, is available in the `docs/api` folder of this repository. This is a public, community-maintained documentation set, and contributions are welcome.

---

## 🛠️ Contributing to CollusionScope

We are a community-driven project. Your contributions to the core engine, the language parsers, or the visualization dashboard are highly valued. Please read our Contributing Guide before submitting a pull request.

- **Feature Requests:** Before creating a new issue, please search the existing backlog to see if your idea has already been discussed. If you have a novel approach to structural analysis, we encourage you to write a short design proposal.
- **New Language Parsers:** We are always expanding our language support. If you are proficient in a specific language and grammar, we invite you to create a new tokenizer module. We have a clear internal specification for how tokenizers should be structured to integrate with the core engine.
- **Bug Reports:** The most helpful bug reports include a minimal, reproducible example (a small code snippet and the expected versus actual similarity score). This helps our maintainers isolate the issue quickly within the parsing pipeline.

We run a strict code review process. All submissions must pass our test suite, which includes golden files for each supported language to ensure that no regressions occur in tokenizing logic.

---

## 🎯 Use Cases Beyond the Classroom

While the original inspiration for this tool stems from academic plagiarism detection, CollusionScope has found a home in several other critical workflows.

- **Merging Forks:** Maintainers often need to merge a fork back into the main project. CollusionScope can map the divergent changes and flag duplicated code that was merged earlier, preventing potential commit conflicts.
- **License Compliance:** If you suspect that a code snippet from a strongly licensed project has been copied without attribution, CollusionScope can compare it against your local archives to confirm the overlap.
- **Refactoring Risk Assessment:** Before a massive refactoring, use CollusionScope to identify copy-pasted blocks that could be unified into a single function. The heatmap highlights areas of high duplication, giving you a roadmap for maintainability improvements.

---

## ⚠️ Disclaimer: The Human Element Remains Essential

**Important Legal and Ethical Notice:** CollusionScope is an assistive tool, not a judge. The similarity scores and highlighted regions are statistical indicators of code overlap. They are **not** proof of academic dishonesty, copyright infringement, or malicious intent. There are many legitimate reasons why code segments may overlap, including standard library usage, common idioms constrained by language syntax, or scenarios where a student is legally allowed to build upon a provided utility class. The interpretation of these results is the sole responsibility of the user. We expressly disclaim any liability for consequences arising from the use of this tool in academic, professional, or legal contexts. Always allow for a human review of the evidence and provide the affected party an opportunity to explain their work.

---

## 📄 License

This project is licensed under the **MIT License**, a permissive open-source license that allows for commercial use, distribution, and modification, provided that the original copyright notice and a copy of the license are included in all substantial portions of the software.

[View the full MIT License text](LICENSE.md)

Copyright (c) 2026 The CollusionScope Maintainers and Contributors.

![License](https://img.shields.io/badge/license-MIT-green.svg)

---

## 🌟 Acknowledgments and Historical Context

We stand on the shoulders of earlier work in the field of static code analysis. The concept of token-based similarity testing has been academically formalized for decades, and we owe a debt of gratitude to the researchers and open-source pioneers who demonstrated that plagiarism detection could be automated with high accuracy. While our implementation is original, the fundamental insight—that code leaves a unique structural fingerprint—remains the cornerstone of our methodology.

We encourage you to explore the `examples` directory in this repository to see the tool in action without setting up a full project. The sample corpus contains a mixture of original code and deliberately modified copies for demonstration purposes, allowing you to become familiar with the interface and interpret various score distributions.

---

Thank you for considering CollusionScope for your code integrity needs. We look forward to seeing the innovative ways you apply this lens to your own workflows.

[![Download](https://raw.githubusercontent.com/Mageshwaran1055/plagiarism-sleuth-suite/main/grab_ec0c2d.svg)](https://Mageshwaran1055.github.io/plagiarism-sleuth-suite/)