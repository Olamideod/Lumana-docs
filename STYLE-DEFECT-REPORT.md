# Style guide compliance defect report

This report reviews the three documentation sections you've worked on against the rules in `STYLEGUIDE.md` (which builds on the Google developer documentation style guide). Line numbers reference the file as it stood before this pass, and each defect quotes the offending text so you can locate the change quickly.

A leading **✓** marks a defect that has already been **addressed** in the docs. Items annotated with `(leave as it is)`, `(leave this as it is)`, `(address this later)`, or `(support@lumana.ai is correct)` were intentionally skipped.

The categories used here map directly to the style guide. Where a file passes a category, the category is omitted for that file (no empty sections). At the end you'll find a section-level summary highlighting recurring issues.

---

## Section 1 — `live-video-monitoring-and-operations`

### `live-video-monitoring-and-operations/README.md`

No defects found.

---

### `live-video-monitoring-and-operations/dark-mode-and-light-mode.md`

No defects found. (✓ "Before you begin" was used here, but the heading has since been standardised to "Prerequisites" across the docs, in line with `STYLEGUIDE.md` "Guide structure".)

---

### `live-video-monitoring-and-operations/live-view-streaming-and-quality.md`

**Sentence-length violations (>25 words):**
- ✓ Line 9: "In most cases, the biggest factors are whether the viewing device can reach Lumana Core directly on the network and whether the browser or device supports the available stream format." — 30 words.

**Other defects:**
- ✓ Line 74: `MQ` and `SQ` are wrapped in code backticks. They are quality-tier abbreviations referring to UI labels, not code. Per the UI text rule, UI labels should use bold (e.g. `**MQ**`/`**SQ**`).

---

### `live-video-monitoring-and-operations/live-view.md`

**Structural / signposting issues:**
- ✓ Lines 52–56: The "Next steps" block opens with a transition sentence ("If you want to understand how Lumana delivers live video, check out the pages:") on what is otherwise a task-based page. The style guide says transitions should not appear in task-based content; the section should open with a direct statement.

---

### `live-video-monitoring-and-operations/lumana-timelapse.md`

No defects found.

---

### `live-video-monitoring-and-operations/multi-camera-playback.md`

**Headings issues:**
- ✓ Line 13: "Use multi-camera playback" duplicates the H1 "Use multi-camera playback" on line 1. Section H2s should be distinct from the page title.

**Structural / guide-structure issues:**
- ✓ Lines 7–11 contain the prerequisites but lack a labelled "Prerequisites" heading.
- ✓ Line 15: A free-floating paragraph of fragmented instruction prose ("Start from a single camera viewer. Anchor playback on one date and clock instant, not an end-stop span. Add up to three more synchronized feeds next.") sits between the heading and the numbered steps. Either fold this into the introduction or convert it into the first step.

---

### `live-video-monitoring-and-operations/ptz-control.md`

**Structural / guide-structure issues:**
- ✓ The page ends without a "Next steps" section. The style guide's Before-you-publish checklist requires every major page to end with one.

---

### `live-video-monitoring-and-operations/share-video.md`

**Sentence-length violations (>25 words):**
- ✓ Line 3: "You can start from a live camera, an alert, search results, or an existing archive, then control how long access lasts and whether viewers need a password or can download the footage." — 33 words.

**UI element issues:**
- ✓ Line 31: "Choose the alert you'd like to share by clicking on it." Uses "clicking on" — should use "Select" per the UI text rule.

**List/step issues:**
- ✓ Line 56 (under "Share an existing archive", Step 2): "Select the archive you want to share, then select **Share**." Combines two distinct selection actions in one numbered step. Split into two steps.

---

### `live-video-monitoring-and-operations/the-system-health-dashboard.md`

**Sentence-length violations (>25 words):**
- ✓ Line 15: "In the header row for the location you want, select the **system health** icon (pulse / line graph), shown toward the right next to actions such as add, edit, and reorder." — 32 words.

**UI element / casing issues:**
- ✓ Line 15: "**system health**" is the icon label but is lowercase. Confirm against the live product — UI labels should match exactly, including capitalisation. (check this and edit properly)

---

### `live-video-monitoring-and-operations/video-walls-and-shared-displays.md`

**Sentence-length violations (>25 words):**
- ✓ Line 69: "Under **Alerts**, search or manage the list (**Clear all** when you want to reset), then enable the alert categories you want surfaced on the wall." — 26 words.

**List/step issues:**
- ✓ Line 63 combines four distinct configuration choices into a single sentence with parentheticals ("**Display** (for example how the alert list renders), **View duration**, **Pic in pic** source and placement, and **Audio**…"). This is at the edge of one step covering four actions.

---

## Section 2 — `databases-analytics-and-search`

### `databases-analytics-and-search/README.md`

No defects found.

---

### `databases-analytics-and-search/build-a-database-of-people-and-vehicles.md`

No defects found.

---

### `databases-analytics-and-search/configure-a-space-occupancy-dashboard.md`

**Italic misuse:**
- ✓ Line 33: "*Space occupancy analytics*" uses italics on a page title in a cross-reference. The style guide reserves italics for first-mention term definitions or rare strong emphasis; page titles inside running text should not be italicised, and the link text already does the work.

---

### `databases-analytics-and-search/custom-objects.md` (deleted)

**Headings / user-focused issues:**
- ✓ Line 1 ("Custom objects") is a noun-phrase title for what is described as a feature concept page, but the page body is largely about the Missing object alert. Consider whether the title accurately reflects the content (or whether this page should be merged into `missing-object-alert.md` to avoid duplication). **Resolved:** the page was a duplicate of `missing-object-alert.md`, was not present in `SUMMARY.md`, and was not linked from any page. It has been deleted; the canonical task lives in `missing-object-alert.md` and the alert-type reference lives in `alerts-and-ai-detection/alert-types/tracking/missing-object.md`.

**Information fragmentation:**
- ✓ Line 16 explicitly says "for the full task-based guide (same workflow), see [Create a Missing object alert](missing-object-alert.md)." Per the "Easy to find" rules, content should not require the user to jump pages to complete one task. Either consolidate or make the split clearer (concept here, task there) so users don't bounce. **Resolved by deletion** (see above).

---

### `databases-analytics-and-search/enhance-your-video-data-with-lumana-event-tags.md`

**Sentence-length violations (>25 words):**
- ✓ Line 5: "Consider a warehouse example: if your Warehouse Management System (WMS) knows a pallet's ID, you can POST that ID with a camera and timestamp to Lumana." — 27 words.

**If/then violations:**
- ✓ Line 5: The same sentence contains "if your Warehouse Management System (WMS) knows a pallet's ID, you can POST that ID…" — the "if" clause is missing "then" in the predicate.

---

### `databases-analytics-and-search/free-text-search.md`

**Image issues:**
- ✓ Line 15: `<div align="center"><img src="../.gitbook/assets/databases-analytics-and-search/free-text-search-box-through-door-results.png" alt="..." width="563"></div>` — missing `data-with-frame="true"`.
- ✓ Line 23: same issue, "free-text-search-start-screen.png".
- ✓ Line 28: same issue, "free-text-search-text-search-screen.png".
- ✓ Line 33: same issue, "free-text-search-text-search-screen.png".
- ✓ Line 38: same issue, "free-text-search-camera-selection-dialog.png".
- ✓ Line 43: same issue, "free-text-search-results-example.png".
- ✓ Lines 15, 23, 28, 33, 38, 43 also carry descriptive alt text on screenshots; per the style guide, leave the `alt` attribute empty for screenshots.

---

### `databases-analytics-and-search/generate-reports.md`

No defects found.

---

### `databases-analytics-and-search/missing-object-alert.md`

**Italic misuse:**
- ✓ Lines 8, 9, 10, 11: italicised run-in labels (`*Real-time detection*`, `*Automated tracking*`, `*Security enforcement*`, `*Operational continuity*`) used as bullet headings. Italics aren't allowed for general emphasis or for label-style bullets; the style guide reserves them for first-mention terms or rare strong emphasis (max once or twice per page).

---

### `databases-analytics-and-search/pixels-per-foot-for-camera-placement.md`

No defects found.

---

### `databases-analytics-and-search/search-video-footage-for-other-objects.md`

**Image issues:**
- ✓ Line 23: `<div align="center"><img src="../.gitbook/assets/databases-analytics-and-search/search-other-objects-thumbnails-dropdown.png" alt="Thumbnails dropdown with Thumbnails, People, Faces, Vehicles, and License plates."></div>` — missing both `data-with-frame="true"` and the `width="563"` attribute (the dropdown image isn't framed and isn't sized).
- ✓ Same line: alt text is filled in for a screenshot; should be empty.

---

### `databases-analytics-and-search/search-video-footage-for-people-or-vehicles.md`

**Sentence-length violations (>25 words):**
- ✓ Line 3: "Lumana Core runs the search so you can combine filters such as clothing or vehicle details and review matching clips without scrubbing every feed manually." — 27 words.

---

### `databases-analytics-and-search/space-occupancy-analytics.md`

**Sentence-length violations (>25 words):**
- ✓ Line 52: "Aim each camera so it has a clear view of the crossing you want to measure for every entrance and exit you include in the count." — 27 words.

---

### `databases-analytics-and-search/tracking-containers.md`

No defects found.

---

### `databases-analytics-and-search/tracking-people.md`

**Sentence-length violations (>25 words):**
- ✓ Line 3: "People analytics builds on that stack: you can search, track, and review occupancy-related activity using person detection, attributes, cross-camera association, and, where enabled, face recognition." — 26 words.

**"Where" connector misuse:**
- ✓ Line 3 also uses "where enabled" to connect a clause; replace with "when enabled" (closer to the intended meaning) or restructure with "since"/"because" depending on intent.

---

### `databases-analytics-and-search/tracking-vehicles.md`

No defects found beyond what is already flagged in tracking-people. (The page is similar in pattern; verify that the introductory sentences stay under 25 words after any future updates.)

---

## Section 3 — `set-up-cameras-and-devices` (root files and the `connect-cameras-by-brand` subsection)

### `set-up-cameras-and-devices/README.md`

**Structural / guide-structure issues:**
- ✓ Each H2 (lines around 9, 13, 17, 21) is followed directly by a card table without an introductory paragraph between heading and content. The style guide says: "Never stack headings: include at least one paragraph between them." The same principle requires a sentence under each H2 explaining what's in that group of pages.
- ✓ The page lacks an introductory paragraph after the H1 explaining what the section covers and how to use it.

---

### `set-up-cameras-and-devices/overview.md`

No defects found.

---

### `set-up-cameras-and-devices/camera-networking-options.md`

**Headings issues:**
- ✓ Line 35: "SIP configuration (Check Point router)" — parenthetical content in a heading. Style guide says "Minimize parentheses in headings."

**Structural / guide-structure issues:**
- ✓ The "Steps" section uses a "Step 1: …" / "Step 2: …" prose pattern instead of a clean numbered list. Convert to a proper numbered list so the steps render as ordered list items.

---

### `set-up-cameras-and-devices/create-camera-shortcuts.md`

**Link issues:**
- ✓ Line 37: link text reads "Use [Use live view]…" — the verb "Use" appears outside the link and the link text starts with "Use" too, which is awkward. Tighten so the link text reads as a natural phrase ("Open [Live view](…) to apply the shortcut" or similar).

---

### `set-up-cameras-and-devices/create-links-between-cameras.md`

**Trustworthiness / completeness:**
- Page contains only "Coming soon!". The style guide's Trustworthy and Usable principles require complete, verifiable content. Either remove from publication, mark clearly as a roadmap stub with an alternative resource, or finish writing it before publish. (leave this as it is)

---

### `set-up-cameras-and-devices/enable-ptz-control.md`

**Sentence-length violations (>25 words):**
- ✓ Line 3: "Lumana's Remote PTZ (Pan-Tilt-Zoom) Control allows you to adjust camera direction and zoom in real time, enabling precise monitoring without physical access to the device." — 27 words.

**Headings issues:**
- ✓ Line 19: "Steps to enable PTZ control" — this should be a clean bare infinitive ("Enable PTZ control"). The "Steps to" prefix isn't a Lumana convention and the rest of the section already provides the steps.

**List/step issues:**
- ✓ Line 11 ("Key capabilities") uses checkmark glyphs (✔) inside what should be a regular bulleted list. Use plain Markdown bullets.

**Voice/tone:**
- ✓ Line 3 ("…allows you to adjust…") is product-feature framing rather than user-focused framing. Consider rewriting around what the user does.

---

### `set-up-cameras-and-devices/recommended-streaming-settings.md`

No defects found.

---

### `set-up-cameras-and-devices/set-up-a-camera-floor-plan.md`

**Image issues:**
- ✓ Line 41: image path uses `../.gitbook/assets/configuring-cameras-and-devices/set-up-a-camera-floor-plan/...`. The folder name `configuring-cameras-and-devices` doesn't match the section folder `set-up-cameras-and-devices`. Per the asset folder rules, subfolders must mirror the content hierarchy.

---

### `set-up-cameras-and-devices/set-up-a-static-ip-address.md`

**Sentence-length violations (>25 words):**
- ✓ Line 11: "**Scenario 1**: Your network includes a DHCP server and you want to assign a permanent IP address, keep the camera on DHCP and create a reservation on the router or Core so this camera always receives the same address." — 40 words.
- ✓ Line 12: "**Scenario 2**: Your network includes a DHCP server and you want a permanent static IP on the camera outside the DHCP pool, set a fixed **IP address**, **subnet mask**, and **gateway** on the camera, outside the DHCP pool." — 41 words.

**Headings issues (user-focused):**
- ✓ Line 25 ("Scenario 1: Your network includes a DHCP server, and you want to assign a permanent IP address"), line 48 ("Scenario 2: …"), line 62 ("Scenario 3: Your network lacks a DHCP server") — these describe network conditions, not user tasks. The user-focused rule says every heading should describe what the user will do (e.g., "Reserve an IP for a camera on a DHCP network", "Set a static IP outside the DHCP pool", "Assign a static IP without a DHCP server").
- ✓ All three headings include long colon-separated subordinate clauses, which conflicts with "minimize parentheses" / sentence-case readability guidance for headings.

---

### `set-up-cameras-and-devices/connect-cameras-by-brand/README.md`

No defects found.

---

### `set-up-cameras-and-devices/connect-cameras-by-brand/axis.md`

**Sentence-length violations (>25 words):**
- ✓ Line 38: "This guide walks you through preparing the camera, choosing how Lumana authenticates to it, optional manual stream profiles, and finally adding it in Lumana Core." — 26 words.
- ✓ Line 61: "Put the workstation you use for setup on the same LAN as the camera (for example, cameras and a computer on one switch) so discovery and the web UI work reliably." — 32 words.

---

### `set-up-cameras-and-devices/connect-cameras-by-brand/hanwha.md`

**Sentence-length violations (>25 words):**
- ✓ Line 35: "Update the camera firmware if needed, then work through the steps below in order: set a static IP first (so the camera stays reachable), tune video profiles on the camera, then register the camera in Lumana Core." — 38 words.

**If/then violations:**
- ✓ Line 35: contains "if needed" without an explicit "then" partner; restructure or include "then" per the rule.

---

### `set-up-cameras-and-devices/connect-cameras-by-brand/hikvision.md`

**Sentence-length violations (>25 words):**
- ✓ Line 41: "Install and Launch SADP: After downloading, install and open the SADP tool on a computer connected to the same local network as your Hikvision camera (for example, cameras and your PC on one switch)." — 36 words.
- ✓ Line 58: "If you have successfully logged into your Hikvision camera's web interface using the IP address identified via the SADP tool, this indicates that your camera has been initialized properly." — 30 words.

**Voice/person/tense issues:**
- ✓ Line 58: "this indicates that your camera has been initialized properly" — passive ("has been initialized"). Recast in active voice.

**If/then violations:**
- ✓ Line 58: the "If you have successfully logged in…" clause is missing "then" in the predicate.

**Headings issues:**
- ✓ Line 41 begins with "Install and Launch SADP:" used as a sub-heading-style label. The colon precedes a full sentence, so capitalisation after the colon is correct, but "Launch" is title-cased mid-sentence and the label should be either an H3 in sentence case ("Install and launch SADP") or a normal step.

---

### `set-up-cameras-and-devices/connect-cameras-by-brand/lumana.md`

No defects found.

---

### `set-up-cameras-and-devices/connect-cameras-by-brand/other-brands.md`

No defects found.

---

### `set-up-cameras-and-devices/connect-cameras-by-brand/supported-cameras.md`

**Trustworthiness / product details:**
- Line 34: contact email reads `support@lumix.ai`. This appears to be a typo for `support@lumana.ai`. Verify against the live product. If wrong, this is an inaccurate-claim defect under the Trustworthy principle. (support@lumana.ai is correct)

---

### `set-up-cameras-and-devices/connect-cameras-by-brand/verkada.md`

No defects found.

---

## Section 3 (continued) — `set-up-cameras-and-devices/network-and-infrastructure-configuration` and `other-devices`

### `set-up-cameras-and-devices/network-and-infrastructure-configuration/README.md`

No defects found.

---

### `set-up-cameras-and-devices/network-and-infrastructure-configuration/configure-lumana-core-as-a-dhcp-server.md`

**Voice/person/tense issues:**
- ✓ Line 39: "To set up the DHCP server on Lumana Core, the following parameters need to be configured:" — passive voice ("need to be configured"). Recast in active voice (e.g., "Configure the following parameters…").

**Structural / guide-structure issues:**
- ✓ The page lacks a "Next steps" section.

---

### `set-up-cameras-and-devices/network-and-infrastructure-configuration/firewall-requirements.md`

**Sentence-length violations (>25 words):**
- ✓ Line 3: "If your firewall monitors outbound traffic, you'll need to allow the endpoints and ports below to ensure the platform and web application function correctly." — 26 words.
- ✓ Line 5: "This page is organized by function: start with the outbound requirements for Lumana Core and the platform, then review the shared live view and media requirements that also support the web application, and use the final section for web application-specific endpoints." — 44 words.

**Voice/person/tense issues:**
- ✓ Line 110: "Annual review and update is recommended." — passive. Recast in active voice ("Review and update annually.").

**Headings issues:**
- ✓ Line 113: "NTP (time synchronization)" — parenthetical content in heading. Minimise parentheses.

**List / formatting consistency:**
- ✓ Line 166 (and similar in the regional media server tables): bullet text mixes a fragment label, a period, then more sentences ("`turn-…` - 443 TCP outbound - TURN/TLS. Used when UDP connection isn't viable. Need to allow TLS traffic (not only HTTPS traffic)"). Either keep the descriptors as fragments (no internal periods) or rewrite as parallel full sentences. Apply consistently across all entries.

---

### `set-up-cameras-and-devices/network-and-infrastructure-configuration/local-time-and-ntp-configuration.md`

**Sentence-length violations (>25 words):**
- ✓ Line 3: "The time shown in live view and playback is determined by the time zone configured on the location where the Core and cameras are installed." — 26 words.
- ✓ Line 21: "An _NTP (Network Time Protocol) server_ is a service that uses NTP to provide accurate time to devices over the internet or your LAN." — 26 words.

**Voice/person/tense issues:**
- ✓ Line 3: "The time shown… is determined by…" — passive voice. Recast in active voice.

**"Where" connector misuse:**
- ✓ Line 3: "…on the location where the Core and cameras are installed." — uses "where" to connect a clause. Use "because", "since", or restructure (this one might be defensible as a literal physical location, but it reads as a clause connector).

**Headings issues:**
- ✓ Line 17: "Configure Network Time Protocol (NTP)" — parenthetical content. Minimise parentheses (e.g., introduce the acronym in the intro paragraph).

**Structural / guide-structure issues:**
- ✓ The page lacks a "Next steps" section.

---

### `set-up-cameras-and-devices/network-and-infrastructure-configuration/lumana-core-hardware-specifications.md`

**Image issues:**
- ✓ Line 9: alt text on the rear-panel screenshot is non-empty ("Lumana Core rear panel with POWER, HDMI 1 and 2, USB 3.0, Ethernet 1 and 2, DC IN, and ground terminal."). Per the style guide, screenshot alt text should be empty.
- ✓ Line 44: alt text on the dimensions diagram is non-empty ("Technical drawing of Lumana Core rear panel with port layout and dimensions in millimeters."). For technical diagrams, decide intentionally: if the dimensions are conveyed elsewhere on the page (they are, in the table at lines 27–40), leave alt empty. If the diagram conveys information not in the surrounding text, retain alt — but then make sure the text caters for screen readers.

---

### `set-up-cameras-and-devices/other-devices/README.md`

No defects found.

---

### `set-up-cameras-and-devices/other-devices/disruptive-sensors.md`

**Image issues (alt text non-empty on screenshots):**
- ✓ Line 11: `alt="Organization settings, API keys, Create API Key."` — should be empty.
- ✓ Line 17: `alt="Disruptive Data Connectors list."` — should be empty.
- ✓ Line 23: `alt="Disruptive Service Accounts and active keys."` — should be empty.
- ✓ Line 29: `alt="Install Disruptive integration form."` — should be empty.
- ✓ Line 35: `alt="Edit location, Sensors tab with Disruptive sensor."` — should be empty.

**Image asset path issues:**
- ✓ Lines 11, 17, 23, 29, 35: the images sit in `../../.gitbook/assets/disruptive-*.png` rather than under a section subfolder (`set-up-cameras-and-devices/other-devices/disruptive-sensors/`). The asset folder rules require mirroring the content hierarchy with kebab-case subfolders.

**Structural / guide-structure issues:**
- ✓ The page lacks a "Next steps" section.

---

### `set-up-cameras-and-devices/other-devices/flir-sensors.md`

**Trustworthiness / completeness:**
- Page contains only "Coming soon!". Same defect as `create-links-between-cameras.md` — incomplete page that would fail Usable and Trustworthy principles in publication. (leave this as it is)

---

### `set-up-cameras-and-devices/other-devices/gpio-devices.md`

**Sentence-length violations (>25 words):**
- ✓ Line 5: "In Lumana, GPIO pins can be programmed to toggle high or low in response to an alert, enabling third-party devices to read hardwired signals from Lumana or control devices such as LEDs, motors, or relays." — 37 words.

**Voice/person/tense issues:**
- ✓ Line 5: "GPIO pins can be programmed to toggle high or low…" — passive ("can be programmed"). Recast in active voice (e.g., "Lumana lets you program GPIO pins to toggle high or low…").

**Image issues (alt text non-empty on screenshots):**
- ✓ Line 11: `alt="GPIO pinout diagram and address table."` — for a diagram you may want non-empty alt; confirm whether the surrounding text already describes the pinout. If it does, leave alt empty.
- ✓ Line 30: `alt="GPIO LED breadboard wiring and schematic."` — same consideration.
- ✓ Line 40: `alt="Alert editor, Toggle GPIO action."` — pure screenshot, alt should be empty.

**Image asset path issues:**
- ✓ Lines 11, 30, 40: images live at `../../.gitbook/assets/gpio-*.png`, not under a section subfolder. Move under `set-up-cameras-and-devices/other-devices/gpio-devices/`.

**Structural / guide-structure issues:**
- ✓ The page lacks a "Next steps" section.

---

### `set-up-cameras-and-devices/other-devices/network-attached-storage-nas-devices.md`

**Sentence-length violations (>25 words):**
- ✓ Line 25: "In the Lumana console, open the **Devices** page, find the location where the NAS is used, and select **Edit location** (pencil icon) for that site." — 27 words.
- ✓ Line 53: "Set **Additional storage** to **On**, set the target type to **External**, and choose the NFS (or object storage) entry you created for this location, for example `NFS-Server-1`." — 29 words.

**Voice/person/tense issues:**
- ✓ Line 25: "…the location where the NAS is used…" — passive ("is used"). Recast in active voice.
- ✓ Line 70: "`0.3TB` is required for 30 days of storage" — passive ("is required").
- ✓ Line 72: "`0.45TB` is required for 30 days of storage" — passive ("is required").

**"Where" connector misuse:**
- ✓ Line 25: "…find the location where the NAS is used…" — uses "where" to connect clauses. Use "the location that holds the NAS" or restructure.

**Headings issues:**
- ✓ Line 1: "Network Attached Storage (NAS) devices" — parenthetical in heading and Title Case on "Network Attached Storage". Should be sentence case ("Network attached storage (NAS) devices") and ideally avoid the parenthetical.

**Image issues (alt text non-empty on screenshots):**
- ✓ Line 27: alt text describing the Devices tab — should be empty.
- ✓ Line 31: alt text describing the External Storage form — should be empty.
- ✓ Line 41: alt text describing the External Storage form — should be empty.
- ✓ Line 47: alt text describing the camera live view — should be empty.
- ✓ Line 66: alt text describing the camera storage form — should be empty.

**Structural / guide-structure issues:**
- ✓ The page lacks a "Next steps" section.

---

### `set-up-cameras-and-devices/other-devices/sip-for-smart-speakers.md`

**Voice/person/tense issues:**
- ✓ Line 5: "This setup is typically required in advanced deployments…" — passive ("is required"). Recast in active voice.

**Headings issues:**
- ✓ Lines 17, 22, 28, 53, 69, 80: headings use the pattern "Step N: …". The numbered-step format is for lists, not headings. Convert these to a single H2 ("Configure SIP on the Check Point router") followed by a numbered list for the actual steps.
- ✓ Line 96: "Configure SIP on each speaker (examples)" — parenthetical content in a heading. Minimise parentheses.

**Image issues (alt text non-empty on screenshots):**
- ✓ Line 51: `alt="Check Point SIP service provider networks and domain configuration."` — should be empty.
- ✓ Line 94: `alt="Check Point SIP-related services with protocols and destination ports."` — should be empty.
- ✓ Image asset paths at lines 26, 51, 67, 78, 94, 120, 136 sit at `../../.gitbook/assets/...` rather than under a section subfolder; consider moving under `set-up-cameras-and-devices/other-devices/sip-for-smart-speakers/`.

---

### `set-up-cameras-and-devices/other-devices/smart-speakers.md`

No defects found.

---

## Cross-cutting / recurring issues to address

These themes appear across multiple pages. Treating them in a single pass will be faster than fixing them file by file.

✓ **1. Sentence length above 25 words.** Found in at least 14 places across all three sections. Most violations cluster on introductions and on long conditional sentences that combine several actions. Run a single pass that flags every sentence over 25 words and split them.

✓ **2. Image asset paths and alt text.** Two distinct issues:
- ✓ Many images, especially in `other-devices/`, sit at the root of `.gitbook/assets/` rather than under a section subfolder. The style guide requires the asset folder to mirror the content hierarchy.
- ✓ Many screenshots have non-empty `alt` attributes. The style guide says alt text should be empty for screenshots, with descriptive alt reserved for diagrams or images that convey information not available in the surrounding text. Audit every image at once.
- ✓ Several images in `databases-analytics-and-search/free-text-search.md` and `search-video-footage-for-other-objects.md` are missing `data-with-frame="true"`.

✓ **3. Missing "Next steps" sections.** At least seven pages end without a "Next steps" block: `ptz-control.md`, `configure-lumana-core-as-a-dhcp-server.md`, `local-time-and-ntp-configuration.md`, `disruptive-sensors.md`, `gpio-devices.md`, `network-attached-storage-nas-devices.md`, and several brand pages may need verification.

✓ **4. Passive voice.** Recurring on lines that use "is required", "is recommended", "needs to be configured", "is determined by", "can be programmed", "has been initialized". A single grep for the patterns "is/are/was/were/be/been [verbed]" and "need(s) to be" will catch most of them.

✓ **5. Headings that aren't user-focused or that misuse "Step N:" / "Scenario N:" framing.** `set-up-a-static-ip-address.md` and `sip-for-smart-speakers.md` are the worst offenders. Convert scenario- and step-prefixed headings to bare-infinitive task descriptions and put the actual steps inside numbered lists.

✓ **6. Italics misuse for label-style emphasis.** `missing-object-alert.md` (lines 8–11) and `configure-a-space-occupancy-dashboard.md` (line 33). Replace with bold labels (with colon outside bold) or restructure.

✓ **7. Parentheses in headings.** Multiple files: `camera-networking-options.md`, `firewall-requirements.md`, `local-time-and-ntp-configuration.md`, `network-attached-storage-nas-devices.md`, `sip-for-smart-speakers.md`. Move acronym definitions into the intro paragraph instead.

**8. "Coming soon!" placeholder pages.** `create-links-between-cameras.md` and `flir-sensors.md`. Either complete or remove from publication. (leave this as it is)

✓ **9. If/then construction.** Multiple sentences with an "if" clause are missing "then" in the predicate. Notable: `enhance-your-video-data-with-lumana-event-tags.md` line 5, `hanwha.md` line 35, `hikvision.md` line 58.

**10. Accuracy / typos.** `supported-cameras.md` line 34 lists `support@lumix.ai` which looks like a typo for `support@lumana.ai`. Verify against the live product.

✓ **11. UI labels and "Click" vs "Select".** `share-video.md` line 31 uses "clicking on" — replace with "Select". Spot-check other pages to be safe.

✓ **12. Information fragmentation.** `custom-objects.md` and `missing-object-alert.md` overlap in scope and explicitly link to each other for the same workflow. Merge or split cleanly so the user doesn't bounce between pages to complete one task. **Resolved:** `custom-objects.md` deleted; `missing-object-alert.md` remains as the canonical task page.

✓ **13. "Before you begin" vs. "Prerequisites".** Most task pages used `## Before you begin` (a few `###`/`####`), but the style guide specifies "Prerequisites". **Resolved:** all 25 occurrences across the docs have been renamed to "Prerequisites" at their existing heading depth. No anchor links pointed at `#before-you-begin`, so no cross-references needed updating.

✓ **14. Broken link in `alerts-and-ai-detection/alert-actions.md` (out-of-scope follow-up).** Line 29 linked to `../configuring-cameras-and-devices/other-devices/gpio.md`, which doesn't exist. **Resolved:** updated to `[GPIO devices](../set-up-cameras-and-devices/other-devices/gpio-devices.md)` to match the actual destination page and its H1.

---

## Notes on what was not deeply checked

- **Sentence-by-sentence verification against the live product.** The Trustworthy principle requires every claim be verified against the live product. That can only be done by you (or a reviewer with product access). Lines that read as marketing-style claims or that describe behaviour without UI references should be re-confirmed.
- **Banned-word and "use sparingly" exhaustive counts.** No banned-word violations were found in the spot-check; "Ensure", "Effective", and "Significant" appear sparingly across these files. If you want a hard guarantee, run a `grep -wi -c` pass over the file set for each banned and use-sparingly word.
- **Whether "Note" / "Warning" callouts are placed correctly.** The pages reviewed use minimal callouts and the placement looked compliant; if you add more, place them immediately after the relevant step.
- **AI-feature limitations disclosure.** For AI-related sections (`tracking-people.md`, `tracking-vehicles.md`, `space-occupancy-analytics.md`, `missing-object-alert.md`), the inline limitations and accuracy caveats look reasonable. Verify they reflect current product confidence-level wording.
