# Lumana documentation writing guide

This guide builds on the Google developer documentation style guide. When something is not covered here, follow Google's guidance. If it's still not clear, choose the option that is easier to read, scan, and understand.

---

## Product names and terminology

Lumana product names must always appear exactly as written, in body text, headings, and UI copy. In code, commands, and configuration, match the syntax exactly.

| Context | Correct | Wrong |
|---|---|---|
| Body text, headings | VMS+ | vms+, VMS |
| Body text, headings | Core / Core Series | core, CORE |
| Body text, headings | DealHub | Dealhub, Deal Hub |
| Body text, headings | VIA-1 | via-1, Via-1 |
| Body text, headings | Lumana Authorized Partners | Lumana authorized partners |
| Body text, headings | Text Search, Classic Search, Smart Search | text search, classic search, smart search |
| Always uppercase | NDAA, SOC 2, HIPAA, GDPR, LPR, ARR, TCV | ndaa, soc 2, hipaa |

Define each term once, then use it consistently everywhere. Do not use "e.g." or "i.e.": write "for example" and "that is" in full.

---

## Voice and tone

Write like you're talking to a security professional or IT administrator who knows their field but doesn't have time for marketing speak. Be direct, be helpful, and skip the hype. Focus on what the user is trying to do, not on how impressive Lumana is.

### Tone qualities

- **Authentic:** Credible, serious domain expertise, never superficial.
- **Focused:** Simplicity despite complexity; don't make readers guess what you mean.
- **Clear:** Active voice, short paragraphs, scannable content with bullet points when helpful.
- **Fresh:** Clean, straightforward wording balanced with technical accuracy.
- **Warm:** Approachable and user-centric; remember users aren't always experts.

### Voice qualities

- Sharp, professional, and trusted by practitioners.
- Active voice required, not passive.
- Always use second person ("you"), never "we" or "let's."
- Technical, but never dry. Confident, but never arrogant.
- Precise, deliberate, trustworthy, and mature.
- Minimize jargon and complex sentences.
- Use plural antecedents and pronouns.
- Always tell the truth.

### Voice markers

Mix these naturally throughout writing:

- **Direct address:** "Here's what you need to know" or "Think of it this way."
- **Casual connectors:** "Now" / "So" / "Here's the thing" at sentence starts.
- **Rhetorical setup:** "Why does this matter?" followed by the answer.
- **Real-world framing:** "In practice" / "Typically" / "Most teams find that."
- **Honest caveats:** "This approach works well, though it has trade-offs."

---

## Sentence and paragraph style

One main idea per sentence. Keep paragraphs to two to four sentences. Avoid nested clauses when a simpler structure works. Write so readers can quickly scan and find what they need.

Vary sentence rhythm. Don't make all sentences the same length: mix short ones (around 8 words) with longer ones (up to 25 words). Use present tense, not future tense. Add intro paragraphs where users need context.

Additional rules:

- Maximum 25 words per sentence. Shorter is better.
- If you start with "if," then include "then" in the predicate.
- Use "may" for permission, "might" for possibility.
- Use "Enter" not "add" for form fields.
- After a colon or a hyphen, proceed with a capital letter.
- Avoid "where" to connect clauses; use conjunctions ("because," "since," "so") instead.
- Avoid marketing words; use technical words instead.
- Use contractions naturally: "you'll need to", "it's important", "don't forget".
- Occasionally start sentences with "And" or "But" when it creates natural flow.

---

## Headings and capitalisation

Use sentence case for all headings (H1 through H6). Make headings descriptive, not clever. Every page must have one H1 that states the topic clearly. Use H2 and H3 to break content into scannable sections.

Never stack headings: include at least one paragraph between them. Never use bold text as a heading; use proper heading markup. Minimize parentheses in headings.

| Good | Bad |
|---|---|
| Connect Lumana Core to the network | Connect Lumana Core To The Network |
| Configure motion detection alerts | Alert magic happens here |
| Set up user permissions | Let's get you set up |

---

## Content types

Each page should have one clear purpose. Do not mix tutorial content with reference material on the same page.

| Type | Purpose |
|---|---|
| Get started | Get to a first successful result as fast as possible. |
| How-to guide | Task-based instructions for a specific goal; assumes some existing knowledge. |
| Concept | Explanations of how Lumana works and why. |
| Reference | API, CLI, and configuration details. |

How-to guides are goal-oriented. They assume the reader already has some experience and knows what they want to accomplish. Get started guides are learning-oriented: they assume less experience and take the reader through a first successful outcome step by step.

---

## Guide structure

Every how-to guide must follow this structure. Each section below is required.

**Introduction:** State what the reader will accomplish by the end of the guide. Be specific about the outcome.

**Prerequisites:** List what the reader needs before starting. Include required hardware or software versions, configuration that must already be in place, knowledge or completed guides, and access requirements.

**Step-by-step instructions:** Walk through the task with numbered steps. Each step must contain one clear action, reference the relevant UI elements or configuration details, and show expected outcomes when they're not obvious.

**Next steps:** Point to related guides or the next logical task. Give the reader clear direction on where to go from here.

---

## Lists, steps, and tables

### Lists

Use bullet lists for unordered information and numbered lists for sequences. Keep list items parallel in structure. Use periods consistently: all items end with a period or none do. Every list needs at least two items. Format four or more related items as a list rather than running them together in prose.

### Steps

Each numbered step is one clear action. If the step produces a visible result, describe it in the line immediately following the step. Never use a numbered list for unordered information.

### Tables

Use tables for parameter lists, option comparisons, and reference data. Do not use tables for layout. Keep headers short and descriptive.

---

## UI text and messages

Match UI labels, buttons, and error messages exactly, including capitalisation. Use bold for buttons and clickable elements, without quotation marks. Use bold for field names and keys.

For error messages, quote the message exactly, then explain what it means and what the reader should do next.

---

## Notes and warnings

Use callouts strategically: do not overuse them. Use a **Note** block for information that prevents common mistakes. Use a **Warning** block for actions that are irreversible or have significant consequences. Place notes and warnings immediately after the step or statement they relate to.

---

## Images and screenshots

Use screenshots when they clarify an important step or result. Write alt text that describes what the reader should notice, not just "screenshot." Do not use images as the only way to convey critical information.

| Good alt text | Bad alt text |
|---|---|
| VMS+ Devices page showing Lumana Core listed with a green online status indicator. | Screenshot |
| Alert settings panel with sensitivity slider set to medium. | Image of settings |

### Asset folder structure

All images and icons live in `.gitbook/assets/`. Use section-based subfolders to mirror the content hierarchy. Keep the hierarchy shallow: a maximum of three levels deep.

```
.gitbook/assets/
├── icons/                          SVG icons used in navigation cards
├── getting-started/                images used in the Getting started section
│   └── mobile-app/                 screenshots specific to the mobile app page
├── alerts-and-ai-detection/        screenshots used in the Alerts section
└── lumana-docs-header.png          images used at the root level stay at the root
```

Rules:

- Use section-based subfolders, not root-based naming.
- Mirror the content hierarchy: name the subfolder after the section where the image appears.
- Use kebab-case for all folder and file names.
- Keep hierarchy to a maximum of three levels: `.gitbook/assets/<section>/<subsection>/image.png`.
- Icons use the `icon-` prefix and live in `icons/`.
- App store badges and shared assets used across multiple pages go in the nearest common parent folder.
- Images added through the GitBook editor land in the root of `.gitbook/assets/` automatically. Move them to the correct subfolder and update the path in the markdown before committing.
- When you add images for a new section, create the subfolder first, then add the images.

---

## Accessibility

Write and structure documentation so it works for people with disabilities and on different devices. Use clear headings and logical structure. Use proper list markup for steps and bullets. Write meaningful link text: not "here" or "this." Include alt text for all images. Avoid deeply nested lists when a simpler structure works.

Use "people with disabilities," not "the disabled" or "disabled people."

---

## Links

Make link text descriptive. Do not use "click here" or raw URLs. Add introductory context before reference links. Every major page should end with a "Next steps" section.

| Good | Bad |
|---|---|
| See the Lumana API reference for authentication details. | Click here. |
| Read about Smart Search in the VMS+ concepts guide. | More info at support.lumana.ai/article/123 |

---

## Numbers, dates, and units

Spell out one through nine. Use numeric form for 10 and above, unless it's a unit or parameter. Use unambiguous date formats: write "21 November 2025" in body text and "2025-11-21" in code or logs.

---

## Inclusive and bias-free language

Avoid terms that stereotype or exclude. Use neutral, precise language. When in doubt, check the Google developer documentation style guide word list.

| Good | Bad |
|---|---|
| IT administrators, security managers | ninja coders, rockstar admins |
| People with disabilities | the disabled, the handicapped |
| Example data, test data | dummy data |

---

## Transitions between sections

Connect sections so the reader always knows where they are and where they're going next. Use two sentences before each new heading: the first closes out what just happened, the second sets up the reason for the next section.

You can also vary transitions naturally. Use a natural bridge ("Once you've completed X, you can move on to Y"), a problem-solution setup ("This raises a question: how do you handle Z?"), or a context shift ("Understanding X helps explain why Y matters"). Don't follow the two-sentence pattern rigidly every time: let the content guide you.

---

## Navigation and naming conventions

Use consistent naming patterns based on content type. These patterns follow Google's developer documentation style guide, which requires bare infinitive verbs for task-based titles.

| Content type | Naming pattern | Examples |
|---|---|---|
| How-to guides | Bare infinitive | "Connect Lumana Core to the network", "Configure alert sensitivity" |
| Get started | Bare infinitive ("Get started" is the only permitted exception) | "Get started", "Set up your first camera" |
| Concepts | Noun phrase | "Architecture overview", "Alert types" |
| Reference | Noun phrase | "Lumana API reference", "VMS+ keyboard shortcuts" |

Be consistent within each section: do not mix naming patterns across pages of the same type.

---

## Word choices

### Banned words

Never use: Foster, Revolutionize, Landscape, Seamless, Robust, Streamline, Delve, Elevate, Facilitate, Groundbreaking, Comprehensive.

### Banned phrases

- "Dives deep" / "Deep dive"
- "This is where X comes in"
- "X is not just about; it's about"
- "X isn't just nice to have; it's..."
- "You're not alone"
- "Thrive in a fast-paced environment"

### Use sparingly

Use each of these a maximum of 2-3 times per page: Ensure, Enhance, Significant(ly), Effective(ly), Essential.

---

## Sentence flow

Natural writing mixes long and short sentences and uses conjunctions to connect ideas. Choppy, uniform sentences read as robotic.

**Prefer:**

- Varied sentence length (for example, 12 words, then 23, then 8).
- Natural conjunctions: "since," "so," "because."
- Contractions in explanatory text.
- Sentences that occasionally start with "And" or "But."
- Transition words between ideas.
- Every heading followed by a description paragraph.

**Avoid:**

- All sentences the same length (18-20 words throughout).
- "Where" to connect clauses incorrectly.
- No contractions anywhere in the text.
- Mechanical transitions: "Additionally," "Furthermore," "Moreover."
- Stacked headings with no description paragraphs.
- Every paragraph exactly 3 sentences.

---

## Before you publish

Before submitting documentation, confirm: every sentence is 25 words or fewer; the writing is in second person throughout; every heading has a paragraph beneath it; all Lumana product terms are spelled correctly; UI elements are bolded and capitalised exactly as they appear in the product; notes and warnings are placed immediately after the relevant step; there is a transition before every new major heading; all lists are parallel in structure and punctuation; and the content is free of marketing language.

---

## How to use this guide

Start with this guide and the Lumana-specific decisions above. If something is not covered here, then follow the Google developer documentation style guide. If it's still unclear, then choose the option that is easier to read, scan, and understand.