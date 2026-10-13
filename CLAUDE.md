# Portfolio ground rules

Rules for every edit to this site. They apply to page text, titles, tags, chart labels, and CSS `content` alike.

## Punctuation
- Never use the middle dot (`·`, `•`, `・`) or long dashes (`—`, `–`).
- Where one of those would go, use a slash: `재무제표/특허/뉴스`, `Jaehee Hur / Portfolio`.
- Ranges use a tilde: `2024.06 ~ 2024.12`, `5~20분`.
- A bold label followed by its description uses a colon: `<b>NER 파이프라인:</b> ...`.
- List markers are drawn with CSS shapes, never with a bullet character.

## Project detail pages (`projects/*.html`)
Every page uses the same structure, in this order:
1. `.project-meta`: one `.project-meta-label` per item (team, division if any, period, note). Never join items with a character.
2. `h1` title, then `.project-detail-desc`.
3. `Skills & Technologies`
4. `Overview`: a short paragraph on how the project is built, followed by a `.flow` flowchart (4 to 6 `.flow-step`s with `.flow-arrow` between them).
5. `Problem`
6. `Solution` (or the page's own architecture sections)
7. Page-specific extras (visualizations, publication, and so on)
8. `Key Achievements` as a `ul.achievement-list`
9. `div.project-pager` (role="navigation"; not a `<nav>`, which gets the sticky site-header style): previous/next project links, in the same order as `projects.html`. Update the neighbours when a project is added, removed, or reordered.

Section titles are in English. Body text is in Korean. Pages use `<html lang="ko">`.

## Facts kept consistent across pages
- Team names: `LG화학 AX기술개발팀` from 2026.01, `LG화학 생명과학/경영혁신/AX팀` for 2022.06 ~ 2025.12.
- A number or claim that appears on a card, a detail page, and `career.html` must match in all three places.
- Tag spelling: `LangChain`, `Plotly/Dash`, `Scikit-learn`, `Data Extraction`.
- `index.html` and `projects.html` share the same card data; change both together.

## Landing and list pages
- `index.html` is the landing page: hero (projects, CV PDF, GitHub, contact links), 4 impact stats, Featured Projects, 6 Selected Projects, Publications (`#publications`), Talks & Recognition.
- `projects.html` lists every project with a category filter. Each card carries `data-category` set to one of `llm`, `quality`, `forecast`, `bio`.
- Every page's nav has Career, Projects, Publications.
- Every card shows its cover from `static/images/covers/<slug>.svg` (16:9). A cover has the category label, one headline figure with a short caption, and a 4-step pipeline. Category colors: `llm` indigo, `quality` green, `forecast` amber, `bio` rose. The headline figure must match the project page.
- `career.html` links each project name to its detail page and ends with Education and Skills.

## Head tags
Every page carries the `<!-- SEO -->` block: description, theme color, SVG favicon, Open Graph tags with `static/images/og.png`. Detail pages use their `.project-detail-desc` as the description.

## Sources
The CV at `static/files/Jaehee_Hur_CV.pdf` is the source for publications, education, skills, and deployment facts. Where the CV and these rules disagree (team names, R&D Planning Agent results), these rules win.
- R&D Planning Agent: detailed results are on hold until the project is reworked. Don't add numbers for it.

## Footer
`Jaehee Hur © 2026 / jaeheehur02@gmail.com` on every page.
