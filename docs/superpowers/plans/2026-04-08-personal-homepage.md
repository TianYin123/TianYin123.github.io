# Personal Homepage Implementation Plan

> **For agentic workers:** REQUIRED: Use superpowers:subagent-driven-development (if subagents available) or superpowers:executing-plans to implement this plan. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Replace the default Academic Pages demo content with a real personal homepage for Zongxian Yang centered on a long-form home page and a five-item navigation.

**Architecture:** Reuse the existing Academic Pages structure instead of redesigning the site. Update site-wide metadata in `_config.yml`, reduce navigation in `_data/navigation.yml`, rewrite the primary page content in `_pages`, and replace example collection items with real publications and minimal starter blog content.

**Tech Stack:** Jekyll, Academic Pages, Markdown, YAML

---

## Chunk 1: Site Shell And Navigation

### Task 1: Update global site metadata

**Files:**
- Modify: `_config.yml`
- Test: local Jekyll build output

- [ ] **Step 1: Write the failing test**

Use content assertions as the test target by identifying current placeholder values that must disappear from generated pages, such as `Your Name`, `Your Sidebar Name`, and the default repository URL.

- [ ] **Step 2: Run test to verify it fails**

Run: `bundle exec jekyll build`
Expected: existing output still contains default placeholder-driven content before edits

- [ ] **Step 3: Write minimal implementation**

Replace placeholder site title, description, repository, author profile fields, and academic/social links with the user's real information.

- [ ] **Step 4: Run test to verify it passes**

Run: `bundle exec jekyll build`
Expected: build succeeds and generated pages reflect the new metadata

- [ ] **Step 5: Commit**

```bash
git add _config.yml
git commit -m "feat: personalize site metadata"
```

### Task 2: Reduce top navigation to the approved five pages

**Files:**
- Modify: `_data/navigation.yml`
- Test: local Jekyll build output

- [ ] **Step 1: Write the failing test**

Use the current navigation entries as the failing baseline by confirming that `Talks`, `Teaching`, `Portfolio`, and `Guide` are still present.

- [ ] **Step 2: Run test to verify it fails**

Run: `bundle exec jekyll build`
Expected: navigation still exposes template-first menu items

- [ ] **Step 3: Write minimal implementation**

Keep only `Home`, `Publications`, `Blog Posts`, `CV`, and `Other Information` in the header navigation.

- [ ] **Step 4: Run test to verify it passes**

Run: `bundle exec jekyll build`
Expected: navigation renders only the approved pages

- [ ] **Step 5: Commit**

```bash
git add _data/navigation.yml
git commit -m "feat: simplify homepage navigation"
```

## Chunk 2: Primary Pages

### Task 3: Rewrite the home page as a long-form academic landing page

**Files:**
- Modify: `_pages/about.md`
- Test: local Jekyll build output for `/`

- [ ] **Step 1: Write the failing test**

Use the current page body as the failing baseline because it still describes the Academic Pages template rather than the user.

- [ ] **Step 2: Run test to verify it fails**

Run: `bundle exec jekyll build`
Expected: home page still contains template introduction text

- [ ] **Step 3: Write minimal implementation**

Replace the template copy with the approved sections:
- intro
- research interests
- selected research/projects
- news/updates
- quick links

- [ ] **Step 4: Run test to verify it passes**

Run: `bundle exec jekyll build`
Expected: home page builds cleanly with the new long-form content

- [ ] **Step 5: Commit**

```bash
git add _pages/about.md
git commit -m "feat: rewrite homepage content"
```

### Task 4: Rewrite the CV page

**Files:**
- Modify: `_pages/cv.md`
- Test: local Jekyll build output for `/cv/`

- [ ] **Step 1: Write the failing test**

Use the default sample education and work experience entries as the failing baseline.

- [ ] **Step 2: Run test to verify it fails**

Run: `bundle exec jekyll build`
Expected: CV page still contains sample GitHub University entries

- [ ] **Step 3: Write minimal implementation**

Replace sample CV content with the user's education, research positions, publications summary, selected projects, and methods/skills.

- [ ] **Step 4: Run test to verify it passes**

Run: `bundle exec jekyll build`
Expected: CV page renders only personalized content

- [ ] **Step 5: Commit**

```bash
git add _pages/cv.md
git commit -m "feat: add academic cv page"
```

### Task 5: Add the Other Information page

**Files:**
- Create: `_pages/other-information.md`
- Test: local Jekyll build output for `/other-information/`

- [ ] **Step 1: Write the failing test**

Use the absence of the page as the failing baseline.

- [ ] **Step 2: Run test to verify it fails**

Run: `bundle exec jekyll build`
Expected: no `Other Information` destination page exists yet

- [ ] **Step 3: Write minimal implementation**

Create a page with two sections:
- interesting work
- life

- [ ] **Step 4: Run test to verify it passes**

Run: `bundle exec jekyll build`
Expected: the new page is generated and linked from the main navigation

- [ ] **Step 5: Commit**

```bash
git add _pages/other-information.md
git commit -m "feat: add other information page"
```

## Chunk 3: Content Collections

### Task 6: Replace sample publications with real publication entries

**Files:**
- Modify or replace: `_publications/*`
- Test: local Jekyll build output for `/publications/`

- [ ] **Step 1: Write the failing test**

Use the current sample publication titles and placeholder citations as the failing baseline.

- [ ] **Step 2: Run test to verify it fails**

Run: `bundle exec jekyll build`
Expected: publications page still shows fake sample papers

- [ ] **Step 3: Write minimal implementation**

Remove or overwrite sample entries and add the user's actual papers, preprints, and manuscript statuses with correct titles, dates, venues, and links where available.

- [ ] **Step 4: Run test to verify it passes**

Run: `bundle exec jekyll build`
Expected: publications page lists only the user's real records

- [ ] **Step 5: Commit**

```bash
git add _publications
git commit -m "feat: add real publications"
```

### Task 7: Clean up demo blog content and add a minimal starter post strategy

**Files:**
- Modify or replace: `_posts/*`
- Test: local Jekyll build output for `/year-archive/`

- [ ] **Step 1: Write the failing test**

Use the current demo post titles and repeated lorem ipsum text as the failing baseline.

- [ ] **Step 2: Run test to verify it fails**

Run: `bundle exec jekyll build`
Expected: blog archive still shows template demo posts

- [ ] **Step 3: Write minimal implementation**

Remove demo posts and keep either:
- no posts with a clean empty-state strategy, or
- one small real introductory post

- [ ] **Step 4: Run test to verify it passes**

Run: `bundle exec jekyll build`
Expected: blog archive no longer shows sample entries and remains valid

- [ ] **Step 5: Commit**

```bash
git add _posts _pages/year-archive.html
git commit -m "feat: personalize blog archive"
```

## Chunk 4: Verification

### Task 8: Verify the personalized site end-to-end

**Files:**
- Verify: `_config.yml`
- Verify: `_data/navigation.yml`
- Verify: `_pages/about.md`
- Verify: `_pages/cv.md`
- Verify: `_pages/other-information.md`
- Verify: `_publications/*`
- Verify: `_posts/*`

- [ ] **Step 1: Write the failing test**

Define acceptance criteria:
- no obvious template placeholder text
- approved navigation only
- personalized homepage and CV
- real publications
- valid Other Information page

- [ ] **Step 2: Run test to verify it fails**

Run: `bundle exec jekyll build`
Expected: before full implementation, at least one acceptance criterion is unmet

- [ ] **Step 3: Write minimal implementation**

Finish remaining content cleanup and fix any broken links, front matter, or formatting issues.

- [ ] **Step 4: Run test to verify it passes**

Run: `bundle exec jekyll build`
Expected: build completes successfully and acceptance criteria are met

- [ ] **Step 5: Commit**

```bash
git add _config.yml _data/navigation.yml _pages _publications _posts
git commit -m "feat: launch personalized academic homepage"
```
