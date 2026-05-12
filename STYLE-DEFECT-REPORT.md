# Style guide compliance defect report (round 3)

This is a fresh review of the same three sections (`live-video-monitoring-and-operations`, `databases-analytics-and-search`, and `set-up-cameras-and-devices`) against `STYLEGUIDE.md`. This pass also verified that the screenshots match the steps they sit next to (image-vs-step accuracy).

The categories used here map directly to the style guide. Where a file passes a category, the category is omitted for that file. Each defect quotes the offending text and gives a line number so you can find it quickly. No files have been edited.

---

## Section 1 — `live-video-monitoring-and-operations`

### `live-video-monitoring-and-operations/README.md`

**Headings / consistency:**
- Card titles mix bare-infinitive and noun-phrase patterns within one section index ("Use live view", "Live view streaming and quality", "PTZ control", "Multi-camera playback", "Use the system health dashboard", "Share video", "Change dark mode and light mode"). Pick one pattern and apply it consistently.

**Product naming:**
- "Use live view" card uses lowercase "live view"; other cards use "Live view" (capitalised). Inconsistent product term.

**Structural:**
- No "Next steps" section. Acceptable for an index/landing page, but worth noting.

---

### `live-video-monitoring-and-operations/dark-mode-and-light-mode.md`

**Image issues (alt text policy):**
- Lines 15, 21, 37: alt text is descriptive ("Dark mode home view with the user menu button highlighted in the lower left.", etc.). Style guide says alt should be empty for screenshots.

(Image-vs-step content verified: user icon, settings menu, theme field, theme dialog all match.)

---

### `live-video-monitoring-and-operations/live-view.md`

**Headings:**
- Line 1 H1 "Use live view" — uses lowercase "live view"; product term elsewhere is "Live view".
- "Open live view", "Use live view controls" — same lowercase issue.

**List/step issues:**
- Lines 24–25 (Use the timeline and thumbnails): step 3 "Change the date, time range, clip duration, or resolution as needed." — vague, no visible result described.
- Lines 44–48 (Use thumbnail actions): step 3 "Use the available actions to scrub through the footage, add cameras to a video wall layout, or archive footage to share it later." — combines three different actions into a single step.

**Image issues:**
- Line 17: alt text not empty ("Live view camera grid and location list."). Should be empty for a screenshot.
- Line 27: alt text not empty for a screenshot.

**Image-vs-step mismatches:**
- Line 33: image `live-view-screenshots/live-view-player-office-hq.png` shows the **HQ** quality toggle in the bottom-center cluster, not bottom-left as the body text describes ("In the bottom left corner of Live view, you can toggle between available stream qualities").

---

### `live-video-monitoring-and-operations/live-view-streaming-and-quality.md`

**Sentence-length violations (>25 words):**
- Line 3: "This page explains how Lumana delivers live video, when local or cloud streaming is used, and how stream quality changes based on your device, browser support, and layout." — 28 words.
- Line 29: "If a camera uses H.265 and the viewing browser or device does not support H.265, then medium-quality (MQ) local streaming may work while high-quality (HQ) local streaming does not." — 29 words.

**May vs might:**
- Line 29: "medium-quality (MQ) local streaming may work" — possibility, should be "might".
- Line 48: "latency and compatibility may vary" — should be "might".
- Line 68: "Lumana may choose a lower quality automatically" — should be "might".
- Line 70: "Lumana may prioritize smoother playback" — should be "might".
- Line 78: "Values may vary by codec" — should be "might".

**Headings:**
- "Manage streaming quality" — bare infinitive on a concept page, inconsistent with the surrounding noun-phrase headings ("Local streaming", "Cloud streaming", "Reference values"). Pick one pattern.
- "How live view delivery works" / "How quality selection works" — uses lowercase "live view" inconsistently with product naming.

**"Where" connector misuse:**
- Line 40: "...remotely or across restricted networks where a direct local connection is not possible." — should be "because" or "so".

**Marketing / vague claims:**
- Line 42: "This is especially useful when you need to access live video from another location..." — borderline marketing intensifier.

**Image issues:**
- Line 32: alt="Diagram showing local streaming from Lumana Core to the viewing device through the local network." — diagram alt OK.
- Line 52: alt="Cloud streaming diagram." — too sparse for a diagram conveying flow info.
- Line 62: alt="Streaming quality diagram." — too sparse for a diagram.

**Image-vs-step mismatches:**
- Line 52: `live-view-cloud-streaming-diagram.png` shows the *local* streaming decision flow (numbered steps ending with "4. Start local live view"), not the cloud streaming path the surrounding text describes.
- Line 62: `live-view-quality-routing-diagram.png` contains spelling errors in the diagram text: "Incomplient" (should be "Incompatible") and "compatibale" (twice; should be "compatible").

**Reference data / typos:**
- The "Reference values" table uses "3480x2160 (8MP)" — likely typo for the standard 8MP resolution **3840x2160**. Repeated four times in the table.

---

### `live-video-monitoring-and-operations/lumana-timelapse.md`

**Headings:**
- Line 40: "Need longer history than snapshot retention allows?" — heading is a question. Style guide requires bare-infinitive (how-to) or noun phrase. Recast as something like "Extend timelapse history beyond retention limits".

**Sentence-length violations (>25 words):**
- Line 26: "Under **Data retention**, open **Snapshot retention days** and choose a period from the list, for example **3 days**, **7 days**, **14 days**, **30 days**, or **90 days** when available." — 28 words.
- Line 37: "Once you understand the default window and the longest option your deployment offers in **Snapshot retention days**, you can decide whether the built-in range is enough for your workflow." — 29 words.

**If/then violations:**
- Line 42: "If you need timelapse history beyond the maximum **Snapshot retention days** value available in your deployment, contact Customer Support to discuss extended storage options." — missing "then".

**UI element / casing inconsistency:**
- Line 25: "open **Edit Camera**" with capital C. Other pages use "**Edit camera**" (lowercase). Verify against the live UI and apply consistently.

**Image issues:**
- Line 19: alt text not empty for a screenshot.
- Line 36: alt="" — correct.

**Image-vs-step mismatches:**
- Line 19: `lumana-timelapse-create-dialog.png` shows a "Create timelapse" dialog (Name, Camera, Timeframe, Duration). The surrounding text discusses default 3-day retention, not how to create a timelapse. Image is misplaced.
- Line 36: `lumana-timelapse-retention-settings.png` shows the dropdown listing "3 days, 7 days, 14 days, 30 days" without "90 days"; step text says options include "3 days, 7 days, 14 days, 30 days, or 90 days when available" — the image partially supports the text but the 90 days option isn't visible.

**Trustworthiness:**
- Line 13 hint: "This is different from Verkada, which defaults to 24 hours." — competitor comparison in product docs is unusual and risks reading as marketing or appearing unverifiable.

---

### `live-video-monitoring-and-operations/multi-camera-playback.md`

**Image issues (broken reference):**
- Line 45: `multi-camera-playback-wall-view.png` — file does not exist on disk. Broken image reference.

**List/step issues:**
- Step 6 (line 30): "Select up to three more cameras inside the picker, then select **Select**." — the SAP-style qualifier rule says when a UI element is named "Select", add a qualifying word ("select the **Select** button"). This isn't qualified.
- Line 32: "If you need fewer rows on screen, then search cameras or drill into locations." — placed inside step 6 but reads as guidance about a different stage.

**Image issues (alt text):**
- Lines 5, 22, 38, 45: alt text not empty for screenshots.

**Image-vs-step mismatches / typos:**
- Line 38: image `multi-camera-playback-synced-view.png` — alt text says "His playback labels"; the image clearly shows "Hls playback" labels (HLS, the streaming protocol). Alt-text typo: "His" should be "HLS".

---

### `live-video-monitoring-and-operations/ptz-control.md`

**Headings:**
- H1 "PTZ control" is a noun phrase but the page is task-based. Per naming conventions, how-to titles should use bare infinitive ("Use PTZ control" or "Control PTZ from Live view").
- "Use PTZ in live view" — lowercase "live view" should be "Live view" to match product naming.

**List/step issues:**
- Lines 12–15: bullet markers use `*` rather than `-` used elsewhere — minor inconsistency.

**UI element issues:**
- Line 3: "**Edit camera**" lowercase "c"; lumana-timelapse.md uses "**Edit Camera**" with capital C. Confirm against live UI.

**Image issues:**
- Lines 10 and 17: alt text not empty for screenshots.

**Structural / guide-structure issues:**
- No Prerequisites section. The page is a how-to and the guide structure requires Introduction, Prerequisites, Steps, Next steps.

(Image-vs-step content verified: live-view PTZ toggle, controls overlay match the steps.)

---

### `live-video-monitoring-and-operations/share-video.md`

**Sentence-length violations (>25 words):**
- Line 35: "Turn **Allow to download** on or off so viewers can save the file or stream only (**Share camera** omits this toggle; **Share archive** and **Share alert** include it)." — 28 words.
- Line 90: long "see…" sentence with three nested links — borderline; tighten if possible.

**If/then violations:**
- Line 36: "Turn **Password** on, then type and confirm a password if viewers must enter one before playback." — "if" clause without "then".

**May vs might:**
- Line 29: "**Existing links** may show a count badge if you saved links before." — possibility, should be "might".

**"Where" connector misuse:**
- Line 39: "send it through another channel where your deployment supports it" — should be "if your deployment supports it" or "when your deployment supports it".

**UI element issues:**
- Line 13: "From live view" — lowercase. Same on line 61 ("the live view page").
- Line 74: "(curved arrow icon; hover shows **Share Alert**)" — capital A, but the body labels above use "**Share alert**" (lowercase a). Verify which the live UI uses and apply consistently.

**Headings issues (bold-as-heading):**
- Line 15: `**Go to Archives**` — used as a section label/heading. The style guide forbids bold-as-heading.
- Line 31: `**Create link and copy or send**` — same issue.

**List/step issues:**
- Line 35: combines an action and reference info in one step.
- The "Choose sharing options" subsection mixes overview info with the actual steps — confusing structure for a how-to.

**Image-vs-step mismatches:**
- Line 48: image `share-video-existing-links-dialog.png` is named "existing-links" but the rendered tab in the image is "Share" (with an "Existing links 2" badge). The image does NOT show the Existing links tab content — it shows the Share/Create-link tab again. The section heading just above it is "Send the link by email or SMS", which the image doesn't illustrate.

---

### `live-video-monitoring-and-operations/the-system-health-dashboard.md`

**Sentence-length violations (>25 words):**
- Line 3: "Use the system health dashboard to check the current status of your Lumana Core, cameras, and storage, and to review recent health history for each camera." — 26 words.

**If/then violations:**
- Line 13: "If another tab is selected at the top of the page (for example **Cameras** or **Map**), select **Devices** so the devices table is visible." — missing "then".
- Line 38: "If this area is unhealthy or offline, alerts and search may be affected." — missing "then".
- Line 41: "If it is unhealthy or offline, storage may be affected." — missing "then".
- Line 45: "If the **Trained** indicator stays unhealthy and you are not sure why, contact your Customer Success Manager." — missing "then".

**May vs might:**
- Line 38: "alerts and search may be affected" — should be "might".
- Line 41: "this indicator may not appear" / "storage may be affected" — should be "might".

**List/step issues:**
- Line 39: "**Storage**: Shows the status of 24/7 local storage on the Core. Retention is based on your 30-day, 60-day, or 90-day subscription." — combines two distinct facts in one bullet.
- Line 42: "**Trained**: …" — long mixed-content list item with multiple sentences and conditions; consider splitting.

**Image-vs-step mismatches:**
- Line 19: image `system-health-dashboard-overview.png` is captioned as a dashboard overview but actually shows the **Devices > Devices list** view with an arrow pointing to where the System Health icon would be in the row header. The step text just above says "The system health dashboard opens and shows the current status…" — image doesn't show the dashboard.

---

### `live-video-monitoring-and-operations/video-walls-and-shared-displays.md`

**Sentence-length violations (>25 words):**
- Line 18 (list item): "Standard camera and alert tiles: Use standard camera tiles and alert tiles when you need to combine live monitoring with event visibility in the same wall." — 27 words.

**Headings:**
- H1 "Video walls and shared displays" is a noun phrase but the page is mostly task-based. Inconsistent with sibling pages such as "Use multi-camera playback", "Use the system health dashboard". Should be "Use video walls and shared displays".

**If/then violations:**
- Line 112: "If you did not use **Save as wall**, quick live view stays temporary until you navigate away." — missing "then".

**May vs might:**
- Line 16: "Use it when you need a temporary wall quickly and may want to save it later." — should be "might".

**UI element issues:**
- Line 50: "On **Walls**, select **Create wall** in the upper-left corner of the page." Image evidence (`video-walls-list.png`) shows Create wall in the upper-RIGHT corner. Step 6 (line 78) correctly says "upper-right corner" for a different screenshot. Step 1 contradicts the screenshot.
- Line 52: alt text "Create wall button in the upper-left of the Walls page" — also wrong.
- Line 100: "Use the upper-right toolbar: **Edit** (**pencil**), full-screen, or **Save as wall**…" — "**pencil**" inside parens is bolded but isn't a UI label; should be plain text.

**List/step issues:**
- Line 54: "Enter a wall name and choose a layout that fits the number of cameras or alert tiles you want to show, and select **Done**." — combines three actions in one step.
- Line 55: "Expand **Cameras** to choose which cameras appear on the wall, and expand **Alerts** to configure alert tiles." — combines two actions.
- Lines 65–68: list items use lowercase after the colon ("choose how the alert renders…") even though they begin imperative full sentences. Per the colon rule, capitalize when a full sentence follows.
- Line 74: combines multiple actions in one step.

**Marketing / vague claims:**
- Line 5: "Lumana offers saved walls plus quick live grids plus secure external walls you can open anywhere." — "plus...plus..." is awkward marketing-style phrasing.
- Line 92: "Quick live view is useful when visibility matters immediately and you need to open a wall fast." — vague marketing tone.

**Visible TODO comment in source:**
- Line 116: HTML comment `<!-- TODO: When the flow is updated for the new UI, add the section "## Create a shared external video wall" (and its steps) back here. -->` — visible in source; should not ship in published docs (or should be tracked outside the file).

---

## Section 2 — `databases-analytics-and-search`

### `databases-analytics-and-search/README.md`

**Sentence-length violations (>25 words):**
- Line 3: "Use this section to build the people and vehicle data Lumana relies on, search footage, set up missing-object alerts, generate reports, and run occupancy and Event Tag workflows." — 28 words.

**Headings / consistency:**
- Card row labels mix patterns: "Tracking people", "Tracking vehicles", "Tracking containers" use gerunds (style guide requires bare-infinitive for how-to titles). Consider "Track people", "Track vehicles", etc. — or, if these are concept pages, change the underlying file titles to noun phrases.

**Banned/use-sparingly words:**
- Card label "Enhance your video data with Lumana Event Tags" uses **Enhance** (use-sparingly word). One occurrence in the section index; tolerable but worth flagging given the same word appears in the underlying page H1.

**Structural:**
- No "Next steps" section.

---

### `databases-analytics-and-search/build-a-database-of-people-and-vehicles.md`

**Sentence-length violations (>25 words):**
- Line 7: "If you plan to use Event Tags or import vehicles from a CSV file, then make sure you also have access to those features in your organization." — 27 words.

**List/step issues:**
- Step 2 of "Create a group" (line 32): "Enter a group name and select the profiles to include." — combines two actions.
- Step 3 (line 37): "Save the group." — does not name the actual button; the screenshot's button is **Create**, not Save.
- "Add a detected vehicle" step 2 (line 60): "Enter the owner name and verify the vehicle details." — combines two actions.
- "Import vehicles from a CSV file" step 3: combines several actions ("Download the template, enter the vehicle data, and upload the completed CSV file").
- Step 4 begins "If you are creating a license plate alert, then…" — conditional/aside, not part of a sequential workflow; better as a separate note.
- Indentation under numbered items is inconsistent (some `1. `, others `1.  ` with double-space). Cosmetic.

**Image-vs-step mismatches:**
- Line 36: `create-group-dialog.png` shows the dialog with a **Create** button, not a Save button — but step 3 says "Save the group."
- Line 64: image shows a dialog with field **Car owner's name** but the step says "Enter the owner name" — close but not the exact UI label.

---

### `databases-analytics-and-search/configure-a-space-occupancy-dashboard.md`

**Sentence-length violations (>25 words):**
- (No new ones in this round; line 18's previous violation was split into two sentences and is now compliant.)

**Voice / passive issues:**
- Line 50: "Once these settings are configured, the occupancy widget starts tracking…" — passive ("are configured"). Active: "After you configure these settings, the occupancy widget starts…"

**If/then violations:**
- Line 40: "If numbers still look wrong after a reset, see [Common accuracy issues]…" — missing "then".

**Image-vs-step mismatches:**
- Line 28: `space-occupancy-widget-entrances-selected-preview.png` is positioned in the "Add the occupancy widget" section but actually shows the *full* settings panel (Reset time, Visualization, Start/End, Weekends, Time) that belongs to the next section "Configure widget settings". Move or rename.

---

### `databases-analytics-and-search/enhance-your-video-data-with-lumana-event-tags.md`

**Sentence-length violations (>25 words):**
- Line 7: "This guide walks you through six steps: generate an API key, create an event tag, post events to the Lumana API, find them in **Search**, and optionally use them in alerts or a **Chart or table** widget." — 38 words.

**Headings:**
- Line 1 H1 contains the use-sparingly word **Enhance**. One occurrence is permitted, but in a page title it reads as marketing. Consider rewording (e.g., "Record external events with Lumana Event Tags").
- "Step 1: Generate an API key" / "Step 2: …" / "Step 3: …" — "Step N:" prefix is unconventional and breaks the bare-infinitive heading pattern.

**UI element issues / trustworthiness:**
- Line 19: "Select **Generate Key** (or the control that starts the create flow). The **Create API Key** dialog opens." — the screenshot at line 23 shows just **Create** as the button; the doc admits uncertainty with "(or the control that starts the create flow)". Pin down the exact button name.
- Line 36: "Select **Create event tag** (or open an existing tag to edit it)." — same hedging pattern.
- Line 7: "after you click the chart" — should use "Select", not "click".
- Line 76 / line 15: "Bearer" sometimes formatted as code (`Bearer`) and sometimes plain. Pick one and apply consistently.

**Image issues (alt text):**
- Lines 23, 38, 42, 144, 152, 164, 176, 186, 193: alt text is descriptive on screenshots; should be empty per the style guide.

**Image-vs-step mismatch:**
- Line 23: image shows **Create API Key** dialog with **Create** button; body text inconsistently refers to "Generate Key" / "Create".

**List/step issues:**
- Step 5 of "Use Search filters" (lines 138–142): "Set the operator (...), then enter the values." — combines two actions.

**Structural / guide-structure issues:**
- No "Next steps" section. Page ends with "Retention and storage".

**Other / typography:**
- Line 72: uses curly apostrophe in "camera's edit screen" (`camera's` with U+2019). Mixed apostrophe usage across the file.

---

### `databases-analytics-and-search/free-text-search.md`

**Sentence-length violations (>25 words):**
- Line 3: "Use free text search to look for people, vehicles, and other objects across your cameras by describing what you want to find in natural language." — 25 words. Borderline.

**Headings / product naming:**
- The page title is "Free text search" but the live UI's page header reads **Text search** (per `free-text-search-text-search-screen.png`), and the search panel has a **Free text** Beta filter. Naming is inconsistent across the file and across the section. Pick the term the product currently uses and align.

**List/step issues:**
- Step 3 (lines 29–33) is essentially a redundant duplicate of step 2's outcome — same image, same content. Remove or consolidate.

**Image issues (file format / frame / alt / path):**
- Lines 15, 23, 28, 33, 38, 43: alt text is empty (`alt=""`) — correct per the style guide. (Resolved from the previous round.)

---

### `databases-analytics-and-search/generate-reports.md`

**Voice / passive issues:**
- Line 47: "When **One time** is selected, **Reporting period** holds the date range." — passive. Recast in active voice.
- Line 89: "All reports are exported as CSV files." — passive. Active: "Lumana exports all reports as CSV files."

**Headings:**
- "Report types" — noun phrase concept-style heading inside a how-to.
- Line 43: "Report modes: One-time or recurring" — fragment after colon should be lowercase per the colon rule. "Report modes: one-time or recurring".
- "One-time report" / "Recurring report" — noun phrases under a how-to; mixes patterns with sibling sections.

**List/step issues:**
- Lines 21–41: numbered list mixes setup steps with reference content (the type definitions). Step 1 combines several actions; step 2 mixes form-fill with conditional branches for One-time vs Recurring.

---

### `databases-analytics-and-search/missing-object-alert.md`

**Sentence-length violations (>25 words):**
- Line 41: "Select the pencil icon <inline icon> next to the camera so you can mark the object the alert should track." — 27 words (around the inline image).
- Line 61: "From the preview, you can save footage to the archive with the archive icon <inline icon>, or use **Share** <inline icon> to share the clip according to your organization's policy." — 36 words.

**Headings:**
- "Why this alert helps" — concept-style heading on a how-to page. The bullets that follow read as marketing rather than user-task framing.

**Marketing / vague claims:**
- Lines 7–11 ("Why this alert helps") contain bold labels ("Real-time detection", "Automated tracking", "Security enforcement", "Operational continuity") that read as sales-pitch bullets. Section adds little operational value.

**List/step issues:**
- Step 4 (line 29): combines several optional actions.
- Step 8 (line 45): "In the **Mark object** dialog, outline the object, then select **Select**." — combines two actions and uses "select **Select**" without qualifying ("the **Select** button" / "the **Select** option").

**Asset folder structure:**
- Image filenames use the `custom-objects-` prefix (e.g., `custom-objects-edit-pencil-icon.png`, `custom-objects-archive-icon.png`) but the page is `missing-object-alert.md`. Per kebab-case section convention the prefix should match the page (`missing-object-`), or the assets should live in a section subfolder.

(Note: the previous round flagged the existence of a separate `custom-objects.md` page; that page no longer exists, so the prefix mismatch is now the only remnant of the old naming.)

---

### `databases-analytics-and-search/pixels-per-foot-for-camera-placement.md`

**Headings:**
- Line 1: "Pixels per foot (PPF) for camera placement" — uses parentheses. Style guide says minimize parentheses in headings. Define PPF in the body and drop the parens.

**Image issues:**
- Diagram images (formulas, PPF chart) have empty alt. The style guide says to provide meaningful alt for diagrams that convey information not in the surrounding text — these formulas qualify.
- Image filenames begin with `tracking-people-...` (e.g., `tracking-people-horizontal-length-formula.png`) but are used on this page. Asset naming should reflect the consuming page (`pixels-per-foot-` or shared `ppf-` prefix).

---

### `databases-analytics-and-search/search-video-footage-for-other-objects.md`

**Voice / passive issues:**
- Line 31: "Download controls are available on the preview when your role allows it." — passive ("are available").

**List/step issues:**
- Step 6 (line 31) combines several actions ("Select a tile to open the preview. Use **Images**, **Video**, **Objects**, or **Faces**…").
- Step 7 (line 39) combines three actions.
- Step 4 (line 25) and step 5 (line 27) feel split awkwardly: step 5 is the result of step 4. Consider combining ("Choose the object type. Matching detections appear as tiles…").

**UI element issues:**
- Line 21: "Open the dropdown labeled **Thumbnails**" — should use "Select the **Thumbnails** dropdown" for the UI verb.

(Image-vs-step content verified: street camera, metadata bar, dropdown, vehicle results, object preview, vehicle objects tab, archive dialog all match.)

---

### `databases-analytics-and-search/search-video-footage-for-people-or-vehicles.md`

**Headings:**
- "Open Search and set the scope" — bare infinitive; combines two actions in heading.

**List/step issues:**
- Step 1 of "Search for a person" (line 41): combines two actions ("select the time range and cameras you want. Then open the **Person** section…").
- Step 1 of "Search for a vehicle" (line 61): same pattern.
- Numbered lists at lines 83–85 and 91–96 use numbered list items as image-overlay annotations rather than procedural steps. Should be a description list or bullet list.

**UI naming inconsistency (cross-image):**
- The Search filter is named **Time period** in some screenshots and **Dwell** in others. Verify the live UI and update both the body text and screenshots.

---

### `databases-analytics-and-search/space-occupancy-analytics.md`

**Sentence-length violations (>25 words):**
- (Previous violations are now within range; line 104 sits at exactly 24 words after rewording.)

**Voice / passive issues:**
- Line 48: "The feature works best when every way into and out of the counted area is covered." — passive.
- Line 81: "Make sure every entrance and exit is covered." — passive.
- Line 100: "When entries are missed more than exits…" — passive.
- Line 104: "When cameras are aimed and count lines exist…" — passive.

**Headings (user-focused):**
- "Key features" with sub-headings "Real-time occupancy tracking", "Historical trend analysis", "Location analysis", "Dashboards and reporting", "Security and compliance" — feature-focused noun phrases on a concept page; consider whether each sub-heading describes what the user does or just what the tool does.

**Other / typography:**
- "Lumana's" uses curly apostrophe in some places and straight elsewhere — inconsistent.

---

### `databases-analytics-and-search/tracking-containers.md`

**Headings:**
- H1 "Tracking containers" — gerund noun phrase. Style guide requires bare infinitive "Track containers" for how-to. (Same pattern with `tracking-people.md` and `tracking-vehicles.md`.)
- "Key benefits" — concept-style heading on a how-to page; the bullets read as marketing.

**Marketing / vague claims:**
- Lines 9–13 ("Key benefits") read as marketing bullets ("Real-time tracking", "Accurate inventory", "Security", "Operations", "Compliance"). Section adds little operational value.

**UI element issues:**
- Line 17: "You can **edit camera**" — "edit camera" here is a verb-phrase, not a UI label, but it's bolded as if it were one. Either capitalise as the UI label (**Edit camera**) or remove the bolding.

---

### `databases-analytics-and-search/tracking-people.md`

**Headings:**
- Line 29: "Cross camera tracking" — missing hyphen. Body text uses "Cross-camera tracking" with hyphen. Inconsistent.

**Voice / passive issues:**
- Line 5: "The platform is designed to install with standard cameras." — passive and awkward phrasing ("designed to install").
- Line 9: "Cameras are added in Lumana and streaming reliably." — passive.
- Line 15: "These capabilities apply when people analytics is enabled…" — passive.
- Line 19: "individuals can be tracked and their crops stored at useful resolution." — passive.

**Image issues (diagram alt text):**
- Line 49 (`tracking-people-face-angle-guidelines.png`) and Line 63 (`tracking-people-distance-to-person-capabilities-diagram.png`): diagrams; should have meaningful alt text per the style guide. Currently empty.

**Other / typography:**
- Line 31: curly apostrophe in `organization's`.

---

### `databases-analytics-and-search/tracking-vehicles.md`

**Headings (bold-as-heading):**
- Line 125: `**Day view**` used as a section divider above an image — bold-as-heading is forbidden. Promote to H4.
- Line 129: `**Night view**` — same issue.

**Headings:**
- Line 31: "Cross camera tracking" — missing hyphen vs body's "Cross-camera tracking".

**Voice / passive issues:**
- Line 11: "Cameras are added in Lumana and streaming reliably." — passive.

**Image issues (diagram alt text):**
- Line 63 (`tracking-vehicles-ppf-requirements-diagram.png`): diagram; should have meaningful alt text.

**Other:**
- "FoV" capitalisation inconsistent (line 91 "FoV drives" vs section heading "Field of view").

---

## Section 3 — `set-up-cameras-and-devices` (root + `connect-cameras-by-brand`)

### `set-up-cameras-and-devices/README.md`

**Sentence-length violations (>25 words):**
- Opening paragraph sentence (47 words): "This section walks you through connecting cameras alongside Lumana Core, adding peripherals such as NAS, sensors, and speakers, stabilizing IP addresses, tuning network paths, and aligning streaming settings with Lumana Core." Split into two or three sentences.

**Headings / consistency:**
- "Recommended setup, networking, and streaming", "Connect cameras by brand", "Other devices", "Network and infrastructure configuration" — mix of bare-infinitive and noun-phrase patterns on the same page. Pick one.

**Asset folder structure:**
- Card icons reference `../.gitbook/assets/icon-*.svg` instead of the `.gitbook/assets/icons/` location described in the asset folder structure rule.

---

### `set-up-cameras-and-devices/overview.md`

**Headings:**
- H1 "Recommended setup tasks" — noun phrase. The page is a how-to (Prerequisites + Steps), so use a bare infinitive ("Set up your cameras and devices").
- Section labels `**Recommended for most sites**` and `**If your cameras support pan, tilt, and zoom**` — bold paragraphs used as headings. The style guide forbids bold-as-heading.

**List/step issues:**
- Numbered list resumes 4–6 after intervening bold pseudo-headings, breaking list semantics. Restructure as one continuous numbered list with sub-headings or split into multiple lists.

**Other / typography:**
- "you'll" uses curly apostrophe; "you're" elsewhere uses straight apostrophe — inconsistent.

**Structural:**
- "Other topics in this section" at the end serves as next steps but isn't titled "Next steps".

---

### `set-up-cameras-and-devices/camera-networking-options.md`

**Headings:**
- "Remote camera access (Camera VPN)" — has parentheses. Could be "Set up remote camera access".
- "When to use this" — vague.
- "Steps" — generic; describe the user's task.
- "Uniview speaker" / "TOA speaker" — noun phrases under a how-to context; should be bare infinitive ("Configure a Uniview speaker").

**"Where" connector misuse:**
- "...for devices on a private network where you need the manufacturer's configuration UI." — should be "when" or restructure.

**List/step issues:**
- Steps mix one-liner imperative steps with no terminal punctuation.
- The "Configure SIP on a Check Point router" steps wrap multiple sub-actions per numbered item.

**Image-vs-step mismatches:**
- `off-premise-sip-provider-service-list.png`: doc table lists `Media_server_1` (capital M) and `Media_server_2`; image shows `media_server_1` (lowercase) and `Media_server_2`. Naming inconsistency.
- `sip-traffic-inspection-rtp-services.png`: image shows 5 RTP services; doc table shows 4. The screenshot's `SIP_DEV_UDP` is missing from the doc table.
- `on-premise-devices-ip-phones.png`: doc table for step 4 shows one row (`Uniview_speaker / Single IP / 192.168.100.30`); image shows three rows (`Hikvision_speaker`, `speaker_toa_1`, `speaker_uniview`) at different IPs. Mismatch.
- `sip-service-ports-table.png`: doc step 5 has `SIP_UDP (5061)` twice; image shows `SIP_DEV_UDP (5061)` instead.
- `sip-account-setup-example.png`: alt text says "Uniview speaker SIP account settings…" but the screenshot is labeled "IP SPEAKER" with no Uniview branding.

**Structural:**
- No "Next steps" section.

---

### `set-up-cameras-and-devices/create-camera-shortcuts.md`

**Headings:**
- "Key benefits" — soft marketing label; consider just "Benefits" or fold into the intro.

**Run-in label colon placement (colon inside bold):**
- `**Follow movement across zones:**` — colon inside bold. Should be `**Follow movement across zones**:`.
- `**Shorten response paths:**` — same fix.
- `**Tie views together on large sites:**` — same fix.

**List/step issues:**
- Step 1: "Open the camera where you want shortcuts, then select **Edit camera**." — combines two actions.
- Step 6: "If you need more shortcuts on the same camera, repeat steps 3 through 5." — missing "then".

**Italics / term definitions:**
- Intro defines "Camera shortcuts" using bold rather than the italics convention for first-mention term definitions. Style guide: italicise the term on first mention.

**Image-vs-step issue:**
- `edit-camera-shortcuts.png` is placed before the numbered steps but illustrates the result of step 2. Per style guide, images should sit immediately after the step they illustrate.

**Other / typography:**
- Curly apostrophes in "camera's" — inconsistent with other files.

---

### `set-up-cameras-and-devices/create-links-between-cameras.md`

**Trustworthiness / completeness:**
- Page contains only "Coming soon!". Same defect as previous rounds — incomplete page that fails Usable and Trustworthy principles.

---

### `set-up-cameras-and-devices/enable-ptz-control.md`

**Headings:**
- H1 "Enable PTZ control" repeated as H2 below intro — duplicated heading.
- "Key capabilities" — "Key" leans marketing.

**Stacked headings / structure:**
- H2 "Prerequisites" sits between intro and the actual steps; "Key capabilities" interrupts the how-to flow with concept content.

**List/step issues:**
- Step 7: "Specify the **port** if it differs from the default `80`." — missing "then" (or restructure).
- Step 8 ("Select **Save** to apply changes.") — does not describe the visible result.

**UI element / capitalisation issues:**
- Step 5: "Select the **driver**." — UI label is "Driver" (capital D). Match exactly.
- Step 6: "Enter the **PTZ control path**." — UI field is labelled "X address", not "PTZ control path". Either rename in the doc or correct the screenshot. Mismatch.

**Image-vs-step mismatches:**
- `live-view-edit-camera-button.png`: step 2 says select the Edit camera **pencil** icon and shows a pencil inline; the screenshot's blue highlight is on the **wrench** (settings) icon, not the pencil. Alt text confirms: "Settings wrench control highlighted in the top toolbar." Major mismatch — text and inline icon disagree with the screenshot.
- `ptz-settings-onvif-address-port.png`: UI labels are "Driver", "X address", "Port number" while the doc text uses "driver" (lowercase), "PTZ control path", "port". Field-name mismatch ("PTZ control path" vs "X address").

---

### `set-up-cameras-and-devices/recommended-streaming-settings.md`

**Sentence-length violations (>25 words):**
- Line 3 (second sentence): "If you use Lumana cameras or a supported brand that Lumana Core sets up for you, you may not need to change anything; otherwise copy the values from [Primary stream settings](#primary-stream-settings) and [Sub stream settings](#sub-stream-settings) into the camera's own settings." — 49 words.
- Page body: "Higher bitrates usually mean more data. Lumana Core still uses **smart storage** so you are not wasting space: video stays high enough quality for **live processing** and **retrospective review**, and **rich recordings are kept when alerts fire**, without hoarding bulk high-bitrate footage when nothing important is happening." — 44-word second sentence.
- Line 188: "This degradation in video quality can severely impair the AI's ability to perform accurate analytics, leading to compromised functionality of Lumana Core's AI engine." — 26 words.
- Line 189: "If the bitrate is set too low, even on CBR, it may lead to poor video quality, characterized by pixelation and blurring, especially in scenes with high motion or complexity." — 31 words.

**If/then violations:**
- "If you do not follow the guidelines, you may see lower results in two areas:" — missing "then".

**May vs might:**
- "you may not need to change anything" — possibility, should be "might".

**Headings:**
- "#### Frequently asked questions" — H4 nested under H2 without intermediate H3. Heading-level skip.

**Marketing / vague claims:**
- "Smarter storage around alerts: Higher bitrates usually mean more data. Lumana Core still uses **smart storage** so you are not wasting space…" reads as marketing. Soften or rewrite as plain reference.
- "Stronger AI learning over time" / "Smarter storage around alerts" — borderline marketing phrases.

**Reference data / typos in tables:**
- "3MP / 3072×1028" — likely typo (3MP is typically 3072×1728).
- "4MP / 2560×1440" — that's 3.7MP/QHD, not strictly 4MP.
- "8MP / 3480×2160" — likely typo for 3840×2160 (4K UHD).

**Structural:**
- No "Next steps" section.

---

### `set-up-cameras-and-devices/set-up-a-camera-floor-plan.md`

**Headings:**
- "Key benefits" — borderline marketing label.
- "Use the camera floor plan feature" — tool-focused ("the camera floor plan feature"). Should be bare infinitive, e.g., "Add a floor plan and place cameras". Style guide: avoid "feature".

**Italics misuse:**
- Line 3: "adding a *floor plan*, an interactive map…" uses asterisk italics. Style guide requires underscore italics: `_floor plan_`.

**List/step issues:**
- Step 6: "Add your image using drag and drop or **Or upload from your computer**. Use a PNG or JPG file." — combines two actions.
- Step 7: "Select the [icon] icon in the top right corner to start adding and positioning your cameras on the floor plan." — combines two actions ("adding AND positioning").
- Step 8: "Select **Add floor plan** to save the floor plan." — combined save action; describing result is OK in next paragraph.

**Image-vs-step mismatches:**
- `floor-plans-menu-overview.png`: step 1 says "top **left** corner" but the screenshot shows the **Floor plans** tab is in the **top RIGHT** corner. Mismatch.
- `edit-floor-plan-layout.png`: step 8 says "Select **Add floor plan** to save"; the screenshot shows a completed floor plan with cameras already placed and labeled, not a pre-save state.

**Voice / phrasing:**
- Line 42: "Now you are able to view the floor plan, when you hover over a camera you will get a live view for it." — uses future tense ("you will get") and reads awkwardly. Recast in present tense.

(Image frames now applied correctly — resolved from the previous round.)

---

### `set-up-cameras-and-devices/set-up-a-static-ip-address.md`

**Sentence-length violations (>25 words):**
- "You likely have DHCP if a router, office firewall, or Lumana Core on the network assigns addresses, and your camera already shows an IP in Lumana without you setting a static address on the device." — 35 words.
- Line 43: "This way, the camera keeps the same IP address after reboots or power interruptions, when the server always offers that lease to this MAC address." — 26 words.
- Line 77: "Assign a temporary static IP to your computer, on the same subnet as the camera (for example, `192.168.1.10`, subnet mask `255.255.255.0`), if the camera did not receive an address automatically." — 34 words.

**If/then violations:**
- "If needed, refer to your computer or operating system documentation for instructions on setting a temporary static IP address." — missing "then".

**Trustworthiness / product details:**
- Line 68: example uses "**Lumix.ai LB800**" — appears to be a non-Lumana brand on a Lumana page. Verify whether LB800 is actually a Lumana-branded device, or use a clearly Lumana-branded example camera.

**UI element issues:**
- Doc text uses "subnet mask" (lowercase) but the UI label is "Subnet mask" (capital S). Match exactly.

**Structural:**
- No "Next steps" section.

(Image frames are now applied correctly — resolved from the previous round.)

---

### `set-up-cameras-and-devices/connect-cameras-by-brand/README.md`

No defects found. (Optional improvement: "wide range" is mild marketing.)

---

### `set-up-cameras-and-devices/connect-cameras-by-brand/axis.md`

**Sentence-length violations (>25 words):**
- "**Admin credentials (recommended)**: Use the camera's root username and password in Lumana Core. This gives Lumana full access to the Axis API and settings, reduces compatibility gaps, and avoids subtle permission errors." — 26 words in the second sentence.
- Line 65: "**First visit** (root password and HTTPS): The first time you open the camera in a browser, you may need to create a self-signed certificate for HTTPS and set the root password." — 30 words.
- "If you cannot activate the camera, reach its web UI, or complete network setup, see the [General troubleshooting guide]() or your Axis documentation for device activation." — 27 words.
- "Add an ONVIF user: Add a user intended for ONVIF access. Use a strong password and assign the **Administrator** role (or the role your organization requires for streaming control)." — 28 words.
- "Manual profiles are needed when Lumana cannot create the required streams automatically (for example, when you connect with lower-privilege credentials) or when you want explicit control over encoder names and quality." — 31 words.

**Headings:**
- H1 "Connect Axis cameras" — bare infinitive, OK. But "AXIS Q16 Series" (caps) appears in body alongside "Axis cameras" — inconsistent product naming.

**If/then violations:**
- "If no DHCP server is present, many Axis cameras default to `192.168.0.90`." — missing "then" (or restructure as a statement of fact).
- "Plan that step if you will use ONVIF in Lumana." — uses future tense "will use"; should be present. Also missing "then".
- "If you cannot activate the camera, reach its web UI, or complete network setup, see…" — missing "then".
- "If the name in Axis and the name in Lumana differ at all, video may not attach." — missing "then".

**Image-vs-step issues:**
- `axis-stream-profile-lumana-main.png`: shows "Maximum" (MBR) bitrate control. The site-wide streaming guidance (in `recommended-streaming-settings.md`) recommends CBR, but the brand-comparison table in that same page lists MBR for Axis main. Cross-doc inconsistency to clarify.

**Structural:**
- No "Next steps" section.

---

### `set-up-cameras-and-devices/connect-cameras-by-brand/hanwha.md`

**Headings:**
- H1 "Connect Hanwha cameras" — bare infinitive, OK.

**If/then violations:**
- "Select the profile row… or select **Add** to create a row if you need one." — missing "then".
- "If your main or Storage row sits on a different profile index, change the numbers in the path to match." — missing "then".

**List/step issues:**
- Step 3 (under "Set a static IP address"): combines five actions ("Open the **IP address** tab, set **IP type** to **Manual**, enter **IP address**, **Subnet mask**, **Gateway**, and DNS servers, then select **Apply**.").
- Multiple other steps combine two or more actions ("Set that row as the **Default** profile and set **Codec** to **H.265**.").

**Image-vs-step mismatch:**
- `hanwha-storage-profile-settings.png`: image shows "Maximum bitrate 2048 kbps" (MBR/VBR mode); doc text says Bitrate control should be CBR. Field/value mismatch.

**Structural:**
- No "Next steps" section.

---

### `set-up-cameras-and-devices/connect-cameras-by-brand/hikvision.md`

**Sentence-length violations (>25 words):**
- "**Detect and Initialize the Camera**: The SADP tool will scan your network and list Hikvision devices. Select your camera, note its IPv4 address and status, and, if the device is not initialized yet, set a password to activate it." — 35 words in the second sentence.
- "Using an **Operator** user with broad remote permissions (often **Select all** in the **Add** user dialog) allows Lumana Core to configure camera settings, including stream settings, more reliably." — 28 words.
- "You can now proceed to [Connect a camera](), which will guide you through the process of adding your camera to Lumana Core and ensuring everything is functioning as expected." — 29 words.

**Future tense / passive:**
- "The SADP tool **will** scan your network…" — should be present tense ("scans").
- "which **will** guide you through the process…" — should be present tense.
- "A confirmation message or indicator should appear, confirming that the new user has been added successfully." — "should appear" + "has been added" passive; recast in active present tense.

**If/then violations:**
- "If you are using admin credentials, you can proceed directly to [Connect a camera]()." — missing "then".

**Use sparingly:**
- "Ensuring everything is functioning as expected" uses "ensuring". One instance, under the limit, but worth noting.

**Capitalisation / UI labels:**
- "**Detect and Initialize the Camera**" uses Title Case — should be sentence case.
- The doc switches between **Digest** and **digest** for the Hikvision-CGI Authentication value. Pick one (the live UI shows "digest" lowercase) and apply consistently.

**List/step issues:**
- The "Activate your camera with the SADP tool" section uses bullets rather than numbered steps for a sequence. Use a numbered list.

**Stacked headings:**
- "Prepare your Hikvision camera" (H3) is followed by a single short paragraph then jumps to "Activate your camera with the SADP tool" (H3) — feels like a stub heading.

**Structural:**
- No "Next steps" section.

---

### `set-up-cameras-and-devices/connect-cameras-by-brand/lumana.md`

**Headings:**
- H1 "Lumana" is just the brand name. Should be "Connect Lumana cameras" to match sibling pages and bare-infinitive convention.

**Run-in label colon placement (colon inside bold):**
- `**Manage device passwords:**`, `**Additional bulk configuration:**`, `**Restore default settings:**`, `**Import configuration:**`, `**Export configuration:**` — colons all inside bold. Move outside.

**Bold-as-heading:**
- `**Import configuration:**` and `**Export configuration:**` are bold labels at paragraph starts (not list items). They function as section headings — should be H3.

**List/step issues:**
- "The following features are available for individual cameras only:" then 3 items, with the third being a run-in bold label — non-parallel item structure.

**If/then violations:**
- "If you run into camera issues, the Lumana Camera Finder application offers debugging tools." — missing "then".

**Structural / depth:**
- Page lacks Prerequisites and connection-to-Lumana-Core steps that the sibling brand pages provide. Asymmetric coverage.
- No "Next steps" section.

**Trustworthiness:**
- Camera labelled "LB800" in screenshots — same Lumix-branded device shown in `set-up-a-static-ip-address.md`. Confirm whether LB800 is a Lumana-branded device.

---

### `set-up-cameras-and-devices/connect-cameras-by-brand/other-brands.md`

**"Where" connector misuse:**
- "alongside [Recommended streaming settings] where applicable" — should be "when applicable".

**Structural / depth:**
- No connection guidance — just a model list. Inconsistent with the README card description that promises "compatibility notes and streaming guidance".
- No "Next steps" section.

**Other / typography:**
- "vendor's" uses curly apostrophe.

---

### `set-up-cameras-and-devices/connect-cameras-by-brand/supported-cameras.md`

**Voice / passive issues:**
- "Most cameras that support ONVIF or RTSP streaming can be integrated with Lumana." — passive ("can be integrated"). Active: "Lumana integrates with most cameras that support ONVIF or RTSP."

**If/then violations:**
- "If your camera is not listed, it may still work if it supports ONVIF or RTSP." — missing "then".
- "Please contact [support@lumana.ai]() if you don't find your camera model on this list." — "Please" is unnecessary; missing "then".

**List/step issues:**
- "- Pelco, and more..." — last bullet ends with "and more..." (ellipsis) and combines a comma list. Awkward and informal.

**Marketing language:**
- "wide range", "flexibility", "fits your deployment needs" — soft marketing tone in the intro.

**Structural:**
- No "Next steps" section.

---

### `set-up-cameras-and-devices/connect-cameras-by-brand/verkada.md`

**Headings:**
- H1 "Verkada" — just the brand name. Should be "Connect Verkada cameras" to match sibling pages.

**Voice / passive issues:**
- "After RTSP is enabled, Verkada provides an RTSP URL." — passive. Active: "After you enable RTSP, Verkada provides an RTSP URL."

**If/then violations:**
- "Make sure Lumana Core is the only client on that URL, or use separate stream endpoints if Verkada provides them." — missing "then".

**List/step issues:**
- Step 1 under "Enable RTSP on the camera" is a single-item numbered list. Style guide requires lists to have at least two items. Convert to prose.
- Step 2 of "Configure the main stream" combines five field entries.

**Structural:**
- No "Next steps" section.

---

## Section 3 (continued) — `network-and-infrastructure-configuration` and `other-devices`

### `set-up-cameras-and-devices/network-and-infrastructure-configuration/README.md`

**Asset folder structure:**
- Card icons live at `.gitbook/assets/` root rather than under `.gitbook/assets/icons/` per the asset folder structure rule.

**Other / cosmetic:**
- Two blank lines between H1 and the first paragraph (cosmetic).

**Structural:**
- No "Next steps" section.

---

### `set-up-cameras-and-devices/network-and-infrastructure-configuration/configure-lumana-core-as-a-dhcp-server.md`

**Voice / passive issues:**
- "This feature is supported on Ethernet 2…" — passive. Recast.
- "When enabled, the DHCP server on Lumana Core provides essential networking services, including:" — passive ("When enabled"); also uses use-sparingly word "essential" in a marketing way.
- "Multiple servers can be specified, separated by commas." — passive.
- "The duration, in seconds, for which an IP address is leased to a device before it needs renewal." — passive.

**Headings (user-focused):**
- "Key DHCP server capabilities" — feature-focused noun phrase inside a how-to. Recast as a user-task heading or fold into the intro.
- "Configuration parameters", "Example configuration", "Address reservation", "Address reservation use cases" — noun phrases on a how-to page; mixes content types.

**UI text exact match (capitalisation):**
- Doc renders field labels as **Starting IP Address**, **Ending IP Address**, **DNS Servers**, **Lease Time** (Title Case). Live UI shows them in sentence case: **Starting IP address**, **Ending IP address**, **DNS servers**, **Lease time**. Match the live product exactly.

**If/then violations:**
- "If another DHCP server is already active on that segment, review the impact before you enable this feature." — missing "then".

**List/step issues:**
- Step 2 combines four actions ("Select **Devices**. Under **Devices by types**, select **Cores** … On the **Devices list**, apply the **Cores** filter … Then select **Edit location**…"). Split.
- Step 3 combines three actions.
- The "Configure address reservation" steps are vague ("Identify the MAC address", "Save the configuration") — they don't reference UI controls.

**Tables vs lists:**
- The "Configuration parameters" content reads as a parameter list and would render better as a table.

**Structural:**
- No "Next steps" section.

**Other / typography:**
- Curly apostrophes used in some places ("Lumana's") — inconsistent.

---

### `set-up-cameras-and-devices/network-and-infrastructure-configuration/firewall-requirements.md`

**Sentence-length violations (>25 words):**
- "Prefer the [API response](#infrastructure-ips) above when your tools can consume it. The table below is a **static reference** grouped by **category** and **region**, useful for ticketing, change control, or firewalls that need explicit rows." — 27-word second sentence.

**Voice / passive issues:**
- "All traffic is encrypted with TLS and DTLS." — passive.
- "If UDP is blocked, TURN/TLS over TCP 443 is used." — passive (and missing "then").

**If/then violations:**
- "If your network firewall monitors outbound traffic, allow the following endpoints for the application itself." — missing "then".
- "If UDP is blocked, TURN/TLS over TCP 443 is used." — missing "then".

**Headings:**
- "OS Updates" — should be "OS updates" (sentence case).
- Multiple stacked H2 → H3 jumps with no intervening paragraph: `## Lumana Core and platform requirements` → `### Infrastructure URLs`; `## Shared live view and media requirements` → `### STUN servers`; `## Lumana Web application requirements` → `### Web application infrastructure`; `### Regional media server details` → `#### US Central`. Add a description paragraph beneath each parent heading.

**Capitalisation after colon (run-in labels):**
- "**Lumana URLs**: A list of domains…" — capital "A" after colon for a fragment; should be lowercase "a list".
- "**Lumana IPs**: An API endpoint that returns…" — same issue.

**Vocabulary inconsistency:**
- "whitelist" used in some places, "allowlist" in others. Pick one (Google/current best practice prefers "allowlist").

**Tables / data consistency:**
- Region naming inconsistent: `ME-West` vs `ME West` (both used). `US-Center` should be `US-Central` to match the heading "US Central".

**List items not parallel:**
- The "OS Updates" list mixes "`archive.ubuntu.com` - ports: 80, 443 TCP outbound" with "`ports.ubuntu.com` - 443 TCP outbound" — inconsistent prefix usage.

**Section title:**
- The page ends with "## Related" instead of the required "## Next steps".

---

### `set-up-cameras-and-devices/network-and-infrastructure-configuration/local-time-and-ntp-configuration.md`

**Sentence-length violations (>25 words):**
- "Configure Network Time Protocol (NTP) so Lumana Core can keep its system time accurate. Use this task if you need to point the Core to a local NTP server instead of the default Lumana NTP servers." — 27-word second sentence.

**If/then violations:**
- "Use this task if you need to point the Core to a local NTP server instead of the default Lumana NTP servers." — "if" without "then" in predicate (subordinator usage; borderline).

**List/step issues:**
- Step 1 (Change the location time zone): combines three actions ("Open **Devices** → **Devices list**. Use the **Cores** filter… On the location row… select **Edit location**.").
- Step 2: combines two actions ("set **Time Zone**, then select **Save**").

**Image issues (alt text):**
- Lines 19 and similar: alt text is descriptive on screenshots; should be empty per the style guide.

(Image-vs-step content verified.)

---

### `set-up-cameras-and-devices/network-and-infrastructure-configuration/lumana-core-hardware-specifications.md`

**Headings:**
- "Product dimensions (mm)" — uses parentheses. Could be "Product dimensions in millimetres".
- Stacked headings: `## Rear panel` is immediately followed by an image (no description paragraph). Same for `## Product dimensions (mm)`. `## Installation` is immediately followed by H3 with no paragraph between. Add intervening text.

**Image-vs-step mismatches:**
- "Lumana Core ships with a **120 V** AC to **12 V DC** power adapter. Connect it to the **POWER** input on the rear panel." The labelled barrel jack on the screenshot is **DC IN**, not **POWER**. **POWER** is the round button next to the HDMI ports. A user told to plug power into "POWER" will look at the wrong port.

**Tables / data consistency:**
- "0 °C ~ 50 °C" / "−40 °C ~ 85 °C" — uses tilde for ranges. Convention is en-dash or "to" ("0 °C to 50 °C").
- "100–240 V ~ 1.8 A (50–60 Hz)" — mixes en-dashes and tilde in one line.

**Information fragmentation:**
- "Connect Lumana Core to the network" links externally to a knowledge-base article rather than living in the docs site.

---

### `set-up-cameras-and-devices/other-devices/README.md`

**Asset folder structure:**
- Card icons reference `../../.gitbook/assets/icon-*.svg` at the assets root, not under `icons/`.

**Headings (user-focused):**
- Card titles like "**FLIR sensors**", "**Disruptive sensors**", "**Smart speakers**", "**GPIO devices**", "**Network attached storage (NAS) devices**" are feature/product names rather than user tasks. The "**Configure SIP for smart speakers**" card is correctly bare-infinitive.

**Structural / cosmetic:**
- Two blank lines between H1 and the first paragraph.

---

### `set-up-cameras-and-devices/other-devices/disruptive-sensors.md`

**List/step issues:**
- Step 1: explanatory paragraph contains three actions ("Log in… navigate to **Organization settings** -> **API Keys**. Generate a key and save it."). Split.
- Step 2: at least three actions; uses "add the Lumana API key from step 1 in **Custom HTTP Request Header**" — should be "enter" not "add" for a form field.
- Steps 3, 4, 5 each combine multiple actions.

**UI text exact match:**
- Doc says **API Keys** (Title Case) in step 1 then **Organization Settings** (Title Case) in step 4. Live UI shows "API keys" and "Organization settings" in sentence case.
- Doc says **Integration** in step 4; UI shows **Integrations** (plural).
- Doc says "In **Data Connector**, create a new connector"; UI shows "Data Connectors" page with "Create New Data Connector" button.
- Doc step 5 says "**Devices** -> **Location** -> **Edit Location**"; UI breadcrumb is "Cameras > Los Gatos, California (Office) > Edit location > Sensors". The doc's nav path doesn't match the actual product navigation; "Edit Location" should be "Edit location".

(Image-vs-step content verified for all five screenshots.)

---

### `set-up-cameras-and-devices/other-devices/flir-sensors.md`

**Trustworthiness / completeness:**
- Page contains only "Coming soon!". Same defect — incomplete page.
- Two blank lines between H1 and body. Exclamation point is informal.

---

### `set-up-cameras-and-devices/other-devices/gpio-devices.md`

**Headings:**
- H1 "GPIO devices" — noun phrase for a how-to page. Bare infinitive ("Connect GPIO devices to Lumana Core") would be more user-focused.
- Stacked headings: `## Connect a device` is followed immediately by `### Parts list` with no description paragraph between. Add intervening text.

**Sentence-length violations (>25 words):**
- "In Lumana, you can program GPIO pins to toggle high or low in response to an alert. Third-party devices can read those hardwired signals from Lumana, or you can drive devices such as LEDs, motors, or relays." — second sentence 27 words.

**Voice / passive issues:**
- "an LED is connected to the GPIO" — passive in "Connect a device" intro. Active rewrite.
- "Once enabled, open the alert editor…" — passive participial phrase.

**List/step issues:**
- Step 3: "Select the GPIO to use. The Core can support up to 4 GPIOs, toggle high or low, and control how long the signal remains active." — combines selection and three configuration descriptions. Split.

**List/step formatting:**
- "Parts list" uses `*` bullet markers; "Wiring notes" uses `-`. Inconsistent in same file.
- "Wiring notes" items are full sentences but lack periods. Style guide says full sentences in lists need periods.

**Image issues (diagram alt text):**
- `gpio-pinout.png` and `gpio-led-wiring.png` are diagrams that carry information not in surrounding text. Style guide says diagrams should have meaningful alt text — currently empty.

---

### `set-up-cameras-and-devices/other-devices/network-attached-storage-nas-devices.md`

**Sentence-length violations (>25 words):**
- "Adding a NAS does not replace Lumana Core. The NAS works alongside the Core as both an additional storage location for longer retention and a backup target for recorded data." — second sentence 30 words.

**Voice / passive issues:**
- "No license is needed for the first 30 days." — passive.
- "The storage device must be reachable on the network by the Lumana Core unit." — passive.
- "Choose your storage type. This can be either **NFS** or **Object Storage**." — second sentence is passive-feeling; active: "Select either **NFS** or **Object storage**."

**Product naming:**
- "smart search functionality" should be **Smart Search** per the product-name table.

**Headings:**
- H1 "Network attached storage (NAS) devices" — uses parentheses. Define NAS in the body.
- "Storage capacity calculation", "Examples of NAS servers", "Examples of HDDs" — noun phrases on a how-to page; mixes content types.

**List/step issues:**
- Step 2 (Add an external storage server): combines three actions.
- Step 3: two actions ("select **External Storage**, then select **Add external storage**").
- Step 5: two actions ("Select **Test**…then select **Save external storage**").
- "Storage capacity calculation" items are a mix of phrases and full sentences but inconsistently lack periods.

**Capitalisation after colon:**
- `* **Path**: combine the NAS IP and export path…` — full sentence after colon should be capitalised. "Combine" should be "Combine" (capital).

**UI labels (exact match):**
- Doc references **External retention** but UI label is "External retention period". Match exactly.
- Doc and screenshot disagree on the example name: doc text uses `NFS-Server-1`; screenshot field shows `NFS-Sever-1` (typo in the screenshot data).

**Bullet style:**
- Mixes `*` and `-` markers across lists in the same file.

**Other / typography:**
- "camera's live view" uses curly apostrophe.

---

### `set-up-cameras-and-devices/other-devices/sip-for-smart-speakers.md`

**Stacked headings:**
- `## Configure SIP on a Check Point router` is followed immediately by `### Prerequisites` with no paragraph between.

**List/step issues:**
- Step 2 (Configure the router section): "Enable VoIP. On the **Access Policy** > **VoIP** screen, enable VoIP." — restates the same action twice.
- Step 3 combines four actions; step 4 combines three; step 5 single-row table is awkward.
- Uniview step 6: "Save." — should be "Select **Save**." Same issue with TOA step 5.
- Uniview step 7: "Verify the speaker's status shows **Registered**." — UI screenshot shows "REG SUCCESS" in the highlighted area, not "Registered".

**UI text exact match:**
- Doc references **SIP_UDP** at port 5061 (twice); image shows **SIP_DEV_UDP**. Service name mismatch (also flagged in `camera-networking-options.md`).
- Doc's step 5 example shows `Uniview_speaker / Single IP / 192.168.100.30`; image shows `Hikvision_speaker` at that IP and different speaker names at others. Mismatch.
- Doc's Uniview SIP fields use "Username, ID"; UI uses "User Name, Auth ID". Mismatch.
- Doc's `media_server_1` / `Media_server_1` casing differs from screenshot. Pick one.

**Voice / passive:**
- Hint "**Note**: SIP credentials (address, username, password) are supplied by your CSM." — passive. Active: "Your CSM provides SIP credentials."

**Bullet style:**
- Mixes `-` and `*` bullets.

**Other / typography:**
- "speaker's own admin interface" / "speaker's status" — Unicode right-single-quotes.

**Tables — formatting:**
- Doc tables escape underscores like `Oregon\_Gateways`, `SIP\_TLS\_AUTH`. Acceptable but inconsistent (some `\_` and some not).

---

### `set-up-cameras-and-devices/other-devices/smart-speakers.md`

**Sentence-length violations (>25 words):**
- "Lumana can also use Session Initiation Protocol (SIP) with supported network speakers. That usually involves firewall or router rules on your side plus SIP account settings on each speaker." — second sentence 28 words.
- "Lumana can work with IP speakers you can trigger over the network with a **REST** API or direct **TCP**/**UDP** messaging. You add the speaker in Lumana, load audio and patterns on the device, then attach alert actions to play those patterns." — second sentence 28 words.

**Voice / passive issues:**
- "the speaker is reachable from Lumana" — passive in the intro to "Configure the TOA IP-A1SC15". Active: "Lumana can reach the speaker."

**Headings:**
- H1 "Smart speakers" — noun phrase for a partly how-to page.
- "Key use cases" — noun phrase concept section inside a how-to.

**Run-in label colons (Key use cases):**
- "**Pre-recorded alarms:**" — colon inside bold. All four "Key use cases" bullets violate the rule. Move colon outside bold.

**List/step issues:**
- Step 2 of "Connect and address the speaker" combines two actions ("Log in to the speaker at its default IP address. Assign a **static IP** that fits your LAN.").
- Step 3 of "Upload media and define a pattern" combines four actions/observations.
- "Add the speaker in VMS+" step 1 admits uncertainty ("(or the add control your site uses)") — verify the actual UI label.
- Step 4: "(or **Save**)" — same uncertainty. "the add fails" reads colloquially; better as "if the connection test fails".
- "Play a pattern from an alert" step 1: "Open the flow to **create** or **edit** an alert." — verbs are bolded as if UI controls but they aren't.
- Step 2: bolds `pattern` and `speaker` even though they're parameter names, not literal UI labels.

**UI text exact match:**
- Doc says "**volume**"; UI says "Input Volume".
- Doc says "username" (one word); UI says "User Name" (two words).

**Other / typography:**
- "speaker's own admin interface" — Unicode right-single-quote.

---

## Cross-cutting / recurring themes

These themes show up across multiple pages. Treating them in a single pass will be more efficient than fixing them file by file.

**1. Sentence length above 25 words.** Recurs across most files; the worst examples are in `set-up-cameras-and-devices/README.md` (47 words), `recommended-streaming-settings.md` (49 + 44 words), `enhance-your-video-data-with-lumana-event-tags.md` line 7 (38 words), `axis.md` line 65 (30) and other long sentences (28, 31), `hikvision.md` line 41 (35), `set-up-a-static-ip-address.md` (35 + 34), `nas-devices.md` (30), `smart-speakers.md` (28 ×2).

**2. If/then construction.** The single most pervasive defect. Dozens of conditional sentences across nearly every file are missing "then" in the predicate. Worst offenders: `the-system-health-dashboard.md` (4 instances), `recommended-streaming-settings.md`, `axis.md` (4+), `hikvision.md`, `lumana.md`, `verkada.md`, `firewall-requirements.md`, `configure-lumana-core-as-a-dhcp-server.md`. Run a single pass.

**3. Image-vs-step factual mismatches.** Several screenshots actively contradict the surrounding text:
- `set-up-a-camera-floor-plan.md`: "top **left** corner" vs screenshot showing top-right.
- `enable-ptz-control.md`: text says pencil icon; screenshot highlights the wrench. Field name "PTZ control path" doesn't match the UI's "X address".
- `lumana-core-hardware-specifications.md`: text tells users to plug power into **POWER**; the labelled power input is **DC IN** (POWER is a button).
- `share-video.md`: "existing-links-dialog" image actually shows the Share/Create-link tab, not the Existing links tab.
- `live-view-streaming-and-quality.md`: "cloud streaming diagram" actually depicts the local-first decision flow. Diagram text contains spelling errors ("Incomplient", "compatibale").
- `system-health-dashboard.md`: dashboard-overview image actually shows Devices list with an arrow.
- `lumana-timelapse.md`: Create-timelapse-dialog image is misplaced next to retention-availability text.
- `multi-camera-playback.md`: `multi-camera-playback-wall-view.png` is missing on disk (broken reference).
- `camera-networking-options.md` and `sip-for-smart-speakers.md`: SIP service rows say `SIP_UDP`; screenshots show `SIP_DEV_UDP`. On-premise device example in doc uses `Uniview_speaker`; screenshot shows `Hikvision_speaker` at that IP.
- `axis.md` and `hanwha.md`: stream profile screenshots show "Maximum"/MBR bitrate while the body text says CBR.
- `nas-devices.md`: doc says `NFS-Server-1`; screenshot's field shows `NFS-Sever-1`.

**4. Image alt-text policy not applied consistently.** Many screenshots still carry descriptive alt text (live-video pages, `enhance-your-video-data-with-lumana-event-tags.md`, `local-time-and-ntp-configuration.md`, `disruptive-sensors.md`, etc.). At the same time, several diagrams that *should* have descriptive alt have empty alt (`gpio-pinout.png`, `gpio-led-wiring.png`, PPF formula images, face-angle diagram, PPF funnel diagrams, hardware dimensions). The rule is: empty alt for screenshots, meaningful alt for diagrams that carry information not in the surrounding text.

**5. Bold-as-heading misuse.** `share-video.md` lines 15 and 31 (`**Go to Archives**`, `**Create link and copy or send**`); `overview.md` (`**Recommended for most sites**`, `**If your cameras support pan, tilt, and zoom**`); `lumana.md` (`**Import configuration:**`, `**Export configuration:**`); `tracking-vehicles.md` lines 125 and 129 (`**Day view**`, `**Night view**`).

**6. Run-in label colon placement (colon inside bold).** `create-camera-shortcuts.md`, `lumana.md`, `smart-speakers.md` all place colons inside bold for run-in labels (`**Label:**` instead of `**Label**:`).

**7. Naming-pattern inconsistency in `connect-cameras-by-brand/`.** `lumana.md` is titled "Lumana" and `verkada.md` is titled "Verkada" (noun) while sibling pages use bare-infinitive titles like "Connect Axis cameras" / "Connect Hanwha cameras" / "Connect Hikvision cameras". Pick one and apply consistently.

**8. Steps that combine multiple actions.** Pervasive in `share-video.md`, `live-view.md`, `multi-camera-playback.md`, `video-walls-and-shared-displays.md`, `build-a-database-of-people-and-vehicles.md`, `enhance-your-video-data-with-lumana-event-tags.md`, `generate-reports.md`, `missing-object-alert.md`, `set-up-a-camera-floor-plan.md`, `hanwha.md`, `verkada.md`, `configure-lumana-core-as-a-dhcp-server.md`, `disruptive-sensors.md`, `nas-devices.md`, `sip-for-smart-speakers.md`, `smart-speakers.md`. Split each into atomic actions or use sub-steps.

**9. Passive voice.** Recurs in `live-view-streaming-and-quality.md`, `generate-reports.md`, `space-occupancy-analytics.md`, `tracking-people.md`, `tracking-vehicles.md`, `search-video-footage-for-other-objects.md`, `configure-lumana-core-as-a-dhcp-server.md`, `firewall-requirements.md`, `gpio-devices.md`, `nas-devices.md`, `smart-speakers.md`, `sip-for-smart-speakers.md`. Common patterns: "is supported", "is enabled", "is exported", "is reachable", "must be reachable", "Once enabled", "are configured".

**10. UI label capitalisation drift.** Doc renders product UI labels in title case while the live UI uses sentence case: "Starting IP Address" → "Starting IP address"; "API Keys" → "API keys"; "Integration" → "Integrations"; "Data Connector" → "Data Connectors"; "External retention" → "External retention period"; "subnet mask" → "Subnet mask"; "username" → "User Name"; "Edit Location" inconsistent with "Edit location"; "Edit Camera" inconsistent with "Edit camera". Pin down each label by checking the live UI.

**11. Future tense / "will".** `axis.md` ("Plan that step if you will use ONVIF"), `hikvision.md` ("The SADP tool will scan your network", "which will guide you"), `set-up-a-camera-floor-plan.md` ("you will get a live view"), `recommended-streaming-settings.md` ("you will need to balance"). Recast in present tense.

**12. May vs might.** `live-view-streaming-and-quality.md` (5 instances), `the-system-health-dashboard.md` (3), `share-video.md` (1), `video-walls-and-shared-displays.md` (1), `recommended-streaming-settings.md` (1). All possibility uses; switch to "might".

**13. Marketing / vague claims.** `missing-object-alert.md` "Why this alert helps", `tracking-containers.md` "Key benefits", `space-occupancy-analytics.md` "Key features", `recommended-streaming-settings.md` ("smart storage", "Smarter storage around alerts", "Stronger AI learning over time"), `video-walls-and-shared-displays.md` ("Lumana offers saved walls plus quick live grids plus secure external walls…"), `enhance-your-video-data-with-lumana-event-tags.md` H1 (uses "Enhance"), `supported-cameras.md` ("wide range", "flexibility", "fits your deployment needs"). Trim or recast as user-task framing.

**14. Stacked headings without intervening paragraphs.** `firewall-requirements.md` (multiple), `lumana-core-hardware-specifications.md` (Rear panel, Product dimensions, Installation), `gpio-devices.md` (Connect a device → Parts list), `sip-for-smart-speakers.md` (Configure SIP on a Check Point router → Prerequisites).

**15. Headings that aren't user-focused or that misuse "Step N:" framing.** `enhance-your-video-data-with-lumana-event-tags.md` uses "Step 1:" / "Step 2:" prefixes that break the bare-infinitive convention. `configure-lumana-core-as-a-dhcp-server.md` "Key DHCP server capabilities", `set-up-a-camera-floor-plan.md` "Use the camera floor plan feature", `enable-ptz-control.md` and `create-camera-shortcuts.md` and `set-up-a-camera-floor-plan.md` "Key benefits"/"Key capabilities".

**16. Heading parentheses.** `lumana-core-hardware-specifications.md` "Product dimensions (mm)"; `pixels-per-foot-for-camera-placement.md` "(PPF)"; `network-attached-storage-nas-devices.md` H1 "(NAS) devices"; `camera-networking-options.md` "Remote camera access (Camera VPN)". Move acronym definitions into the body.

**17. "Coming soon!" placeholder pages.** `create-links-between-cameras.md`, `flir-sensors.md`. Either complete or remove from publication.

**18. Asset folder structure.** README cards across multiple sections reference `../.gitbook/assets/icon-*.svg` instead of `.gitbook/assets/icons/`. Several screenshots from older content still live at the assets root rather than in section subfolders (`dhcp-*.png`, `ntp-*.png`, `nas-*.png`, `check-point-*.png`, `sip-*.png`, `on-premise-*.png`, `off-premise-*.png`, `toa-speaker-*.png`, `live-view-ptz-*.png`). The `missing-object-alert.md` images use a `custom-objects-` prefix that doesn't match the consuming page; the `pixels-per-foot-for-camera-placement.md` images reuse `tracking-people-...` filenames.

**19. Bullet-style inconsistency.** `gpio-devices.md`, `nas-devices.md`, `sip-for-smart-speakers.md` mix `*` and `-` bullets within the same file.

**20. Curly vs straight apostrophes.** Inconsistent across most files (`'` mixed with `'`).

**21. Italics with `*` instead of `_`.** `set-up-a-camera-floor-plan.md` uses `*floor plan*` instead of `_floor plan_`.

**22. "Where" used to connect clauses.** `live-view-streaming-and-quality.md` line 40, `share-video.md` line 39, `camera-networking-options.md` ("for devices on a private network where you need the manufacturer's UI"), `other-brands.md` ("where applicable").

**23. Single-item lists.** `verkada.md` "Enable RTSP on the camera" step 1 is a one-item numbered list.

**24. Duplicate / orphaned content.**
- `lumana-timelapse.md`: image of a "Create timelapse" dialog sits next to text about retention; the actual create flow is not documented.
- `multi-camera-playback.md`: `multi-camera-playback-wall-view.png` is referenced but missing on disk.
- The `custom-objects-` image prefix on `missing-object-alert.md` is a remnant of the deleted `custom-objects.md` page.

**25. Reference data typos.**
- `recommended-streaming-settings.md` table: `3MP / 3072×1028` (probably 1728), `4MP / 2560×1440` (3.7MP/QHD, not 4MP), `8MP / 3480×2160` (probably 3840×2160).
- `live-view-streaming-and-quality.md` "Reference values" table: `3480x2160 (8MP)` repeated four times — likely 3840×2160.
- `live-view-quality-routing-diagram.png`: "Incomplient" / "compatibale" misspellings.

**26. Trustworthiness flags.**
- `set-up-a-static-ip-address.md` line 68 and `lumana.md` use a "Lumix.ai LB800" example camera on Lumana-branded pages. Verify whether LB800 is a Lumana-branded device; if not, use a Lumana model.
- `lumana-timelapse.md` competitor comparison ("This is different from Verkada, which defaults to 24 hours.") is unusual for product docs.

**27. Heading-level skips.** `recommended-streaming-settings.md` jumps to H4 "Frequently asked questions" without an intermediate H3.

---

## Notes on what was not deeply checked

- **Trustworthiness against the live product.** Many UI label and field-name flags above are best-guess based on screenshots; only you (or a reviewer with product access) can confirm each label.
- **Banned-word and "use sparingly" exhaustive counts.** Spot-checks found "Enhance" in one H1 and one card label, and occasional "essential"/"effective"/"significant" usage at low counts. A `grep -wi -c` pass per word would give a hard guarantee.
- **AI-feature limitations disclosure.** For `tracking-people.md`, `tracking-vehicles.md`, `space-occupancy-analytics.md`, and `missing-object-alert.md`, the inline limitations and accuracy caveats look reasonable. Verify they reflect current product confidence-level wording.
