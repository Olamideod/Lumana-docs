# Lumana documentation writing guide

This guide builds on the Google developer documentation style guide. When something isn't covered here, follow Google's guidance. If it's still not clear, choose the option that's easier to read, scan, and understand.

---

## Core documentation principles

Every piece of documentation must meet six standards before it's ready to publish. Use these as your checklist every time you write or review.

**User-focused.** Write for what the user wants to do, not what the tool is. Every heading and section should answer one question: what will the user accomplish here?

**Trustworthy.** Verify every claim against the live product before you publish. Don't write from memory. If you can't confirm it, don't include it.

**Easy to understand.** Reduce the cognitive load for the reader. Use plain language, active voice, and short sentences. If a sentence is hard to write, it's hard to read.

**Easy to find.** Structure content around how users think and move through tasks. Users scan, skip, and search. Make it easy to land in the right place and know where to go next.

**Usable.** Write so a user can complete the task unaided, with no guesswork. If a user needs to ask for help after reading your documentation, the documentation isn't done.

**Style compliant.** Use active voice, second person ("you"), present tense, and plain language throughout. No sentence exceeds 25 words.

---

## User-focused writing

Write for what the user wants to do, not what the tool is. This is the most important principle and the easiest to get wrong.

**Tool-focused writing** names features and describes what exists. **User-focused writing** describes tasks and outcomes. It tells the user what they can accomplish.

| Tool-focused (wrong) | User-focused (correct) |
|---|---|
| Alert Configuration Panel | Configure an alert |
| Camera Management | Add and manage cameras |
| User Permissions | Set up user access |
| Smart Search | Search for events using Smart Search |

Read every heading and section intro you write. If it describes the product, rewrite it to describe what the user will do or achieve.

---

## Trustworthy writing

One wrong step makes users question everything else on the page. Follow these rules every time you write or update documentation.

- Open the product as you write. Perform every step you document in the live product.
- Don't write from memory. If you're not certain a claim is accurate, verify it against the live product or a confirmed source.
- Document known limitations inline, where users will encounter them. Don't move them to a separate troubleshooting section.
- If you can't verify a claim, don't include it. An omission is better than an error.
- When you update documentation, check every step and screenshot against the current product state.

When documenting AI-powered features, acknowledge confidence levels, environmental factors, and detection accuracy honestly. Don't describe AI features as infallible.

---

## Writing for clarity

Reduce how hard the reader has to think. Every sentence should be plain, active, and direct.

### The caveman technique

Use this technique when a sentence is too complex or abstract to fix directly.

**Step 1 — Strip the sentence to its bare meaning.** Write it in the shortest, most primitive form you can. Grammar doesn't matter here. You're finding the meaning, not writing the final sentence.

**Step 2 — Identify the core idea.** What is the sentence actually saying? Remove abstractions.

**Step 3 — Rebuild it cleanly.** Rewrite from the stripped version using plain language, active voice, and second person.

**Example:**

- Original: *"The interface provides the ability to instruct the operating system to render items between event dispatches."*
- Stripped: *"Interface tell operating system. Render item between event."*
- Rebuilt: *"Use the interface to render items between events."*

The stripped version is never the final output. It's a middle step that forces you to find the meaning before you rewrite. The rebuilt version is your starting point for the final output — not the final output itself. Before you publish the rebuilt version, check it against all six core principles: user-focused, trustworthy, easy to understand, easy to find, usable, and style compliant. Only then is it done.

---

## Writing for usability

Write so a user can complete the task unaided, with no guesswork.

- Each numbered step contains one clear action. Don't combine two actions in one step.
- If a step produces a visible result, describe it in the line immediately after the step.
- Don't assume the user knows what comes next. Tell them.
- If a user has to choose between options, explain what each option means and when to use it.
- Add a "Next steps" section at the end of every page. Always tell the user where to go after they finish.

The test is simple. If a user follows your documentation exactly and can't complete the task, the documentation needs rewriting.

---

## Easy to find

Structure content around how users think and move through tasks, not around how the product is organised.

When content is structured around product features rather than user goals, users have to jump between sections to complete one task. This is called **information fragmentation**.

**To avoid information fragmentation:**

- Map the full end-to-end flow of a task before you start writing.
- Organise content to match that flow. Headings should follow the task sequence, not the product menu structure.
- Each section stands on its own. A user arriving from search or a sidebar link should understand the section without reading what came before it.
- Use cross-links at the point where the user needs them, not at the end of the page.

The test: if a user has to jump between three different pages to complete one task, the content is fragmented. Reorganise around the task.

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

Define each term once, then use it consistently everywhere. Don't use "e.g." or "i.e." Write "for example" and "that is" in full.

---

## Voice and tone

Write like you're talking to a security professional or IT administrator who knows their field but doesn't have time for marketing language. Be direct, be helpful, and skip the hype. Focus on what the user is trying to do, not on how impressive Lumana is.

### Tone qualities

- **Authentic:** Credible, serious domain expertise, never superficial.
- **Focused:** Simplicity despite complexity. Don't make readers guess what you mean.
- **Clear:** Active voice, short paragraphs, scannable content with bullet points when helpful.
- **Fresh:** Clean, straightforward wording balanced with technical accuracy.
- **Warm:** Approachable and user-centric. Remember users aren't always experts.

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

## Audience and user roles

Lumana documentation is written for two primary user profiles.

**The director (security manager)** is responsible for monitoring, reviewing alerts, and managing day-to-day security operations. Not always technical. They need clear, task-focused guidance on using the platform without deep configuration knowledge.

**The installer (expert)** is responsible for deploying hardware, configuring cameras, setting up alerts, and managing the system. Technical and experienced. They need precise, complete instructions including admin-level configuration steps.

When content applies only to administrators or installers, mark it clearly so directors and end users can skip it. Don't bury admin-only steps inside general user flows without signalling who they're for.

---

## AI limitations and managing expectations

AI limitations are the number one customer friction point. Documentation must set accurate expectations about what Lumana's AI can and cannot do.

- Don't describe AI features as infallible. Acknowledge that confidence levels, lighting conditions, camera placement, and other factors affect detection accuracy.
- When documenting AI-powered alerts, explain the confidence level setting and what it means for false positives and missed detections.
- Configuration, installation, and AI limitation guidance are the highest priority content areas.

If a feature has known limitations, document them inline where users will encounter them, not only in a separate troubleshooting section.

---

## Sentence and paragraph rules

One main idea per sentence. Keep paragraphs to two to four sentences. Avoid nested clauses when a simpler structure works.

Vary sentence rhythm. Mix short ones (around 8 words) with longer ones (up to 25 words). Use present tense, not future tense.

Additional rules:

- Maximum 25 words per sentence. Shorter is better.
- If you start with "if," then include "then" in the predicate.
  - Not: "If you need updates, use Option A."
  - Use: "If you need updates, then use Option A."
- Use "may" for permission, "might" for possibility.
- Use "Enter" not "add" for form fields.
- After a colon or a hyphen, capitalize when a full sentence follows. Use lowercase when what follows is a phrase or fragment.
  - Full sentence: "Note: This action is irreversible."
  - Fragment: "Options: daily, weekly, or monthly."
- Avoid "where" to connect clauses. Use "because," "since," or "so" instead.
  - Not: "Teams maintain duplicate codebases where maintenance costs double."
  - Use: "Teams maintain duplicate codebases, so maintenance costs double."
- Avoid marketing words. Use technical words instead.
- Don't use em-dashes.
- Use contractions naturally: "you'll need to", "it's important", "don't forget".
- Occasionally start sentences with "And" or "But" when it creates natural flow.

---

## Headings and capitalisation

Use sentence case for all headings (H1 through H6). Make headings descriptive, not clever. Every page must have one H1 that states the topic clearly. Use H2 and H3 to break content into scannable sections.

Never stack headings: include at least one paragraph between them. Never use bold text as a heading. Use proper heading markup. Minimize parentheses in headings.

| Good | Bad |
|---|---|
| Connect Lumana Core to the network | Connect Lumana Core To The Network |
| Configure motion detection alerts | Alert magic happens here |
| Set up user permissions | Let's get you set up |

---

## Content types

Each page should have one clear purpose. Don't mix tutorial content with reference material on the same page.

| Type | Purpose |
|---|---|
| Get started | Get to a first successful result as fast as possible. |
| How-to guide | Task-based instructions for a specific goal. Assumes some existing knowledge. |
| Concept | Explanations of how Lumana works and why. |
| Reference | API, CLI, and configuration details. |

How-to guides are goal-oriented. They assume the reader already has some experience. Get started guides are learning-oriented. They take the reader through a first successful outcome step by step.

---

## Guide structure

Every how-to guide must follow this structure. Each section below is required.

**Introduction:** State what the reader will accomplish by the end of the guide. Be specific about the outcome.

**Prerequisites:** List what the reader needs before starting. Include required hardware or software versions, configuration that must already be in place, and access requirements.

**Step-by-step instructions:** Walk through the task with numbered steps. Each step must contain one clear action and reference the relevant UI elements. Show expected outcomes when they're not obvious.

**Next steps:** Point to related guides or the next logical task. Give the reader clear direction on where to go from here.

---

## Lists, steps, and tables

Use the right format for the right content. Lists work for unordered information, steps work for sequences, and tables work for comparisons and reference data. Mixing these up creates confusion and breaks the reader's flow.

### Lists

Use bullet lists for unordered information and numbered lists for sequences. Keep list items parallel in structure. Every list needs at least two items. Format four or more related items as a list rather than running them together in prose.

**Periods in lists:** Use periods when list items contain full sentences. Omit periods when list items are phrases or fragments. Apply consistently across all items in the same list.

- Full sentences: "Select **Save** to apply your changes. The dashboard exits edit mode."
- Phrases or fragments: "Daily, weekly, or monthly"

**Mixed-structure list items:** When a list item opens with a definition-style label followed by full sentences of explanation, treat the item as a full sentence entry. Use a period at the end and lowercase after the colon.

- **Blocking period:** The minimum time in seconds between consecutive alerts for the same condition. Set to 0 to allow back-to-back alerts.

### Steps

Each numbered step is one clear action. If the step produces a visible result, describe it in the line immediately after the step. Never use a numbered list for unordered information.

### Tables

Use tables for parameter lists, option comparisons, and reference data. Don't use tables for layout. Keep headers short and descriptive.

---

## UI text and messages

Match UI labels, buttons, and error messages exactly, including capitalisation. Use bold for buttons and clickable elements, without quotation marks. Use bold for field names and keys. Place colons outside bold formatting, not inside.

- Not: **Add widgets:**
- Use: **Add widgets**:

Use **select** for all UI interactions, not "click." "Click" assumes a mouse. "Select" works across mouse, touch, and keyboard.

- Not: "Click **Save**."
- Use: "Select **Save**."

For error messages, quote the message exactly. Then explain what it means and what the reader should do next.

---

## Notes and warnings

Use callouts strategically. Don't overuse them. Use a **Note** block for information that prevents common mistakes. Use a **Warning** block for actions that are irreversible or have significant consequences. Place notes and warnings immediately after the step or statement they relate to.

---

## Images and screenshots

Use screenshots when they clarify an important step or result. Don't use images as the only way to convey critical information.

### Alt text

Don't write alt text for screenshots in Lumana documentation. Leave the `alt` attribute empty. Alt text is reserved for diagrams or images that convey information not available in the surrounding text.

### Image frames

All images must use a frame. The frame provides a consistent visual boundary and prevents screenshots from blending into the page background.

Use this format for every image:

```html
<div align="center" data-with-frame="true"><img src="../.gitbook/assets/IMAGE-NAME.png" alt="" width="563"></div>
```

The `data-with-frame="true"` attribute renders the frame around the image. Don't remove it. Match the path prefix (`../` or `../../` or `../../../`) to the location of the page relative to the assets folder. Use `width="563"` as the default. Use a smaller width for narrow UI elements such as dropdowns or counters.

### Asset folder structure

All images and icons live in `.gitbook/assets/`. Use section-based subfolders to mirror the content hierarchy. Keep the hierarchy to a maximum of three levels deep.

```
.gitbook/assets/
├── icons/
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

Rules:

- Use section-based subfolders, not root-based naming.
- Mirror the content hierarchy. Name the subfolder after the section where the image appears.
- Use kebab-case for all folder and file names.
- Icons use the `icon-` prefix and live in `icons/`.
- Move images added through the GitBook editor from the root to the correct subfolder. Update the path in the markdown before committing.
- When you add images for a new section, create the subfolder first, then add the images.

---

## Accessibility

Write and structure documentation so it works for people with disabilities and on different devices. Use clear headings and logical structure. Use proper list markup for steps and bullets. Write meaningful link text: not "here" or "this." Avoid deeply nested lists when a simpler structure works.

Use "people with disabilities," not "the disabled" or "disabled people."

---

## Links and signposting

Make link text descriptive. Don't use "click here" or raw URLs. Every major page should end with a "Next steps" section.

**Inline linking is the preferred approach** for web-based documentation. Embed links naturally as part of the sentence so the reader stays in context and understands why the link is relevant before selecting it.

- Not: "For configuration details, see the [Widgets](#) section."
- Use: "Each widget type has its own configuration options, covered in the [Widgets](#) section."

**"See X for Y" is acceptable in limited cases:** when the reference is the subject of the sentence, when flagging a major topic shift, or when the linked content is a warning or prerequisite. Don't use "see" as a casual signpost.

If the link belongs in the sentence, inline it. If it doesn't belong in the sentence, put it in a related links section at the end of the page.

| Good | Bad |
|---|---|
| Each widget type has its own configuration options, covered in the [Widgets](#) section. | For configuration details, see the [Widgets](#) section. |
| Read about Smart Search in the [VMS+ concepts guide](#). | Click here for more info. |

---

## Transitions between sections

Transitions between sections depend on the content type.

**For narrative or conceptual content,** use a short transition before each new heading to close the current section and set up the next. Keep it to one or two sentences. Don't force it if the sections are clearly distinct.

- Natural bridge: "Once you've set up X, you can move on to Y."
- Problem-solution: "This raises a question: how do you handle Z?"
- Context shift: "Understanding X helps explain why Y matters."

**For task-based or reference documentation,** don't add transitions between sections. Users rarely read these pages from top to bottom. They arrive at a specific section from search or a sidebar link. Each section should open with a direct statement and stand on its own.

The test: if removing the sentence between two sections leaves both sections fully clear, the sentence doesn't belong.

---

## Navigation and naming conventions

Use consistent naming patterns based on content type. These patterns follow the Google developer documentation style guide, which requires bare infinitive verbs for task-based titles.

| Content type | Naming pattern | Examples |
|---|---|---|
| How-to guides | Bare infinitive | "Connect Lumana Core to the network", "Configure alert sensitivity" |
| Get started | Bare infinitive ("Get started" is the only permitted exception) | "Get started", "Set up your first camera" |
| Concepts | Noun phrase | "Architecture overview", "Alert types" |
| Reference | Noun phrase | "Lumana API reference", "VMS+ keyboard shortcuts" |

Be consistent within each section. Don't mix naming patterns across pages of the same type.

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
- Transition words between ideas within a section.
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

Before submitting documentation, confirm all of the following:

- Every sentence is 25 words or fewer.
- The writing is in second person ("you") throughout.
- Every heading has a paragraph beneath it.
- All Lumana product terms are spelled correctly.
- UI elements are bolded and capitalised exactly as they appear in the product.
- Notes and warnings are placed immediately after the relevant step.
- Transitions appear only in narrative or conceptual content, not in task-based or reference documentation.
- Each section in task-based documentation opens with a direct statement and stands on its own.
- Links are inline where the context makes them relevant. "See X" is used only when the reference is the subject of the sentence or signals a major topic shift.
- All lists are parallel in structure and punctuation.
- The content is free of marketing language.
- Every heading describes a user task or outcome, not a product feature.
- Every claim has been verified against the live product. Nothing is written from memory.
- The content is structured around user tasks, not product menus or feature lists.
- A user can complete every task unaided, with no guesswork.

---

## How to use this guide

Start with this guide and the Lumana-specific decisions above. If something isn't covered here, then follow the Google developer documentation style guide. If it's still unclear, then choose the option that's easier to read, scan, and understand.

---

## Editing checklist

Run every page through this checklist before you submit. Each row maps a specific rule from this guide to one of the six documentation standards. If any item fails, revise before publishing.

**Applies to all page types:** Trustworthy, Easy to understand, and Style compliance apply to every page — how-to guides, get started guides, concept pages, and reference pages.

**Applies to task-based pages only:** User-focused heading rules, Usability, and the Easy to find transition rule apply to how-to guides, get started guides, and reference pages. Concept pages use noun phrase headings and may include transitions between sections. Skip the step and usability checks when reviewing conceptual content.

| Criterion | What to check |
|---|---|
| **User-focused** | Every heading uses a bare infinitive and describes a user task or outcome, not a product feature. |
| | Every section intro tells the user what they'll accomplish. |
| | No heading names a feature, panel, or tool without connecting it to a user goal. |
| | Content is structured around the user's task flow, not the product menu or feature list. |
| **Trustworthy** | Every step has been performed in the live product before publishing. |
| | Every claim is verified against the live product or a confirmed source. Nothing is written from memory. |
| | All Lumana product names are spelled exactly as specified in the terminology table. |
| | All UI labels, buttons, and error messages match the live product exactly, including capitalisation. |
| | Known limitations are documented inline where users will encounter them, not only in a troubleshooting section. |
| | All screenshots match the current product state. |
| **Easy to understand** | Every sentence is plain, active, and direct. |
| | No sentence exceeds 25 words. |
| | The caveman technique was applied to any sentence that was complex before rewriting. The rebuilt version passed all six criteria before publishing. |
| | No passive voice anywhere on the page. |
| | No jargon or unnecessarily complex vocabulary. |
| | Sentence length varies naturally. Not all sentences are the same length. |
| | No banned words or phrases appear on the page. |
| | Words used sparingly — Ensure, Enhance, Significant(ly), Effective(ly), Essential — appear a maximum of 2-3 times. |
| | No mechanical transitions: "Additionally," "Furthermore," "Moreover." |
| | "Where" is not used to connect clauses. "Because," "since," or "so" is used instead. |
| **Easy to find** | Each section stands on its own. A user arriving from search or a sidebar link can follow it without reading what came before. |
| | Headings follow the task sequence, not the product menu structure. |
| | Cross-links appear at the point where the user needs them, not only at the end of the page. |
| | Inline linking is used as the default. "See X for Y" appears only when the reference is the subject of the sentence or signals a major topic shift. |
| | All link text is descriptive. No "click here" or raw URLs. |
| | Transitions appear only in narrative or conceptual content. Task-based and reference sections have no transitions between them. |
| | Every major page ends with a "Next steps" section. |
| | A user doesn't need to jump between multiple pages to complete one task. |
| **Usability** | Each numbered step contains one clear action. No step combines two actions. |
| | Every step that produces a visible result describes that result in the line immediately after the step. |
| | Every option presented to the user is explained — what it means and when to use it. |
| | Notes and warnings appear immediately after the step or statement they relate to. |
| | Every list has at least two items. |
| | Numbered lists are used only for sequences, not for unordered information. |
| | A user can complete every task unaided, with no guesswork. |
| **Style compliance** | Active voice is used throughout. No passive constructions. |
| | Second person ("you") is used throughout. "We" and "let's" don't appear anywhere. |
| | Present tense is used throughout. No future tense. |
| | All headings are sentence case. No title case. |
| | Every heading has at least one paragraph beneath it. No stacked headings. |
| | UI elements are bold without quotation marks. Colons appear outside bold formatting. |
| | "Select" is used for all UI interactions. "Click" doesn't appear anywhere. |
| | "Enter" is used for form fields. "Add" is not used for form fields. |
| | "May" is used for permission. "Might" is used for possibility. |
| | Every "if" clause includes "then" in the predicate. |
| | No em-dashes appear anywhere on the page. |
| | Contractions are used naturally throughout. |
| | All list items are parallel in structure and punctuation. Periods appear on full sentence items. Periods are omitted on phrases and fragments. |
| | "E.g." and "i.e." don't appear anywhere. "For example" and "that is" are used instead. |
| | The page is free of marketing language. |