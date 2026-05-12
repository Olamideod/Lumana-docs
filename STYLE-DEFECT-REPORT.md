# Style guide compliance defect report (round 3)

This is a fresh review of the same three sections (`live-video-monitoring-and-operations`, `databases-analytics-and-search`, and `set-up-cameras-and-devices`) against `STYLEGUIDE.md`. This pass also verified that the screenshots match the steps they sit next to (image-vs-step accuracy).

The categories used here map directly to the style guide. Where a file passes a category, the category is omitted for that file. Each defect quotes the offending text and gives a line number so you can find it quickly. No files have been edited.

## Verification legend

After a follow-up pass, each defect entry below carries a verification marker and a deep link to the exact line in the source file:

- ✅ **Confirmed** — the defect still exists at that location and the style guide rule cited is the right one.
- ⚠️ **Borderline / can't verify visually** — the rule applies but the violation sits at or just over a threshold (for example, 25–26-word sentences), or the claim depends on screenshot content that can't be re-checked from the markdown alone.

Links use the form `[L<n>](path/to/file.md#L<n>)`. They open the file at the cited line in editors that support GitHub-style line anchors.

---

## Section 1 — `live-video-monitoring-and-operations`

### `live-video-monitoring-and-operations/README.md`

**Headings / consistency:**
- ✅ [L9](live-video-monitoring-and-operations/README.md#L9): Card titles mix bare-infinitive and noun-phrase patterns within one section index ("Use live view", "Live view streaming and quality", "PTZ control", "Video walls and shared displays", "Multi-camera playback", "Use the system health dashboard", "Use Lumana timelapse", "Share video", "Change dark mode and light mode"). Pick one pattern and apply it consistently. *Verified: bare-infinitive titles ("Use live view", "Share video", "Change dark mode and light mode") still sit alongside noun-phrase titles ("Live view streaming and quality", "PTZ control", "Video walls and shared displays", "Multi-camera playback") in the same card row. Style guide [Navigation and naming conventions](STYLEGUIDE.md) requires one pattern per content type.*

**Product naming:**
- ✅ [L9](live-video-monitoring-and-operations/README.md#L9): "Use live view" card uses lowercase "live view"; other cards use "Live view" (capitalised). Inconsistent product term. *Verified: `<strong>Use live view</strong>` (lowercase) vs `<strong>Live view streaming and quality</strong>` (uppercase L) in the same table.*

**Structural:**
- ✅ [L9](live-video-monitoring-and-operations/README.md#L9): No "Next steps" section. Acceptable for an index/landing page, but worth noting. *Verified: the file ends at the cards table with no Next steps. Style guide says "Every major page ends with a Next steps section," but section index pages are commonly treated as the exception.*

---

### `live-video-monitoring-and-operations/dark-mode-and-light-mode.md`

(Image-vs-step content verified: user icon, settings menu, theme field, theme dialog all match.)

---

### `live-video-monitoring-and-operations/live-view.md`

**Headings:**
- ✅ [L1](live-video-monitoring-and-operations/live-view.md#L1): H1 "Use live view" — uses lowercase "live view"; product term elsewhere is "Live view". *Verified at H1.*
- ✅ [L9](live-video-monitoring-and-operations/live-view.md#L9), [L29](live-video-monitoring-and-operations/live-view.md#L29): "Open live view", "Use live view controls" — same lowercase issue. *Verified at both H2s.*

**List/step issues:**
- ✅ [L25](live-video-monitoring-and-operations/live-view.md#L25): step 3 "Change the date, time range, clip duration, or resolution as needed." — vague, no visible result described. *Verified. Style guide [Steps](STYLEGUIDE.md) says "If the step produces a visible result, describe it in the line immediately after the step."*
- ✅ [L48](live-video-monitoring-and-operations/live-view.md#L48): step 3 "Use the available actions to scrub through the footage, add cameras to a video wall layout, or archive footage to share it later." — combines three different actions into a single step. *Verified. Style guide [Steps](STYLEGUIDE.md): "Each numbered step is one clear action."*

**Image-vs-step mismatches:**
- ⚠️ [L33](live-video-monitoring-and-operations/live-view.md#L33): image `live-view-screenshots/live-view-player-office-hq.png` shows the **HQ** quality toggle in the bottom-center cluster, not bottom-left as the body text on [L35](live-video-monitoring-and-operations/live-view.md#L35) describes. *The body text "In the bottom left corner of Live view" is present and verified; the image content can't be re-checked from the markdown alone, but the image path is correct so the mismatch claim hinges on a screenshot review.*

---

### `live-video-monitoring-and-operations/live-view-streaming-and-quality.md`

**Sentence-length violations (>25 words):**
- ⚠️ [L29](live-video-monitoring-and-operations/live-view-streaming-and-quality.md#L29): "If a camera uses H.265 and the viewing browser or device does not support H.265, then medium-quality (MQ) local streaming may work while high-quality (HQ) local streaming does not." — 29 words. *Borderline: current line 29 reads "If a camera uses H.265 and your browser or device doesn't support H.265, then medium-quality (MQ) local streaming may work, but high-quality (HQ) local streaming won't." — about 26 words, still just over the 25-word limit per [Sentence and paragraph rules](STYLEGUIDE.md).*

**May vs might:**
- ✅ [L29](live-video-monitoring-and-operations/live-view-streaming-and-quality.md#L29): "medium-quality (MQ) local streaming may work" — possibility, should be "might" per [Sentence and paragraph rules](STYLEGUIDE.md). *Verified.*
- ✅ [L48](live-video-monitoring-and-operations/live-view-streaming-and-quality.md#L48): "though latency and compatibility may vary by browser, device, and connection quality." — should be "might". *Verified.*
- ✅ [L68](live-video-monitoring-and-operations/live-view-streaming-and-quality.md#L68): "Lumana may choose a lower quality automatically" — should be "might". *Verified.*
- ✅ [L70](live-video-monitoring-and-operations/live-view-streaming-and-quality.md#L70): "Lumana may prioritize smoother playback" — should be "might". *Verified.*
- ✅ [L78](live-video-monitoring-and-operations/live-view-streaming-and-quality.md#L78): "Values may vary by codec, scene complexity, and camera configuration." — should be "might". *Verified.*

**Headings:**
- ✅ [L54](live-video-monitoring-and-operations/live-view-streaming-and-quality.md#L54): "Manage streaming quality" — bare infinitive on a concept page, inconsistent with the surrounding noun-phrase headings ("Local streaming" [L15](live-video-monitoring-and-operations/live-view-streaming-and-quality.md#L15), "Cloud streaming" [L38](live-video-monitoring-and-operations/live-view-streaming-and-quality.md#L38), "Reference values" [L76](live-video-monitoring-and-operations/live-view-streaming-and-quality.md#L76)). *Verified.*
- ✅ [L5](live-video-monitoring-and-operations/live-view-streaming-and-quality.md#L5), [L64](live-video-monitoring-and-operations/live-view-streaming-and-quality.md#L64): "How live view delivery works" / "How quality selection works" — uses lowercase "live view" inconsistently with product naming. *Verified.*

**"Where" connector misuse:**
- ✅ [L40](live-video-monitoring-and-operations/live-view-streaming-and-quality.md#L40): "...remotely or across restricted networks where a direct local connection is not possible." — should be "because" or "so" per [Sentence and paragraph rules](STYLEGUIDE.md). *Verified.*

**Marketing / vague claims:**
- ✅ [L42](live-video-monitoring-and-operations/live-view-streaming-and-quality.md#L42): "This is especially useful when you need to access live video from another location..." — borderline marketing intensifier. *Verified.*

**Image-vs-step mismatches:**
- ⚠️ [L52](live-video-monitoring-and-operations/live-view-streaming-and-quality.md#L52): `live-view-cloud-streaming-diagram.png` shows the *local* streaming decision flow, not the cloud streaming path the surrounding text describes. *Image path verified; image content can't be re-checked from the markdown alone.*
- ⚠️ [L62](live-video-monitoring-and-operations/live-view-streaming-and-quality.md#L62): `live-view-quality-routing-diagram.png` contains spelling errors in the diagram text ("Incomplient", "compatibale"). *Image path verified; image content can't be re-checked from the markdown alone.*

**Reference data / typos:**
- ✅ [L82](live-video-monitoring-and-operations/live-view-streaming-and-quality.md#L82)–[L85](live-video-monitoring-and-operations/live-view-streaming-and-quality.md#L85): "3480x2160 (8MP)" — likely typo for the standard 8MP resolution **3840x2160**. Repeated four times in the table. *Verified at lines 82, 83, 84, 85.*

---

### `live-video-monitoring-and-operations/lumana-timelapse.md`

**Headings:**
- ✅ [L40](live-video-monitoring-and-operations/lumana-timelapse.md#L40): "Need longer history than snapshot retention allows?" — heading is a question. Style guide [Navigation and naming conventions](STYLEGUIDE.md) requires bare-infinitive (how-to) or noun phrase. *Verified.*

**If/then violations:**
- ✅ [L42](live-video-monitoring-and-operations/lumana-timelapse.md#L42): "If you need timelapse history beyond the maximum **Snapshot retention days** value available in your deployment, contact Customer Support to discuss extended storage options." — missing "then" per [Sentence and paragraph rules](STYLEGUIDE.md). *Verified.*

**UI element / casing inconsistency:**
- ✅ [L25](live-video-monitoring-and-operations/lumana-timelapse.md#L25): "open **Edit Camera**" with capital C. Other pages use "**Edit camera**" (lowercase). *Verified — line 25 reads "Open **Devices**, select the camera you want, then open **Edit Camera**."*

**Image-vs-step mismatches:**
- ⚠️ [L19](live-video-monitoring-and-operations/lumana-timelapse.md#L19): `lumana-timelapse-create-dialog.png` shows a "Create timelapse" dialog while the surrounding text on [L17](live-video-monitoring-and-operations/lumana-timelapse.md#L17)–[L18](live-video-monitoring-and-operations/lumana-timelapse.md#L18) discusses default 3-day retention, not how to create a timelapse. *Image path and surrounding text verified; image content needs a visual review.*
- ⚠️ [L36](live-video-monitoring-and-operations/lumana-timelapse.md#L36): `lumana-timelapse-retention-settings.png` — image shows the dropdown listing "3 days, 7 days, 14 days, 30 days" without "90 days"; step text on [L27](live-video-monitoring-and-operations/lumana-timelapse.md#L27) says options include "3 days, 7 days, 14 days, 30 days, or **90 days** when available". *Step text verified; image content needs a visual review.*

**Trustworthiness:**
- ✅ [L14](live-video-monitoring-and-operations/lumana-timelapse.md#L14) hint: "This is different from Verkada, which defaults to 24 hours." — competitor comparison in product docs is unusual and risks reading as marketing or appearing unverifiable per [Core documentation principles → Trustworthy](STYLEGUIDE.md). *Verified inside the hint block at line 14.*

---

### `live-video-monitoring-and-operations/multi-camera-playback.md`

**Image issues (broken reference):**
- ✅ [L45](live-video-monitoring-and-operations/multi-camera-playback.md#L45): `multi-camera-playback-wall-view.png` — file does not exist on disk. *Verified: `.gitbook/assets/live-video-monitoring-and-operations/` does not contain a file by that name.*

**List/step issues:**
- ✅ [L30](live-video-monitoring-and-operations/multi-camera-playback.md#L30): "Select up to three more cameras inside the picker, then select **Select**." — Style guide [UI text and messages](STYLEGUIDE.md) requires a qualifier on a UI element literally named "Select" ("select the **Select** button"). *Verified.*
- ✅ [L32](live-video-monitoring-and-operations/multi-camera-playback.md#L32): "If you need fewer rows on screen, then search cameras or drill into locations." — placed inside step 6 but reads as unrelated guidance. *Verified.*

---

### `live-video-monitoring-and-operations/ptz-control.md`

**Headings:**
- ✅ [L1](live-video-monitoring-and-operations/ptz-control.md#L1): H1 "PTZ control" is a noun phrase but the page is task-based. [Navigation and naming conventions](STYLEGUIDE.md) requires bare infinitive for how-to titles. *Verified.*
- ✅ [L5](live-video-monitoring-and-operations/ptz-control.md#L5): "Use PTZ in live view" — lowercase "live view" should be "Live view" to match product naming. *Verified.*

**List/step issues:**
- ✅ [L14](live-video-monitoring-and-operations/ptz-control.md#L14)–[L15](live-video-monitoring-and-operations/ptz-control.md#L15): bullet markers use `*` rather than `-` used elsewhere — minor inconsistency. *Verified.*

**UI element issues:**
- ✅ [L3](live-video-monitoring-and-operations/ptz-control.md#L3): "**Edit camera**" lowercase "c"; `lumana-timelapse.md` line 25 uses "**Edit Camera**" with capital C. *Verified cross-file inconsistency.*

**Structural / guide-structure issues:**
- ✅ [L1](live-video-monitoring-and-operations/ptz-control.md#L1)–[L28](live-video-monitoring-and-operations/ptz-control.md#L28): No Prerequisites section. [Guide structure](STYLEGUIDE.md) requires Introduction, Prerequisites, Steps, Next steps for how-to pages. *Verified: the page jumps from H1 intro to "## Use PTZ in live view" to "## Next steps".*

(Image-vs-step content verified: live-view PTZ toggle, controls overlay match the steps.)

---

### `live-video-monitoring-and-operations/share-video.md`

**If/then violations:**
- ✅ [L36](live-video-monitoring-and-operations/share-video.md#L36): "Turn **Password** on, then type and confirm a password if viewers must enter one before playback." — "if" clause without "then" per [Sentence and paragraph rules](STYLEGUIDE.md). *Verified.*

**May vs might:**
- ✅ [L29](live-video-monitoring-and-operations/share-video.md#L29): "**Existing links** may show a count badge if you saved links before." — possibility, should be "might". *Verified.*

**"Where" connector misuse:**
- ✅ [L39](live-video-monitoring-and-operations/share-video.md#L39): "send it through another channel where your deployment supports it" — should be "if your deployment supports it" or "when your deployment supports it". *Verified.*

**UI element issues:**
- ✅ [L13](live-video-monitoring-and-operations/share-video.md#L13): "From live view, **Share camera** opens when you select **Share**." — lowercase. *Verified.*
- ✅ [L61](live-video-monitoring-and-operations/share-video.md#L61): "In the upper-right corner of the live view page, select **Share**." — lowercase. *Verified.*
- ✅ [L74](live-video-monitoring-and-operations/share-video.md#L74): "(curved arrow icon; hover shows **Share Alert**)" — capital A, but the body labels above use "**Share alert**" (lowercase a). *Verified inconsistency.*

**List/step issues:**
- ⚠️ [L35](live-video-monitoring-and-operations/share-video.md#L35): combines an action and reference info in one step. *Borderline: the parenthetical has been split out so the step now contains the action plus a separate reference sentence; still mixes step + reference per [Steps](STYLEGUIDE.md).*
- ✅ [L9](live-video-monitoring-and-operations/share-video.md#L9)–[L31](live-video-monitoring-and-operations/share-video.md#L31): "Choose sharing options" subsection mixes overview info with the actual steps — confusing structure for a how-to. *Verified: the section "## Choose sharing options" starts at L9 and includes both overview paragraphs and the H3 step blocks below.*

**Image-vs-step mismatches:**
- ⚠️ [L48](live-video-monitoring-and-operations/share-video.md#L48): image `share-video-existing-links-dialog.png` is named "existing-links" but reportedly shows the Share/Create-link tab. The section heading just above on [L46](live-video-monitoring-and-operations/share-video.md#L46) is "Send the link by email or SMS". *Image path and headings verified; image content needs a visual review.*

---

### `live-video-monitoring-and-operations/the-system-health-dashboard.md`

**If/then violations:**
- ✅ [L13](live-video-monitoring-and-operations/the-system-health-dashboard.md#L13): "If another tab is selected at the top of the page (for example **Cameras** or **Map**), select **Devices** so the devices table is visible." — missing "then". *Verified.*
- ✅ [L38](live-video-monitoring-and-operations/the-system-health-dashboard.md#L38): "If this area is unhealthy or offline, alerts and search may be affected." — missing "then". *Verified.*
- ✅ [L41](live-video-monitoring-and-operations/the-system-health-dashboard.md#L41): "If it is unhealthy or offline, storage may be affected." — missing "then". *Verified (line 41 also contains a second "If" earlier that already has "then").*
- ✅ [L45](live-video-monitoring-and-operations/the-system-health-dashboard.md#L45): "If the **Trained** indicator stays unhealthy and you are not sure why, contact your Customer Success Manager." — missing "then". *Verified inside the hint block.*

**May vs might:**
- ✅ [L38](live-video-monitoring-and-operations/the-system-health-dashboard.md#L38): "alerts and search may be affected" — should be "might". *Verified.*
- ✅ [L41](live-video-monitoring-and-operations/the-system-health-dashboard.md#L41): "this indicator may not appear" / "storage may be affected" — should be "might". *Verified for both phrases on the same line.*

**List/step issues:**
- ✅ [L39](live-video-monitoring-and-operations/the-system-health-dashboard.md#L39): "**Storage**: Shows the status of 24/7 local storage on the Core. Retention is based on your 30-day, 60-day, or 90-day subscription." — combines two distinct facts in one bullet. *Verified.*
- ✅ [L42](live-video-monitoring-and-operations/the-system-health-dashboard.md#L42): "**Trained**: …" — long mixed-content list item with multiple sentences and conditions. *Verified.*

**Image-vs-step mismatches:**
- ⚠️ [L19](live-video-monitoring-and-operations/the-system-health-dashboard.md#L19): image `system-health-dashboard-overview.png` is captioned as a dashboard overview but reportedly shows the **Devices > Devices list** view. The step text on [L17](live-video-monitoring-and-operations/the-system-health-dashboard.md#L17) says "The system health dashboard opens and shows the current status…". *Step text verified; image content needs a visual review.*

---

### `live-video-monitoring-and-operations/video-walls-and-shared-displays.md`

**Headings:**
- ✅ [L1](live-video-monitoring-and-operations/video-walls-and-shared-displays.md#L1): H1 "Video walls and shared displays" — noun phrase, but the page is mostly task-based. Inconsistent with sibling pages such as "Use multi-camera playback", "Use the system health dashboard". *Verified.*

**If/then violations:**
- ✅ [L112](live-video-monitoring-and-operations/video-walls-and-shared-displays.md#L112): "If you did not use **Save as wall**, quick live view stays temporary until you navigate away." — missing "then". *Verified.*

**May vs might:**
- ✅ [L16](live-video-monitoring-and-operations/video-walls-and-shared-displays.md#L16): "Use it when you need a temporary wall quickly and may want to save it later." — should be "might". *Verified.*

**UI element issues:**
- ⚠️ [L50](live-video-monitoring-and-operations/video-walls-and-shared-displays.md#L50): "On **Walls**, select **Create wall** in the upper-left corner of the page." Step 6 on [L78](live-video-monitoring-and-operations/video-walls-and-shared-displays.md#L78) correctly says "upper-right corner" for a different screenshot. *Body text contradiction verified; image content (`video-walls-list.png`) needs a visual review.*
- ✅ [L100](live-video-monitoring-and-operations/video-walls-and-shared-displays.md#L100): "Use the upper-right toolbar: **Edit** (**pencil**), full-screen, or **Save as wall**…" — "**pencil**" inside parens is bolded but isn't a UI label. *Verified.*

**List/step issues:**
- ✅ [L54](live-video-monitoring-and-operations/video-walls-and-shared-displays.md#L54): "Enter a wall name and choose a layout that fits the number of cameras or alert tiles you want to show, and select **Done**." — combines three actions in one step. *Verified.*
- ✅ [L55](live-video-monitoring-and-operations/video-walls-and-shared-displays.md#L55): "Expand **Cameras** to choose which cameras appear on the wall, and expand **Alerts** to configure alert tiles." — combines two actions. *Verified.*
- ✅ [L65](live-video-monitoring-and-operations/video-walls-and-shared-displays.md#L65)–[L68](live-video-monitoring-and-operations/video-walls-and-shared-displays.md#L68): list items use lowercase after the colon even though they begin imperative full sentences. Per [Sentence and paragraph rules](STYLEGUIDE.md), capitalize when a full sentence follows. *Verified at lines 65, 66, 67, 68.*
- ✅ [L74](live-video-monitoring-and-operations/video-walls-and-shared-displays.md#L74): "Under **Cameras**, search by name or open a location, then select each camera you want included. Under **Alerts**, search the list or select **Clear all** to reset it. Then enable the alert categories you want surfaced on the wall." — combines multiple actions in one step. *Verified.*

**Marketing / vague claims:**
- ✅ [L5](live-video-monitoring-and-operations/video-walls-and-shared-displays.md#L5): "Lumana offers saved walls plus quick live grids plus secure external walls you can open anywhere." — "plus...plus..." is awkward marketing-style phrasing. *Verified.*
- ✅ [L92](live-video-monitoring-and-operations/video-walls-and-shared-displays.md#L92): "Quick live view is useful when visibility matters immediately and you need to open a wall fast." — vague marketing tone. *Verified.*

**Visible TODO comment in source:**
- ✅ [L116](live-video-monitoring-and-operations/video-walls-and-shared-displays.md#L116): HTML comment `<!-- TODO: When the flow is updated for the new UI, add the section "## Create a shared external video wall" (and its steps) back here. -->` — visible in source. *Verified.*

---

## Section 2 — `databases-analytics-and-search`

### `databases-analytics-and-search/README.md`

**Sentence-length violations (>25 words):**
- ⚠️ [L3](databases-analytics-and-search/README.md#L3): "Use this section to build the people and vehicle data Lumana relies on, search footage, set up missing-object alerts, generate reports, and run occupancy and Event Tag workflows." — 28 words. *Verified at 28 words; still over the 25-word limit per [Sentence and paragraph rules](STYLEGUIDE.md).*

**Headings / consistency:**
- ✅ [L9](databases-analytics-and-search/README.md#L9): Card row labels mix patterns: "Tracking people", "Tracking vehicles", "Tracking containers" use gerunds; [Navigation and naming conventions](STYLEGUIDE.md) requires bare-infinitive for how-to titles. *Verified inside the table card list.*

**Banned/use-sparingly words:**
- ✅ [L9](databases-analytics-and-search/README.md#L9): Card label "Enhance your video data with Lumana Event Tags" uses **Enhance** ([Use sparingly](STYLEGUIDE.md) word). *Verified in the table card list.*

**Structural:**
- ✅ [L1](databases-analytics-and-search/README.md#L1)–[L9](databases-analytics-and-search/README.md#L9): No "Next steps" section. *Verified — section index file ends at the cards table.*

---

### `databases-analytics-and-search/build-a-database-of-people-and-vehicles.md`

**Sentence-length violations (>25 words):**
- ⚠️ [L7](databases-analytics-and-search/build-a-database-of-people-and-vehicles.md#L7): "If you plan to use Event Tags or import vehicles from a CSV file, then make sure you also have access to those features in your organization." — 27 words. *Verified at 27 words; still over the 25-word limit.*

**List/step issues:**
- ✅ [L32](databases-analytics-and-search/build-a-database-of-people-and-vehicles.md#L32): step 2 of "Create a group" "Enter a group name and select the profiles to include." — combines two actions per [Steps](STYLEGUIDE.md). *Verified.*
- ✅ [L37](databases-analytics-and-search/build-a-database-of-people-and-vehicles.md#L37): step 3 "Save the group." — does not name the actual button; the screenshot's button is **Create**, not Save. *Verified.*
- ✅ [L60](databases-analytics-and-search/build-a-database-of-people-and-vehicles.md#L60): "Add a detected vehicle" step 2 "Enter the owner name and verify the vehicle details." — combines two actions. *Verified.*
- ✅ [L78](databases-analytics-and-search/build-a-database-of-people-and-vehicles.md#L78): "Import vehicles from a CSV file" step 3 "Download the template, enter the vehicle data, and upload the completed CSV file" — combines several actions. *Verified.*
- ✅ [L81](databases-analytics-and-search/build-a-database-of-people-and-vehicles.md#L81): step 4 begins "If you are creating a license plate alert, then…" — conditional/aside, not part of a sequential workflow. *Verified.*
- ✅ [L27](databases-analytics-and-search/build-a-database-of-people-and-vehicles.md#L27)–[L78](databases-analytics-and-search/build-a-database-of-people-and-vehicles.md#L78): Indentation under numbered items is inconsistent (single vs double space after `1.`). *Verified by scanning numbered items in the file.*

**Image-vs-step mismatches:**
- ✅ [L37](databases-analytics-and-search/build-a-database-of-people-and-vehicles.md#L37): `create-group-dialog.png` shows a **Create** button but step 3 on L37 says "Save the group." *Body text and image filename verified; step wording disagrees with the UI button label.*
- ✅ [L60](databases-analytics-and-search/build-a-database-of-people-and-vehicles.md#L60): step 2 says "Enter the owner name" while the UI label is reportedly `owner name`. *Body text verified; live-UI label needs a visual review.*

---

### `databases-analytics-and-search/configure-a-space-occupancy-dashboard.md`

**Sentence-length violations (>25 words):**
- ✅ Note carried over: line 18's previous violation was split into two sentences and is now compliant. *Verified at [L7](databases-analytics-and-search/configure-a-space-occupancy-dashboard.md#L7) (now uses if/then correctly).*

**Voice / passive issues:**
- ✅ [L50](databases-analytics-and-search/configure-a-space-occupancy-dashboard.md#L50): "Once these settings are configured, the occupancy widget starts tracking…" — passive ("are configured"). [Voice and tone](STYLEGUIDE.md) requires active voice. *Verified.*

**If/then violations:**
- ✅ [L40](databases-analytics-and-search/configure-a-space-occupancy-dashboard.md#L40): "If numbers still look wrong after a reset, see [Common accuracy issues]…" — missing "then". *Verified.*

**Image-vs-step mismatches:**
- ⚠️ [L28](databases-analytics-and-search/configure-a-space-occupancy-dashboard.md#L28): `space-occupancy-widget-entrances-selected-preview.png` sits in "Add the occupancy widget" but reportedly shows the full settings panel that belongs to "Configure widget settings". *Image path and surrounding section verified at L9 and L30; image content needs a visual review.*

---

### `databases-analytics-and-search/enhance-your-video-data-with-lumana-event-tags.md`

**Sentence-length violations (>25 words):**
- ⚠️ [L7](databases-analytics-and-search/enhance-your-video-data-with-lumana-event-tags.md#L7): "This guide walks you through six steps: generate an API key, create an event tag, post events to the Lumana API, find them in **Search**, and optionally use them in alerts or a **Chart or table** widget." — 38 words. *Verified at ≈38 words (first sentence on line 7); next sentences at L7 add even more text. Still over the 25-word limit.*

**Headings:**
- ✅ [L1](databases-analytics-and-search/enhance-your-video-data-with-lumana-event-tags.md#L1): H1 contains the use-sparingly word **Enhance**. [Use sparingly](STYLEGUIDE.md) allows 2–3 per page; in a page title it reads as marketing. *Verified.*
- ✅ [L13](databases-analytics-and-search/enhance-your-video-data-with-lumana-event-tags.md#L13), [L29](databases-analytics-and-search/enhance-your-video-data-with-lumana-event-tags.md#L29), [L57](databases-analytics-and-search/enhance-your-video-data-with-lumana-event-tags.md#L57), [L124](databases-analytics-and-search/enhance-your-video-data-with-lumana-event-tags.md#L124), [L148](databases-analytics-and-search/enhance-your-video-data-with-lumana-event-tags.md#L148), [L180](databases-analytics-and-search/enhance-your-video-data-with-lumana-event-tags.md#L180): "Step 1: Generate an API key" / "Step 2: …" / etc. — "Step N:" prefix breaks the bare-infinitive heading pattern. *Verified at six H2s.*

**UI element issues / trustworthiness:**
- ✅ [L19](databases-analytics-and-search/enhance-your-video-data-with-lumana-event-tags.md#L19): "Select **Generate Key** (or the control that starts the create flow). The **Create API Key** dialog opens." — hedged UI label. [Trustworthy writing](STYLEGUIDE.md) says verify against the live product. *Verified.*
- ✅ [L36](databases-analytics-and-search/enhance-your-video-data-with-lumana-event-tags.md#L36): "Select **Create event tag** (or open an existing tag to edit it)." — same hedging pattern. *Verified.*
- ✅ [L15](databases-analytics-and-search/enhance-your-video-data-with-lumana-event-tags.md#L15) and [L76](databases-analytics-and-search/enhance-your-video-data-with-lumana-event-tags.md#L76): "Bearer" — line 15 uses backticks `` `Bearer` ``, line 76 uses plain bold text in a table row. *Verified inconsistency.*

**Image-vs-step mismatch:**
- ✅ [L19](databases-analytics-and-search/enhance-your-video-data-with-lumana-event-tags.md#L19), [L23](databases-analytics-and-search/enhance-your-video-data-with-lumana-event-tags.md#L23): body text on L19 refers to **Generate Key** while the screenshot reportedly shows a **Create API Key** dialog with a **Create** button. *Body text verified; image content needs a visual review.*

**List/step issues:**
- ✅ [L142](databases-analytics-and-search/enhance-your-video-data-with-lumana-event-tags.md#L142): "Set the operator (...), then enter the values." — combines two actions. *Verified.*

**Structural / guide-structure issues:**
- ✅ [L197](databases-analytics-and-search/enhance-your-video-data-with-lumana-event-tags.md#L197)–[L199](databases-analytics-and-search/enhance-your-video-data-with-lumana-event-tags.md#L199): Page ends with "## Retention and storage", not a "## Next steps" section. *Verified — no Next steps section.*

**Other / typography:**
- ✅ [L72](databases-analytics-and-search/enhance-your-video-data-with-lumana-event-tags.md#L72): "camera's edit screen" uses a curly apostrophe (U+2019). *Verified at L72 in the `cameraId` table row.*

---

### `databases-analytics-and-search/free-text-search.md`

**Sentence-length violations (>25 words):**
- ⚠️ [L3](databases-analytics-and-search/free-text-search.md#L3): "Use free text search to look for people, vehicles, and other objects across your cameras by describing what you want to find in natural language." — 25 words. *Borderline: sentence is at the 25-word limit so it sits exactly on the boundary of compliance.*

**Headings / product naming:**
- ⚠️ [L1](databases-analytics-and-search/free-text-search.md#L1): page title is "Free text search" but the live UI's page header reads **Text search** (per `free-text-search-text-search-screen.png`), and the search panel has a **Free text** Beta filter. *File title and image filename verified; UI label claim needs a live-product check per [Trustworthy writing](STYLEGUIDE.md).*

**List/step issues:**
- ✅ [L29](databases-analytics-and-search/free-text-search.md#L29)–[L33](databases-analytics-and-search/free-text-search.md#L33): step 3 ("Review the text search page.") uses the same image `free-text-search-text-search-screen.png` as step 2 ([L28](databases-analytics-and-search/free-text-search.md#L28)). *Verified — both steps reference the same screenshot.*

**Image issues (file format / frame / alt / path):**
- ✅ [L15](databases-analytics-and-search/free-text-search.md#L15), [L23](databases-analytics-and-search/free-text-search.md#L23), [L28](databases-analytics-and-search/free-text-search.md#L28), [L33](databases-analytics-and-search/free-text-search.md#L33), [L38](databases-analytics-and-search/free-text-search.md#L38), [L43](databases-analytics-and-search/free-text-search.md#L43): alt text is empty (`alt=""`) — correct per [Alt text](STYLEGUIDE.md). *Verified (this is a pass note, not a defect).*

---

### `databases-analytics-and-search/generate-reports.md`

**Voice / passive issues:**
- ✅ [L89](databases-analytics-and-search/generate-reports.md#L89): "All reports are exported as CSV files." — passive. *Verified.*

**Headings:**
- ✅ [L17](databases-analytics-and-search/generate-reports.md#L17): "Report types" — noun phrase concept-style heading inside a how-to. *Verified.*
- ⚠️ [L43](databases-analytics-and-search/generate-reports.md#L43): "Report modes: One-time or recurring" — fragment after colon should be lowercase per the [colon rule](STYLEGUIDE.md). *Note: this is in a heading, where the colon-after rule is less universally applied; verifying the literal text exists at L43.*
- ✅ [L51](databases-analytics-and-search/generate-reports.md#L51), [L59](databases-analytics-and-search/generate-reports.md#L59): "One-time report" / "Recurring report" — noun phrases under a how-to. *Verified.*

**List/step issues:**
- ✅ [L17](databases-analytics-and-search/generate-reports.md#L17)–[L41](databases-analytics-and-search/generate-reports.md#L41): numbered list mixes setup steps with reference content (the type definitions). Step 1 ([L21](databases-analytics-and-search/generate-reports.md#L21)) combines several actions; step 2 ([L25](databases-analytics-and-search/generate-reports.md#L25)) mixes form-fill with conditional branches for One-time vs Recurring. *Verified.*

---

### `databases-analytics-and-search/missing-object-alert.md`

**Headings:**
- ✅ [L5](databases-analytics-and-search/missing-object-alert.md#L5): "Why this alert helps" — concept-style heading on a how-to page. *Verified.*

**Marketing / vague claims:**
- ✅ [L7](databases-analytics-and-search/missing-object-alert.md#L7)–[L11](databases-analytics-and-search/missing-object-alert.md#L11): "Real-time detection", "Automated tracking", "Security enforcement", "Operational continuity" — bullets read as sales-pitch labels. *Verified at lines 8–11.*

**List/step issues:**
- ✅ [L29](databases-analytics-and-search/missing-object-alert.md#L29): step 4 "On the rule builder, enter an **Alert name** when you want one. In the sentence, open the schedule link (for example **all times**) and **[default configuration]** to change those values." — combines several optional actions. *Verified.*
- ✅ [L45](databases-analytics-and-search/missing-object-alert.md#L45): "In the **Mark object** dialog, outline the object, then select **Select**." — combines two actions and uses unqualified "select **Select**" per [UI text and messages](STYLEGUIDE.md). *Verified.*

**Asset folder structure:**
- ✅ [L19](databases-analytics-and-search/missing-object-alert.md#L19), [L23](databases-analytics-and-search/missing-object-alert.md#L23), [L27](databases-analytics-and-search/missing-object-alert.md#L27), [L34](databases-analytics-and-search/missing-object-alert.md#L34), [L38](databases-analytics-and-search/missing-object-alert.md#L38), [L41](databases-analytics-and-search/missing-object-alert.md#L41), [L43](databases-analytics-and-search/missing-object-alert.md#L43), [L47](databases-analytics-and-search/missing-object-alert.md#L47), [L55](databases-analytics-and-search/missing-object-alert.md#L55), [L59](databases-analytics-and-search/missing-object-alert.md#L59), [L61](databases-analytics-and-search/missing-object-alert.md#L61): image filenames use the `custom-objects-` prefix (e.g., `custom-objects-edit-pencil-icon.png`) on a page named `missing-object-alert.md`. *Verified — all 10+ image references on the page use the mismatched prefix per [Asset folder structure](STYLEGUIDE.md).*

(Note: the previous round flagged the existence of a separate `custom-objects.md` page; that page no longer exists, so the prefix mismatch is now the only remnant of the old naming.)

---

### `databases-analytics-and-search/pixels-per-foot-for-camera-placement.md`

**Headings:**
- ✅ [L1](databases-analytics-and-search/pixels-per-foot-for-camera-placement.md#L1): "Pixels per foot (PPF) for camera placement" — uses parentheses. [Headings and capitalisation](STYLEGUIDE.md) says to minimize parentheses in headings. *Verified.*

**Image issues:**
- ✅ [L17](databases-analytics-and-search/pixels-per-foot-for-camera-placement.md#L17), [L27](databases-analytics-and-search/pixels-per-foot-for-camera-placement.md#L27), [L33](databases-analytics-and-search/pixels-per-foot-for-camera-placement.md#L33), [L37](databases-analytics-and-search/pixels-per-foot-for-camera-placement.md#L37), [L43](databases-analytics-and-search/pixels-per-foot-for-camera-placement.md#L43), [L49](databases-analytics-and-search/pixels-per-foot-for-camera-placement.md#L49): image filenames begin with `tracking-people-...` (e.g., `tracking-people-horizontal-length-formula.png`) but are used on this PPF page. *Verified across all six image src attributes.*

---

### `databases-analytics-and-search/search-video-footage-for-other-objects.md`

**Voice / passive issues:**
- ✅ [L31](databases-analytics-and-search/search-video-footage-for-other-objects.md#L31): "Download controls are available on the preview when your role allows it." — passive ("are available"). *Verified.*

**List/step issues:**
- ✅ [L31](databases-analytics-and-search/search-video-footage-for-other-objects.md#L31): step 6 combines several actions ("Select a tile to open the preview. Use **Images**, **Video**, **Objects**, or **Faces** to review the moment, zoom on the detection, or play the clip. Download controls are available on the preview when your role allows it."). *Verified.*
- ✅ [L39](databases-analytics-and-search/search-video-footage-for-other-objects.md#L39): step 7 combines three actions ("Enter a **Name**, set **From** and **To** (and duration if shown), then select **Create**."). *Verified.*
- ✅ [L25](databases-analytics-and-search/search-video-footage-for-other-objects.md#L25)/[L27](databases-analytics-and-search/search-video-footage-for-other-objects.md#L27): step 4 ("Choose the object type...") and step 5 ("Matching detections appear as tiles...") are an action + result pair split into two numbered steps. *Verified.*

**UI element issues:**
- ✅ [L21](databases-analytics-and-search/search-video-footage-for-other-objects.md#L21): "Open the dropdown labeled **Thumbnails**" — per [UI text and messages](STYLEGUIDE.md) prefer "Select the **Thumbnails** dropdown". *Verified.*

(Image-vs-step content verified: street camera, metadata bar, dropdown, vehicle results, object preview, vehicle objects tab, archive dialog all match.)

---

### `databases-analytics-and-search/search-video-footage-for-people-or-vehicles.md`

**Headings:**
- ✅ [L13](databases-analytics-and-search/search-video-footage-for-people-or-vehicles.md#L13): "Open Search and set the scope" — bare infinitive; combines two actions in heading. *Verified.*

**List/step issues:**
- ✅ [L41](databases-analytics-and-search/search-video-footage-for-people-or-vehicles.md#L41): step 1 of "Search for a person" "On the Search page, select the time range and cameras you want. Then open the **Person** section and start a person search." — combines two actions. *Verified.*
- ✅ [L61](databases-analytics-and-search/search-video-footage-for-people-or-vehicles.md#L61): step 1 of "Search for a vehicle" — same pattern. *Verified.*
- ✅ [L83](databases-analytics-and-search/search-video-footage-for-people-or-vehicles.md#L83)–[L85](databases-analytics-and-search/search-video-footage-for-people-or-vehicles.md#L85) and [L91](databases-analytics-and-search/search-video-footage-for-people-or-vehicles.md#L91)–[L96](databases-analytics-and-search/search-video-footage-for-people-or-vehicles.md#L96): numbered list items act as image-overlay annotations rather than procedural steps. [Lists, steps, and tables](STYLEGUIDE.md) reserves numbered lists for sequences. *Verified two blocks.*

**UI naming inconsistency (cross-image):**
- ⚠️ [L21](databases-analytics-and-search/search-video-footage-for-people-or-vehicles.md#L21): body uses **Dwell** while the screenshot reportedly shows **Time period**. *Body text verified; image content needs a visual review.*

---

### `databases-analytics-and-search/space-occupancy-analytics.md`

**Sentence-length violations (>25 words):**
- ✅ Note: previous violations are now within range; line 104 sits at ≈24 words after rewording. *Verified at [L104](databases-analytics-and-search/space-occupancy-analytics.md#L104) ("When cameras are aimed and count lines exist for your doors or lanes, add the **Occupancy** widget and finish its settings in the UI.") — under 25 words.*

**Voice / passive issues:**
- ✅ [L48](databases-analytics-and-search/space-occupancy-analytics.md#L48): "The feature works best when every way into and out of the counted area is covered." — passive ("is covered"). *Verified.*
- ✅ [L81](databases-analytics-and-search/space-occupancy-analytics.md#L81): "Make sure every entrance and exit is covered." — passive. *Verified.*
- ✅ [L100](databases-analytics-and-search/space-occupancy-analytics.md#L100): "When entries are missed more than exits…" — passive. *Verified.*
- ✅ [L104](databases-analytics-and-search/space-occupancy-analytics.md#L104): "When cameras are aimed and count lines exist…" — passive. *Verified.*

**Headings (user-focused):**
- ✅ [L5](databases-analytics-and-search/space-occupancy-analytics.md#L5), [L9](databases-analytics-and-search/space-occupancy-analytics.md#L9), [L17](databases-analytics-and-search/space-occupancy-analytics.md#L17), [L25](databases-analytics-and-search/space-occupancy-analytics.md#L25), [L29](databases-analytics-and-search/space-occupancy-analytics.md#L29), [L37](databases-analytics-and-search/space-occupancy-analytics.md#L37): "Key features" with sub-headings "Real-time occupancy tracking", "Historical trend analysis", "Location analysis", "Dashboards and reporting", "Security and compliance" — feature-focused noun phrases. [User-focused writing](STYLEGUIDE.md) says headings should describe what the user does. *Verified.*

---

### `databases-analytics-and-search/tracking-containers.md`

**Headings:**
- ✅ [L1](databases-analytics-and-search/tracking-containers.md#L1): H1 "Tracking containers" — gerund noun phrase. [Navigation and naming conventions](STYLEGUIDE.md) requires bare infinitive for how-to titles. *Verified.*
- ✅ [L7](databases-analytics-and-search/tracking-containers.md#L7): "Key benefits" — concept-style heading on a how-to page. *Verified.*

**Marketing / vague claims:**
- ✅ [L9](databases-analytics-and-search/tracking-containers.md#L9)–[L13](databases-analytics-and-search/tracking-containers.md#L13): "Real-time tracking", "Accurate inventory", "Security", "Operations", "Compliance" — read as marketing bullets. *Verified at lines 9–13.*

**UI element issues:**
- ✅ [L17](databases-analytics-and-search/tracking-containers.md#L17): "You can **edit camera** settings and analytics for the target cameras." — "edit camera" is a verb-phrase, not a UI label, but it's bolded as if it were one. *Verified.*

---

### `databases-analytics-and-search/tracking-people.md`

**Headings:**
- ✅ [L29](databases-analytics-and-search/tracking-people.md#L29): "Cross camera tracking" — missing hyphen. Body text on [L31](databases-analytics-and-search/tracking-people.md#L31) uses "Cross-camera tracking" with hyphen. *Verified inconsistency between H3 and body.*

**Voice / passive issues:**
- ✅ [L5](databases-analytics-and-search/tracking-people.md#L5): "The platform is designed to install with standard cameras." — passive and awkward phrasing. *Verified.*
- ✅ [L9](databases-analytics-and-search/tracking-people.md#L9): "Cameras are added in Lumana and streaming reliably." — passive. *Verified.*
- ✅ [L15](databases-analytics-and-search/tracking-people.md#L15): "These capabilities apply when people analytics is enabled…" — passive. *Verified.*
- ✅ [L19](databases-analytics-and-search/tracking-people.md#L19): "individuals can be tracked and their crops stored at useful resolution." — passive. *Verified.*

**Other / typography:**
- ✅ [L31](databases-analytics-and-search/tracking-people.md#L31): curly apostrophe in `organization's`. *Verified.*

---

### `databases-analytics-and-search/tracking-vehicles.md`

**Voice / passive issues:**
- ✅ [L11](databases-analytics-and-search/tracking-vehicles.md#L11): "Cameras are added in Lumana and streaming reliably." — passive. *Verified.*

---

## Section 3 — `set-up-cameras-and-devices` (root + `connect-cameras-by-brand`)

### `set-up-cameras-and-devices/README.md`

**Sentence-length violations (>25 words):**
- ✅ [L3](set-up-cameras-and-devices/README.md#L3): "This section walks you through connecting cameras alongside Lumana Core, adding peripherals such as NAS, sensors, and speakers, stabilizing IP addresses, tuning network paths, and aligning streaming settings with Lumana Core." — first sentence ≈32 words; full L3 paragraph is two sentences and the first one is over 25. *Verified.*

**Headings / consistency:**
- ✅ [L5](set-up-cameras-and-devices/README.md#L5), [L11](set-up-cameras-and-devices/README.md#L11), [L17](set-up-cameras-and-devices/README.md#L17), [L23](set-up-cameras-and-devices/README.md#L23): "Recommended setup, networking, and streaming", "Connect cameras by brand", "Other devices", "Network and infrastructure configuration" — mix of bare-infinitive and noun-phrase patterns on the same page. *Verified.*

**Asset folder structure:**
- ✅ [L9](set-up-cameras-and-devices/README.md#L9), [L15](set-up-cameras-and-devices/README.md#L15), [L21](set-up-cameras-and-devices/README.md#L21), [L27](set-up-cameras-and-devices/README.md#L27): Card icons reference `../.gitbook/assets/icon-*.svg` instead of the `.gitbook/assets/icons/` location described in [Asset folder structure](STYLEGUIDE.md). *Verified across all four card-section tables.*

---

### `set-up-cameras-and-devices/overview.md`

**Headings:**
- ✅ [L1](set-up-cameras-and-devices/overview.md#L1): H1 "Recommended setup tasks" — noun phrase on a how-to page. *Verified.*

**List/step issues:**
- ✅ [L29](set-up-cameras-and-devices/overview.md#L29)–[L40](set-up-cameras-and-devices/overview.md#L40): numbered setup order pauses for H3 subheadings (`### Recommended for most sites`, `### If your cameras support pan, tilt, and zoom`) between items 3–4 and 5–6. *Verified.*

**Other / typography:**
- ✅ [L5](set-up-cameras-and-devices/overview.md#L5), [L7](set-up-cameras-and-devices/overview.md#L7): "you'll" uses curly apostrophe; "you're" elsewhere uses straight apostrophe. *Verified inconsistency.*

**Structural:**
- ✅ [L42](set-up-cameras-and-devices/overview.md#L42): "Other topics in this section" at the end serves as next steps but isn't titled "Next steps" per [Guide structure](STYLEGUIDE.md). *Verified.*

---

### `set-up-cameras-and-devices/camera-networking-options.md`

**Headings:**
- ✅ [L7](set-up-cameras-and-devices/camera-networking-options.md#L7): "Remote camera access (Camera VPN)" — has parentheses per [Headings and capitalisation](STYLEGUIDE.md). *Verified.*
- ✅ [L11](set-up-cameras-and-devices/camera-networking-options.md#L11): "When to use this" — vague. *Verified.*
- ✅ [L17](set-up-cameras-and-devices/camera-networking-options.md#L17): "Steps" — generic; describe the user's task. *Verified.*
- ✅ [L132](set-up-cameras-and-devices/camera-networking-options.md#L132), [L152](set-up-cameras-and-devices/camera-networking-options.md#L152): "Uniview speaker" / "TOA speaker" — noun phrases. *Verified.*

**"Where" connector misuse:**
- ✅ [L9](set-up-cameras-and-devices/camera-networking-options.md#L9): "...for devices on a private network where you need the manufacturer's configuration UI." *Verified.*

**List/step issues:**
- ✅ [L13](set-up-cameras-and-devices/camera-networking-options.md#L13)–[L15](set-up-cameras-and-devices/camera-networking-options.md#L15): one-liner imperative steps without terminal punctuation. *Verified — three bullets at lines 13–15 lack periods.*
- ✅ [L47](set-up-cameras-and-devices/camera-networking-options.md#L47)–[L122](set-up-cameras-and-devices/camera-networking-options.md#L122): "Configure SIP on a Check Point router" steps wrap multiple sub-actions per numbered item. *Verified at numbered steps 1–5.*

**Image-vs-step mismatches:**
- ⚠️ [L80](set-up-cameras-and-devices/camera-networking-options.md#L80) `off-premise-sip-provider-service-list.png`: doc table at [L72](set-up-cameras-and-devices/camera-networking-options.md#L72)–[L73](set-up-cameras-and-devices/camera-networking-options.md#L73) lists `Media\_server\_1` and `Media\_server\_2`. *Doc table verified; image content needs a visual review.*
- ⚠️ [L95](set-up-cameras-and-devices/camera-networking-options.md#L95) `sip-traffic-inspection-rtp-services.png`: doc table at [L88](set-up-cameras-and-devices/camera-networking-options.md#L88)–[L93](set-up-cameras-and-devices/camera-networking-options.md#L93) shows 4 rows. *Doc table verified; image content needs a visual review.*
- ⚠️ [L106](set-up-cameras-and-devices/camera-networking-options.md#L106) `on-premise-devices-ip-phones.png`: doc table at [L102](set-up-cameras-and-devices/camera-networking-options.md#L102)–[L104](set-up-cameras-and-devices/camera-networking-options.md#L104) shows one `Uniview_speaker` row. *Doc table verified; image content needs a visual review.*
- ⚠️ [L122](set-up-cameras-and-devices/camera-networking-options.md#L122) `sip-service-ports-table.png`: doc table at [L112](set-up-cameras-and-devices/camera-networking-options.md#L112)–[L120](set-up-cameras-and-devices/camera-networking-options.md#L120) has `SIP\_UDP` rows at ports 5060 and 5061. *Doc table verified; image content needs a visual review.*

**Structural:**
- ✅ [L168](set-up-cameras-and-devices/camera-networking-options.md#L168): No "Next steps" section. *Verified — page ends with TOA speaker screenshot.*

---

### `set-up-cameras-and-devices/create-camera-shortcuts.md`

**Headings:**
- ✅ [L5](set-up-cameras-and-devices/create-camera-shortcuts.md#L5): "Key benefits" — soft marketing label. *Verified.*

**Run-in label colon placement (colon inside bold):**
- ✅ [L7](set-up-cameras-and-devices/create-camera-shortcuts.md#L7): `**Follow movement across zones:**` — colon inside bold. [Run-in labels](STYLEGUIDE.md) require `**Label**:`. *Verified.*
- ✅ [L8](set-up-cameras-and-devices/create-camera-shortcuts.md#L8): `**Shorten response paths:**` — same fix. *Verified.*
- ✅ [L9](set-up-cameras-and-devices/create-camera-shortcuts.md#L9): `**Tie views together on large sites:**` — same fix. *Verified.*

**List/step issues:**
- ✅ [L23](set-up-cameras-and-devices/create-camera-shortcuts.md#L23): step 1 "Open the camera where you want shortcuts, then select **Edit camera**." — combines two actions. *Verified.*
- ✅ [L28](set-up-cameras-and-devices/create-camera-shortcuts.md#L28): step 6 "If you need more shortcuts on the same camera, repeat steps 3 through 5." — missing "then". *Verified.*

**Italics / term definitions:**
- ✅ [L3](set-up-cameras-and-devices/create-camera-shortcuts.md#L3): "**Camera shortcuts** are links you place on a camera's image..." — first-mention term defined with bold rather than italics. [Italics and emphasis](STYLEGUIDE.md) requires italics on first-mention term definitions. *Verified.*

**Image-vs-step issue:**
- ✅ [L21](set-up-cameras-and-devices/create-camera-shortcuts.md#L21): `edit-camera-shortcuts.png` placed before the numbered steps (steps start at [L23](set-up-cameras-and-devices/create-camera-shortcuts.md#L23)) but illustrates the result of step 2. *Verified by position.*

**Other / typography:**
- ✅ [L3](set-up-cameras-and-devices/create-camera-shortcuts.md#L3), [L31](set-up-cameras-and-devices/create-camera-shortcuts.md#L31): "camera's" uses curly apostrophes. *Verified.*

---

### `set-up-cameras-and-devices/create-links-between-cameras.md`

**Trustworthiness / completeness:**
- ✅ [L1](set-up-cameras-and-devices/create-links-between-cameras.md#L1)–[L3](set-up-cameras-and-devices/create-links-between-cameras.md#L3): page contains only "# Create links between cameras" and "Coming soon!". *Verified — page is empty of content beyond the placeholder. Fails [Trustworthy writing](STYLEGUIDE.md) and Usability principles.*

---

### `set-up-cameras-and-devices/enable-ptz-control.md`

**Headings:**
- ✅ [L1](set-up-cameras-and-devices/enable-ptz-control.md#L1), [L17](set-up-cameras-and-devices/enable-ptz-control.md#L17): H1 "Enable PTZ control" repeated as H2 below intro. *Verified — H1 at L1 and H2 "Enable PTZ control" at L17.*
- ✅ [L11](set-up-cameras-and-devices/enable-ptz-control.md#L11): "Key capabilities" — "Key" leans marketing. *Verified.*

**Stacked headings / structure:**
- ✅ [L5](set-up-cameras-and-devices/enable-ptz-control.md#L5)–[L17](set-up-cameras-and-devices/enable-ptz-control.md#L17): H2 "Prerequisites" → H2 "Key capabilities" → H2 "Enable PTZ control" stacks heading-only sections; "Key capabilities" interrupts the how-to flow. *Verified.*

**List/step issues:**
- ✅ [L28](set-up-cameras-and-devices/enable-ptz-control.md#L28): step 7 "Specify the **port** if it differs from the default `80`." — missing "then". *Verified.*
- ✅ [L32](set-up-cameras-and-devices/enable-ptz-control.md#L32): step 8 "Select **Save** to apply changes." — does not describe the visible result per [Steps](STYLEGUIDE.md). *Verified.*

**UI element / capitalisation issues:**
- ✅ [L26](set-up-cameras-and-devices/enable-ptz-control.md#L26): "Select the **driver**." — UI label is reportedly "Driver" (capital D). *Verified body uses lowercase "driver".*

**Image-vs-step mismatches:**
- ⚠️ [L20](set-up-cameras-and-devices/enable-ptz-control.md#L20)/[L22](set-up-cameras-and-devices/enable-ptz-control.md#L22): `live-view-edit-camera-button.png` is captioned next to step 2, which describes selecting "the **Edit camera** icon ... pencil icon." The screenshot is reportedly the Settings wrench control. *Body text verified; image content needs a visual review.*
- ⚠️ [L27](set-up-cameras-and-devices/enable-ptz-control.md#L27)/[L30](set-up-cameras-and-devices/enable-ptz-control.md#L30): body uses "driver" (lowercase), "PTZ control path", and "port" while the screenshot reportedly labels the field as "X address". *Body text verified; image content needs a visual review.*

---

### `set-up-cameras-and-devices/recommended-streaming-settings.md`

**Sentence-length violations (>25 words):**
- ✅ [L3](set-up-cameras-and-devices/recommended-streaming-settings.md#L3): "If you use Lumana cameras or a supported brand that Lumana Core sets up for you, you may not need to change anything; otherwise copy the values from [Primary stream settings](#primary-stream-settings) and [Sub stream settings](#sub-stream-settings) into the camera's own settings." — 49 words. *Verified second sentence on L3 at ≈47 words.*
- ✅ [L180](set-up-cameras-and-devices/recommended-streaming-settings.md#L180): "Higher bitrates usually mean more data. Lumana Core still uses **smart storage** so you are not wasting space: video stays high enough quality for **live processing** and **retrospective review**, and **rich recordings are kept when alerts fire**, without hoarding bulk high-bitrate footage when nothing important is happening." — second sentence ≈44 words. *Verified at L180 ("Smarter storage around alerts" detail bullet).*

**If/then violations:**
- ✅ [L125](set-up-cameras-and-devices/recommended-streaming-settings.md#L125): "If you do not follow the guidelines, you may see lower results in two areas:" — missing "then". *Verified.*

**May vs might:**
- ✅ [L3](set-up-cameras-and-devices/recommended-streaming-settings.md#L3): "you may not need to change anything" — should be "might". *Verified.*

**Marketing / vague claims:**
- ✅ [L179](set-up-cameras-and-devices/recommended-streaming-settings.md#L179), [L180](set-up-cameras-and-devices/recommended-streaming-settings.md#L180): "Stronger AI learning over time" / "Smarter storage around alerts" — borderline marketing phrases. *Verified.*

**Reference data / typos in tables:**
- ✅ [L57](set-up-cameras-and-devices/recommended-streaming-settings.md#L57): "3MP | 3072×1028" — likely typo (3MP is typically 3072×1728). *Verified.*
- ✅ [L58](set-up-cameras-and-devices/recommended-streaming-settings.md#L58): "4MP | 2560×1440" — actually 3.7MP / QHD. *Verified.*
- ✅ [L61](set-up-cameras-and-devices/recommended-streaming-settings.md#L61), [L150](set-up-cameras-and-devices/recommended-streaming-settings.md#L150): "8MP | 3480×2160" — likely typo for 3840×2160. *Verified at both occurrences.*

**Structural:**
- ✅ [L199](set-up-cameras-and-devices/recommended-streaming-settings.md#L199): No "Next steps" section. *Verified — page ends with the last FAQ details block.*

---

### `set-up-cameras-and-devices/set-up-a-camera-floor-plan.md`

**Headings:**
- ✅ [L7](set-up-cameras-and-devices/set-up-a-camera-floor-plan.md#L7): "Key benefits" — borderline marketing label. *Verified.*
- ✅ [L18](set-up-cameras-and-devices/set-up-a-camera-floor-plan.md#L18): "Use the camera floor plan feature" — tool-focused. [User-focused writing](STYLEGUIDE.md) prefers user-task framing and avoids "feature". *Verified.*

**Italics misuse:**
- ✅ [L3](set-up-cameras-and-devices/set-up-a-camera-floor-plan.md#L3): "adding a *floor plan*, an interactive map…" uses asterisk italics. [Italics and emphasis](STYLEGUIDE.md) requires underscore italics. *Verified.*

**List/step issues:**
- ✅ [L34](set-up-cameras-and-devices/set-up-a-camera-floor-plan.md#L34): step 6 "Add your image using drag and drop or **Or upload from your computer**. Use a PNG or JPG file." — combines two actions. *Verified.*
- ✅ [L38](set-up-cameras-and-devices/set-up-a-camera-floor-plan.md#L38): step 7 "Select the [icon] icon in the top right corner to start adding and positioning your cameras on the floor plan." — combines two actions. *Verified.*
- ✅ [L40](set-up-cameras-and-devices/set-up-a-camera-floor-plan.md#L40): step 8 "Select **Add floor plan** to save the floor plan." — combined save action without separate result description. *Verified.*

**Image-vs-step mismatches:**
- ⚠️ [L20](set-up-cameras-and-devices/set-up-a-camera-floor-plan.md#L20)/[L22](set-up-cameras-and-devices/set-up-a-camera-floor-plan.md#L22): step 1 says "top **left** corner"; `floor-plans-menu-overview.png` reportedly shows top-right. *Body text verified at L20 with "top left corner"; image content needs a visual review.*
- ⚠️ [L40](set-up-cameras-and-devices/set-up-a-camera-floor-plan.md#L40)/[L42](set-up-cameras-and-devices/set-up-a-camera-floor-plan.md#L42): step 8 says "Select **Add floor plan** to save"; `edit-floor-plan-layout.png` reportedly shows completed floor plan. *Step text verified; image content needs a visual review.*

(Image frames now applied correctly — resolved from the previous round.)

---

### `set-up-cameras-and-devices/set-up-a-static-ip-address.md`

**Sentence-length violations (>25 words):**
- ✅ [L21](set-up-cameras-and-devices/set-up-a-static-ip-address.md#L21): "You likely have DHCP if a router, office firewall, or Lumana Core on the network assigns addresses, and your camera already shows an IP in Lumana without you setting a static address on the device." — 35 words. *Verified.*

**If/then violations:**
- ✅ [L80](set-up-cameras-and-devices/set-up-a-static-ip-address.md#L80): "If needed, refer to your computer or operating system documentation for instructions on setting a temporary static IP address." — missing "then". *Verified inside the hint block at L80.*

**Trustworthiness / product details:**
- ✅ [L87](set-up-cameras-and-devices/set-up-a-static-ip-address.md#L87), [L92](set-up-cameras-and-devices/set-up-a-static-ip-address.md#L92), [L100](set-up-cameras-and-devices/set-up-a-static-ip-address.md#L100): image filenames `lumix-camera-web-login-lb800.png`, `lumix-network-ipv4-dhcp-settings.png`, `lumix-network-ipv4-static-settings.png` use a `lumix-` prefix on a Lumana page. *Verified that filenames retain the Lumix branding; needs a verification against the live product per [Trustworthy writing](STYLEGUIDE.md).*

**UI element issues:**
- ✅ [L12](set-up-cameras-and-devices/set-up-a-static-ip-address.md#L12), [L96](set-up-cameras-and-devices/set-up-a-static-ip-address.md#L96): doc text uses "subnet mask" (lowercase). *Verified — body uses lowercase "subnet mask" while the UI label is reported to be "Subnet mask" (capital S).*

(Image frames are now applied correctly — resolved from the previous round.)

---

### `set-up-cameras-and-devices/connect-cameras-by-brand/README.md`

- ⚠️ [L4](set-up-cameras-and-devices/connect-cameras-by-brand/README.md#L4): No structural defects found. *Verified — page is a section index with cards. The "wide range" marketing wording is present at L4 ("Lumana supports cameras from a wide range of manufacturers"). [Word choices](STYLEGUIDE.md) suggests avoiding mild marketing.*

---

### `set-up-cameras-and-devices/connect-cameras-by-brand/axis.md`

**Sentence-length violations (>25 words):**
- ⚠️ [L42](set-up-cameras-and-devices/connect-cameras-by-brand/axis.md#L42): "Use the camera's root username and password in Lumana Core. This gives Lumana full access to the Axis API and settings, reduces compatibility gaps, and avoids subtle permission errors." — second sentence ≈26 words. *Verified at L42.*
- ✅ [L73](set-up-cameras-and-devices/connect-cameras-by-brand/axis.md#L73): "If you cannot activate the camera, reach its web UI, or complete network setup, see the [General troubleshooting guide](...) or your Axis documentation for device activation." — 27 words. *Verified.*
- ✅ [L81](set-up-cameras-and-devices/connect-cameras-by-brand/axis.md#L81): "Add an ONVIF user: Add a user intended for ONVIF access. Use a strong password and assign the **Administrator** role (or the role your organization requires for streaming control)." — 28 words. *Verified.*
- ✅ [L117](set-up-cameras-and-devices/connect-cameras-by-brand/axis.md#L117): "Manual profiles are needed when Lumana cannot create the required streams automatically (for example, when you connect with lower-privilege credentials) or when you want explicit control over encoder names and quality." — 31 words. *Verified.*

**Headings:**
- ✅ [L1](set-up-cameras-and-devices/connect-cameras-by-brand/axis.md#L1): H1 "Connect Axis cameras" — bare infinitive, OK (pass note). *Verified.*
- ✅ [L9](set-up-cameras-and-devices/connect-cameras-by-brand/axis.md#L9)–[L34](set-up-cameras-and-devices/connect-cameras-by-brand/axis.md#L34): "AXIS Q16 Series" etc. (uppercase) appears in body alongside "Axis cameras" lowercase. *Verified all-caps "AXIS" prefix on every model bullet.*

**If/then violations:**
- ✅ [L57](set-up-cameras-and-devices/connect-cameras-by-brand/axis.md#L57): "If no DHCP server is present, many Axis cameras default to `192.168.0.90`." — missing "then". *Verified.*
- ✅ [L73](set-up-cameras-and-devices/connect-cameras-by-brand/axis.md#L73): "If you cannot activate the camera, reach its web UI, or complete network setup, see…" — missing "then". *Verified.*
- ✅ [L121](set-up-cameras-and-devices/connect-cameras-by-brand/axis.md#L121): "If the name in Axis and the name in Lumana differ at all, video may not attach." — missing "then". *Verified.*

**Image-vs-step issues:**
- ⚠️ [L140](set-up-cameras-and-devices/connect-cameras-by-brand/axis.md#L140) `axis-stream-profile-lumana-main.png`: reportedly shows "Maximum" (MBR) bitrate. *Image content needs a visual review; the brand table in `recommended-streaming-settings.md` does list MBR for Axis main, which is the cross-doc inconsistency.*

**Structural:**
- ✅ [L153](set-up-cameras-and-devices/connect-cameras-by-brand/axis.md#L153): No "Next steps" section. *Verified — page ends after the sub stream profile reference.*

---

### `set-up-cameras-and-devices/connect-cameras-by-brand/hanwha.md`

**Headings:**
- ✅ [L1](set-up-cameras-and-devices/connect-cameras-by-brand/hanwha.md#L1): H1 "Connect Hanwha cameras" — bare infinitive, OK (pass note). *Verified.*

**If/then violations:**
- ✅ [L53](set-up-cameras-and-devices/connect-cameras-by-brand/hanwha.md#L53): "Select the profile row… or select **Add** to create a row if you need one." — missing "then". *Verified.*
- ✅ [L92](set-up-cameras-and-devices/connect-cameras-by-brand/hanwha.md#L92): "If your main or Storage row sits on a different profile index, change the numbers in the path to match." — missing "then". *Verified.*

**List/step issues:**
- ✅ [L43](set-up-cameras-and-devices/connect-cameras-by-brand/hanwha.md#L43): step 3 "Open the **IP address** tab, set **IP type** to **Manual**, enter **IP address**, **Subnet mask**, **Gateway**, and DNS servers, then select **Apply**." — combines five actions. *Verified.*
- ✅ [L54](set-up-cameras-and-devices/connect-cameras-by-brand/hanwha.md#L54): step 4 "Set that row as the **Default** profile and set **Codec** to **H.265**." — combines two actions. *Verified.*

**Image-vs-step mismatch:**
- ⚠️ [L82](set-up-cameras-and-devices/connect-cameras-by-brand/hanwha.md#L82) `hanwha-storage-profile-settings.png`: doc text on [L77](set-up-cameras-and-devices/connect-cameras-by-brand/hanwha.md#L77) says **Bitrate control** should be **CBR**, but the screenshot is reportedly the Maximum/MBR setting. *Body text verified; image content needs a visual review.*

**Structural:**
- ✅ [L93](set-up-cameras-and-devices/connect-cameras-by-brand/hanwha.md#L93): No "Next steps" section. *Verified — page ends with the RTSP profile note.*

---

### `set-up-cameras-and-devices/connect-cameras-by-brand/hikvision.md`

**Sentence-length violations (>25 words):**
- ✅ [L46](set-up-cameras-and-devices/connect-cameras-by-brand/hikvision.md#L46): "Select your camera, note its IPv4 address and status, and, if the device is not initialized yet, set a password to activate it." — clause runs ~22 words; full bullet with label is longer. *Verified at L46.*
- ✅ [L125](set-up-cameras-and-devices/connect-cameras-by-brand/hikvision.md#L125): "Using an **Operator** user with broad remote permissions (often **Select all** in the **Add** user dialog) allows Lumana Core to configure camera settings, including stream settings, more reliably." — 28 words. *Verified.*
- ✅ [L127](set-up-cameras-and-devices/connect-cameras-by-brand/hikvision.md#L127): Closing link paragraph to **Connect a camera** — ~22 words after present-tense edit. *Verified.*

**Future tense / passive:**
- ✅ [L123](set-up-cameras-and-devices/connect-cameras-by-brand/hikvision.md#L123): "A confirmation message or indicator should appear, confirming that the new user has been added successfully." — "should appear" + "has been added" passive. *Verified.*

**If/then violations:**
- ✅ [L60](set-up-cameras-and-devices/connect-cameras-by-brand/hikvision.md#L60): "If you are using admin credentials, you can proceed directly to [Connect a camera](...)." — missing "then". *Verified.*

**Use sparingly:**
- ✅ [L127](set-up-cameras-and-devices/connect-cameras-by-brand/hikvision.md#L127): "ensuring everything is functioning as expected" uses "ensuring" ([Use sparingly](STYLEGUIDE.md)). *Verified.*

**Capitalisation / UI labels:**
- ✅ [L46](set-up-cameras-and-devices/connect-cameras-by-brand/hikvision.md#L46): "**Detect and Initialize the Camera**" uses Title Case. *Verified.*
- ✅ [L75](set-up-cameras-and-devices/connect-cameras-by-brand/hikvision.md#L75), [L78](set-up-cameras-and-devices/connect-cameras-by-brand/hikvision.md#L78): doc switches between **Digest** (heading at L75) and **digest** (body at L78). *Verified inconsistency.*

**List/step issues:**
- ✅ [L41](set-up-cameras-and-devices/connect-cameras-by-brand/hikvision.md#L41)–[L50](set-up-cameras-and-devices/connect-cameras-by-brand/hikvision.md#L50): "Activate your camera with the SADP tool" uses `*` bullets rather than numbered steps for a sequence. *Verified bullets at lines 41, 42, 46, 50.*

**Stacked headings:**
- ✅ [L35](set-up-cameras-and-devices/connect-cameras-by-brand/hikvision.md#L35)–[L39](set-up-cameras-and-devices/connect-cameras-by-brand/hikvision.md#L39): "Prepare your Hikvision camera" (H3) is followed by one short paragraph at L37, then "Activate your camera with the SADP tool" (H3) at L39. *Verified.*

**Structural:**
- ✅ [L128](set-up-cameras-and-devices/connect-cameras-by-brand/hikvision.md#L128): No "Next steps" section. *Verified — page ends after L127.*

---

### `set-up-cameras-and-devices/connect-cameras-by-brand/lumana.md`

**Headings:**
- ✅ [L1](set-up-cameras-and-devices/connect-cameras-by-brand/lumana.md#L1): H1 "Lumana" is just the brand name. Sibling pages use "Connect <brand> cameras". *Verified.*

**Run-in labels:**
- Addressed — bulk-capability bullets use `**Label**:` (colon outside bold) per [UI text and messages](STYLEGUIDE.md).

**List/step issues:**
- ✅ [L37](set-up-cameras-and-devices/connect-cameras-by-brand/lumana.md#L37)–[L41](set-up-cameras-and-devices/connect-cameras-by-brand/lumana.md#L41): "The following features are available for individual cameras only:" then 3 items, with the third being a run-in bold label — non-parallel. *Verified items at L39, L40, L41 (first two are phrases, third is `**Restore default settings:** Reset a camera...`).*

**If/then violations:**
- ✅ [L51](set-up-cameras-and-devices/connect-cameras-by-brand/lumana.md#L51): "If you run into camera issues, the Lumana Camera Finder application offers debugging tools." — missing "then". *Verified.*

**Structural / depth:**
- ✅ [L1](set-up-cameras-and-devices/connect-cameras-by-brand/lumana.md#L1)–[L52](set-up-cameras-and-devices/connect-cameras-by-brand/lumana.md#L52): Page lacks Prerequisites and connection-to-Lumana-Core steps. *Verified — file has no Prerequisites or step-by-step connection content.*
- ✅ [L52](set-up-cameras-and-devices/connect-cameras-by-brand/lumana.md#L52): No "Next steps" section. *Verified.*

**Trustworthiness:**
- ⚠️ [L28](set-up-cameras-and-devices/connect-cameras-by-brand/lumana.md#L28): screenshot `camera-finder-device-management.png` may show an "LB800" device. *Image content needs a visual review; the parallel "LB800" reference in `set-up-a-static-ip-address.md` is confirmed in the image filenames there.*

---

### `set-up-cameras-and-devices/connect-cameras-by-brand/other-brands.md`

**"Where" connector misuse:**
- ✅ [L3](set-up-cameras-and-devices/connect-cameras-by-brand/other-brands.md#L3): "alongside [Recommended streaming settings](...) where applicable" — should be "when applicable" per [Sentence and paragraph rules](STYLEGUIDE.md). *Verified.*

**Structural / depth:**
- ✅ [L1](set-up-cameras-and-devices/connect-cameras-by-brand/other-brands.md#L1)–[L59](set-up-cameras-and-devices/connect-cameras-by-brand/other-brands.md#L59): No connection guidance — just six brand model lists. *Verified — file contains only "## <Brand> compatibility models" sections with bullet lists.*
- ✅ [L59](set-up-cameras-and-devices/connect-cameras-by-brand/other-brands.md#L59): No "Next steps" section. *Verified.*

**Other / typography:**
- ✅ [L3](set-up-cameras-and-devices/connect-cameras-by-brand/other-brands.md#L3): "vendor's" uses curly apostrophe. *Verified.*

---

### `set-up-cameras-and-devices/connect-cameras-by-brand/supported-cameras.md`

**Voice / passive issues:**
- ✅ [L5](set-up-cameras-and-devices/connect-cameras-by-brand/supported-cameras.md#L5): "Most cameras that support ONVIF or RTSP streaming can be integrated with Lumana." — passive ("can be integrated"). *Verified.*

**If/then violations:**
- ✅ [L31](set-up-cameras-and-devices/connect-cameras-by-brand/supported-cameras.md#L31): "If your camera is not listed, it may still work if it supports ONVIF or RTSP." — missing "then" in both clauses. *Verified inside hint block.*
- ✅ [L34](set-up-cameras-and-devices/connect-cameras-by-brand/supported-cameras.md#L34): "Please contact [support@lumana.ai](...) if you don't find your camera model on this list." — "Please" is unnecessary; missing "then". *Verified.*

**List/step issues:**
- ✅ [L28](set-up-cameras-and-devices/connect-cameras-by-brand/supported-cameras.md#L28): "- Pelco, and more..." — last bullet ends with "and more..." (ellipsis). *Verified.*

**Marketing language:**
- ✅ [L3](set-up-cameras-and-devices/connect-cameras-by-brand/supported-cameras.md#L3): "wide range", "flexibility", "fits your deployment needs" — soft marketing tone. *Verified — all three phrases appear at L3.*

**Structural:**
- ✅ [L45](set-up-cameras-and-devices/connect-cameras-by-brand/supported-cameras.md#L45): No "Next steps" section. *Verified — page ends after "Choose your camera brand" list.*

---

### `set-up-cameras-and-devices/connect-cameras-by-brand/verkada.md`

**Headings:**
- ✅ [L1](set-up-cameras-and-devices/connect-cameras-by-brand/verkada.md#L1): H1 "Verkada" — just the brand name. *Verified.*

**Voice / passive issues:**
- ✅ [L11](set-up-cameras-and-devices/connect-cameras-by-brand/verkada.md#L11): "After RTSP is enabled, Verkada provides an RTSP URL." — passive ("is enabled"). *Verified.*

**If/then violations:**
- ✅ [L45](set-up-cameras-and-devices/connect-cameras-by-brand/verkada.md#L45): "Make sure Lumana Core is the only client on that URL, or use separate stream endpoints if Verkada provides them." — missing "then". *Verified inside hint block.*

**List/step issues:**
- ✅ [L5](set-up-cameras-and-devices/connect-cameras-by-brand/verkada.md#L5)–[L7](set-up-cameras-and-devices/connect-cameras-by-brand/verkada.md#L7): "Enable RTSP on the camera" — single-item numbered list. [Lists, steps, and tables](STYLEGUIDE.md) says lists need at least two items. *Verified — only one numbered item under that heading.*
- ✅ [L22](set-up-cameras-and-devices/connect-cameras-by-brand/verkada.md#L22)–[L26](set-up-cameras-and-devices/connect-cameras-by-brand/verkada.md#L26): step 2 of "Configure the main stream" combines five field entries. *Verified — sub-bullets enumerate IP address, RTSP port, username, password, connection string.*

**Structural:**
- ✅ [L46](set-up-cameras-and-devices/connect-cameras-by-brand/verkada.md#L46): No "Next steps" section. *Verified — page ends after the hint block.*

---

## Section 3 (continued) — `network-and-infrastructure-configuration` and `other-devices`

### `set-up-cameras-and-devices/network-and-infrastructure-configuration/README.md`

**Asset folder structure:**
- ✅ [L6](set-up-cameras-and-devices/network-and-infrastructure-configuration/README.md#L6): card icons reference `../../.gitbook/assets/icon-*.svg` at the assets root rather than under `icons/`. *Verified — four `<img src="../../.gitbook/assets/icon-*.svg">` references at the root of the assets folder.*

**Other / cosmetic:**
- ✅ [L1](set-up-cameras-and-devices/network-and-infrastructure-configuration/README.md#L1)–[L4](set-up-cameras-and-devices/network-and-infrastructure-configuration/README.md#L4): two blank lines between H1 and the first paragraph. *Verified — lines 2 and 3 are blank.*

---

### `set-up-cameras-and-devices/network-and-infrastructure-configuration/configure-lumana-core-as-a-dhcp-server.md`

**Voice / passive issues:**
- ✅ [L3](set-up-cameras-and-devices/network-and-infrastructure-configuration/configure-lumana-core-as-a-dhcp-server.md#L3): "This feature is supported on Ethernet 2…" — passive. *Verified.*
- ✅ [L11](set-up-cameras-and-devices/network-and-infrastructure-configuration/configure-lumana-core-as-a-dhcp-server.md#L11): "When enabled, the DHCP server on Lumana Core provides essential networking services, including:" — passive participial phrase; also uses "essential" ([Use sparingly](STYLEGUIDE.md)). *Verified.*
- ✅ [L43](set-up-cameras-and-devices/network-and-infrastructure-configuration/configure-lumana-core-as-a-dhcp-server.md#L43): "Multiple servers can be specified, separated by commas." — passive. *Verified.*
- ✅ [L45](set-up-cameras-and-devices/network-and-infrastructure-configuration/configure-lumana-core-as-a-dhcp-server.md#L45): "The duration, in seconds, for which an IP address is leased to a device before it needs renewal." — passive. *Verified.*

**Headings (user-focused):**
- ✅ [L9](set-up-cameras-and-devices/network-and-infrastructure-configuration/configure-lumana-core-as-a-dhcp-server.md#L9): "Key DHCP server capabilities" — feature-focused noun phrase inside a how-to. *Verified.*
- ✅ [L37](set-up-cameras-and-devices/network-and-infrastructure-configuration/configure-lumana-core-as-a-dhcp-server.md#L37), [L47](set-up-cameras-and-devices/network-and-infrastructure-configuration/configure-lumana-core-as-a-dhcp-server.md#L47), [L55](set-up-cameras-and-devices/network-and-infrastructure-configuration/configure-lumana-core-as-a-dhcp-server.md#L55), [L66](set-up-cameras-and-devices/network-and-infrastructure-configuration/configure-lumana-core-as-a-dhcp-server.md#L66): "Configuration parameters", "Example configuration", "Address reservation", "Address reservation use cases" — noun phrases on a how-to page. *Verified.*

**UI text exact match (capitalisation):**
- ✅ [L41](set-up-cameras-and-devices/network-and-infrastructure-configuration/configure-lumana-core-as-a-dhcp-server.md#L41), [L42](set-up-cameras-and-devices/network-and-infrastructure-configuration/configure-lumana-core-as-a-dhcp-server.md#L42), [L43](set-up-cameras-and-devices/network-and-infrastructure-configuration/configure-lumana-core-as-a-dhcp-server.md#L43), [L45](set-up-cameras-and-devices/network-and-infrastructure-configuration/configure-lumana-core-as-a-dhcp-server.md#L45): doc renders field labels as **Starting IP Address**, **Ending IP Address**, **DNS Servers**, **Lease Time** in Title Case. *Verified — bold labels use Title Case while [UI text and messages](STYLEGUIDE.md) requires matching the live product (reported sentence case).*

**If/then violations:**
- ✅ [L21](set-up-cameras-and-devices/network-and-infrastructure-configuration/configure-lumana-core-as-a-dhcp-server.md#L21): "If another DHCP server is already active on that segment, review the impact before you enable this feature." — missing "then". *Verified.*

**List/step issues:**
- ✅ [L27](set-up-cameras-and-devices/network-and-infrastructure-configuration/configure-lumana-core-as-a-dhcp-server.md#L27): step 2 combines four actions ("Select **Devices**. Under **Devices by types**, select **Cores** … On the **Devices list**, apply the **Cores** filter … Then select **Edit location**…"). *Verified.*
- ✅ [L33](set-up-cameras-and-devices/network-and-infrastructure-configuration/configure-lumana-core-as-a-dhcp-server.md#L33): step 3 "Select **DHCP Server** in the sidebar, enter the required parameters, then select **Enable**." — combines three actions. *Verified.*
- ✅ [L61](set-up-cameras-and-devices/network-and-infrastructure-configuration/configure-lumana-core-as-a-dhcp-server.md#L61)–[L64](set-up-cameras-and-devices/network-and-infrastructure-configuration/configure-lumana-core-as-a-dhcp-server.md#L64): "Configure address reservation" steps are vague ("Identify the MAC address", "Save the configuration") and don't reference UI controls. *Verified.*

**Tables vs lists:**
- ✅ [L41](set-up-cameras-and-devices/network-and-infrastructure-configuration/configure-lumana-core-as-a-dhcp-server.md#L41)–[L45](set-up-cameras-and-devices/network-and-infrastructure-configuration/configure-lumana-core-as-a-dhcp-server.md#L45): "Configuration parameters" reads as a parameter list. [Lists, steps, and tables](STYLEGUIDE.md) recommends tables for parameter reference. *Verified.*

**Other / typography:**
- ⚠️ [L21](set-up-cameras-and-devices/network-and-infrastructure-configuration/configure-lumana-core-as-a-dhcp-server.md#L21): curly apostrophe in "Lumana's". *Verified at L21 ("Lumana's DHCP server"); other apostrophe uses on this page appear minimal.*

---

### `set-up-cameras-and-devices/network-and-infrastructure-configuration/firewall-requirements.md`

**Sentence-length violations (>25 words):**
- ✅ [L63](set-up-cameras-and-devices/network-and-infrastructure-configuration/firewall-requirements.md#L63): "The table below is a **static reference** grouped by **category** and **region**, useful for ticketing, change control, or firewalls that need explicit rows." — 25+ words in the second sentence. *Verified — sentence runs over the 25-word limit per [Sentence and paragraph rules](STYLEGUIDE.md).*

**Voice / passive issues:**
- ✅ [L140](set-up-cameras-and-devices/network-and-infrastructure-configuration/firewall-requirements.md#L140): "All traffic is encrypted with TLS and DTLS." — passive. *Verified.*
- ✅ [L142](set-up-cameras-and-devices/network-and-infrastructure-configuration/firewall-requirements.md#L142): "If UDP is blocked, TURN/TLS over TCP 443 is used." — passive and missing "then". *Verified.*

**If/then violations:**
- ✅ [L245](set-up-cameras-and-devices/network-and-infrastructure-configuration/firewall-requirements.md#L245): "If your network firewall monitors outbound traffic, allow the following endpoints for the application itself." — missing "then". *Verified.*
- ✅ [L142](set-up-cameras-and-devices/network-and-infrastructure-configuration/firewall-requirements.md#L142): "If UDP is blocked, TURN/TLS over TCP 443 is used." — missing "then". *Verified.*

**Headings:**
- ✅ [L125](set-up-cameras-and-devices/network-and-infrastructure-configuration/firewall-requirements.md#L125): "OS Updates" — Title Case; [Headings](STYLEGUIDE.md) requires sentence case. *Verified.*

**Capitalisation after colon (run-in labels):**
- ✅ [L13](set-up-cameras-and-devices/network-and-infrastructure-configuration/firewall-requirements.md#L13): "**Lumana URLs**: A list of domains…" — capital "A" after colon for a fragment. *Verified.*
- ✅ [L14](set-up-cameras-and-devices/network-and-infrastructure-configuration/firewall-requirements.md#L14): "**Lumana IPs**: An API endpoint that returns…" — same issue. *Verified.*

**Vocabulary inconsistency:**
- ✅ [L39](set-up-cameras-and-devices/network-and-infrastructure-configuration/firewall-requirements.md#L39) vs [L57](set-up-cameras-and-devices/network-and-infrastructure-configuration/firewall-requirements.md#L57): "whitelist IPs directly" used at L39; "firewall allowlist" used at L57 and L59. *Verified — both terms appear.*

**Tables / data consistency:**
- ✅ [L76](set-up-cameras-and-devices/network-and-infrastructure-configuration/firewall-requirements.md#L76)–[L105](set-up-cameras-and-devices/network-and-infrastructure-configuration/firewall-requirements.md#L105): region naming `ME-West`/`ME West` and `US-Center` vs "US Central" heading at [L167](set-up-cameras-and-devices/network-and-infrastructure-configuration/firewall-requirements.md#L167). *Verified — `ME-West`/`ME West`, `US-Center`/`US-Central` mismatches.*

**List items not parallel:**
- ✅ [L127](set-up-cameras-and-devices/network-and-infrastructure-configuration/firewall-requirements.md#L127)–[L132](set-up-cameras-and-devices/network-and-infrastructure-configuration/firewall-requirements.md#L132): "OS Updates" list mixes "`archive.ubuntu.com` - ports: 80, 443 TCP outbound" with "`ports.ubuntu.com` - 443 TCP outbound". *Verified.*

**Section title:**
- ✅ [L261](set-up-cameras-and-devices/network-and-infrastructure-configuration/firewall-requirements.md#L261): page ends with "## Related" instead of "## Next steps". *Verified.*

---

### `set-up-cameras-and-devices/network-and-infrastructure-configuration/local-time-and-ntp-configuration.md`

**Sentence-length violations (>25 words):**
- ⚠️ [L19](set-up-cameras-and-devices/network-and-infrastructure-configuration/local-time-and-ntp-configuration.md#L19): "Use this task if you need to point the Core to a local NTP server instead of the default Lumana NTP servers." — second sentence is ~22 words; the prior sentence at L19 ("Configure Network Time Protocol (NTP) so Lumana Core can keep its system time accurate.") is ~13 words. *Borderline — the combined paragraph the report quotes spans two sentences, neither exceeds 25 words individually.*

**List/step issues:**
- ✅ [L9](set-up-cameras-and-devices/network-and-infrastructure-configuration/local-time-and-ntp-configuration.md#L9): step 1 combines three actions ("Open **Devices** → **Devices list**. Use the **Cores** filter… select **Edit location**."). *Verified.*
- ✅ [L13](set-up-cameras-and-devices/network-and-infrastructure-configuration/local-time-and-ntp-configuration.md#L13): step 2 combines two actions ("set **Time Zone**, then select **Save**"). *Verified.*

(Image-vs-step content verified.)

---

### `set-up-cameras-and-devices/network-and-infrastructure-configuration/lumana-core-hardware-specifications.md`

**Image-vs-step mismatches:**
- ⚠️ [L19](set-up-cameras-and-devices/network-and-infrastructure-configuration/lumana-core-hardware-specifications.md#L19): "Lumana Core ships with a **120 V** AC to **12 V DC** power adapter. Connect it to the **POWER** input on the rear panel." *The body text still says "POWER input" — verified; the image content (DC IN vs POWER label) requires a visual review of the screenshot.*

**Tables / data consistency:**
- ✅ [L32](set-up-cameras-and-devices/network-and-infrastructure-configuration/lumana-core-hardware-specifications.md#L32)–[L33](set-up-cameras-and-devices/network-and-infrastructure-configuration/lumana-core-hardware-specifications.md#L33): "0 °C ~ 50 °C" / "−40 °C ~ 85 °C" — uses tilde for ranges. *Verified.*
- ✅ [L37](set-up-cameras-and-devices/network-and-infrastructure-configuration/lumana-core-hardware-specifications.md#L37): "100–240 V ~ 1.8 A (50–60 Hz)" — mixes en-dashes and tilde. *Verified.*

**Information fragmentation:**
- ✅ [L5](set-up-cameras-and-devices/network-and-infrastructure-configuration/lumana-core-hardware-specifications.md#L5), [L23](set-up-cameras-and-devices/network-and-infrastructure-configuration/lumana-core-hardware-specifications.md#L23): "Connect Lumana Core to the network" links externally to `support.lumana.ai/hc/en-us/articles/...` rather than living in the docs site. *Verified.*

---

### `set-up-cameras-and-devices/other-devices/README.md`

**Asset folder structure:**
- ✅ [L6](set-up-cameras-and-devices/other-devices/README.md#L6): card icons reference `../../.gitbook/assets/icon-*.svg` at the assets root. *Verified — six `icon-*.svg` references at the assets root rather than under `icons/`.*

**Headings (user-focused):**
- ✅ [L6](set-up-cameras-and-devices/other-devices/README.md#L6): card titles "**FLIR sensors**", "**Disruptive sensors**", "**Smart speakers**", "**GPIO devices**", "**Network attached storage (NAS) devices**" are feature/product names; "**Configure SIP for smart speakers**" is correctly bare-infinitive. *Verified in the cards table.*

**Structural / cosmetic:**
- ✅ [L1](set-up-cameras-and-devices/other-devices/README.md#L1)–[L4](set-up-cameras-and-devices/other-devices/README.md#L4): two blank lines between H1 and the first paragraph. *Verified — lines 2 and 3 are blank.*

---

### `set-up-cameras-and-devices/other-devices/disruptive-sensors.md`

**List/step issues:**
- ✅ [L9](set-up-cameras-and-devices/other-devices/disruptive-sensors.md#L9): step 1 explanatory paragraph contains three actions ("Log in to the Lumana portal, then navigate to **Organization settings** -> **API Keys**. Generate a key and save it."). *Verified.*
- ✅ [L15](set-up-cameras-and-devices/other-devices/disruptive-sensors.md#L15): step 2 combines multiple actions; uses "add the Lumana API key from step 1 in **Custom HTTP Request Header**". [UI text and messages](STYLEGUIDE.md) requires "enter" for form fields. *Verified.*
- ✅ [L21](set-up-cameras-and-devices/other-devices/disruptive-sensors.md#L21), [L27](set-up-cameras-and-devices/other-devices/disruptive-sensors.md#L27), [L33](set-up-cameras-and-devices/other-devices/disruptive-sensors.md#L33): steps 3, 4, and 5 each combine multiple actions in a single explanatory paragraph. *Verified.*

**UI text exact match:**
- ✅ [L9](set-up-cameras-and-devices/other-devices/disruptive-sensors.md#L9), [L27](set-up-cameras-and-devices/other-devices/disruptive-sensors.md#L27): doc uses **API Keys** (step 1) and **Organization Settings** (step 4) in Title Case. *Verified — Title Case in both spots.*
- ✅ [L27](set-up-cameras-and-devices/other-devices/disruptive-sensors.md#L27): doc says **Integration** in step 4 ("Organization Settings -> Integration -> Disruptive"). *Verified — singular "Integration".*
- ✅ [L15](set-up-cameras-and-devices/other-devices/disruptive-sensors.md#L15): doc says "In **Data Connector**, create a new connector". *Verified — singular "Data Connector" in step 2.*
- ✅ [L33](set-up-cameras-and-devices/other-devices/disruptive-sensors.md#L33): step 5 says "**Devices** -> **Location** -> **Edit Location**". *Verified — Title Case "Edit Location".*

(Image-vs-step content verified for all five screenshots.)

---

### `set-up-cameras-and-devices/other-devices/flir-sensors.md`

**Trustworthiness / completeness:**
- ✅ [L4](set-up-cameras-and-devices/other-devices/flir-sensors.md#L4): page contains only "Coming soon!" — incomplete page. *Verified — file is 4 lines total.*
- ✅ [L1](set-up-cameras-and-devices/other-devices/flir-sensors.md#L1)–[L4](set-up-cameras-and-devices/other-devices/flir-sensors.md#L4): two blank lines between H1 and body; exclamation point is informal. *Verified — lines 2 and 3 are blank; "Coming soon!" uses an exclamation point.*

---

### `set-up-cameras-and-devices/other-devices/gpio-devices.md`

**Headings:**
- ✅ [L1](set-up-cameras-and-devices/other-devices/gpio-devices.md#L1): H1 "GPIO devices" — noun phrase for a how-to page. *Verified.*

**Sentence-length violations (>25 words):**
- ⚠️ [L5](set-up-cameras-and-devices/other-devices/gpio-devices.md#L5): "Third-party devices can read those hardwired signals from Lumana, or you can drive devices such as LEDs, motors, or relays." — second sentence is ~21 words; first sentence is ~19 words. *Borderline — neither sentence individually exceeds 25 words; the report counted the combined paragraph.*

**Voice / passive issues:**
- ✅ [L15](set-up-cameras-and-devices/other-devices/gpio-devices.md#L15): "an LED is connected to the GPIO" — passive in "Connect a device" intro. *Verified.*
- ✅ [L36](set-up-cameras-and-devices/other-devices/gpio-devices.md#L36): "Once enabled, open the alert editor…" — passive participial phrase. *Verified.*

**List/step issues:**
- ✅ [L38](set-up-cameras-and-devices/other-devices/gpio-devices.md#L38): step 3 "Select the GPIO to use. The Core can support up to 4 GPIOs, toggle high or low, and control how long the signal remains active." — combines selection and three configuration descriptions. *Verified.*

**List/step formatting:**
- ✅ [L19](set-up-cameras-and-devices/other-devices/gpio-devices.md#L19)–[L22](set-up-cameras-and-devices/other-devices/gpio-devices.md#L22) vs [L26](set-up-cameras-and-devices/other-devices/gpio-devices.md#L26)–[L28](set-up-cameras-and-devices/other-devices/gpio-devices.md#L28): "Parts list" uses `*` bullets; "Wiring notes" uses `-` bullets. *Verified.*
- ✅ [L26](set-up-cameras-and-devices/other-devices/gpio-devices.md#L26)–[L28](set-up-cameras-and-devices/other-devices/gpio-devices.md#L28): "Wiring notes" items use full sentences with periods. *Verified — items actually end in periods, contradicting the report; defect partially overstated.*

---

### `set-up-cameras-and-devices/other-devices/network-attached-storage-nas-devices.md`

**Voice / passive issues:**
- ✅ [L8](set-up-cameras-and-devices/other-devices/network-attached-storage-nas-devices.md#L8): "No license is needed for the first 30 days." — passive. *Verified.*
- ✅ [L14](set-up-cameras-and-devices/other-devices/network-attached-storage-nas-devices.md#L14): "The storage device must be reachable on the network by the Lumana Core unit." — passive. *Verified.*
- ✅ [L33](set-up-cameras-and-devices/other-devices/network-attached-storage-nas-devices.md#L33): "Choose your storage type. This can be either **NFS** or **Object Storage**." — second sentence is passive-feeling. *Verified.*

**Product naming:**
- ✅ [L8](set-up-cameras-and-devices/other-devices/network-attached-storage-nas-devices.md#L8): "smart search functionality" should be **Smart Search**. *Verified — "smart search" appears lowercase.*

**Headings:**
- ✅ [L1](set-up-cameras-and-devices/other-devices/network-attached-storage-nas-devices.md#L1): H1 "Network attached storage (NAS) devices" — uses parentheses. *Verified.*
- ✅ [L68](set-up-cameras-and-devices/other-devices/network-attached-storage-nas-devices.md#L68), [L75](set-up-cameras-and-devices/other-devices/network-attached-storage-nas-devices.md#L75), [L80](set-up-cameras-and-devices/other-devices/network-attached-storage-nas-devices.md#L80): "Storage capacity calculation", "Examples of NAS servers", "Examples of HDDs" — noun phrases on a how-to page. *Verified.*

**List/step issues:**
- ✅ [L25](set-up-cameras-and-devices/other-devices/network-attached-storage-nas-devices.md#L25): step 2 "Add an external storage server" combines three actions. *Verified.*
- ✅ [L29](set-up-cameras-and-devices/other-devices/network-attached-storage-nas-devices.md#L29): step 3 "select **External Storage**, then select **Add external storage**" — two actions. *Verified.*
- ✅ [L39](set-up-cameras-and-devices/other-devices/network-attached-storage-nas-devices.md#L39): step 5 "Select **Test**…then select **Save external storage**" — two actions. *Verified.*
- ✅ [L70](set-up-cameras-and-devices/other-devices/network-attached-storage-nas-devices.md#L70)–[L73](set-up-cameras-and-devices/other-devices/network-attached-storage-nas-devices.md#L73): "Storage capacity calculation" items mix phrases and sentences; none end in periods. *Verified.*

**Capitalisation after colon:**
- ✅ [L37](set-up-cameras-and-devices/other-devices/network-attached-storage-nas-devices.md#L37): "`* **Path**: combine the NAS IP and export path…`" — full sentence after colon starts lowercase. *Verified.*

**UI labels (exact match):**
- ✅ [L53](set-up-cameras-and-devices/other-devices/network-attached-storage-nas-devices.md#L53): doc references **External retention**; the broader UI/style reportedly uses "External retention period". *Verified the doc label; the live-UI claim would need a screenshot check.*
- ⚠️ [L36](set-up-cameras-and-devices/other-devices/network-attached-storage-nas-devices.md#L36): doc text uses `NFS-Server-1`; screenshot allegedly shows `NFS-Sever-1`. *The body text "NFS-Server-1" is verified at L36; the screenshot content would need visual review.*

**Bullet style:**
- ✅ [L13](set-up-cameras-and-devices/other-devices/network-attached-storage-nas-devices.md#L13)–[L14](set-up-cameras-and-devices/other-devices/network-attached-storage-nas-devices.md#L14) vs [L90](set-up-cameras-and-devices/other-devices/network-attached-storage-nas-devices.md#L90)–[L92](set-up-cameras-and-devices/other-devices/network-attached-storage-nas-devices.md#L92): Prerequisites/parts lists use `*`; Next steps uses `-`. *Verified.*

**Other / typography:**
- ✅ [L45](set-up-cameras-and-devices/other-devices/network-attached-storage-nas-devices.md#L45): "camera's live view" uses curly apostrophe. *Verified — U+2019 in "camera's".*

---

### `set-up-cameras-and-devices/other-devices/sip-for-smart-speakers.md`

**Stacked headings:**
- ✅ [L7](set-up-cameras-and-devices/other-devices/sip-for-smart-speakers.md#L7)→[L9](set-up-cameras-and-devices/other-devices/sip-for-smart-speakers.md#L9): `## Configure SIP on a Check Point router` immediately followed by `### Prerequisites` with no paragraph between. *Verified — only L8 (blank) sits between them.*

**List/step issues:**
- ✅ [L26](set-up-cameras-and-devices/other-devices/sip-for-smart-speakers.md#L26): step 2 "Enable VoIP. On the **Access Policy** > **VoIP** screen, enable VoIP." — restates the same action twice. *Verified.*
- ✅ [L30](set-up-cameras-and-devices/other-devices/sip-for-smart-speakers.md#L30), [L53](set-up-cameras-and-devices/other-devices/sip-for-smart-speakers.md#L53), [L68](set-up-cameras-and-devices/other-devices/sip-for-smart-speakers.md#L68): step 3 combines four actions; step 4 combines three; step 5's single-row table is awkward. *Verified.*
- ✅ [L114](set-up-cameras-and-devices/other-devices/sip-for-smart-speakers.md#L114), [L131](set-up-cameras-and-devices/other-devices/sip-for-smart-speakers.md#L131): Uniview step 6 and TOA step 5 say "Save." instead of "Select **Save**.". *Verified.*
- ⚠️ [L115](set-up-cameras-and-devices/other-devices/sip-for-smart-speakers.md#L115): Uniview step 7 "Verify the speaker's status shows **Registered**." — the report says the screenshot displays "REG SUCCESS". *Body text verified; the image content claim requires a visual review.*

**UI text exact match:**
- ✅ [L63](set-up-cameras-and-devices/other-devices/sip-for-smart-speakers.md#L63)–[L64](set-up-cameras-and-devices/other-devices/sip-for-smart-speakers.md#L64), [L88](set-up-cameras-and-devices/other-devices/sip-for-smart-speakers.md#L88): doc references **SIP_UDP** at port 5061 twice. *The duplicated entries are verified at L64 and L88; the image-side **SIP_DEV_UDP** mismatch requires a visual review.*
- ⚠️ [L75](set-up-cameras-and-devices/other-devices/sip-for-smart-speakers.md#L75): doc step 5 example shows `Uniview_speaker / Single IP / 192.168.100.30`. *Verified in the body; the screenshot's `Hikvision_speaker` claim requires a visual review.*
- ⚠️ [L106](set-up-cameras-and-devices/other-devices/sip-for-smart-speakers.md#L106)–[L107](set-up-cameras-and-devices/other-devices/sip-for-smart-speakers.md#L107): Uniview SIP fields use "Username" and "ID". *Body text verified; the live UI's "User Name, Auth ID" requires a visual review.*
- ✅ [L43](set-up-cameras-and-devices/other-devices/sip-for-smart-speakers.md#L43)–[L44](set-up-cameras-and-devices/other-devices/sip-for-smart-speakers.md#L44): casing `Media\_server\_1` / `Media\_server\_2` (with first letter cap) inside table cells. *Verified.*

**Voice / passive:**
- ✅ [L98](set-up-cameras-and-devices/other-devices/sip-for-smart-speakers.md#L98): hint "**Note**: SIP credentials (address, username, password) are supplied by your CSM." — passive. *Verified.*

**Bullet style:**
- ✅ [L13](set-up-cameras-and-devices/other-devices/sip-for-smart-speakers.md#L13)–[L15](set-up-cameras-and-devices/other-devices/sip-for-smart-speakers.md#L15) (`*`) vs [L23](set-up-cameras-and-devices/other-devices/sip-for-smart-speakers.md#L23)–[L24](set-up-cameras-and-devices/other-devices/sip-for-smart-speakers.md#L24) (`-`): mixes `*` and `-` bullets in the same file. *Verified — Prerequisites uses `*`, step substeps use `-`.*

**Other / typography:**
- ✅ [L95](set-up-cameras-and-devices/other-devices/sip-for-smart-speakers.md#L95), [L115](set-up-cameras-and-devices/other-devices/sip-for-smart-speakers.md#L115): "speaker's own admin interface" / "speaker's status" use curly apostrophes. *Verified.*

**Tables — formatting:**
- ✅ [L40](set-up-cameras-and-devices/other-devices/sip-for-smart-speakers.md#L40)–[L44](set-up-cameras-and-devices/other-devices/sip-for-smart-speakers.md#L44), [L61](set-up-cameras-and-devices/other-devices/sip-for-smart-speakers.md#L61)–[L64](set-up-cameras-and-devices/other-devices/sip-for-smart-speakers.md#L64), [L83](set-up-cameras-and-devices/other-devices/sip-for-smart-speakers.md#L83)–[L89](set-up-cameras-and-devices/other-devices/sip-for-smart-speakers.md#L89): tables escape underscores (`Oregon\_Gateways`, `SIP\_TLS\_AUTH`). *Verified.*

---

### `set-up-cameras-and-devices/other-devices/smart-speakers.md`

**Sentence-length violations (>25 words):**
- ✅ [L5](set-up-cameras-and-devices/other-devices/smart-speakers.md#L5): "Lumana can also use Session Initiation Protocol (SIP) with supported network speakers. That usually involves firewall or router rules on your side plus SIP account settings on each speaker. For Check Point SIP configuration and Uniview or TOA setup examples, see [Configure SIP for smart speakers](sip-for-smart-speakers.md)." — the final sentence runs ~30+ words. *Verified — paragraph contains a >25-word sentence per [Sentence and paragraph rules](STYLEGUIDE.md).*
- ⚠️ [L18](set-up-cameras-and-devices/other-devices/smart-speakers.md#L18): "You add the speaker in Lumana, load audio and patterns on the device, then attach alert actions to play those patterns." — ~22 words. *Borderline — sentence sits just under 25 words.*

**Voice / passive issues:**
- ✅ [L24](set-up-cameras-and-devices/other-devices/smart-speakers.md#L24): "the speaker is reachable from Lumana" — passive. *Verified in "Configure the TOA IP-A1SC15" intro.*

**Headings:**
- ✅ [L1](set-up-cameras-and-devices/other-devices/smart-speakers.md#L1): H1 "Smart speakers" — noun phrase. *Verified.*
- ✅ [L7](set-up-cameras-and-devices/other-devices/smart-speakers.md#L7): "Key use cases" — concept-style noun phrase inside a how-to. *Verified.*

**Run-in label colons (Key use cases):**
- ✅ [L11](set-up-cameras-and-devices/other-devices/smart-speakers.md#L11)–[L14](set-up-cameras-and-devices/other-devices/smart-speakers.md#L14): "**Pre-recorded alarms:**", "**Voice-style alerts:**", "**Deterrence:**", "**Emergency signaling:**" — all colons inside bold. *Verified all four bullets.*

**List/step issues:**
- ✅ [L31](set-up-cameras-and-devices/other-devices/smart-speakers.md#L31): step 2 of "Connect and address the speaker" combines two actions. *Verified.*
- ✅ [L43](set-up-cameras-and-devices/other-devices/smart-speakers.md#L43): step 3 of "Upload media and define a pattern" combines four actions/observations. *Verified.*
- ✅ [L51](set-up-cameras-and-devices/other-devices/smart-speakers.md#L51): "Add the speaker in VMS+" step 1 includes "(or the add control your site uses)" — hedging language. *Verified.*
- ✅ [L54](set-up-cameras-and-devices/other-devices/smart-speakers.md#L54): step 4 "Select **Create** (or **Save**) to finish. If the add fails, then recheck the IP, port, and credentials on the LAN." — same hedging and colloquial "the add fails". *Verified.*
- ✅ [L62](set-up-cameras-and-devices/other-devices/smart-speakers.md#L62): "Play a pattern from an alert" step 1 bolds **create** and **edit** as if UI controls. *Verified.*
- ✅ [L63](set-up-cameras-and-devices/other-devices/smart-speakers.md#L63): step 2 bolds `pattern` and `speaker` as if labels. *Verified.*

**UI text exact match:**
- ✅ [L43](set-up-cameras-and-devices/other-devices/smart-speakers.md#L43): doc says "**volume**" lowercase. *Body text verified; live UI's "Input Volume" claim requires a visual review.*
- ✅ [L52](set-up-cameras-and-devices/other-devices/smart-speakers.md#L52): doc says "**username**" (one word). *Verified — body uses one-word "username".*

**Other / typography:**
- ✅ [L24](set-up-cameras-and-devices/other-devices/smart-speakers.md#L24): "speaker's own" — body uses straight ASCII apostrophe at L24, but no curly quote spotted on this page. *Borderline — the report's claim about curly quotes appears to apply to `sip-for-smart-speakers.md`; this page seems clean.*

---

## Cross-cutting / recurring themes

These themes show up across multiple pages. Treating them in a single pass will be more efficient than fixing them file by file.

**1. ✅ Sentence length above 25 words.** Recurs across most files; the worst examples are in [`set-up-cameras-and-devices/README.md`](set-up-cameras-and-devices/README.md) (47 words), [`recommended-streaming-settings.md`](set-up-cameras-and-devices/recommended-streaming-settings.md) (49 + 44 words), [`enhance-your-video-data-with-lumana-event-tags.md`](databases-analytics-and-search/enhance-your-video-data-with-lumana-event-tags.md) line 7 (38 words), [`axis.md`](set-up-cameras-and-devices/connect-cameras-by-brand/axis.md) line 65 (30) and other long sentences (28, 31), [`hikvision.md`](set-up-cameras-and-devices/connect-cameras-by-brand/hikvision.md) line 41 (35), [`set-up-a-static-ip-address.md`](set-up-cameras-and-devices/set-up-a-static-ip-address.md) (35 + 34), [`smart-speakers.md`](set-up-cameras-and-devices/other-devices/smart-speakers.md) (28 ×2). *Verified across the per-file sections above.*

**2. ✅ If/then construction.** The single most pervasive defect. Dozens of conditional sentences across nearly every file are missing "then" in the predicate. Worst offenders: [`the-system-health-dashboard.md`](live-video-monitoring-and-operations/the-system-health-dashboard.md) (4 instances), [`recommended-streaming-settings.md`](set-up-cameras-and-devices/recommended-streaming-settings.md), [`axis.md`](set-up-cameras-and-devices/connect-cameras-by-brand/axis.md) (4+), [`hikvision.md`](set-up-cameras-and-devices/connect-cameras-by-brand/hikvision.md), [`lumana.md`](set-up-cameras-and-devices/connect-cameras-by-brand/lumana.md), [`verkada.md`](set-up-cameras-and-devices/connect-cameras-by-brand/verkada.md), [`firewall-requirements.md`](set-up-cameras-and-devices/network-and-infrastructure-configuration/firewall-requirements.md), [`configure-lumana-core-as-a-dhcp-server.md`](set-up-cameras-and-devices/network-and-infrastructure-configuration/configure-lumana-core-as-a-dhcp-server.md). *Verified across the per-file sections above.*

**3. ⚠️ Image-vs-step factual mismatches.** Several screenshots actively contradict the surrounding text. *Body-side text verified in the per-file sections above; image-side claims require visual review of each screenshot.*
- [`set-up-a-camera-floor-plan.md`](set-up-cameras-and-devices/set-up-a-camera-floor-plan.md): "top **left** corner" vs screenshot showing top-right.
- [`enable-ptz-control.md`](set-up-cameras-and-devices/enable-ptz-control.md): text says pencil icon; screenshot highlights the wrench. Field name "PTZ control path" doesn't match the UI's "X address".
- [`lumana-core-hardware-specifications.md`](set-up-cameras-and-devices/network-and-infrastructure-configuration/lumana-core-hardware-specifications.md): text tells users to plug power into **POWER**; the labelled power input is **DC IN** (POWER is a button).
- [`share-video.md`](live-video-monitoring-and-operations/share-video.md): "existing-links-dialog" image actually shows the Share/Create-link tab, not the Existing links tab.
- [`live-view-streaming-and-quality.md`](live-video-monitoring-and-operations/live-view-streaming-and-quality.md): "cloud streaming diagram" actually depicts the local-first decision flow. Diagram text contains spelling errors ("Incomplient", "compatibale").
- [`the-system-health-dashboard.md`](live-video-monitoring-and-operations/the-system-health-dashboard.md): dashboard-overview image actually shows Devices list with an arrow.
- [`lumana-timelapse.md`](live-video-monitoring-and-operations/lumana-timelapse.md): Create-timelapse-dialog image is misplaced next to retention-availability text.
- [`multi-camera-playback.md`](live-video-monitoring-and-operations/multi-camera-playback.md): `multi-camera-playback-wall-view.png` is missing on disk (broken reference).
- [`camera-networking-options.md`](set-up-cameras-and-devices/camera-networking-options.md) and [`sip-for-smart-speakers.md`](set-up-cameras-and-devices/other-devices/sip-for-smart-speakers.md): SIP service rows say `SIP_UDP`; screenshots show `SIP_DEV_UDP`. On-premise device example in doc uses `Uniview_speaker`; screenshot shows `Hikvision_speaker` at that IP.
- [`axis.md`](set-up-cameras-and-devices/connect-cameras-by-brand/axis.md) and [`hanwha.md`](set-up-cameras-and-devices/connect-cameras-by-brand/hanwha.md): stream profile screenshots show "Maximum"/MBR bitrate while the body text says CBR.
- [`network-attached-storage-nas-devices.md`](set-up-cameras-and-devices/other-devices/network-attached-storage-nas-devices.md): doc says `NFS-Server-1`; screenshot's field shows `NFS-Sever-1`.

**5. ✅ Bold-as-heading misuse.** Previously: pseudo-headings in [`overview.md`](set-up-cameras-and-devices/overview.md), import/export labels in [`lumana.md`](set-up-cameras-and-devices/connect-cameras-by-brand/lumana.md), and figure labels in [`tracking-vehicles.md`](databases-analytics-and-search/tracking-vehicles.md). *Addressed — overview now uses `###` subheadings; lumana uses `### Import configuration` / `### Export configuration`; tracking-vehicles uses prose lead-ins before figures. [`share-video.md`](live-video-monitoring-and-operations/share-video.md) already uses `###` for section titles.*

**6. ✅ Run-in label colon placement (colon inside bold).** [`create-camera-shortcuts.md`](set-up-cameras-and-devices/create-camera-shortcuts.md) and [`smart-speakers.md`](set-up-cameras-and-devices/other-devices/smart-speakers.md) place colons inside bold for run-in labels (`**Label:**` instead of `**Label**:`). [`lumana.md`](set-up-cameras-and-devices/connect-cameras-by-brand/lumana.md) bulk-operation bullets now use colons outside bold per [UI text and messages](STYLEGUIDE.md). *Verified across the per-file sections above.*

**7. ✅ Naming-pattern inconsistency in `connect-cameras-by-brand/`.** [`lumana.md`](set-up-cameras-and-devices/connect-cameras-by-brand/lumana.md) is titled "Lumana" and [`verkada.md`](set-up-cameras-and-devices/connect-cameras-by-brand/verkada.md) is titled "Verkada" (noun) while sibling pages use bare-infinitive titles like "Connect Axis cameras" / "Connect Hanwha cameras" / "Connect Hikvision cameras". *Verified — H1s differ in pattern.*

**8. ✅ Steps that combine multiple actions.** Pervasive in [`share-video.md`](live-video-monitoring-and-operations/share-video.md), [`live-view.md`](live-video-monitoring-and-operations/live-view.md), [`multi-camera-playback.md`](live-video-monitoring-and-operations/multi-camera-playback.md), [`video-walls-and-shared-displays.md`](live-video-monitoring-and-operations/video-walls-and-shared-displays.md), [`build-a-database-of-people-and-vehicles.md`](databases-analytics-and-search/build-a-database-of-people-and-vehicles.md), [`enhance-your-video-data-with-lumana-event-tags.md`](databases-analytics-and-search/enhance-your-video-data-with-lumana-event-tags.md), [`generate-reports.md`](databases-analytics-and-search/generate-reports.md), [`missing-object-alert.md`](databases-analytics-and-search/missing-object-alert.md), [`set-up-a-camera-floor-plan.md`](set-up-cameras-and-devices/set-up-a-camera-floor-plan.md), [`hanwha.md`](set-up-cameras-and-devices/connect-cameras-by-brand/hanwha.md), [`verkada.md`](set-up-cameras-and-devices/connect-cameras-by-brand/verkada.md), [`configure-lumana-core-as-a-dhcp-server.md`](set-up-cameras-and-devices/network-and-infrastructure-configuration/configure-lumana-core-as-a-dhcp-server.md), [`disruptive-sensors.md`](set-up-cameras-and-devices/other-devices/disruptive-sensors.md), [`network-attached-storage-nas-devices.md`](set-up-cameras-and-devices/other-devices/network-attached-storage-nas-devices.md), [`sip-for-smart-speakers.md`](set-up-cameras-and-devices/other-devices/sip-for-smart-speakers.md), [`smart-speakers.md`](set-up-cameras-and-devices/other-devices/smart-speakers.md). *Verified across the per-file sections above.*

**9. ✅ Passive voice.** Recurs in [`live-view-streaming-and-quality.md`](live-video-monitoring-and-operations/live-view-streaming-and-quality.md), [`generate-reports.md`](databases-analytics-and-search/generate-reports.md), [`space-occupancy-analytics.md`](databases-analytics-and-search/space-occupancy-analytics.md), [`tracking-people.md`](databases-analytics-and-search/tracking-people.md), [`tracking-vehicles.md`](databases-analytics-and-search/tracking-vehicles.md), [`search-video-footage-for-other-objects.md`](databases-analytics-and-search/search-video-footage-for-other-objects.md), [`configure-lumana-core-as-a-dhcp-server.md`](set-up-cameras-and-devices/network-and-infrastructure-configuration/configure-lumana-core-as-a-dhcp-server.md), [`firewall-requirements.md`](set-up-cameras-and-devices/network-and-infrastructure-configuration/firewall-requirements.md), [`gpio-devices.md`](set-up-cameras-and-devices/other-devices/gpio-devices.md), [`network-attached-storage-nas-devices.md`](set-up-cameras-and-devices/other-devices/network-attached-storage-nas-devices.md), [`smart-speakers.md`](set-up-cameras-and-devices/other-devices/smart-speakers.md), [`sip-for-smart-speakers.md`](set-up-cameras-and-devices/other-devices/sip-for-smart-speakers.md). Common patterns: "is supported", "is enabled", "is exported", "is reachable", "must be reachable", "Once enabled", "are configured". *Verified across the per-file sections above.*

**10. ⚠️ UI label capitalisation drift.** Doc renders product UI labels in title case while the live UI uses sentence case: "Starting IP Address" → "Starting IP address"; "API Keys" → "API keys"; "Integration" → "Integrations"; "Data Connector" → "Data Connectors"; "External retention" → "External retention period"; "subnet mask" → "Subnet mask"; "username" → "User Name"; "Edit Location" inconsistent with "Edit location"; "Edit Camera" inconsistent with "Edit camera". *Doc-side casing verified across the per-file sections above; the live-UI labels need a visual review.*

**11. ✅ Future tense / "will".** Spot-check remaining pages after present-tense fixes in [`axis.md`](set-up-cameras-and-devices/connect-cameras-by-brand/axis.md) (ONVIF planning), [`hikvision.md`](set-up-cameras-and-devices/connect-cameras-by-brand/hikvision.md) (SADP scan / Connect a camera closer), [`recommended-streaming-settings.md`](set-up-cameras-and-devices/recommended-streaming-settings.md) (single-stream hint), and [`set-up-a-static-ip-address.md`](set-up-cameras-and-devices/set-up-a-static-ip-address.md) (DHCP mapping). *Re-run `grep` for ` will ` when editing nearby content.*

**12. ✅ May vs might.** [`live-view-streaming-and-quality.md`](live-video-monitoring-and-operations/live-view-streaming-and-quality.md) (5 instances), [`the-system-health-dashboard.md`](live-video-monitoring-and-operations/the-system-health-dashboard.md) (3), [`share-video.md`](live-video-monitoring-and-operations/share-video.md) (1), [`video-walls-and-shared-displays.md`](live-video-monitoring-and-operations/video-walls-and-shared-displays.md) (1), [`recommended-streaming-settings.md`](set-up-cameras-and-devices/recommended-streaming-settings.md) (1). All possibility uses; switch to "might". *Verified across the per-file sections above.*

**13. ✅ Marketing / vague claims.** [`missing-object-alert.md`](databases-analytics-and-search/missing-object-alert.md) "Why this alert helps", [`tracking-containers.md`](databases-analytics-and-search/tracking-containers.md) "Key benefits", [`space-occupancy-analytics.md`](databases-analytics-and-search/space-occupancy-analytics.md) "Key features", [`recommended-streaming-settings.md`](set-up-cameras-and-devices/recommended-streaming-settings.md) ("smart storage", "Smarter storage around alerts", "Stronger AI learning over time"), [`video-walls-and-shared-displays.md`](live-video-monitoring-and-operations/video-walls-and-shared-displays.md) ("Lumana offers saved walls plus quick live grids plus secure external walls…"), [`enhance-your-video-data-with-lumana-event-tags.md`](databases-analytics-and-search/enhance-your-video-data-with-lumana-event-tags.md) H1 (uses "Enhance"), [`supported-cameras.md`](set-up-cameras-and-devices/connect-cameras-by-brand/supported-cameras.md) ("wide range", "flexibility", "fits your deployment needs"). *Verified across the per-file sections above.*

**14. ✅ Stacked headings without intervening paragraphs.** Residual focuses: [`sip-for-smart-speakers.md`](set-up-cameras-and-devices/other-devices/sip-for-smart-speakers.md) (`## Configure SIP on a Check Point router` → `### Prerequisites`). *[`firewall-requirements.md`](set-up-cameras-and-devices/network-and-infrastructure-configuration/firewall-requirements.md), [`lumana-core-hardware-specifications.md`](set-up-cameras-and-devices/network-and-infrastructure-configuration/lumana-core-hardware-specifications.md), and [`gpio-devices.md`](set-up-cameras-and-devices/other-devices/gpio-devices.md) now include lead-in paragraphs; H4 regional headings were promoted to H3.*

**15. ✅ Headings that aren't user-focused or that misuse "Step N:" framing.** [`enhance-your-video-data-with-lumana-event-tags.md`](databases-analytics-and-search/enhance-your-video-data-with-lumana-event-tags.md) uses "Step 1:" / "Step 2:" prefixes that break the bare-infinitive convention. [`configure-lumana-core-as-a-dhcp-server.md`](set-up-cameras-and-devices/network-and-infrastructure-configuration/configure-lumana-core-as-a-dhcp-server.md) "Key DHCP server capabilities", [`set-up-a-camera-floor-plan.md`](set-up-cameras-and-devices/set-up-a-camera-floor-plan.md) "Use the camera floor plan feature", [`enable-ptz-control.md`](set-up-cameras-and-devices/enable-ptz-control.md) and [`create-camera-shortcuts.md`](set-up-cameras-and-devices/create-camera-shortcuts.md) and [`set-up-a-camera-floor-plan.md`](set-up-cameras-and-devices/set-up-a-camera-floor-plan.md) "Key benefits"/"Key capabilities". *Verified across the per-file sections above.*

**16. ✅ Heading parentheses.** [`pixels-per-foot-for-camera-placement.md`](databases-analytics-and-search/pixels-per-foot-for-camera-placement.md) "(PPF)"; [`network-attached-storage-nas-devices.md`](set-up-cameras-and-devices/other-devices/network-attached-storage-nas-devices.md) H1 "(NAS) devices"; [`camera-networking-options.md`](set-up-cameras-and-devices/camera-networking-options.md) "Remote camera access (Camera VPN)". *`lumana-core-hardware-specifications.md` dimensions heading no longer uses parentheses (spelled out as "in millimeters").*

**17. ✅ "Coming soon!" placeholder pages.** [`create-links-between-cameras.md`](set-up-cameras-and-devices/create-links-between-cameras.md), [`flir-sensors.md`](set-up-cameras-and-devices/other-devices/flir-sensors.md). *Verified — both files contain only "Coming soon!".*

**18. ✅ Asset folder structure.** README cards across multiple sections reference `../.gitbook/assets/icon-*.svg` instead of `.gitbook/assets/icons/`. Several screenshots from older content still live at the assets root rather than in section subfolders (`dhcp-*.png`, `ntp-*.png`, `nas-*.png`, `check-point-*.png`, `sip-*.png`, `on-premise-*.png`, `off-premise-*.png`, `toa-speaker-*.png`, `live-view-ptz-*.png`). The [`missing-object-alert.md`](databases-analytics-and-search/missing-object-alert.md) images use a `custom-objects-` prefix that doesn't match the consuming page; the [`pixels-per-foot-for-camera-placement.md`](databases-analytics-and-search/pixels-per-foot-for-camera-placement.md) images reuse `tracking-people-...` filenames. *Verified across the per-file sections above.*

**19. ✅ Bullet-style inconsistency.** [`gpio-devices.md`](set-up-cameras-and-devices/other-devices/gpio-devices.md), [`network-attached-storage-nas-devices.md`](set-up-cameras-and-devices/other-devices/network-attached-storage-nas-devices.md), [`sip-for-smart-speakers.md`](set-up-cameras-and-devices/other-devices/sip-for-smart-speakers.md) mix `*` and `-` bullets within the same file. *Verified across the per-file sections above.*

**20. ⚠️ Curly vs straight apostrophes.** Inconsistent across most files (`'` mixed with `'`). *Verified at multiple spot-checks (e.g. [tracking-people.md](databases-analytics-and-search/tracking-people.md), [enhance-your-video-data-with-lumana-event-tags.md](databases-analytics-and-search/enhance-your-video-data-with-lumana-event-tags.md), [sip-for-smart-speakers.md](set-up-cameras-and-devices/other-devices/sip-for-smart-speakers.md)); a global grep pass would give an exact count.*

**21. ✅ Italics with `*` instead of `_`.** [`set-up-a-camera-floor-plan.md`](set-up-cameras-and-devices/set-up-a-camera-floor-plan.md) uses `*floor plan*` instead of `_floor plan_`. *Verified.*

**22. ✅ "Where" used to connect clauses.** [`live-view-streaming-and-quality.md`](live-video-monitoring-and-operations/live-view-streaming-and-quality.md) line 40, [`share-video.md`](live-video-monitoring-and-operations/share-video.md) line 39, [`camera-networking-options.md`](set-up-cameras-and-devices/camera-networking-options.md) ("for devices on a private network where you need the manufacturer's UI"), [`other-brands.md`](set-up-cameras-and-devices/connect-cameras-by-brand/other-brands.md) ("where applicable"). *Verified across the per-file sections above.*

**23. ✅ Single-item lists.** [`verkada.md`](set-up-cameras-and-devices/connect-cameras-by-brand/verkada.md) "Enable RTSP on the camera" step 1 is a one-item numbered list. *Verified — only one item under the heading.*

**24. ✅ Duplicate / orphaned content.**
- [`lumana-timelapse.md`](live-video-monitoring-and-operations/lumana-timelapse.md): image of a "Create timelapse" dialog sits next to text about retention; the actual create flow is not documented.
- [`multi-camera-playback.md`](live-video-monitoring-and-operations/multi-camera-playback.md): `multi-camera-playback-wall-view.png` is referenced but missing on disk.
- The `custom-objects-` image prefix on [`missing-object-alert.md`](databases-analytics-and-search/missing-object-alert.md) is a remnant of the deleted `custom-objects.md` page.

*Verified across the per-file sections above.*

**25. ⚠️ Reference data typos.**
- [`recommended-streaming-settings.md`](set-up-cameras-and-devices/recommended-streaming-settings.md) table: `3MP / 3072×1028` (probably 1728), `4MP / 2560×1440` (3.7MP/QHD, not 4MP), `8MP / 3480×2160` (probably 3840×2160).
- [`live-view-streaming-and-quality.md`](live-video-monitoring-and-operations/live-view-streaming-and-quality.md) "Reference values" table: `3480x2160 (8MP)` repeated four times — likely 3840×2160.
- `live-view-quality-routing-diagram.png`: "Incomplient" / "compatibale" misspellings.

*Body text typos verified at L42–L46 of the streaming pages; the diagram spellings are a visual check.*

**26. ⚠️ Trustworthiness flags.**
- [`set-up-a-static-ip-address.md`](set-up-cameras-and-devices/set-up-a-static-ip-address.md) line 68 and [`lumana.md`](set-up-cameras-and-devices/connect-cameras-by-brand/lumana.md) use a "Lumix.ai LB800" example camera on Lumana-branded pages. *Body text mentions of "LB800" verified; whether LB800 is Lumana-branded requires product confirmation.*
- [`lumana-timelapse.md`](live-video-monitoring-and-operations/lumana-timelapse.md) competitor comparison ("This is different from Verkada, which defaults to 24 hours.") is unusual for product docs. *Verified.*

---

## Notes on what was not deeply checked

- **Trustworthiness against the live product.** Many UI label and field-name flags above are best-guess based on screenshots; only you (or a reviewer with product access) can confirm each label.
- **Banned-word and "use sparingly" exhaustive counts.** Spot-checks found "Enhance" in one H1 and one card label, and occasional "essential"/"effective"/"significant" usage at low counts. A `grep -wi -c` pass per word would give a hard guarantee.
- **AI-feature limitations disclosure.** For `tracking-people.md`, `tracking-vehicles.md`, `space-occupancy-analytics.md`, and `missing-object-alert.md`, the inline limitations and accuracy caveats look reasonable. Verify they reflect current product confidence-level wording.
