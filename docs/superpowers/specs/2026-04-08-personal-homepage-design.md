# Personal Homepage Design

**Date:** 2026-04-08

## Goal

Convert the default `academicpages` template into a personal academic homepage for Zongxian Yang with a long-form landing page and a reduced navigation focused on the content that is currently relevant.

## Target Audience

- Faculty members and potential collaborators
- PhD application and academic network visitors
- Peers who want a quick view of research interests and selected work
- General visitors looking for a more personal view beyond publications

## Information Architecture

The site keeps only five top-level pages in the main navigation:

- `Home`
- `Publications`
- `Blog Posts`
- `CV`
- `Other Information`

The following default template pages are removed from the main navigation and treated as non-primary content:

- `Talks`
- `Teaching`
- `Portfolio`
- `Guide`

## Home Page Design

The home page uses a long-form structure and becomes the main narrative entry point for the site.

### Section 1: Intro

Show the name, current role, affiliation, near-term academic transition, and a concise academic biography in English.

### Section 2: Research Interests

List the user's long-term and current research interests in a compact, scannable format. These should emphasize:

- LLM reasoning
- Trustworthy and verifiable medical AI
- Medical agents and clinical workflow abstraction
- Multimodal and VLM reasoning
- Reflection, self-correction, and synthetic data

### Section 3: Selected Research / Projects

Feature the most representative works with short summaries, role, method keywords, and links when available. Priority items:

- `Med-REFL`
- `QM-ToT`
- `Better Eyes, Better Thoughts`
- One additional representative project or thesis if useful

### Section 4: News / Updates

Display a short reverse-chronological list of recent milestones such as accepted papers, submitted work, lab transitions, and the PhD start.

### Section 5: Quick Links

Provide direct links to:

- Publications
- CV
- Google Scholar
- GitHub

## Publications Page

Keep the template's publications archive model, but replace sample content with the user's real papers and preprints. The page should reflect the current stage of the user's publication record rather than template demo entries.

## Blog Posts Page

Keep a blog page in navigation. The structure remains available even if the content starts minimal. This page is intended for research notes, reading notes, and project write-ups.

## CV Page

Rewrite the CV page as a structured academic CV with sections for:

- Education
- Positions and research experience
- Publications and manuscripts
- Selected projects
- Honors or notable outcomes if appropriate
- Skills and methods

## Other Information Page

This page mixes academic-adjacent and personal content. It contains two subsections:

### Interesting Work

Curate a short list of papers, labs, researchers, projects, or personal websites that the user finds inspiring or worth following.

### Life

Include lightweight personal content such as daily-life photos, hobbies, or short informal notes.

## Content Principles

- Keep the tone academic, clear, and concise
- Use English for the public-facing website unless a small Chinese note is specifically useful
- Avoid placeholder template text on public pages
- Prefer real content over empty sections
- Allow the site to grow incrementally without exposing irrelevant template features

## Repository Impact

The implementation should primarily update:

- `_config.yml`
- `_data/navigation.yml`
- `_pages/about.md`
- `_pages/cv.md`
- `_pages/year-archive.html` or related blog-facing content if needed
- a new `_pages/other-information.md`
- `_publications/*`
- `_posts/*` as needed

## Non-Goals

- Building talk or teaching sections now
- Preserving template tutorial content in the primary navigation
- Introducing a custom visual redesign beyond the existing theme structure
