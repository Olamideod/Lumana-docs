# Documentation revamp tracker

This doc has two parts:
1. The list of pages that have already been revamped against the new UI (images and steps updated).
2. Open issues and questions for the SME and product team — pages that are blocked because the feature couldn't be located in the new UI, looks removed, or seems outdated.

---

## Part 1 — Pages revamped against the new UI

### Set up cameras and devices
- Set up a camera floor plan
- Set up a static IP address
- Enable PTZ control
- Create camera shortcuts
- Disruptive sensors
- Other devices / NAS devices
- Smart speakers
- Configure Lumana Core as a DHCP server
- Local time and NTP configuration

### Databases, analytics, and search
- Build a database of people and vehicles
- Configure a space occupancy dashboard
- Enhance your video data with Lumana Event Tags
- Free text search
- Generate reports
- Create a missing object alert (same content as Custom objects)
- Search the video footage for other objects
- Search video footage for people and vehicles
- Tracking containers

### Live video monitoring and operations
- Change dark mode and light mode
- Live video streaming and quality
- Use live view
- Use Lumana timelapse
- Multi-camera playback
- Use PTZ control
- Share video
- Use the system health dashboard
- Video walls and shared displays

---

## Part 2 — Open issues and questions

Each issue lists where we got blocked and the specific question we need answered before we can finish the page.

---

### Issue 1 — Shared external video wall: confirm the new UI flow

**Page:** Video walls and shared displays
**Section:** "Create a shared external video wall" (was meant to sit before Next steps)
**Status:** Section removed pending confirmation. The current page has a TODO comment placeholder.

**Context:** Previously, this section documented building a shared external video wall by generating an API key, collecting camera IDs, choosing a resolution, and assembling a URL of this form:

```
https://external-walls.lumana.ai/live-view-wall.html?resolution=<0|1|2>&cameraNames=1&cameraIds=<CAMERA_ID1>,<CAMERA_ID2>&token=<YOUR_API_TOKEN>
```

…with `resolution` mapped to 0 = SQ, 1 = MQ, 2 = HQ, and `cameraNames=1` toggling on-screen camera names.

**Questions:**
- Is this URL-based shared external video wall flow still supported in the new UI?
- If yes, does the URL format still match what's above, and does the camera ID still come from "Edit camera"? Are there any new query parameters?
- Where in the new UI does the user generate the API key for this purpose? Has that path changed since the previous "Settings → Organization Settings → API Keys" location?
- If no, is there a replacement flow we should document in its place?

---

### Issue 2 — Multi-camera playback: green-highlight on timeline still in the new UI?

**Page:** Multi-camera playback
**Section:** Just before Next steps (currently sits as an info hint)

**Context:** The page currently includes this hint:

> In search-based playback, a green highlight on a camera timeline marks frames where the searched object appears, like in the image below.

**Questions:**
- Does the green-highlight indicator still exist in the new multi-camera playback UI?
- If yes, is the screenshot we're using still accurate, or do we need a new capture?
- If no, what is the replacement (different colour, different indicator, removed entirely)?

---

### Issue 3 — Lumana timelapse: where is the "Create timelapse" screen in the new UI?

**Page:** Use Lumana timelapse
**Doc link:** https://docs.lumana.ai/live-video-monitoring-and-operations/lumana-timelapse#understand-timelapse-availability

**Context:** The page currently documents the **Snapshot retention days** setting under camera **Storage**, but the actual entry point to *create* a timelapse from a camera (the "Create timelapse" dialog with camera, timeframe, and duration controls) can't be found in the new UI.

**Questions:**
- Where in the new UI does a user start a new timelapse? (Live view? Camera page? Devices?)
- Has the "Create timelapse" dialog been redesigned, renamed, or removed?
- If removed: what is the supported workflow for generating a timelapse video now?

---

### Issue 4 — People directory and vehicles directory: where do these live in the new UI?

**Page:** Build a database of people and vehicles
**Affected sections:** People directory (saved profiles, unsaved people, groups), Vehicles directory ("Vehicles seen on camera", "Existing vehicles", manual upload, CSV import).

**Context:** The page documents the people directory and vehicles directory as the place to organize detected items into saved profiles and groups. The current screenshots reflect the older UI.

**Questions:**
- In the new UI, where do users access the people directory? Is it still under **Database** in the sidebar?
- Same question for the vehicles directory and the **Add from file** / **Import from file** controls.
- Has the "groups" workflow (Create group → name → add people → save) changed or moved?
- If anything has been renamed (for example "directory" → "library"), please confirm the new wording so we use the live UI labels exactly.

---

### Issue 5 — Tracking containers: where is the "Analytics" sidebar in Edit camera?

**Page:** Tracking containers
**Doc link:** https://docs.lumana.ai/databases-analytics-and-search/tracking-containers#enable-container-detection-on-a-camera

**Context:** The "Enable container detection on a camera" steps tell users to:
1. Open the camera.
2. Select **Edit camera**.
3. In the sidebar, select **Analytics**.
4. Under **Custom capabilities**, select **Container**.
5. Select **Save**.

The **Analytics** option in the Edit camera sidebar can't be located in the new UI.

**Questions:**
- Has **Analytics** been moved, renamed, or merged into another tab in Edit camera?
- Where do users now toggle container detection (and other custom capabilities) on a camera in the new UI?
- Is **Container** still the correct label under **Custom capabilities**, or has the option been renamed?

---

### Issue 6 — Free text search: is the feature still supported?

**Page:** Free text search
**Doc link:** https://docs.lumana.ai/databases-analytics-and-search/free-text-search

**Context:** The page documents opening **Search**, then selecting **Switch to text search** to enter natural-language queries (for example "person in a black shirt walking through a door"). The **Switch to text search** control can't be found from the search icon in the new UI.

**Questions:**
- Is free text search still a supported feature in the new UI?
- If yes, where is the entry point now? (Has it moved out of **Search**, or has the toggle been replaced with something else, like a unified query bar?)
- If no, is there a replacement we should document, or should we deprecate this page?

---

### Issue 7 — Event Tags: where do users generate the API key in the new UI?

**Page:** Enhance your video data with Lumana Event Tags
**Doc link:** https://docs.lumana.ai/databases-analytics-and-search/enhance-your-video-data-with-lumana-event-tags#step-1-generate-an-api-key

**Context:** Step 1 directs users to:
1. Open **Organization → Organization settings**.
2. Select **API keys** in the left menu.
3. Select **Generate Key** to open the **Create API Key** dialog.

The **API keys** entry in **Organization settings** can't be found in the new UI.

**Questions:**
- In the new UI, where does the user create and manage API keys for Event Tags? Is it still under **Organization settings**, or has it moved (for example into a **Developer** or **Integrations** section)?
- Are the field labels in the create-key dialog still **API Key name** and **Expiration**, with copy/download for the secret?
- Are the limits (10 API keys, 10 event tag definitions) still accurate?

---

## Notes for reviewers

- For each open issue, please point us to the exact UI path (top-level menu → submenu → control) and, ideally, drop a screenshot so we can match the live product wording exactly.
- If a feature has been retired, please say so explicitly so we can remove the page from publication or redirect it to the replacement.
- Where labels have only been renamed, the new label is enough — we'll handle the surrounding prose.
