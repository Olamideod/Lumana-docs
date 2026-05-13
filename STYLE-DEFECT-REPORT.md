# Style guide compliance defect report (round 3)

This note keeps **cross-cutting themes** from round 3. The former per-file `set-up-cameras-and-devices` defect list was retired after a May 2026 follow-up; the **`live-video-monitoring-and-operations`** and **`databases-analytics-and-search`** lists were removed earlier the same way.

The categories used here map directly to the style guide. Many reported items have been fixed in the repo since this review; use search in the target file if a cross-cutting link misses.

## Verification legend

After a follow-up pass, each defect entry below carries a verification marker and a deep link to the exact line in the source file:

- ✅ **Confirmed** — the defect still exists at that location and the style guide rule cited is the right one.
- ⚠️ **Borderline / can't verify visually** — the rule applies but the violation sits at or just over a threshold (for example, 25–26-word sentences), or the claim depends on screenshot content that can't be re-checked from the markdown alone.

Links use the form `[L<n>](path/to/file.md#L<n>)`. They open the file at the cited line in editors that support GitHub-style line anchors.

---

Round-3 `set-up-cameras-and-devices` defects that lived in the former per-file section (lines covering README through `smart-speakers.md`) were fixed or superseded in a May 2026 documentation pass: headings and VPN/SIP steps, `SIP_DEV_UDP` tables, floor plan and PTZ wording, Core **DC IN** power copy, Axis/Hanwha bitrate notes, Lumana camera prerequisites and next steps, NAS retention wording, and related cleanup. Re-run `STYLEGUIDE.md` review after large edits if you need fresh anchors.

## Cross-cutting / recurring themes

These themes show up across multiple pages. Treating them in a single pass will be more efficient than fixing them file by file.

**1. ✅ Sentence length above 25 words.** *Largely addressed in this pass* for section indexes, streaming reference pages, camera onboarding guides, firewall text, and device pages; keep splitting long sentences when you touch nearby content.

**2. ✅ If/then construction.** *Largely addressed in this pass* for sentence-initial **If** clauses across live ops, analytics, and setup pages; keep adding an explicit **then** in the predicate when the **If** opens the sentence ([Sentence and paragraph rules](STYLEGUIDE.md)).

**3. ⚠️ Image-vs-step factual mismatches.** *May 2026 setup pass aligned many tables and narratives with common SmartConsole and camera UI labels. Replace screenshots and re-verify when the product UI changes.*

**5. ✅ Bold-as-heading misuse.** Previously: pseudo-headings in [`overview.md`](set-up-cameras-and-devices/overview.md), import/export labels in [`lumana.md`](set-up-cameras-and-devices/connect-cameras-by-brand/lumana.md), and figure labels in [`tracking-vehicles.md`](databases-analytics-and-search/tracking-vehicles.md). *Addressed — overview now uses `###` subheadings; lumana uses `### Import configuration` / `### Export configuration`; tracking-vehicles uses prose lead-ins before figures. [`share-video.md`](live-video-monitoring-and-operations/share-video.md) already uses `###` for section titles.*

**6. ✅ Run-in label colon placement (colon inside bold).** *Addressed on [`smart-speakers.md`](set-up-cameras-and-devices/other-devices/smart-speakers.md) key use cases (May 2026). [`create-camera-shortcuts.md`](set-up-cameras-and-devices/create-camera-shortcuts.md) uses `**Label**:` per [UI text and messages](STYLEGUIDE.md). [`lumana.md`](set-up-cameras-and-devices/connect-cameras-by-brand/lumana.md) bulk-operation bullets use colons outside bold.*

**7. ✅ Naming-pattern inconsistency in `connect-cameras-by-brand/`.** *Addressed in source (May 2026): [`lumana.md`](set-up-cameras-and-devices/connect-cameras-by-brand/lumana.md) and [`verkada.md`](set-up-cameras-and-devices/connect-cameras-by-brand/verkada.md) now use “Connect … cameras” H1s like sibling brand pages.*

**8. ✅ Steps that combine multiple actions.** Still common on many setup and analytics pages. *Partially reduced in recent edits on [`live-view.md`](live-video-monitoring-and-operations/live-view.md), [`multi-camera-playback.md`](live-video-monitoring-and-operations/multi-camera-playback.md), [`build-a-database-of-people-and-vehicles.md`](databases-analytics-and-search/build-a-database-of-people-and-vehicles.md), [`video-walls-and-shared-displays.md`](live-video-monitoring-and-operations/video-walls-and-shared-displays.md) (Create wall flow split into single-action steps May 2026), [`share-video.md`](live-video-monitoring-and-operations/share-video.md), [`enhance-your-video-data-with-lumana-event-tags.md`](databases-analytics-and-search/enhance-your-video-data-with-lumana-event-tags.md), [`generate-reports.md`](databases-analytics-and-search/generate-reports.md), [`search-video-footage-for-other-objects.md`](databases-analytics-and-search/search-video-footage-for-other-objects.md), [`set-up-a-camera-floor-plan.md`](set-up-cameras-and-devices/set-up-a-camera-floor-plan.md), [`hanwha.md`](set-up-cameras-and-devices/connect-cameras-by-brand/hanwha.md), [`verkada.md`](set-up-cameras-and-devices/connect-cameras-by-brand/verkada.md), [`disruptive-sensors.md`](set-up-cameras-and-devices/other-devices/disruptive-sensors.md), [`network-attached-storage-nas-devices.md`](set-up-cameras-and-devices/other-devices/network-attached-storage-nas-devices.md), [`sip-for-smart-speakers.md`](set-up-cameras-and-devices/other-devices/sip-for-smart-speakers.md), [`smart-speakers.md`](set-up-cameras-and-devices/other-devices/smart-speakers.md). [`configure-lumana-core-as-a-dhcp-server.md`](set-up-cameras-and-devices/network-and-infrastructure-configuration/configure-lumana-core-as-a-dhcp-server.md) navigation and reservation procedures were split into single-action steps (May 2026).*

**9. ✅ Passive voice.** *Largely addressed in this pass* on DHCP, firewall, GPIO, NAS, SIP hints, smart speakers, supported cameras, Verkada, and several analytics pages; rephrase remaining "is/was/been" constructions when you edit those sections.

**10. ⚠️ UI label capitalisation drift.** Doc renders product UI labels in title case while the live UI uses sentence case: "Starting IP Address" → "Starting IP address"; "API Keys" → "API keys"; "Integration" → "Integrations"; "Data Connector" → "Data Connectors"; "External retention" → "External retention period"; "subnet mask" → "Subnet mask"; "username" → "User Name"; "Edit Location" inconsistent with "Edit location"; "Edit Camera" inconsistent with "Edit camera". *Doc-side casing was spot-checked during the May 2026 setup pass; live UI labels still need a visual review when you have product access.*

**11. ✅ Future tense / "will".** Spot-check remaining pages after present-tense fixes in [`axis.md`](set-up-cameras-and-devices/connect-cameras-by-brand/axis.md) (ONVIF planning), [`hikvision.md`](set-up-cameras-and-devices/connect-cameras-by-brand/hikvision.md) (SADP scan / Connect a camera closer), [`recommended-streaming-settings.md`](set-up-cameras-and-devices/recommended-streaming-settings.md) (single-stream hint), and [`set-up-a-static-ip-address.md`](set-up-cameras-and-devices/set-up-a-static-ip-address.md) (DHCP mapping). *Re-run `grep` for ` will ` when editing nearby content.*

**12. ✅ May vs might.** Fixed across [`live-view-streaming-and-quality.md`](live-video-monitoring-and-operations/live-view-streaming-and-quality.md), [`the-system-health-dashboard.md`](live-video-monitoring-and-operations/the-system-health-dashboard.md), [`share-video.md`](live-video-monitoring-and-operations/share-video.md), [`video-walls-and-shared-displays.md`](live-video-monitoring-and-operations/video-walls-and-shared-displays.md), and [`recommended-streaming-settings.md`](set-up-cameras-and-devices/recommended-streaming-settings.md) FAQ bodies (May 2026). Run `grep -w may` when editing long guides for stragglers.

**13. ✅ Marketing / vague claims.** *Reduced on [`missing-object-alert.md`](databases-analytics-and-search/missing-object-alert.md), [`supported-cameras.md`](set-up-cameras-and-devices/connect-cameras-by-brand/supported-cameras.md), [`recommended-streaming-settings.md`](set-up-cameras-and-devices/recommended-streaming-settings.md), and [`connect-cameras-by-brand/README.md`](set-up-cameras-and-devices/connect-cameras-by-brand/README.md) (May 2026). [`tracking-containers.md`](databases-analytics-and-search/tracking-containers.md) and [`space-occupancy-analytics.md`](databases-analytics-and-search/space-occupancy-analytics.md) already use task-focused sections from an earlier rewrite.*

**14. ✅ Stacked headings without intervening paragraphs.** Residual focuses: [`sip-for-smart-speakers.md`](set-up-cameras-and-devices/other-devices/sip-for-smart-speakers.md) (`## Configure SIP on a Check Point router` → `### Prerequisites`). *[`firewall-requirements.md`](set-up-cameras-and-devices/network-and-infrastructure-configuration/firewall-requirements.md), [`lumana-core-hardware-specifications.md`](set-up-cameras-and-devices/network-and-infrastructure-configuration/lumana-core-hardware-specifications.md), and [`gpio-devices.md`](set-up-cameras-and-devices/other-devices/gpio-devices.md) now include lead-in paragraphs; H4 regional headings were promoted to H3.*

**15. ✅ Headings that aren't user-focused or that misuse "Step N:" framing.** *Prior round-3 anchors for [`enhance-your-video-data-with-lumana-event-tags.md`](databases-analytics-and-search/enhance-your-video-data-with-lumana-event-tags.md), DHCP capabilities, floor-plan feature framing, and camera-shortcuts "Key benefits" were addressed in source (May 2026). [`enable-ptz-control.md`](set-up-cameras-and-devices/enable-ptz-control.md) “Key capabilities” block removed earlier.*

**16. ✅ Heading parentheses.** [`network-attached-storage-nas-devices.md`](set-up-cameras-and-devices/other-devices/network-attached-storage-nas-devices.md) H1 "(NAS) devices"; [`camera-networking-options.md`](set-up-cameras-and-devices/camera-networking-options.md) "Remote camera access (Camera VPN)". *`lumana-core-hardware-specifications.md` dimensions heading no longer uses parentheses (spelled out as "in millimeters"). [`pixels-per-foot-for-camera-placement.md`](databases-analytics-and-search/pixels-per-foot-for-camera-placement.md) H1 no longer uses a `(PPF)` suffix (May 2026).*

**17. ✅ "Coming soon!" placeholder pages.** [`create-links-between-cameras.md`](set-up-cameras-and-devices/create-links-between-cameras.md) and [`flir-sensors.md`](set-up-cameras-and-devices/other-devices/flir-sensors.md) now use short stubs that point to related guides and Support instead of a lone exclamation headline.

**18. ✅ Asset folder structure.** SVG icon cards resolve under `.gitbook/assets/icons/`, and README `<img>` paths were updated repo-wide (May 2026). *Many setup screenshots still live at the assets root (`dhcp-*.png`, `ntp-*.png`, and similar) rather than under per-section folders—normalize when you replace those assets.*

**19. ✅ Bullet-style inconsistency.** *[`gpio-devices.md`](set-up-cameras-and-devices/other-devices/gpio-devices.md) unified to `-` in Parts list / Wiring notes (May 2026). Prerequisites vs body may still mix `*` and `-` in long guides—normalize when you touch a page.*

**20. ⚠️ Curly vs straight apostrophes.** Inconsistent across many files (`'` mixed with `'`). *Spot-check when you edit sensitive strings.*

**21. ✅ Italics with `*` instead of `_`.** *Addressed on [`set-up-a-camera-floor-plan.md`](set-up-cameras-and-devices/set-up-a-camera-floor-plan.md) (May 2026).*

**22. ✅ "Where" used to connect clauses.** *Camera VPN intro in [`camera-networking-options.md`](set-up-cameras-and-devices/camera-networking-options.md) now uses **if you need** instead of **where you need** (May 2026). [`other-brands.md`](set-up-cameras-and-devices/connect-cameras-by-brand/other-brands.md) vendor wording was normalized in the same pass.*

**23. ✅ Single-item lists.** *Addressed for [`verkada.md`](set-up-cameras-and-devices/connect-cameras-by-brand/verkada.md) — “Enable RTSP” is no longer a one-item numbered list (May 2026). Re-scan other pages after large edits.*

**24. ✅ Duplicate / orphaned content.** *Live-video timelapse placement addressed in source (May 2026).*

**25. ⚠️ Reference data typos.**
- [`recommended-streaming-settings.md`](set-up-cameras-and-devices/recommended-streaming-settings.md) "4MP" row still pairs the label **4MP** with a **2560×1440** (QHD) resolution; confirm whether the label or the resolution should change for accuracy.
- `live-view-quality-routing-diagram.png` (if still in assets): diagram text spells **Incomplient** / **compatibale**; the page no longer embeds this image (May 2026)—delete or replace the asset on a repo hygiene pass.

**26. ⚠️ Trustworthiness flags.**
- [`set-up-a-static-ip-address.md`](set-up-cameras-and-devices/set-up-a-static-ip-address.md) line 68 and [`lumana.md`](set-up-cameras-and-devices/connect-cameras-by-brand/lumana.md) use a "Lumix.ai LB800" example camera on Lumana-branded pages. *Body text mentions of "LB800" verified; whether LB800 is Lumana-branded requires product confirmation.*

---

## Notes on what was not deeply checked

- **Trustworthiness against the live product.** Many UI label and field-name flags above are best-guess based on screenshots; only you (or a reviewer with product access) can confirm each label.
- **Banned-word and "use sparingly" exhaustive counts.** The Event Tags section card no longer uses **Enhance**; the Event Tags guide title is "Add Lumana Event Tags to your video data". A `grep -wi` pass per banned word would still give a hard guarantee on long pages.
- **AI-feature limitations disclosure.** For `tracking-people.md`, `tracking-vehicles.md`, `space-occupancy-analytics.md`, and `missing-object-alert.md`, the inline limitations and accuracy caveats look reasonable. Verify they reflect current product confidence-level wording.
