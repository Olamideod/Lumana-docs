# REST APIs

This book documents Lumana HTTP usage where guides exist in these pages. There is no separate OpenAPI/Swagger file in this repository for every endpoint.

## Event tag ingestion

Use this when you need to send events for a **custom event tag** you defined under **Organization database** → **Event tags**.

| Item | Value |
|------|--------|
| **Method and URL** | `POST https://access.lumana.ai/v1/events-tag/insert` |
| **Auth** | `Authorization: Bearer <API key>` (create under **Organization** → **Organization settings** → **API keys** → **Generate Key**; use **Bearer Token** in Postman) |
| **Event type ID in JSON** | `eventTypeId` — copy the **Event type ID** from the **Event tags** table in the portal (same row as your tag **Name**) |

Request body also requires `orgId`, `cameraId`, `timestamp` (Unix epoch **milliseconds**), and `fields` (keys must match the field **Name** values on that tag).

**End-to-end guide** (create tag, cURL example, verify data, dashboard counts): [Enhance your video data with Lumana Event Tags](../databases-analytics-and-search/enhance-your-video-data-with-lumana-event-tags.md).

**Dashboard widget** (**Datasource** → **Event tags**, axes, empty chart troubleshooting): [Event tags (Chart or table)](../dashboards/widgets/chart-or-table-event-tags.md).
