# Space occupancy analytics

Space occupancy analytics uses your cameras and Lumana’s analytics to track how many people or vehicles are in a defined space over time. You get live counts plus historical views so you can monitor current occupancy, review trends, and compare how a space is used across hours or days.

## Key features

Space occupancy can support several operational uses.

### Real-time occupancy tracking

Analytics process the video stream to estimate how many people or vehicles are in monitored areas. You can:

- Monitor utilization and spot overcrowding or quiet periods.
- Compare live counts to occupancy limits your organization defines.
- React to changing counts with staffing, access, or routing adjustments.

### Historical trend analysis

Occupancy is stored over time so you can review patterns. That helps you:

- Identify peak hours and adjust schedules or operations.
- Inform layout changes from movement patterns.
- Plan space and resources using longer-range usage data.

### Location analysis

You don't need to cover the whole floor with cameras. Aim coverage at every path in and out of the zone; that often needs fewer devices than full-floor monitoring. Counts stay trustworthy only if nobody can bypass a line you rely on. How virtual lines and crossings work is explained in [How space occupancy works](#how-space-occupancy-works).

### Dashboards and reporting

Use dashboards to present occupancy metrics in one place. You can:

- See live and historical data together.
- Compare zones or sites when your setup supports multiple lines or spaces.
- Export or share reports when you need evidence for audits, compliance, or planning. Details depend on your widget and export options. See [Occupancy](../dashboards/widgets/occupancy.md).

### Security and compliance

Occupancy data supports operational safety and policy checks. For example:

- Track counts against maximum occupancy for busy areas.
- Use current totals when you plan for evacuations or headcount checks.
- Review unusual spikes or drops in occupancy that may deserve follow-up.

## How space occupancy works

Space occupancy relies on cameras that watch entry and exit points. You place virtual count lines on the video so crossings count as in or out. Lumana maintains a running total from those crossings. Multiple cameras can feed one logical space so you cover every doorway or lane that matters.

The feature works best when every way into and out of the counted area is covered. If someone can enter or leave without crossing a line, the total will drift from the real number inside.

## Choose a camera placement

Camera placement affects counting accuracy. Aim each camera so it has a clear view of the crossing you want to measure for every entrance and exit you include in the count.

### Overhead camera placement

Use overhead placement when counting accuracy matters most and you can mount the camera to look straight down across the path.

- *Placement*: Mount directly above the entrance so movement crosses the field of view horizontally.
- *Key benefit*: Highest counting accuracy, including when several people enter or leave at once.
- *Best for*: High-traffic doors or lanes with simultaneous in/out traffic.
- *Limitation*: A top-down angle limits how useful the same view is for face or license plate detail.

<div align="center" data-with-frame="true"><img src="../.gitbook/assets/databases-analytics-and-search/space-occupancy-top-down-camera-placement.png" alt="Overhead camera view with a virtual count line across a doorway, In and Out labels on the line." width="563"></div>

### Front-facing camera placement

Use front-facing placement when you want occupancy counts and a view that is also useful for identification (for example face or plate workflows where the scene supports it).

- *Placement*: Mount at eye level or slightly above, roughly 8–10 feet in front of the entry or exit.
- *Key benefit*: Same feed can support occupancy trends and clearer identity context than a strict top-down shot.
- *Best for*: Spaces where you monitor occupancy and still need a forward view of people or vehicles.
- *Limitation*: Crowding can cause overlap and small counting mismatches.

<div align="center" data-with-frame="true"><img src="../.gitbook/assets/databases-analytics-and-search/space-occupancy-front-facing-camera-placement.png" alt="Front-facing entrance view with a virtual count line on the floor, In and Out labels." width="563"></div>

### Maintain counting accuracy

Whatever angle you choose, the same conditions usually apply:

- *Clear sightlines*: Keep doors, pillars, signage, or furniture from blocking the crossing.
- *Lighting*: Poor light hurts detection; change aim, add light, or use cameras suited to low light or infrared if your devices support it.
- *Full access-point coverage*: Partial coverage produces wrong totals; count every path in and out of the space.

## Common accuracy issues

Even with good placement, counts can mislead if rules or the scene are wrong.

### Reset while the space is occupied

Occupancy is entries minus exits (with reset rules you configure). If the count resets to zero while people are still inside, later exits can drive the total negative or otherwise confuse the chart. The system is not wrong about the exits. It is missing the true starting population.

For example, if five people remain when the reset runs, the next exits subtract from zero and the line can go below zero.

{% hint style="info" %}
Schedule resets when the space is empty, or align with your [widget reset settings](configure-a-space-occupancy-dashboard.md) so the baseline matches reality.
{% endhint %}

### Occlusion at the entrance or exit

Counting needs a clear crossing. If people are hidden by objects, architecture, or each other, the model can miss an in or out. When entries are missed more than exits (or the reverse), the running total drifts. Severe imbalance can also contribute to strange negatives over time.

## Configure a space occupancy dashboard

When cameras are aimed and count lines exist for your doors or lanes, add the **Occupancy** widget and finish its settings in the UI. Follow [Configure a space occupancy dashboard](configure-a-space-occupancy-dashboard.md).

## Next steps

- Use [Configure a space occupancy dashboard](configure-a-space-occupancy-dashboard.md) for the step-by-step widget flow (calculation, reset schedule, viewing hours).
- Read [Occupancy](../dashboards/widgets/occupancy.md) for widget options, calculations, and exports.
