# REST APIs

The Lumana REST API lets you post structured events from external systems and tie them to camera footage by time and camera. You'll use it to send event tag data to Lumana, where it becomes searchable and available for visualization on any dashboard.

Lumana authenticates every API request using API keys as Bearer tokens. You generate your key under **Organization**, then **Organization settings**, then **API keys**, then **Generate Key**. Store the secret securely because Lumana won't show it again.

## Available endpoints

The Lumana API currently supports event tag ingestion. The full endpoint reference, including request fields, response schemas, error codes, and a cURL example, is in the [Lumana API reference](api-reference.md).

## Related guides

If you're setting up event tags for the first time, start with the end-to-end setup guide before calling the API. It walks you through generating an API key, creating an event tag, posting your first event, and verifying the data.

- [Enhance your video data with Lumana Event Tags](../databases-analytics-and-search/enhance-your-video-data-with-lumana-event-tags.md) — full setup, cURL example, and data verification steps.
- [Event tags (Chart or table)](../dashboards/widgets/chart-or-table-event-tags.md) — configure the dashboard widget to visualize event tag data after your first successful POST.