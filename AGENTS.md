# AGENTS.md - AWS AI Certification Study Guide

## Project Overview

This is a MkDocs-based documentation project containing AWS AI/ML certification study materials. The project uses Material theme and is written in Portuguese (Brazil).

---

## Build Commands

### Development Server
```bash
cd /home/william/Documentos/certificates_study_guide/certificacoes/AI
mkdocs serve
```
Runs live-reloading server at http://localhost:8000

### Build for Production
```bash
cd /home/william/Documentos/certificates_study_guide/certificacoes/AI
mkdocs build
```
Output goes to `/site` directory (gitignored)

### Deploy to GitHub Pages
```bash
cd /home/william/Documentos/certificates_study_guide/certificacoes/AI
mkdocs gh-deploy
```

---

## Linting

### Markdown Lint
```bash
# Check markdown files for issues
markdownlint "**/*.md"
```

### Link Validation
```bash
# Validate internal links
mkdocs build --strict
```

### Spelling Check (optional)
```bash
# Install and run spell checker
pip install pyspelling
pyspelling
```

---

## Project Structure

```
certificacoes/AI/
├── docs/
│   ├── Dominios/           # Study domain chapters (1-7)
│   │   ├── 1.Fundamentals_IA_Machine_Learning.md
│   │   ├── 2.Fundamentos de ia generativa.md
│   │   ├── 3.Prompt Enginnering.md
│   │   ├── 4.Responsibilities_AI.md
│   │   ├── 5.Aplicacao de Modelos de fundacao.md
│   │   ├── 6.Seguranca_Governanca.md
│   │   └── 7.todos_os_servicos.md
│   ├── Servicos/
│   │   └── sagemaker.md
│   ├── resumo.md           # Main summary
│   └── meu_resumo.md       # Personal notes
├── .agents/
│   └── workflows/
│       └── aistudy.md      # Agent workflow instructions
├── .venv/                  # Virtual environment
└── mkdocs.yml             # MkDocs configuration
```

---

## Code Style Guidelines

### Markdown Formatting

1. **Headers**: Use ATX-style headers (`#`, `##`, `###`)
   ```markdown
   # Main Title
   ## Section
   ### Subsection
   ```

2. **Tables**: Use semantic alignment (`:` for alignment markers)
   ```markdown
   | Column 1 | Column 2 |
   | :--- | :--- |
   | Content | Content |
   ```

3. **Lists**: Use `-` for unordered, `1.` for ordered
   ```markdown
   - Item
   - Item
     - Nested item
   ```

4. **Code blocks**: Use fenced code blocks with language
   ```markdown
   ```python
   def example():
       pass
   ```
   ```

### Admonitions (MkDocs-specific)

Use Material theme admonitions for callouts:

```markdown
!!! note
    Informative content

!!! tip
    Helpful advice

!!! important
    Critical information

!!! warning
    Cautionary notice
```

### File Naming

- Domain files: `N.Topic_Name.md` (e.g., `1.Fundamentals_IA_Machine_Learning.md`)
- Service files: `servicename.md` (e.g., `sagemaker.md`)
- Use lowercase with underscores for general files

### Content Organization

1. **Tables first**: Lead with comparison/definition tables
2. **Tips in admonitions**: Use `!!! tip` for exam strategies
3. **Visual hierarchy**: Use emojis sparingly for quick scanning
4. **Portuguese with English terms**: Keep English technical terms, Portuguese explanations

### Writing Style

- Use clear, concise Portuguese
- Include practical examples
- Add exam tips with `!!! tip` callouts
- Structure for quick review (tables, lists)
- Reference AWS services accurately

### Links

- Use relative links for internal docs
- Use absolute URLs for external AWS documentation
- Link format: `[link text](path/to/file.md)` for internal

---

## Existing Agent Instructions

From `.agents/workflows/aistudy.md`:
> **Always format**: Format text in MkDocs mode according to project standards.

---

## Common Tasks

### Adding New Domain
1. Create file in `docs/Dominios/N.Name.md`
2. Update `mkdocs.yml` navigation section

### Adding New Service
1. Create file in `docs/Servicos/servicename.md`
2. Add to nav in `mkdocs.yml`

### Testing Changes
```bash
mkdocs serve --dev-addr=127.0.0.1:8000
```
View at http://localhost:8000

---

## Dependencies

- mkdocs
- mkdocs-material
- Python 3.x

Install with:
```bash
pip install mkdocs mkdocs-material
```
