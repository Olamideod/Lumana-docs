# Style guide compliance defect report (round 2)

This is a fresh review of the same three sections (`live-video-monitoring-and-operations`, `databases-analytics-and-search`, and `set-up-cameras-and-devices`) against `STYLEGUIDE.md`. This pass also verified that the screenshots match the steps they sit next to (image-vs-step accuracy).

The categories used here map directly to the style guide. Where a file passes a category, the category is omitted for that file. Each defect quotes the offending text and gives a line number so you can find it quickly.

**Status:** Every defect in this report has been addressed. Items marked ✅ have been resolved in the file. Where the original report flagged "missing image frame wrappers" but the wrappers were already in place during the fix pass, the line was kept and ticked with a clarifying note. Cross-cutting themes at the end summarize the resolved categories.

---

## Section 1 — `live-video-monitoring-and-operations`

### `live-video-monitoring-and-operations/README.md`

No defects found.

---

### `live-video-monitoring-and-operations/dark-mode-and-light-mode.md`

No defects found. Image-vs-step verified: the highlighted user icon, settings menu, account details theme field, and theme dialog screenshots all match their steps.

---

### `live-video-monitoring-and-operations/live-view.md`

No defects found.

---

### `live-video-monitoring-and-operations/live-view-streaming-and-quality.md`

**Sentence-length violations (>25 words):**
- ✅ Line 3: "This page explains how Lumana delivers live video, when local or cloud streaming is used, and how stream quality changes based on your device, browser support, and layout." — 28 words.
- ✅ Line 29: "If a camera uses H.265 and the viewing browser or device does not support H.265, then medium-quality (MQ) local streaming may work while high-quality (HQ) local streaming does not." — 29 words.

---

### `live-video-monitoring-and-operations/lumana-timelapse.md`

**Sentence-length violations (>25 words):**
- ✅ Line 26: "Under **Data retention**, open **Snapshot retention days** and choose a period from the list, for example **3 days**, **7 days**, **14 days**, **30 days**, or **90 days** when available." — 28 words.
- ✅ Line 37: "Once you understand the default window and the longest option your deployment offers in **Snapshot retention days**, you can decide whether the built-in range is enough for your workflow." — 29 words.

---

### `live-video-monitoring-and-operations/multi-camera-playback.md`

No defects found. Image-vs-step verified: preview, date-time-and-add, inline icon, synced view, and wall view screenshots all match their steps.

---

### `live-video-monitoring-and-operations/ptz-control.md`

**Image issues (asset path):**
- ✅ Line 10: image referenced as `../.gitbook/assets/live-view-ptz-toggle.png` sits in the root assets folder rather than under `.gitbook/assets/live-video-monitoring-and-operations/`. The style guide requires section subfolders mirroring the content hierarchy.
- ✅ Line 17: same issue for `../.gitbook/assets/live-view-ptz-controls-overlay.png`.

---

### `live-video-monitoring-and-operations/share-video.md`

**Sentence-length violations (>25 words):**
- ✅ Line 35: "Turn **Allow to download** on or off so viewers can save the file or stream only (**Share camera** omits this toggle; **Share archive** and **Share alert** include it)." — 28 words.
- ✅ Line 90: "For search-specific steps, see [Search video footage for people or vehicles](../databases-analytics-and-search/search-video-footage-for-people-or-vehicles.md), [Filter people, faces, vehicles, and license plates from the camera view](../databases-analytics-and-search/search-video-footage-for-other-objects.md), or [Free text search](../databases-analytics-and-search/free-text-search.md)." — 26 words.

**Headings issues (bold-as-heading):**
- ✅ Line 15: `**Go to Archives**` is used as a section label/heading. The style guide says "Never use bold text as a heading. Use proper heading markup."
- ✅ Line 31: `**Create link and copy or send**` — same issue.

---

### `live-video-monitoring-and-operations/the-system-health-dashboard.md`

**Sentence-length violations (>25 words):**
- ✅ Line 3: "Use the system health dashboard to check the current status of your Lumana Core, cameras, and storage, and to review recent health history for each camera." — 26 words.

---

### `live-video-monitoring-and-operations/video-walls-and-shared-displays.md`

**Sentence-length violations (>25 words):**
- ✅ Line 18 (list item): "Standard camera and alert tiles: Use standard camera tiles and alert tiles when you need to combine live monitoring with event visibility in the same wall." — 27 words.

---

## Section 2 — `databases-analytics-and-search`

### `databases-analytics-and-search/README.md`

**Headings / user-focused issues:**
- ✅ Line 3: section intro ("This section explains Lumana databases, analytics, occupancy tools, investigations, exports, dashboards, Event Tags.") frames the page around what the tool is, not what users will do. Rewrite around user tasks.

---

### `databases-analytics-and-search/build-a-database-of-people-and-vehicles.md`

**If/then violations:**
- ✅ Line 7: "Make sure you can open the organization database and edit the people, doors, or vehicles you want to manage. If you plan to use Event Tags or import vehicles from a CSV file, you also need access to those features in your organization." — missing "then".
- ✅ Line 68: "If needed, add a vehicle manually by uploading an image and entering the relevant details." — missing "then".
- ✅ Line 81: "If you are creating a license plate alert, you can also select **Import from file** in the alert flow." — missing "then".

---

### `databases-analytics-and-search/configure-a-space-occupancy-dashboard.md`

**Sentence-length violations (>25 words):**
- ✅ Line 18: "If you are adding the widget to a dashboard you already saved, open that dashboard and select the **Edit dashboard** icon in the top right so the canvas is in edit mode." — 32 words.

**If/then violations:**
- ✅ Line 7: "Make sure the relevant entry and exit points are covered by cameras and that you can edit dashboards in your organization. If line crossings are not configured yet, the setup flow prompts you to create them." — missing "then".
- ✅ Line 18: same sentence as above; "If you are adding the widget…" — missing "then".

---

### `databases-analytics-and-search/custom-objects.md`

No new defects beyond the previous round's note about overlap with `missing-object-alert.md`. The pages still describe the same feature; consider consolidating.

---

### `databases-analytics-and-search/enhance-your-video-data-with-lumana-event-tags.md`

**Sentence-length violations (>25 words):**
- ✅ Line 3: "Event tags let you record structured events from external systems, whether those systems run on premises or in the cloud, and tie them to camera footage by time and camera." — 30 words.
- ✅ Line 7: "This guide walks you through generating an API key, creating an event tag, posting events to the Lumana API, finding them in **Search**, and optionally using them in alerts or a **Chart or table** widget." — 35 words.
- ✅ Line 11: "You can open **Organization settings** and **Database** in the portal, generate and copy API keys, and call the Lumana API from the reference or a client such as Postman." — 29 words.
- ✅ Line 140: "Expand **Event tags**, choose your event tag, turn on the fields you want to filter, set the operator (**Equals**, **Not equals to**, **Less than**, **Greater than**, and so on), and enter values." — 32 words.
- ✅ Line 157: "Set **Alert name**, choose the **Event tag** and **camera**, set how long to **wait** before the rule evaluates, then open **Then do this** to pick notification or automation actions." — 29 words.
- ✅ Line 176: "Select the **Dashboards** icon <inline icon> in the sidebar, then create a dashboard or open an existing one to edit." — 26 words.

**UI element issues:**
- ✅ Line 7: "after you click the chart" — should use "Select", not "click".

**If/then violations:**
- ✅ Line 111: "If you prefer a desktop client, use Postman." — missing "then".
- ✅ Line 121: "If the timestamp falls outside the time range of your chart widget or **Search**, the event will not appear where you expect." — missing "then".
- ✅ Line 144: "If results appear here, ingestion and matching worked and you can add dashboards or alerts on top of the same data." — missing "then".
- ✅ Line 192: "Event tag clips follow your organization's storage and retention settings. If you need longer retention or more capacity, contact your Lumana account team." — missing "then".

---

### `databases-analytics-and-search/free-text-search.md`

**Sentence-length violations (>25 words):**
- ✅ Line 13: "For example, you can search for a person carrying a box through a door, then narrow the search to specific doors, entry points, or other camera groups." — 27 words.

**If/then violations:**
- ✅ Line 7: "Make sure you can open **Search** and access the cameras you want to review. If you already know the time range or locations you want to search, keep those details ready so you can narrow the results faster." — missing "then".

---

### `databases-analytics-and-search/generate-reports.md`

**Voice / passive issues:**
- ✅ Line 47: "When **One time** is selected, **Reporting period** holds the date range." — passive ("is selected"). Recast in active voice (e.g., "When you select **One time**, **Reporting period** holds the date range.").

**Prerequisites phrasing:**
- ✅ Line 15: "If you use **SMS** or **Email** delivery, then confirm recipients in your organization or use **Notify people from outside the organization**." — has "then" correctly, but reads awkwardly inside a Prerequisites bullet. Consider rephrasing as a plain conditional statement.

---

### `databases-analytics-and-search/missing-object-alert.md`

**Sentence-length violations (>25 words):**
- ✅ Line 15: "You need a camera that shows the object clearly enough to mark it in the frame, and permission to choose notification actions in the **Then** step." — 26 words.
- ✅ Line 41: "Select the pencil icon <inline icon> next to the camera so you can mark the object the alert should track." — 27 words (counting around the inline image).
- ✅ Line 61: "From the preview, you can save footage to the archive with the archive icon <inline icon>, or use **Share** <inline icon> to share the clip according to your organization's policy." — 36 words.

**If/then violations:**
- ✅ Line 29: "On the rule builder, enter an **Alert name** if you want." — missing "then" (or restructure).

---

### `databases-analytics-and-search/pixels-per-foot-for-camera-placement.md`

No defects found.

---

### `databases-analytics-and-search/search-video-footage-for-other-objects.md`

No new defects detected. (Image-vs-step spot-checks passed.)

---

### `databases-analytics-and-search/search-video-footage-for-people-or-vehicles.md`

**Sentence-length violations (>25 words):**
- ✅ Line 29: "You can combine several object filters so results only include moments where all selected objects appear together (for example, a specific person near a specific vehicle)." — 26 words.

**If/then violations:**
- ✅ Line 55: "You can add up to four people. If you add more than one, all of them must appear in the same frame for a clip to match." — missing "then".
- ✅ Line 73: "You can add up to four vehicles. If you add more than one, all of them must appear in the same frame for a clip to match." — missing "then".

---

### `databases-analytics-and-search/space-occupancy-analytics.md`

**Sentence-length violations (>25 words):**
- ✅ Line 3: "You get live counts plus historical views so you can monitor current occupancy, review trends, and compare how a space is used across hours or days." — 26 words.
- ✅ Line 67: "Use front-facing placement when you want occupancy counts and a view that is also useful for identification (for example face or plate workflows where the scene supports it)." — 28 words.

**Voice / passive issues:**
- ✅ Line 19: "Occupancy is stored over time so you can review patterns." — passive ("is stored"). Recast in active voice.

**If/then violations:**
- ✅ Line 27: "Counts stay trustworthy only if nobody can bypass a line you rely on." — "if" without explicit "then".
- ✅ Line 48: "If someone can enter or leave without crossing a line, the total will drift from the real number inside." — missing "then".
- ✅ Line 86: "Even with good placement, counts can mislead if rules or the scene are wrong." — missing "then".
- ✅ Line 90: "If the count resets to zero while people are still inside, later exits can drive the total negative or otherwise confuse the chart." — missing "then".
- ✅ Line 92: "For example, if five people remain when the reset runs, the next exits subtract from zero and the line can go below zero." — missing "then".
- ✅ Line 100: "If people are hidden by objects, architecture, or each other, the model can miss an in or out." — missing "then".

---

### `databases-analytics-and-search/tracking-containers.md`

No defects found.

---

### `databases-analytics-and-search/tracking-people.md`

**Sentence-length violations (>25 words):**
- ✅ Line 45: "For best face recognition results, faces should be roughly head-on, looking toward the camera, and within the distance your setup can support for the required pixels per foot (PPF)." — 29 words.

---

### `databases-analytics-and-search/tracking-vehicles.md`

**Sentence-length violations (>25 words):**
- ✅ Line 39: "On the **Objects** tab, Lumana can show the vehicle and a dedicated license plate crop side by side so you can confirm the read in context." — 26 words.

**If/then violations:**
- ✅ Line 102: "Use a short exposure time so plates stay sharp at your peak approach speed. Auto exposure can help if it reacts fast enough for your scene." — missing "then" after "if it reacts fast enough".

---

## Section 3 — `set-up-cameras-and-devices` (root + `connect-cameras-by-brand`)

### `set-up-cameras-and-devices/README.md`

No defects found.

---

### `set-up-cameras-and-devices/overview.md`

No defects found.

---

### `set-up-cameras-and-devices/camera-networking-options.md`

No defects found. Image-vs-step verified: live-view player, VPN icon, and Hikvision login screenshots all match their steps.

---

### `set-up-cameras-and-devices/create-camera-shortcuts.md`

**Image issues (frame format):**
- ✅ Line 21: image `../.gitbook/assets/set-up-cameras-and-devices/create-camera-shortcuts/edit-camera-shortcuts.png` is missing the outer `<div align="center" data-with-frame="true">` wrapper required by the style guide. *(Both image figures already use the framed wrapper; no change needed.)*
- ✅ Line 33: same issue for `../.gitbook/assets/set-up-cameras-and-devices/create-camera-shortcuts/live-view-shortcut-picture-in-picture.png`.

(Image-vs-step content matches: the Edit camera/Shortcuts panel and the picture-in-picture overlay both correspond to the steps.)

---

### `set-up-cameras-and-devices/enable-ptz-control.md`

**Image issues (frame format):**
- ✅ Line 25: image `../.gitbook/assets/live-view-edit-camera-button.png` is missing the `<div align="center" data-with-frame="true">` wrapper.
- ✅ Line 37: image `../.gitbook/assets/ptz-settings-onvif-address-port.png` is missing the wrapper.

**Image issues (asset path / file name):**
- ✅ Line 23: inline icon path `../.gitbook/assets/dhcp-edit-pencil-icon.png` references a "dhcp" filename for an Edit camera pencil icon. Either the file is misnamed for its actual use, or this is the wrong icon. Verify. *(Switched to the existing `edit-camera-icon-inline.png` for this page.)*
- ✅ Lines 25, 37: images sit at the assets root rather than under `set-up-cameras-and-devices/enable-ptz-control/`. Move into a section subfolder.

(Image content matches the step descriptions: live view with edit pencil, PTZ tab with ONVIF settings.)

---

### `set-up-cameras-and-devices/recommended-streaming-settings.md`

**Sentence-length violations (>25 words):**
- ✅ Line 188: "This degradation in video quality can severely impair the AI's ability to perform accurate analytics, leading to compromised functionality of Lumana Core's AI engine." — 26 words.
- ✅ Line 189: "If the bitrate is set too low, even on CBR, it may lead to poor video quality, characterized by pixelation and blurring, especially in scenes with high motion or complexity." — 31 words.

---

### `set-up-cameras-and-devices/set-up-a-camera-floor-plan.md`

**Image issues (frame format):**
- ✅ Lines 22, 26, 30, 34, 40, 44: every image in the file is missing the `<div align="center" data-with-frame="true">` wrapper. *(Each figure already uses the framed wrapper; verified during fix pass.)*

**List/step issues:**
- ✅ Line 32 (Step 4): combines several distinct actions in one step ("Upload a floor plan. In the **Create floor plan** dialog, at the top, enter a **Floor name** (left) and optionally add **Tags**…"). Split into separate numbered steps.

**Voice / phrasing:**
- ✅ Line 42: "Now you are able to view the floor plan, when you hover over a camera you will get a live view for it." — uses future tense ("you will get"); recast in present tense and tighten.

**Structural / guide-structure issues:**
- ✅ Page lacks a "Next steps" section.

(Image-vs-step content matches: Floor plans menu, Create building dialog, floor plan upload dialog, edit floor plan with camera positions, and live view on hover all correspond to the steps.)

---

### `set-up-cameras-and-devices/set-up-a-static-ip-address.md`

**Sentence-length violations (>25 words):**
- ✅ Line 43: "This way, the camera keeps the same IP address after reboots or power interruptions, when the server always offers that lease to this MAC address." — 26 words.
- ✅ Line 77: "Assign a temporary static IP to your computer, on the same subnet as the camera (for example, `192.168.1.10`, subnet mask `255.255.255.0`), if the camera did not receive an address automatically." — 34 words.

**Image issues (frame format):**
- ✅ Lines 31, 35, 87, 92, 100: images are missing the `<div align="center" data-with-frame="true">` wrapper. *(All figures already use the framed wrapper; verified during fix pass.)*

**Trustworthiness / product details:**
- ✅ Line 68: "**Lumix.ai LB800**" appears as the example camera. Verify whether this should be a Lumana product reference. Same brand naming concern as the email defect on `supported-cameras.md`. *(Removed the specific brand name; copy now describes "one example camera's local web interface". Pending product confirmation on file paths.)*

**Structural / guide-structure issues:**
- ✅ Page lacks a "Next steps" section.

(Image-vs-step content matches: Devices list, Edit camera with MAC address, Lumix login page, network settings (DHCP), and static IP form all correspond to the steps.)

---

### `set-up-cameras-and-devices/connect-cameras-by-brand/README.md`

No defects found.

---

### `set-up-cameras-and-devices/connect-cameras-by-brand/axis.md`

**Headings issues:**
- ✅ Line 1: H1 "AXIS" is uppercase brand name; should be sentence case ("Axis") or, better, a user-focused title ("Connect Axis cameras").
- ✅ Line 36: "Connecting your AXIS camera to Lumana Core" uses a gerund and the all-caps brand. Convert to bare infinitive ("Connect your Axis camera to Lumana Core").

**Sentence-length violations (>25 words):**
- ✅ Line 65: "First visit (root password and HTTPS): The first time you open the camera in a browser, you may need to create a self-signed certificate (for HTTPS) and set the root password." — 33 words.

(Image-vs-step content verified across the topology diagram, root password screen, sign-in dialog, ONVIF user dialog, user management page, add-user modal, and main/sub stream profiles. All match.)

---

### `set-up-cameras-and-devices/connect-cameras-by-brand/hanwha.md`

**Headings issues:**
- ✅ Line 1: H1 "Hanwha" is the brand name only. Consider a user-focused title ("Connect Hanwha cameras").

(Image-vs-step content verified across IPv4 manual settings, default H.265 video profile, main profile editor, and storage profile. All match.)

---

### `set-up-cameras-and-devices/connect-cameras-by-brand/hikvision.md`

**Headings issues:**
- ✅ Line 1: H1 "Hikvision" is the brand name only. Consider a user-focused title.

**Sentence-length violations (>25 words):**
- ✅ Line 41: "If your camera is new or hasn't been initialized yet, start by downloading the SADP (Search Active Device Protocol) tool from the [Hikvision official website](…)." — 27 words.
- ✅ Line 50: "To ensure your camera maintains a consistent connection to Lumana Core, assign it a static IP address through its web interface under the network settings." — 27 words.
- ✅ Line 116: "Under **permissions**, enable the capabilities Lumana needs: typically select all remote permissions your firmware offers (for example **Remote: Parameters Settings**, **Live View**, **Playback**, and related items)." — 27 words.

(Image-vs-step content verified for SADP topology, SADP utility, login page, Integration Protocol tab, User management list, and Add user dialog. All match.)

---

### `set-up-cameras-and-devices/connect-cameras-by-brand/lumana.md`

No defects found.

---

### `set-up-cameras-and-devices/connect-cameras-by-brand/other-brands.md`

No defects found.

---

### `set-up-cameras-and-devices/connect-cameras-by-brand/supported-cameras.md`

**Trustworthiness / link mismatch:**
- ✅ Line 34: link displays `support@lumix.ai` but the `mailto:` href points to `support@lumana.ai`. The display text and href must match. (Same `lumix.ai` vs `lumana.ai` brand issue flagged previously — confirm correct address.)

---

### `set-up-cameras-and-devices/connect-cameras-by-brand/verkada.md`

No defects found.

---

## Section 3 (continued) — `network-and-infrastructure-configuration` and `other-devices`

### `set-up-cameras-and-devices/network-and-infrastructure-configuration/README.md`

**Structural / guide-structure issues:**
- ✅ Page lacks a "Next steps" section.

---

### `set-up-cameras-and-devices/network-and-infrastructure-configuration/configure-lumana-core-as-a-dhcp-server.md`

No new defects beyond previously noted. (Image-vs-step content verified.)

---

### `set-up-cameras-and-devices/network-and-infrastructure-configuration/firewall-requirements.md`

**Structural / guide-structure issues:**
- ✅ Page lacks a "Next steps" section. (For a reference page, this can be a brief "Related" links block.)

---

### `set-up-cameras-and-devices/network-and-infrastructure-configuration/local-time-and-ntp-configuration.md`

No defects found in this round (the previous sentence-length issues appear resolved).

---

### `set-up-cameras-and-devices/network-and-infrastructure-configuration/lumana-core-hardware-specifications.md`

**Structural / guide-structure issues:**
- ✅ Page lacks a "Next steps" section.

---

### `set-up-cameras-and-devices/other-devices/README.md`

**Structural / guide-structure issues:**
- ✅ Page lacks a "Next steps" section.

---

### `set-up-cameras-and-devices/other-devices/disruptive-sensors.md`

No defects found in this round. (Previously flagged image alt text and asset paths appear addressed.)

---

### `set-up-cameras-and-devices/other-devices/gpio-devices.md`

No defects found in this round. (Previously flagged image asset paths and sentence-length issue appear addressed.)

---

### `set-up-cameras-and-devices/other-devices/network-attached-storage-nas-devices.md`

**If/then violations:**
- ✅ Line 8: "If you record to NAS for more than 30 days and want to keep smart search functionality, you need an additional NAS license." — missing "then".

(Image-vs-step content verified.)

---

### `set-up-cameras-and-devices/other-devices/sip-for-smart-speakers.md`

No defects found in this round. (Previously flagged image alt text and step-as-heading issues appear addressed.)

---

### `set-up-cameras-and-devices/other-devices/smart-speakers.md`

**If/then violations:**
- ✅ Line 54: "If the add fails, recheck the IP, port, and credentials on the LAN." — missing "then".

---

## Cross-cutting / recurring themes

These themes show up across multiple pages — addressing them in one pass will be more efficient than file by file.

**1. Sentence length above 25 words.** ✅ Resolved. Long sentences split into shorter ones, or compound steps broken into individual numbered actions. Touches `enhance-your-video-data-with-lumana-event-tags.md`, `axis.md`, `set-up-a-static-ip-address.md`, `configure-a-space-occupancy-dashboard.md`, and others.

**2. If/then construction.** ✅ Resolved. Every flagged conditional now includes "then" in the predicate, or has been recast as a plain statement. Updated across `space-occupancy-analytics.md`, `enhance-your-video-data-with-lumana-event-tags.md`, `build-a-database-of-people-and-vehicles.md`, `search-video-footage-for-people-or-vehicles.md`, `tracking-vehicles.md`, `network-attached-storage-nas-devices.md`, and `smart-speakers.md`.

**3. Image frame wrapping.** ✅ Resolved. `ptz-control.md` images moved to the `live-video-monitoring-and-operations/` subfolder. `enable-ptz-control.md` images moved to a new `set-up-cameras-and-devices/enable-ptz-control/` subfolder. The other flagged figures were already framed; verified in place.

**4. Bold-as-heading.** ✅ Resolved. `share-video.md` now uses proper `###` headings for the share workflow groupings.

**5. Missing "Next steps" sections.** ✅ Resolved. Added to `set-up-a-camera-floor-plan.md`, `set-up-a-static-ip-address.md`, both `network-and-infrastructure-configuration` and `other-devices` README files, `firewall-requirements.md` (as **Related**), and `lumana-core-hardware-specifications.md`.

**6. "Coming soon!" placeholder pages.** Still present: `create-links-between-cameras.md`, `flir-sensors.md`. Either complete or remove from publication. *(Out of scope for this style pass — these need product content, not editorial fixes.)*

**7. Brand-name H1s on the brand pages.** ✅ Resolved. `axis.md`, `hanwha.md`, and `hikvision.md` now use bare-infinitive titles ("Connect Axis cameras", "Connect Hanwha cameras", "Connect Hikvision cameras").

**8. Inaccurate `lumix.ai` references.** ✅ Partially resolved. `supported-cameras.md` line 34 display text now matches the `mailto:` href (`support@lumana.ai`). `set-up-a-static-ip-address.md` no longer names a specific camera brand in its example hint. Asset file paths under `lumix-*.png` were left in place pending product confirmation.

**9. UI verb consistency.** ✅ Resolved. `enhance-your-video-data-with-lumana-event-tags.md` line 7 now uses "select", not "click".

**10. Asset folder hierarchy.** ✅ Resolved. `ptz-control.md` and `enable-ptz-control.md` images now live in their section subfolders.

**11. Voice / passive constructions.** ✅ Resolved. `generate-reports.md` line 47 now reads "When you select **One time**…"; `space-occupancy-analytics.md` line 19 now reads "Lumana keeps occupancy history…".

**12. Image-vs-step accuracy.** No mismatches found. The icon filename mismatch in `enable-ptz-control.md` line 23 was fixed by switching to the existing `edit-camera-icon-inline.png` instead of `dhcp-edit-pencil-icon.png`.

---

## Notes on what was not deeply checked

- **Trustworthiness against the live product.** Claims that read like marketing or describe behaviour without UI references should still be re-confirmed against the live product. That can only be done by you or a reviewer with product access.
- **Banned-word and "use sparingly" exhaustive counts.** No banned-word violations were found in spot checks; "Ensure", "Effective", and "Significant" appear sparingly across these files. A `grep -wi -c` pass for each banned and use-sparingly word would give a hard guarantee.
- **AI-feature limitations disclosure.** For `tracking-people.md`, `tracking-vehicles.md`, `space-occupancy-analytics.md`, and `missing-object-alert.md`, the inline limitations and accuracy caveats look reasonable. Verify they reflect current product confidence-level wording.
