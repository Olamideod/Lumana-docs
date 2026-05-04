# Lumana documentation — Claude instructions

This is the Lumana product documentation project. All writing, editing, and structural work must follow the rules in this file. These rules come directly from the project style guide (STYLEGUIDE.md). Apply them to every file you touch.

---

## Project overview

- **Product:** Lumana — a security camera analytics and monitoring platform
- **Git workflow:** Work on the `staging` branch. Never push directly to `main`.
- **IA reference:** See `IA.md` for the proposed information architecture for both user profiles.
- **User journey maps:** See `user-journey-map.md` for the full documentation audit.
- **Navigation:** `SUMMARY.md` defines the live navigation. Check it before making structural claims.

---

## User profiles

Two profiles only. Never create content that merges them without signalling which profile it serves.

### The director

| | |
|---|---|
| **Actor** | A security manager responsible for monitoring, reviewing alerts, and managing day-to-day security operations. Not always technical. No admin access. Needs clear, task-focused guidance without deep configuration knowledge. |
| **Scenario** | The director has been given access to a configured Lumana system. They need to use it independently to monitor their facility, respond to incidents, analyze trends, and report to stakeholders. |
| **Goal** | Use Lumana confidently and independently for day-to-day security operations without relying on IT or an installer. |
| **Expectation** | The director expects to see their cameras, receive alerts, search for footage, and build reports without learning technical concepts first. |

Write for the director when: the task involves monitoring live feeds, responding to alerts, searching footage, archiving evidence, using the mobile app, or reviewing dashboards and reports. Keep language plain. Never assume familiarity with configuration, AI concepts, or admin settings.

### The installer

| | |
|---|---|
| **Actor** | A technical expert responsible for deploying hardware, configuring cameras, setting up alerts, and managing the system. Experienced in hardware and network installation. May not have a background in AI, machine learning, or statistics. Full admin access. Needs complete instructions including admin-level configuration steps. |
| **Scenario** | The installer is deploying Lumana at a new customer site. They need to set up hardware, configure the system, build out alert rules, connect third-party integrations, and hand the system off to the director for day-to-day use. |
| **Goal** | Deploy a fully configured Lumana system that works as specified and can be operated independently by the director without installer support. |
| **Expectation** | The installer expects complete technical specifications, exact configuration steps, and a clear signal that each stage is complete before moving to the next. |

Write for the installer when: the task involves hardware setup, alert configuration, system administration, integrations, or API work. Be precise and complete. Never omit a step because it seems obvious. Always indicate when a stage is complete before moving to the next. When documenting AI settings such as confidence thresholds, explain what the value controls and how environment affects it — the installer is technically experienced but may not have an AI or statistics background.

When content applies only to installers or admins, mark it clearly. Never bury admin-only steps inside general user flows without signalling who they're for.

---

## Six documentation standards

Every piece of content must meet all six before it's ready to publish.

1. **User-focused.** Write for what the user wants to do, not what the tool is. Every heading describes a user task or outcome, not a product feature.
2. **Trustworthy.** Verify every claim against the live product before publishing. Don't write from memory. If you can't confirm it, don't include it.
3. **Easy to understand.** Use plain language, active voice, and short sentences. If a sentence is hard to write, it's hard to read.
4. **Easy to find.** Structure content around how users think and move through tasks, not around how the product is organised.
5. **Usable.** Write so a user can complete the task unaided, with no guesswork.
6. **Style compliant.** Active voice, second person ("you"), present tense, plain language. No sentence exceeds 25 words.

---

## Sentence rules

- Maximum 25 words per sentence. Shorter is better.
- One main idea per sentence.
- Active voice required. No passive constructions.
- Second person ("you") throughout. Never "we" or "let's."
- Present tense throughout. No future tense.
- If you start with "if," then include "then" in the predicate.
  - Wrong: "If you need updates, use Option A."
  - Right: "If you need updates, then use Option A."
- Use "may" for permission. Use "might" for possibility.
- Never use em-dashes.
- Use contractions naturally: "you'll need to," "it's important," "don't forget."
- Occasionally start sentences with "And" or "But" when it creates natural flow.
- Avoid "where" to connect clauses. Use "because," "since," or "so" instead.
  - Wrong: "Teams maintain duplicate codebases where maintenance costs double."
  - Right: "Teams maintain duplicate codebases, so maintenance costs double."
- Vary sentence length. Mix short ones (around 8 words) with longer ones (up to 25 words). Don't make all sentences the same length.
- No mechanical transitions: "Additionally," "Furthermore," "Moreover."
- Don't use "e.g." or "i.e." Write "for example" and "that is" in full.

---

## Paragraph rules

- Keep paragraphs to two to four sentences.
- Avoid nested clauses when a simpler structure works.
- Every heading must have at least one paragraph beneath it. Never stack headings.

---

## Heading rules

- Sentence case for all headings (H1 through H6). No title case.
- Every page has one H1 that states the topic clearly.
- Use H2 and H3 to break content into scannable sections.
- Heading naming conventions by content type:
  - How-to guides: bare infinitive ("Connect Lumana Core to the network")
  - Get started: bare infinitive ("Get started" is the only permitted exception)
  - Concepts: noun phrase ("Alert types," "Architecture overview")
  - Reference: noun phrase ("Lumana API reference")
- Never use bold text as a heading. Use proper heading markup.
- Minimize parentheses in headings.

---

## Word choices

### Banned words — never use
Foster, Revolutionize, Landscape, Seamless, Robust, Streamline, Delve, Elevate, Facilitate, Groundbreaking, Comprehensive.

### Banned phrases — never use
- "Dives deep" / "Deep dive"
- "This is where X comes in"
- "X is not just about; it's about"
- "X isn't just nice to have; it's..."
- "You're not alone"
- "Thrive in a fast-paced environment"

### Use sparingly — maximum 2-3 times per page
Ensure, Enhance, Significant(ly), Effective(ly), Essential.

### Banned word for alerts
Never use "fire" or "fires" when referring to alerts triggering. Use "trigger" or "triggers" instead.

---

## Product names and terminology

Always spell these exactly as shown.

| Term | Correct | Wrong |
|---|---|---|
| VMS+ | VMS+ | vms+, VMS |
| Core / Core Series | Core / Core Series | core, CORE |
| DealHub | DealHub | Dealhub, Deal Hub |
| VIA-1 | VIA-1 | via-1, Via-1 |
| Lumana Authorized Partners | Lumana Authorized Partners | Lumana authorized partners |
| Text Search, Classic Search, Smart Search | Text Search, Classic Search, Smart Search | text search, classic search |
| NDAA, SOC 2, HIPAA, GDPR, LPR | Always uppercase | ndaa, soc 2 |

Define each term once. Use it consistently everywhere after that.

---

## UI text rules

- Use **select** for all UI interactions. Never use "click."
- When a UI element is named "Select," add a qualifying word to break the repetition. Use "Select the **Select** button" or "Select the **Select** option" — not "Select **Select**." This follows SAP's pattern of qualifying UI elements by type.
- Use **Enter** for form fields. Never use "add" for form fields.
- Bold all UI labels, buttons, field names, and clickable elements. No quotation marks around them.
- Place colons outside bold formatting, not inside.
  - Wrong: **Add widgets:**
  - Right: **Add widgets**:
- Match UI labels exactly, including capitalisation, as they appear in the live product.
- For error messages: quote the message exactly, then explain what it means and what the user should do next.

---

## Content types

Each page has one clear purpose. Never mix content types on the same page.

| Type | Purpose |
|---|---|
| Get started | Gets the user to a first successful result as fast as possible. |
| How-to guide | Task-based instructions for a specific goal. Assumes some existing knowledge. |
| Concept | Explains how Lumana works and why. |
| Reference | API, CLI, and configuration details. |

---

## Page structure for how-to guides

Every how-to guide must follow this structure in this order:

1. **Introduction:** State what the reader will accomplish. Be specific about the outcome.
2. **Prerequisites:** List what the reader needs before starting — hardware, software, configuration, and access requirements.
3. **Step-by-step instructions:** Numbered steps. One clear action per step. Describe the visible result after any step that produces one.

---

## Lists, steps, and tables

**Lists:**
- Bullet lists for unordered information. Numbered lists for sequences.
- Every list needs at least two items.
- Format four or more related items as a list, not prose.
- Keep list items parallel in structure.
- Periods on full-sentence items. No periods on phrases or fragments. Apply consistently across all items in the same list.
- Mixed-structure items (definition label + full sentences): use a period at the end, lowercase after the colon.

**Steps:**
- Each step is one clear action. Never combine two actions in one step.
- If a step produces a visible result, describe it in the line immediately after the step.
- Never use a numbered list for unordered information.

**Tables:**
- Use for parameter lists, option comparisons, and reference data.
- Don't use for layout.
- Keep headers short and descriptive.

---

## Notes and warnings

- Use `{% hint style="info" %}` for notes that prevent common mistakes.
- Use `{% hint style="warning" %}` for actions that are irreversible or have significant consequences.
- Place notes and warnings immediately after the step or statement they relate to.
- Don't overuse callouts. Use them strategically.

---

## Images and screenshots

**Format — use this exact format for every image:**

```html
<div align="center" data-with-frame="true"><img src="../.gitbook/assets/IMAGE-NAME.png" alt="" width="563"></div>
```

- `data-with-frame="true"` is required on every image. Don't remove it.
- `alt=""` — leave empty for screenshots. Alt text is only for diagrams that convey information not available in the surrounding text.
- `width="563"` is the default. Use a smaller width for narrow UI elements such as dropdowns or counters.
- Match the path prefix (`../` or `../../` or `../../../`) to the page's location relative to the assets folder.
- Never use `<figure>` or `<figcaption>` tags.
- Never use `align="center"` inside `<figure>` — use it only on the wrapping `<div>`.

**Asset folder structure:**

```
.gitbook/assets/
├── icons/                    SVG icons — use icon- prefix
├── getting-started/
│   └── mobile-app/
├── alerts-and-ai-detection/
├── dashboards/
│   ├── main/
│   ├── filter/
│   └── widgets/
│       ├── shared/
│       └── chart-or-table/
└── lumana-docs-header.png
```

- Use section-based subfolders. Mirror the content hierarchy.
- Use kebab-case for all folder and file names.
- Images added through the GitBook editor land in the root. Move them to the correct subfolder and update the path before committing.

---

## Links and signposting

- Inline linking is the default. Embed links naturally as part of the sentence.
- Don't use "click here" or raw URLs as link text.
- "See X for Y" is acceptable only when the reference is the subject of the sentence, when flagging a major topic shift, or when the linked content is a warning or prerequisite.
- Cross-links appear at the point where the user needs them, not only at the end of the page.

---

## Transitions between sections

- Conceptual content: use a short transition (one to two sentences) before each new heading.
- Task-based and reference content: no transitions between sections. Each section opens with a direct statement and stands on its own.
- Test: if removing the sentence between two sections leaves both sections fully clear, the sentence doesn't belong.

---

## AI limitations

AI limitations are the number one customer friction point.

- Never describe AI features as infallible.
- Always acknowledge that confidence levels, lighting conditions, camera placement, and other factors affect detection accuracy.
- When documenting AI-powered alerts, explain the confidence level setting and what it means for false positives and missed detections.
- Document known limitations inline where users will encounter them. Don't move them to a separate troubleshooting section.

---

## Information architecture

- The full IA for both profiles is in `IA.md`.
- The director's navigation uses goal-based section names, not product-based names.
- The installer sees the full admin navigation.
- Sections missing from `SUMMARY.md` but present as folders: `api-reference`, `integrations`, `software-integrations`, `whats-new`, `changelog`, `faq-and-reference`. These need to be added to `SUMMARY.md`.
- Chart or table sub-pages (Objects, Alerts, Event tags) exist as files but are not in `SUMMARY.md`. Add them under Chart or table in the Dashboards section.

---

## Caveman technique

Use this when a sentence is too complex to fix directly.

1. Strip the sentence to its bare meaning. Grammar doesn't matter. Find the meaning.
2. Identify the core idea. Remove abstractions.
3. Rebuild cleanly using plain language, active voice, and second person.

The stripped version is never the final output. The rebuilt version is a starting point — check it against all six documentation standards before publishing.

---

## Editing checklist

Run every page through this before submitting.

**User-focused**
- [ ] Every heading uses a bare infinitive and describes a user task or outcome, not a product feature.
- [ ] Every section intro tells the user what they'll accomplish.
- [ ] No heading names a feature, panel, or tool without connecting it to a user goal.
- [ ] Content is structured around the user's task flow, not the product menu or feature list.

**Trustworthy**
- [ ] Every step has been performed in the live product before publishing.
- [ ] Every claim is verified against the live product or a confirmed source.
- [ ] All Lumana product names are spelled exactly as specified.
- [ ] All UI labels, buttons, and error messages match the live product exactly, including capitalisation.
- [ ] Known limitations are documented inline where users will encounter them.
- [ ] All screenshots match the current product state.

**Easy to understand**
- [ ] Every sentence is plain, active, and direct.
- [ ] No sentence exceeds 25 words.
- [ ] No passive voice anywhere on the page.
- [ ] No jargon or unnecessarily complex vocabulary.
- [ ] Sentence length varies naturally.
- [ ] No banned words or phrases.
- [ ] Sparingly-used words appear a maximum of 2-3 times.
- [ ] No mechanical transitions.
- [ ] "Where" is not used to connect clauses.

**Easy to find**
- [ ] Each section stands on its own.
- [ ] Headings follow the task sequence, not the product menu structure.
- [ ] Cross-links appear at the point where the user needs them.
- [ ] Inline linking is used as the default.
- [ ] All link text is descriptive.
- [ ] Transitions appear only in narrative or conceptual content.
- [ ] A user doesn't need to jump between multiple pages to complete one task.

**Usability**
- [ ] Each numbered step contains one clear action.
- [ ] Every step that produces a visible result describes that result immediately after the step.
- [ ] Every option is explained — what it means and when to use it.
- [ ] Notes and warnings appear immediately after the step or statement they relate to.
- [ ] Every list has at least two items.
- [ ] Numbered lists are used only for sequences.
- [ ] A user can complete every task unaided, with no guesswork.

**Style compliance**
- [ ] Active voice throughout. No passive constructions.
- [ ] Second person ("you") throughout. "We" and "let's" don't appear.
- [ ] Present tense throughout. No future tense.
- [ ] All headings are sentence case.
- [ ] Every heading has at least one paragraph beneath it.
- [ ] UI elements are bold without quotation marks. Colons appear outside bold formatting.
- [ ] "Select" is used for all UI interactions. "Click" doesn't appear.
- [ ] "Enter" is used for form fields. "Add" is not used for form fields.
- [ ] "May" is used for permission. "Might" is used for possibility.
- [ ] Every "if" clause includes "then" in the predicate.
- [ ] No em-dashes anywhere.
- [ ] Contractions are used naturally.
- [ ] All list items are parallel in structure and punctuation.
- [ ] "E.g." and "i.e." don't appear. "For example" and "that is" are used instead.
- [ ] The page is free of marketing language.
- [ ] "Trigger" is used for alerts, not "fire."