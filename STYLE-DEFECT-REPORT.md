# Style guide compliance defect report (round 3)

This is a fresh review of **`set-up-cameras-and-devices`** against `STYLEGUIDE.md`. This pass also verified that the screenshots match the steps they sit next to (image-vs-step accuracy). The **`live-video-monitoring-and-operations`** and **`databases-analytics-and-search`** round-3 items were closed in a May 2026 follow-up and are no longer listed here.

The categories used here map directly to the style guide. Where a file passes a category, the category is omitted for that file. Each defect quotes the offending text and gives a line number so you can find it quickly. Many reported items have been fixed in the repo since this review; re-open cited lines to confirm current state.

**May 2026 audit:** Items below were removed from this report **only** after checking the current markdown in git: if the cited text or structure no longer matched the defect, the bullet was deleted. Round-3 line anchors can be stale—use search in the target file if a link misses.

## Verification legend

After a follow-up pass, each defect entry below carries a verification marker and a deep link to the exact line in the source file:

- ✅ **Confirmed** — the defect still exists at that location and the style guide rule cited is the right one.
- ⚠️ **Borderline / can't verify visually** — the rule applies but the violation sits at or just over a threshold (for example, 25–26-word sentences), or the claim depends on screenshot content that can't be re-checked from the markdown alone.

Links use the form `[L<n>](path/to/file.md#L<n>)`. They open the file at the cited line in editors that support GitHub-style line anchors.

---

## Section 1 — `set-up-cameras-and-devices` (root + `connect-cameras-by-brand`)

### `set-up-cameras-and-devices/README.md`

**Headings / consistency:**
- ✅ [L5](set-up-cameras-and-devices/README.md#L5), [L11](set-up-cameras-and-devices/README.md#L11), [L17](set-up-cameras-and-devices/README.md#L17), [L23](set-up-cameras-and-devices/README.md#L23): "Recommended setup, networking, and streaming", "Connect cameras by brand", "Other devices", "Network and infrastructure configuration" — mix of bare-infinitive and noun-phrase patterns on the same page. *Verified.*

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

### `set-up-cameras-and-devices/create-links-between-cameras.md`

**Trustworthiness / completeness:**
- ✅ [L1](set-up-cameras-and-devices/create-links-between-cameras.md#L1)–[L3](set-up-cameras-and-devices/create-links-between-cameras.md#L3): page contains only "# Create links between cameras" and "Coming soon!". *Verified — page is empty of content beyond the placeholder. Fails [Trustworthy writing](STYLEGUIDE.md) and Usability principles.*

---

### `set-up-cameras-and-devices/enable-ptz-control.md`

**Image-vs-step mismatches:**
- ⚠️ [L20](set-up-cameras-and-devices/enable-ptz-control.md#L20)/[L22](set-up-cameras-and-devices/enable-ptz-control.md#L22): `live-view-edit-camera-button.png` is captioned next to step 2, which describes selecting "the **Edit camera** icon ... pencil icon." The screenshot is reportedly the Settings wrench control. *Body text verified; image content needs a visual review.*
- ⚠️ [L27](set-up-cameras-and-devices/enable-ptz-control.md#L27)/[L30](set-up-cameras-and-devices/enable-ptz-control.md#L30): body uses "driver" (lowercase), "PTZ control path", and "port" while the screenshot reportedly labels the field as "X address". *Body text verified; image content needs a visual review.*

---

### `set-up-cameras-and-devices/set-up-a-camera-floor-plan.md`

**Image-vs-step mismatches:**
- ⚠️ [L20](set-up-cameras-and-devices/set-up-a-camera-floor-plan.md#L20)/[L22](set-up-cameras-and-devices/set-up-a-camera-floor-plan.md#L22): step 1 says "top **left** corner"; `floor-plans-menu-overview.png` reportedly shows top-right. *Body text verified at L20 with "top left corner"; image content needs a visual review.*
- ⚠️ [L40](set-up-cameras-and-devices/set-up-a-camera-floor-plan.md#L40)/[L42](set-up-cameras-and-devices/set-up-a-camera-floor-plan.md#L42): step 8 says "Select **Add floor plan** to save"; `edit-floor-plan-layout.png` reportedly shows completed floor plan. *Step text verified; image content needs a visual review.*

---

### `set-up-cameras-and-devices/set-up-a-static-ip-address.md`

**Trustworthiness / product details:**
- ✅ [L87](set-up-cameras-and-devices/set-up-a-static-ip-address.md#L87), [L92](set-up-cameras-and-devices/set-up-a-static-ip-address.md#L92), [L100](set-up-cameras-and-devices/set-up-a-static-ip-address.md#L100): image filenames `lumix-camera-web-login-lb800.png`, `lumix-network-ipv4-dhcp-settings.png`, `lumix-network-ipv4-static-settings.png` use a `lumix-` prefix on a Lumana page. *Verified that filenames retain the Lumix branding; needs a verification against the live product per [Trustworthy writing](STYLEGUIDE.md).*

**UI element issues:**
- ✅ [L12](set-up-cameras-and-devices/set-up-a-static-ip-address.md#L12), [L96](set-up-cameras-and-devices/set-up-a-static-ip-address.md#L96): doc text uses "subnet mask" (lowercase). *Verified — body uses lowercase "subnet mask" while the UI label is reported to be "Subnet mask" (capital S).*

---

### `set-up-cameras-and-devices/connect-cameras-by-brand/axis.md`

**Headings:**
- ✅ [L1](set-up-cameras-and-devices/connect-cameras-by-brand/axis.md#L1): H1 "Connect Axis cameras" — bare infinitive, OK (pass note). *Verified.*
- ✅ [L9](set-up-cameras-and-devices/connect-cameras-by-brand/axis.md#L9)–[L34](set-up-cameras-and-devices/connect-cameras-by-brand/axis.md#L34): "AXIS Q16 Series" etc. (uppercase) appears in body alongside "Axis cameras" lowercase. *Verified all-caps "AXIS" prefix on every model bullet.*

**Image-vs-step issues:**
- ⚠️ [L140](set-up-cameras-and-devices/connect-cameras-by-brand/axis.md#L140) `axis-stream-profile-lumana-main.png`: reportedly shows "Maximum" (MBR) bitrate. *Image content needs a visual review; the brand table in `recommended-streaming-settings.md` does list MBR for Axis main, which is the cross-doc inconsistency.*

**Structural:**
- ✅ [L153](set-up-cameras-and-devices/connect-cameras-by-brand/axis.md#L153): No "Next steps" section. *Verified — page ends after the sub stream profile reference.*

---

### `set-up-cameras-and-devices/connect-cameras-by-brand/hanwha.md`

**Headings:**
- ✅ [L1](set-up-cameras-and-devices/connect-cameras-by-brand/hanwha.md#L1): H1 "Connect Hanwha cameras" — bare infinitive, OK (pass note). *Verified.*

**List/step issues:**
- ✅ [L43](set-up-cameras-and-devices/connect-cameras-by-brand/hanwha.md#L43): step 3 "Open the **IP address** tab, set **IP type** to **Manual**, enter **IP address**, **Subnet mask**, **Gateway**, and DNS servers, then select **Apply**." — combines five actions. *Verified.*
- ✅ [L54](set-up-cameras-and-devices/connect-cameras-by-brand/hanwha.md#L54): step 4 "Set that row as the **Default** profile and set **Codec** to **H.265**." — combines two actions. *Verified.*

**Image-vs-step mismatch:**
- ⚠️ [L82](set-up-cameras-and-devices/connect-cameras-by-brand/hanwha.md#L82) `hanwha-storage-profile-settings.png`: doc text on [L77](set-up-cameras-and-devices/connect-cameras-by-brand/hanwha.md#L77) says **Bitrate control** should be **CBR**, but the screenshot is reportedly the Maximum/MBR setting. *Body text verified; image content needs a visual review.*

**Structural:**
- ✅ [L93](set-up-cameras-and-devices/connect-cameras-by-brand/hanwha.md#L93): No "Next steps" section. *Verified — page ends with the RTSP profile note.*

---

### `set-up-cameras-and-devices/connect-cameras-by-brand/hikvision.md`

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

**Structural / depth:**
- ✅ [L1](set-up-cameras-and-devices/connect-cameras-by-brand/lumana.md#L1)–[L52](set-up-cameras-and-devices/connect-cameras-by-brand/lumana.md#L52): Page lacks Prerequisites and connection-to-Lumana-Core steps. *Verified — file has no Prerequisites or step-by-step connection content.*
- ✅ [L52](set-up-cameras-and-devices/connect-cameras-by-brand/lumana.md#L52): No "Next steps" section. *Verified.*

**Trustworthiness:**
- ⚠️ [L28](set-up-cameras-and-devices/connect-cameras-by-brand/lumana.md#L28): screenshot `camera-finder-device-management.png` may show an "LB800" device. *Image content needs a visual review; the parallel "LB800" reference in `set-up-a-static-ip-address.md` is confirmed in the image filenames there.*

---

### `set-up-cameras-and-devices/connect-cameras-by-brand/other-brands.md`

**Structural / depth:**
- ✅ [L1](set-up-cameras-and-devices/connect-cameras-by-brand/other-brands.md#L1)–[L59](set-up-cameras-and-devices/connect-cameras-by-brand/other-brands.md#L59): No connection guidance — just six brand model lists. *Verified — file contains only "## <Brand> compatibility models" sections with bullet lists.*
- ✅ [L59](set-up-cameras-and-devices/connect-cameras-by-brand/other-brands.md#L59): No "Next steps" section. *Verified.*

**Other / typography:**
- ✅ [L3](set-up-cameras-and-devices/connect-cameras-by-brand/other-brands.md#L3): "vendor's" uses curly apostrophe. *Verified.*

---

### `set-up-cameras-and-devices/connect-cameras-by-brand/supported-cameras.md`

**List/step issues:**
- ✅ [L28](set-up-cameras-and-devices/connect-cameras-by-brand/supported-cameras.md#L28): "- Pelco, and more..." — last bullet ends with "and more..." (ellipsis). *Verified.*

**Structural:**
- ✅ [L45](set-up-cameras-and-devices/connect-cameras-by-brand/supported-cameras.md#L45): No "Next steps" section. *Verified — page ends after "Choose your camera brand" list.*

---

### `set-up-cameras-and-devices/connect-cameras-by-brand/verkada.md`

**List/step issues:**
- ✅ [L22](set-up-cameras-and-devices/connect-cameras-by-brand/verkada.md#L22)–[L26](set-up-cameras-and-devices/connect-cameras-by-brand/verkada.md#L26): step 2 of "Configure the main stream" combines five field entries. *Verified — sub-bullets enumerate IP address, RTSP port, username, password, connection string.*

**Structural:**
- ✅ [L46](set-up-cameras-and-devices/connect-cameras-by-brand/verkada.md#L46): No "Next steps" section. *Verified — page ends after the hint block.*

---

## Section 1 (continued) — `network-and-infrastructure-configuration` and `other-devices`

### `set-up-cameras-and-devices/network-and-infrastructure-configuration/README.md`

**Other / cosmetic:**
- ✅ [L1](set-up-cameras-and-devices/network-and-infrastructure-configuration/README.md#L1)–[L4](set-up-cameras-and-devices/network-and-infrastructure-configuration/README.md#L4): two blank lines between H1 and the first paragraph. *Verified — lines 2 and 3 are blank.*

---

### `set-up-cameras-and-devices/network-and-infrastructure-configuration/configure-lumana-core-as-a-dhcp-server.md`

**UI text exact match (capitalisation):**
- ✅ [L53](set-up-cameras-and-devices/network-and-infrastructure-configuration/configure-lumana-core-as-a-dhcp-server.md#L53), [L54](set-up-cameras-and-devices/network-and-infrastructure-configuration/configure-lumana-core-as-a-dhcp-server.md#L54), [L55](set-up-cameras-and-devices/network-and-infrastructure-configuration/configure-lumana-core-as-a-dhcp-server.md#L55), [L57](set-up-cameras-and-devices/network-and-infrastructure-configuration/configure-lumana-core-as-a-dhcp-server.md#L57): bold labels for pool and lease fields — confirm sentence case vs Title Case against the live DHCP Server form ([UI text and messages](STYLEGUIDE.md)).

---

### `set-up-cameras-and-devices/network-and-infrastructure-configuration/firewall-requirements.md`

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

**List/step issues:**
- ✅ [L9](set-up-cameras-and-devices/network-and-infrastructure-configuration/local-time-and-ntp-configuration.md#L9): step 1 combines three actions ("Open **Devices** → **Devices list**. Use the **Cores** filter… select **Edit location**."). *Verified.*
- ✅ [L13](set-up-cameras-and-devices/network-and-infrastructure-configuration/local-time-and-ntp-configuration.md#L13): step 2 combines two actions ("set **Time Zone**, then select **Save**"). *Verified.*

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

---

### `set-up-cameras-and-devices/other-devices/flir-sensors.md`

**Trustworthiness / completeness:**
- ✅ [L4](set-up-cameras-and-devices/other-devices/flir-sensors.md#L4): page contains only "Coming soon!" — incomplete page. *Verified — file is 4 lines total.*
- ✅ [L1](set-up-cameras-and-devices/other-devices/flir-sensors.md#L1)–[L4](set-up-cameras-and-devices/other-devices/flir-sensors.md#L4): two blank lines between H1 and body; exclamation point is informal. *Verified — lines 2 and 3 are blank; "Coming soon!" uses an exclamation point.*

---

### `set-up-cameras-and-devices/other-devices/gpio-devices.md`

**List/step issues:**
- ✅ [L38](set-up-cameras-and-devices/other-devices/gpio-devices.md#L38): step 3 "Select the GPIO to use. The Core can support up to 4 GPIOs, toggle high or low, and control how long the signal remains active." — combines selection and three configuration descriptions. *Verified.*

---

### `set-up-cameras-and-devices/other-devices/network-attached-storage-nas-devices.md`

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

**Bullet style:**
- ✅ [L13](set-up-cameras-and-devices/other-devices/sip-for-smart-speakers.md#L13)–[L15](set-up-cameras-and-devices/other-devices/sip-for-smart-speakers.md#L15) (`*`) vs [L23](set-up-cameras-and-devices/other-devices/sip-for-smart-speakers.md#L23)–[L24](set-up-cameras-and-devices/other-devices/sip-for-smart-speakers.md#L24) (`-`): mixes `*` and `-` bullets in the same file. *Verified — Prerequisites uses `*`, step substeps use `-`.*

**Other / typography:**
- ✅ [L95](set-up-cameras-and-devices/other-devices/sip-for-smart-speakers.md#L95), [L115](set-up-cameras-and-devices/other-devices/sip-for-smart-speakers.md#L115): "speaker's own admin interface" / "speaker's status" use curly apostrophes. *Verified.*

**Tables — formatting:**
- ✅ [L40](set-up-cameras-and-devices/other-devices/sip-for-smart-speakers.md#L40)–[L44](set-up-cameras-and-devices/other-devices/sip-for-smart-speakers.md#L44), [L61](set-up-cameras-and-devices/other-devices/sip-for-smart-speakers.md#L61)–[L64](set-up-cameras-and-devices/other-devices/sip-for-smart-speakers.md#L64), [L83](set-up-cameras-and-devices/other-devices/sip-for-smart-speakers.md#L83)–[L89](set-up-cameras-and-devices/other-devices/sip-for-smart-speakers.md#L89): tables escape underscores (`Oregon\_Gateways`, `SIP\_TLS\_AUTH`). *Verified.*

---

### `set-up-cameras-and-devices/other-devices/smart-speakers.md`

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

**1. ✅ Sentence length above 25 words.** *Largely addressed in this pass* for section indexes, streaming reference pages, camera onboarding guides, firewall text, and device pages; keep splitting long sentences when you touch nearby content.

**2. ✅ If/then construction.** *Largely addressed in this pass* for sentence-initial **If** clauses across live ops, analytics, and setup pages; keep adding an explicit **then** in the predicate when the **If** opens the sentence ([Sentence and paragraph rules](STYLEGUIDE.md)).

**3. ⚠️ Image-vs-step factual mismatches.** Several screenshots actively contradict the surrounding text. *Body-side text verified in the per-file sections above; image-side claims require visual review of each screenshot.*
- [`set-up-a-camera-floor-plan.md`](set-up-cameras-and-devices/set-up-a-camera-floor-plan.md): "top **left** corner" vs screenshot showing top-right.
- [`enable-ptz-control.md`](set-up-cameras-and-devices/enable-ptz-control.md): body now references an inline pencil icon in step 2; still verify `live-view-edit-camera-button.png` matches (round 3 claimed a wrench vs pencil mismatch) and that field labels match the PTZ form screenshot.
- [`lumana-core-hardware-specifications.md`](set-up-cameras-and-devices/network-and-infrastructure-configuration/lumana-core-hardware-specifications.md): text tells users to plug power into **POWER**; the labelled power input is **DC IN** (POWER is a button).
- [`camera-networking-options.md`](set-up-cameras-and-devices/camera-networking-options.md) and [`sip-for-smart-speakers.md`](set-up-cameras-and-devices/other-devices/sip-for-smart-speakers.md): SIP service rows say `SIP_UDP`; screenshots show `SIP_DEV_UDP`. On-premise device example in doc uses `Uniview_speaker`; screenshot shows `Hikvision_speaker` at that IP.
- [`axis.md`](set-up-cameras-and-devices/connect-cameras-by-brand/axis.md) and [`hanwha.md`](set-up-cameras-and-devices/connect-cameras-by-brand/hanwha.md): stream profile screenshots show "Maximum"/MBR bitrate while the body text says CBR.
- [`network-attached-storage-nas-devices.md`](set-up-cameras-and-devices/other-devices/network-attached-storage-nas-devices.md): doc says `NFS-Server-1`; screenshot's field shows `NFS-Sever-1`.

**5. ✅ Bold-as-heading misuse.** Previously: pseudo-headings in [`overview.md`](set-up-cameras-and-devices/overview.md), import/export labels in [`lumana.md`](set-up-cameras-and-devices/connect-cameras-by-brand/lumana.md), and figure labels in [`tracking-vehicles.md`](databases-analytics-and-search/tracking-vehicles.md). *Addressed — overview now uses `###` subheadings; lumana uses `### Import configuration` / `### Export configuration`; tracking-vehicles uses prose lead-ins before figures. [`share-video.md`](live-video-monitoring-and-operations/share-video.md) already uses `###` for section titles.*

**6. ✅ Run-in label colon placement (colon inside bold).** [`smart-speakers.md`](set-up-cameras-and-devices/other-devices/smart-speakers.md) still places colons inside bold for run-in labels (`**Label:**` instead of `**Label**:`). [`create-camera-shortcuts.md`](set-up-cameras-and-devices/create-camera-shortcuts.md) fixed to `**Label**:` (May 2026). [`lumana.md`](set-up-cameras-and-devices/connect-cameras-by-brand/lumana.md) bulk-operation bullets use colons outside bold per [UI text and messages](STYLEGUIDE.md).

**7. ✅ Naming-pattern inconsistency in `connect-cameras-by-brand/`.** *Addressed in source (May 2026): [`lumana.md`](set-up-cameras-and-devices/connect-cameras-by-brand/lumana.md) and [`verkada.md`](set-up-cameras-and-devices/connect-cameras-by-brand/verkada.md) now use “Connect … cameras” H1s like sibling brand pages.*

**8. ✅ Steps that combine multiple actions.** Still common on many setup and analytics pages. *Partially reduced in recent edits on [`live-view.md`](live-video-monitoring-and-operations/live-view.md), [`multi-camera-playback.md`](live-video-monitoring-and-operations/multi-camera-playback.md), [`build-a-database-of-people-and-vehicles.md`](databases-analytics-and-search/build-a-database-of-people-and-vehicles.md), [`video-walls-and-shared-displays.md`](live-video-monitoring-and-operations/video-walls-and-shared-displays.md) (Create wall flow split into single-action steps May 2026), [`share-video.md`](live-video-monitoring-and-operations/share-video.md), [`enhance-your-video-data-with-lumana-event-tags.md`](databases-analytics-and-search/enhance-your-video-data-with-lumana-event-tags.md), [`generate-reports.md`](databases-analytics-and-search/generate-reports.md), [`search-video-footage-for-other-objects.md`](databases-analytics-and-search/search-video-footage-for-other-objects.md), [`set-up-a-camera-floor-plan.md`](set-up-cameras-and-devices/set-up-a-camera-floor-plan.md), [`hanwha.md`](set-up-cameras-and-devices/connect-cameras-by-brand/hanwha.md), [`verkada.md`](set-up-cameras-and-devices/connect-cameras-by-brand/verkada.md), [`disruptive-sensors.md`](set-up-cameras-and-devices/other-devices/disruptive-sensors.md), [`network-attached-storage-nas-devices.md`](set-up-cameras-and-devices/other-devices/network-attached-storage-nas-devices.md), [`sip-for-smart-speakers.md`](set-up-cameras-and-devices/other-devices/sip-for-smart-speakers.md), [`smart-speakers.md`](set-up-cameras-and-devices/other-devices/smart-speakers.md). [`configure-lumana-core-as-a-dhcp-server.md`](set-up-cameras-and-devices/network-and-infrastructure-configuration/configure-lumana-core-as-a-dhcp-server.md) navigation and reservation procedures were split into single-action steps (May 2026).*

**9. ✅ Passive voice.** *Largely addressed in this pass* on DHCP, firewall, GPIO, NAS, SIP hints, smart speakers, supported cameras, Verkada, and several analytics pages; rephrase remaining "is/was/been" constructions when you edit those sections.

**10. ⚠️ UI label capitalisation drift.** Doc renders product UI labels in title case while the live UI uses sentence case: "Starting IP Address" → "Starting IP address"; "API Keys" → "API keys"; "Integration" → "Integrations"; "Data Connector" → "Data Connectors"; "External retention" → "External retention period"; "subnet mask" → "Subnet mask"; "username" → "User Name"; "Edit Location" inconsistent with "Edit location"; "Edit Camera" inconsistent with "Edit camera". *Doc-side casing verified across the per-file sections above; the live-UI labels need a visual review.*

**11. ✅ Future tense / "will".** Spot-check remaining pages after present-tense fixes in [`axis.md`](set-up-cameras-and-devices/connect-cameras-by-brand/axis.md) (ONVIF planning), [`hikvision.md`](set-up-cameras-and-devices/connect-cameras-by-brand/hikvision.md) (SADP scan / Connect a camera closer), [`recommended-streaming-settings.md`](set-up-cameras-and-devices/recommended-streaming-settings.md) (single-stream hint), and [`set-up-a-static-ip-address.md`](set-up-cameras-and-devices/set-up-a-static-ip-address.md) (DHCP mapping). *Re-run `grep` for ` will ` when editing nearby content.*

**12. ✅ May vs might.** Fixed across [`live-view-streaming-and-quality.md`](live-video-monitoring-and-operations/live-view-streaming-and-quality.md), [`the-system-health-dashboard.md`](live-video-monitoring-and-operations/the-system-health-dashboard.md), [`share-video.md`](live-video-monitoring-and-operations/share-video.md), [`video-walls-and-shared-displays.md`](live-video-monitoring-and-operations/video-walls-and-shared-displays.md), and [`recommended-streaming-settings.md`](set-up-cameras-and-devices/recommended-streaming-settings.md) FAQ bodies (May 2026). Run `grep -w may` when editing long guides for stragglers.

**13. ✅ Marketing / vague claims.** *Reduced on [`missing-object-alert.md`](databases-analytics-and-search/missing-object-alert.md), [`supported-cameras.md`](set-up-cameras-and-devices/connect-cameras-by-brand/supported-cameras.md), [`recommended-streaming-settings.md`](set-up-cameras-and-devices/recommended-streaming-settings.md), and [`connect-cameras-by-brand/README.md`](set-up-cameras-and-devices/connect-cameras-by-brand/README.md) (May 2026). [`tracking-containers.md`](databases-analytics-and-search/tracking-containers.md) and [`space-occupancy-analytics.md`](databases-analytics-and-search/space-occupancy-analytics.md) already use task-focused sections from an earlier rewrite.*

**14. ✅ Stacked headings without intervening paragraphs.** Residual focuses: [`sip-for-smart-speakers.md`](set-up-cameras-and-devices/other-devices/sip-for-smart-speakers.md) (`## Configure SIP on a Check Point router` → `### Prerequisites`). *[`firewall-requirements.md`](set-up-cameras-and-devices/network-and-infrastructure-configuration/firewall-requirements.md), [`lumana-core-hardware-specifications.md`](set-up-cameras-and-devices/network-and-infrastructure-configuration/lumana-core-hardware-specifications.md), and [`gpio-devices.md`](set-up-cameras-and-devices/other-devices/gpio-devices.md) now include lead-in paragraphs; H4 regional headings were promoted to H3.*

**15. ✅ Headings that aren't user-focused or that misuse "Step N:" framing.** *Prior round-3 anchors for [`enhance-your-video-data-with-lumana-event-tags.md`](databases-analytics-and-search/enhance-your-video-data-with-lumana-event-tags.md), DHCP capabilities, floor-plan feature framing, and camera-shortcuts "Key benefits" were addressed in source (May 2026). [`enable-ptz-control.md`](set-up-cameras-and-devices/enable-ptz-control.md) “Key capabilities” block removed earlier.*

**16. ✅ Heading parentheses.** [`network-attached-storage-nas-devices.md`](set-up-cameras-and-devices/other-devices/network-attached-storage-nas-devices.md) H1 "(NAS) devices"; [`camera-networking-options.md`](set-up-cameras-and-devices/camera-networking-options.md) "Remote camera access (Camera VPN)". *`lumana-core-hardware-specifications.md` dimensions heading no longer uses parentheses (spelled out as "in millimeters"). [`pixels-per-foot-for-camera-placement.md`](databases-analytics-and-search/pixels-per-foot-for-camera-placement.md) H1 no longer uses a `(PPF)` suffix (May 2026).*

**17. ✅ "Coming soon!" placeholder pages.** [`create-links-between-cameras.md`](set-up-cameras-and-devices/create-links-between-cameras.md), [`flir-sensors.md`](set-up-cameras-and-devices/other-devices/flir-sensors.md). *Verified — both files contain only "Coming soon!".*

**18. ✅ Asset folder structure.** SVG icon cards now resolve under `.gitbook/assets/icons/`, and README `<img>` paths were updated repo-wide (May 2026). *Many setup screenshots still live at the assets root (`dhcp-*.png`, `ntp-*.png`, and similar) rather than under per-section folders—normalize when you replace those assets. [`missing-object-alert`](databases-analytics-and-search/missing-object-alert.md) and [`pixels-per-foot-for-camera-placement`](databases-analytics-and-search/pixels-per-foot-for-camera-placement.md) image basenames now match their pages.*

**19. ✅ Bullet-style inconsistency.** [`network-attached-storage-nas-devices.md`](set-up-cameras-and-devices/other-devices/network-attached-storage-nas-devices.md), [`sip-for-smart-speakers.md`](set-up-cameras-and-devices/other-devices/sip-for-smart-speakers.md) mix `*` and `-` bullets within the same file. *[`gpio-devices.md`](set-up-cameras-and-devices/other-devices/gpio-devices.md) unified to `-` in Parts list / Wiring notes (May 2026).*

**20. ⚠️ Curly vs straight apostrophes.** Inconsistent across many files (`'` mixed with `'`). *Spot-checks: [enhance-your-video-data-with-lumana-event-tags.md](databases-analytics-and-search/enhance-your-video-data-with-lumana-event-tags.md), [sip-for-smart-speakers.md](set-up-cameras-and-devices/other-devices/sip-for-smart-speakers.md); [tracking-people.md](databases-analytics-and-search/tracking-people.md) `organization's` is straight ASCII (May 2026).*

**21. ✅ Italics with `*` instead of `_`.** *Addressed on [`set-up-a-camera-floor-plan.md`](set-up-cameras-and-devices/set-up-a-camera-floor-plan.md) (May 2026).*

**22. ✅ "Where" used to connect clauses.** Residual example: [`camera-networking-options.md`](set-up-cameras-and-devices/camera-networking-options.md) (“…private network where you need the manufacturer's configuration UI”). *Fixed in [`live-view-streaming-and-quality.md`](live-video-monitoring-and-operations/live-view-streaming-and-quality.md), [`share-video.md`](live-video-monitoring-and-operations/share-video.md), [`other-brands.md`](set-up-cameras-and-devices/connect-cameras-by-brand/other-brands.md) (May 2026).*

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
