# Awesome LLM Knowledge Bases [![Awesome](https://awesome.re/badge.svg)](https://awesome.re) [![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md) [![CC0](https://img.shields.io/badge/license-CC0-blue.svg)](LICENSE)

> Andrej Karpathy's [viral post](https://x.com/karpathy/status/1907477278835749189) on LLM Knowledge Bases hit 1.7M views. This is the definitive resource list for the workflow he described.

> **"raw data from a given number of sources is collected, then compiled by an LLM into a .md wiki, then operated on by various CLIs by the LLM to do Q&A and to incrementally enhance the wiki, and all of it viewable in Obsidian. You rarely ever write or edit the wiki manually, it's the domain of the LLM."**
>
> — [Andrej Karpathy](https://x.com/karpathy/status/1907477278835749189), Apr 3, 2026

The workflow: **Ingest → Compile → Lint → View → Query → Enhance → Repeat.**

**Part of the [LLM KB Ecosystem](https://github.com/SingggggYee):** [karpathy-kb-template](https://github.com/SingggggYee/karpathy-kb-template) | [wiki-compiler](https://github.com/SingggggYee/wiki-compiler) | [kb-lint](https://github.com/SingggggYee/kb-lint)

---

## Contents

- [Data Ingestion](#data-ingestion)
- [Wiki Compilation](#wiki-compilation)
- [Knowledge Base Linting](#knowledge-base-linting)
- [Obsidian Plugins](#obsidian-plugins)
- [IDE & Viewers](#ide--viewers)
- [RAG & Search](#rag--search)
- [LLM Agents & Frameworks](#llm-agents--frameworks)
- [Visualization & Output](#visualization--output)
- [Synthetic Data & Fine-tuning](#synthetic-data--fine-tuning)
- [Workflows & Guides](#workflows--guides)
- [Similar Projects](#similar-projects)
- [Contributing](#contributing)

---

## Data Ingestion

Tools for converting web pages, PDFs, papers, and other sources into clean markdown.

- [Obsidian Web Clipper](https://obsidian.md/clipper) - Browser extension that clips web pages directly into your Obsidian vault as markdown.
- [Markdownload](https://github.com/deathau/markdownload) - Browser extension to convert web pages to markdown files.
- [Jina Reader](https://github.com/jina-ai/reader) - Converts any URL to LLM-friendly markdown via `r.jina.ai`. Handles JavaScript-rendered pages.
- [Docling](https://github.com/DS4SD/docling) - IBM's document conversion library. Parses PDFs, DOCX, PPTX, HTML to markdown with table and figure extraction.
- [Marker](https://github.com/VikParuchuri/marker) - Converts PDF, EPUB, and MOBI to markdown with high accuracy. Handles complex layouts, tables, and equations.
- [Trafilatura](https://github.com/adbar/trafilatura) - Python library for web scraping and text extraction. Focuses on main content extraction from web pages.
- [Pandoc](https://github.com/jgm/pandoc) - Universal document converter. Converts between dozens of formats including markdown, LaTeX, DOCX, and HTML.
- [pdf2md](https://github.com/jzillmann/pdf-to-markdown) - Converts PDF files to markdown, preserving structure and formatting.
- [Unstructured](https://github.com/Unstructured-IO/unstructured) - General-purpose document parsing library. Handles PDFs, images, HTML, Word docs, and more.
- [Firecrawl](https://github.com/mendableai/firecrawl) - Crawls websites and converts pages to clean markdown. Built for LLM consumption.
- [Crawl4AI](https://github.com/unclecode/crawl4ai) - Open-source LLM-friendly web crawler that outputs clean markdown with structured extraction.
- [MarkItDown](https://github.com/microsoft/markitdown) - Microsoft's Python tool for converting various file formats (PDF, DOCX, XLSX, PPTX, images, audio) to markdown.
- [Zerox](https://github.com/getomni-ai/zerox) - Zero-shot PDF OCR to markdown using vision models. Simple API for document extraction.
- [MinerU](https://github.com/opendatalab/MinerU) - High-quality document content extraction tool supporting PDF to markdown/JSON conversion.

## Wiki Compilation

LLM-powered tools that organize, compile, and structure knowledge into coherent wikis.

- **[wiki-compiler](https://github.com/SingggggYee/wiki-compiler)** - LLM-driven compiler that organizes raw markdown fragments into a structured, interlinked wiki.
- [LLM Knowledge Base](https://github.com/arturseo-geo/llm-knowledge-base) - A schema standard for LLM-compiled knowledge bases. Ships an AGENTS.md spec, file templates, a worked example (AI alignment), and a structured learning layer with spaced repetition and gap tracking.
- [Fabric](https://github.com/danielmiessler/fabric) - AI-powered framework for augmenting humans. Includes patterns for extracting and organizing knowledge.
- [Khoj](https://github.com/khoj-inc/khoj) - Personal AI assistant that indexes your markdown notes and documents for natural language interaction.
- [Quivr](https://github.com/QuivrHQ/quivr) - Personal productivity assistant that ingests documents and builds a searchable knowledge base.
- [Mem0](https://github.com/mem0ai/mem0) - Memory layer for AI applications. Persists and organizes knowledge across interactions.

## Knowledge Base Linting

Tools for checking consistency, finding gaps, and maintaining quality in markdown knowledge bases.

- **[kb-lint](https://github.com/SingggggYee/kb-lint)** - Linter for markdown knowledge bases. Detects broken links, orphan pages, inconsistent terminology, and coverage gaps.
- [Markdownlint](https://github.com/DavidAnson/markdownlint) - Style checker and linting tool for markdown files. Enforces consistent formatting.
- [markdown-link-check](https://github.com/tcort/markdown-link-check) - Checks all hyperlinks in markdown files for broken or dead links.
- [Obsidian Linter](https://github.com/platers/obsidian-linter) - Obsidian plugin that enforces consistent markdown formatting and style rules across your vault.
- [Vale](https://github.com/errata-ai/vale) - Prose linter that brings code-like linting to natural language. Supports custom style rules.

## Obsidian Plugins

Obsidian plugins that enhance the knowledge base workflow.

- [Obsidian Copilot](https://github.com/logancyang/obsidian-copilot) - AI assistant inside Obsidian. Chat with your notes, generate content, and get suggestions using multiple LLM providers.
- [Smart Connections](https://github.com/brianpetro/obsidian-smart-connections) - AI-powered note connections. Finds related notes using embeddings and enables chat with your vault.
- [Dataview](https://github.com/blacksmithgu/obsidian-dataview) - Query engine for your vault. Treat your notes as a database with inline queries and JavaScript API.
- [Marp Slides](https://github.com/samuele-cozzi/obsidian-marp-slides) - Create presentation slides from markdown notes using the Marp framework.
- [Templater](https://github.com/SilentVoid13/Templater) - Advanced template engine for Obsidian. Create dynamic templates with JavaScript execution.
- [Obsidian Git](https://github.com/Vinzent03/obsidian-git) - Automatic backup and version control for your vault using Git.
- [Local GPT](https://github.com/pfrankov/obsidian-local-gpt) - Run local LLMs directly within Obsidian for private AI-assisted note-taking.
- [Text Generator](https://github.com/nhaouari/obsidian-textgenerator-plugin) - AI text generation plugin supporting multiple providers. Generates, rewrites, and summarizes within notes.
- [Canvas](https://obsidian.md/canvas) - Built-in infinite canvas for visual knowledge mapping and spatial organization of notes.

## IDE & Viewers

Applications for viewing, editing, and navigating markdown knowledge bases.

- [Obsidian](https://obsidian.md) - The gold standard for local-first markdown knowledge bases. Graph view, backlinks, plugins ecosystem.
- [Logseq](https://github.com/logseq/logseq) - Open-source outliner-style knowledge base with bidirectional linking and graph visualization.
- [Notion](https://notion.so) - All-in-one workspace with databases, wikis, and AI features. Cloud-based.
- [Foam](https://github.com/foambubble/foam) - Personal knowledge management and sharing system built on VS Code and markdown.
- [Dendron](https://github.com/dendronhq/dendron) - Developer-focused knowledge management tool built on VS Code. Hierarchical note organization.
- [SiYuan](https://github.com/siyuan-note/siyuan) - Privacy-first personal knowledge management system with block-level references and sync.
- [Zettlr](https://github.com/Zettlr/Zettlr) - Markdown editor designed for academic writing and Zettelkasten-style note-taking.
- [Marktext](https://github.com/marktext/marktext) - Simple and elegant open-source markdown editor with real-time preview.

## RAG & Search

Retrieval-Augmented Generation frameworks and local search engines for querying knowledge bases.

- [LlamaIndex](https://github.com/run-llama/llama_index) - Data framework for connecting custom data sources to LLMs. Indexing, retrieval, and query engines.
- [LangChain](https://github.com/langchain-ai/langchain) - Framework for developing LLM-powered applications with chains, agents, and retrieval.
- [Haystack](https://github.com/deepset-ai/haystack) - End-to-end NLP framework for building RAG pipelines, search systems, and question answering.
- [RAGFlow](https://github.com/infiniflow/ragflow) - Open-source RAG engine with deep document understanding and chunk-level citation.
- [Chroma](https://github.com/chroma-core/chroma) - Open-source embedding database. Simple API for storing and querying document embeddings.
- [Qdrant](https://github.com/qdrant/qdrant) - High-performance vector similarity search engine with filtering and payload support.
- [Milvus](https://github.com/milvus-io/milvus) - Cloud-native vector database for scalable similarity search and AI applications.
- [txtai](https://github.com/neuml/txtai) - All-in-one embeddings database for semantic search, LLM orchestration, and language model workflows.
- [Vanna](https://github.com/vanna-ai/vanna) - RAG framework for SQL generation. Train on your database schema and documentation.

## LLM Agents & Frameworks

AI coding agents and frameworks for operating on knowledge bases via CLI.

- [Claude Code](https://docs.anthropic.com/en/docs/claude-code) - Anthropic's agentic CLI for Claude. Operates on files, runs commands, and iterates on codebases and knowledge bases.
- [Cursor](https://cursor.com) - AI code editor with deep codebase understanding. Chat, edit, and generate across files.
- [Aider](https://github.com/Aider-AI/aider) - AI pair programming in your terminal. Works with local Git repos and supports multiple LLM providers.
- [OpenAI Codex CLI](https://github.com/openai/codex) - OpenAI's lightweight coding agent that runs in the terminal with sandboxed execution.
- [Continue](https://github.com/continuedev/continue) - Open-source AI code assistant for VS Code and JetBrains. Supports multiple models.
- [Open Interpreter](https://github.com/OpenInterpreter/open-interpreter) - Natural language interface for your computer. Runs code locally to complete tasks.
- [CrewAI](https://github.com/crewAIInc/crewAI) - Framework for orchestrating role-playing AI agents that collaborate on complex tasks.
- [AutoGen](https://github.com/microsoft/autogen) - Microsoft's framework for building multi-agent conversational AI systems.
- [Pydantic AI](https://github.com/pydantic/pydantic-ai) - Agent framework built on Pydantic for type-safe, structured AI application development.

## Visualization & Output

Tools for turning knowledge base content into presentations, diagrams, and visual outputs.

- [Marp](https://github.com/marp-team/marp) - Markdown presentation ecosystem. Convert markdown files to slides, PDFs, and HTML presentations.
- [Mermaid](https://github.com/mermaid-js/mermaid) - Generate diagrams and flowcharts from markdown-like text. Supported natively in GitHub markdown.
- [D3.js](https://github.com/d3/d3) - JavaScript library for data-driven visualizations. Create interactive charts and graphs from knowledge base data.
- [Markmap](https://github.com/markmap/markmap) - Visualize markdown documents as interactive mind maps.
- [Matplotlib](https://github.com/matplotlib/matplotlib) - Python plotting library for generating charts, graphs, and figures from data.
- [Excalidraw](https://github.com/excalidraw/excalidraw) - Virtual whiteboard for sketching hand-drawn-style diagrams. Has an Obsidian integration.
- [Slidev](https://github.com/slidevjs/slidev) - Presentation slides for developers using markdown and Vue components.
- [reveal.js](https://github.com/hakimel/reveal.js) - HTML presentation framework with markdown support and a rich plugin ecosystem.

## Synthetic Data & Fine-tuning

Tools for distilling knowledge bases into training data and fine-tuned model weights.

- [Distilabel](https://github.com/argilla-io/distilabel) - Framework for synthetic data generation and AI feedback. Create training datasets from knowledge bases.
- [Axolotl](https://github.com/axolotl-ai-cloud/axolotl) - Streamlined fine-tuning tool supporting multiple architectures. LoRA, QLoRA, full fine-tuning.
- [Unsloth](https://github.com/unslothai/unsloth) - Fast LLM fine-tuning with 2x speed and 60% less memory. Supports Llama, Mistral, and more.
- [LitGPT](https://github.com/Lightning-AI/litgpt) - Hackable implementation of open-source LLMs for pretraining, fine-tuning, and deployment.
- [MLX](https://github.com/ml-explore/mlx) - Apple's array framework for machine learning on Apple silicon. Efficient local fine-tuning.
- [Argilla](https://github.com/argilla-io/argilla) - Collaboration platform for AI engineers and domain experts to build high-quality datasets.

## Workflows & Guides

Blog posts, tutorials, and videos about building LLM knowledge bases.

- [Karpathy's Tweet Thread (Apr 2026)](https://x.com/karpathy/status/1907477278835749189) - The viral thread that crystallized the raw data → LLM → wiki → CLI workflow.
- [Building a Second Brain (Tiago Forte)](https://www.buildingasecondbrain.com) - The original methodology for personal knowledge management that inspired many tools in this list.
- [Zettelkasten Method](https://zettelkasten.de/introduction/) - The atomic note-taking method. Foundation for tools like Obsidian and Logseq.
- [Obsidian Hub](https://publish.obsidian.md/hub) - Community-maintained documentation, guides, and resources for Obsidian workflows.
- [LlamaIndex Documentation](https://docs.llamaindex.ai) - Comprehensive guides on building RAG pipelines over document collections.
- [Simon Willison's Blog](https://simonwillison.net) - Prolific coverage of LLM tools, workflows, and practical AI engineering.

## Similar Projects

Existing knowledge base, second brain, and personal wiki projects.

- [Awesome Knowledge Management](https://github.com/brettkromkamp/awesome-knowledge-management) - Curated list of knowledge management tools and resources.
- [Awesome Obsidian](https://github.com/kmaasrud/awesome-obsidian) - Curated list of Obsidian resources, plugins, and themes.
- [Second Brain](https://github.com/KasperZuttworthy/Second-Brain) - Resources and tools for building a digital second brain.
- [Awesome Zettelkasten](https://github.com/fzslm/awesome-zettelkasten) - Curated list of Zettelkasten tools, guides, and resources.
- [Project Memex](https://en.wikipedia.org/wiki/Memex) - Vannevar Bush's 1945 vision of a personal knowledge device — the ancestor of this entire space.

---

## Contributing

Contributions welcome! Please read the [contributing guidelines](CONTRIBUTING.md) first.

---

## License

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)

To the extent possible under law, the authors have waived all copyright and related or neighboring rights to this work.
