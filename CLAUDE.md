# Homara Brain

## What this repo is

An **Obsidian vault** — not a codebase. Strategic, operational, SEO, content, and product knowledge for **Homara**, a home & garden affiliate comparison site (Amazon + Awin). Treat it as organisational memory.

The actual application lives in the sibling repo `/Users/martiwarda/Projects/homara/homara-web` (React + Vite + TypeScript + Supabase). Strategy decisions captured here in `02-Estrategia/` and `05-Producto/` may need to be reflected back to that codebase.

## Vault structure

- `00-Sistema` — vault governance: naming conventions, tagging, MOC index.
- `01-Empresa` — vision, mission, brand identity, business model.
- `02-Estrategia` — OKRs, KPIs, roadmap, risks, quarterly planning.
- `03-SEO` — keyword research, content architecture, technical SEO, interlinking.
- `04-Contenido` — editorial pipeline, calendar, briefs, style guide.
- `05-Producto` — tech stack decisions, Supabase schema, analytics, admin panel.
- `06-Monetizacion` — affiliate programs (Amazon, Awin), tracking, future services.
- `07-Categorias` — product categories (Cocina, Hogar, Jardín, Muebles, Terraza), seasonality.
- `08-Operaciones` — workflows, QA, content maintenance.
- `09-Crecimiento` — experiments, hypotheses, growth roadmap, internationalisation.
- `10-Mercado` — competitive analysis, buyer personas, market trends.
- `_Plantillas` — reusable templates (`Plantilla-Decision`, `Plantilla-Articulo`, `Plantilla-Brief-IA`, `Plantilla-Experimento`, …).
- `_Diario` — daily logs.
- `_Adjuntos` — attachments.
- `Inicio.md` — root MOC. Each numbered area also has its own `_MOC-*.md` hub.

## Conventions

- **Wikilinks first.** Reference notes via `[[Note name]]`, not file paths. When pointing the user at content, prefer the wikilink form.
- **Tags.** `#area/<area>`, `#tipo/<type>`, `#estado/<status>`, `#prio/<priority>`. Keep tags consistent with what's already in use — search before inventing new ones.
- **Status values.** `estado: vigente` (current, authoritative) vs `estado: borrador` (draft, in progress).
- **Templates.** New notes that fit a known shape should start from `_Plantillas/Plantilla-*.md`. Don't invent a structure if a template already exists.
- **Language.** Vault content is in **Spanish** — match the existing tone and vocabulary when editing notes. `.claude/` infrastructure and this file stay in English.

## Workflows

Two skills govern this repo. Both auto-trigger when their description matches.

- **`ship`** — branch-per-turn workflow. Phase A (branch + commit + push) runs automatically when you edit any tracked file. Phase B (PR + squash-merge to `main`) only runs after the user says "ship it" or equivalent. **Never push to `main` directly.**
- **`brain-autofetch`** — a `UserPromptSubmit` hook fast-forwards `main` from `origin` before each prompt. If the user asks "is the brain up to date?" or wants to disable it, see that skill.

## Don'ts

- Don't run code-style commands (`npm …`, `pytest`, build/lint/test). This is a docs vault; there's nothing to build.
- Don't invent file paths. Search wikilinks and MOCs first; if you can't find a target, ask.
- Don't bypass `ship` — no direct commits on `main`, no `git add -A`, no `--no-verify`.
- Don't translate vault content to English unilaterally. Keep Spanish unless the user explicitly asks otherwise.
