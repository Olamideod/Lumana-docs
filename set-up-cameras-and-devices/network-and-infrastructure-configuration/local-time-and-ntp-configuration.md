# Local time and NTP configuration

The time shown in live view and playback is determined by the time zone configured on the location where the core and cameras are installed.

## Change the location time zone

1. Hover the name of the relevant location and click *Edit location*.

![Edit location button on location card.](../../.gitbook/assets/ntp-edit-location.png)

2. Edit the *Time Zone* field.

![Edit Location, Time Zone field.](../../.gitbook/assets/ntp-location-timezone-field.png)

## Configure Network Time Protocol (NTP)

Lumana Core requires connection to a Network Time Protocol (NTP) server to synchronize time correctly.

Lumana's default NTP servers are:

- `0.pool.ntp.org`
- `1.pool.ntp.org`
- `0.fr.pool.ntp.org`

If you want to use a local NTP server instead:

1. Click the *edit* icon for the core you want to update.
2. Select *NTP*.
3. Click *Add server* and enter the URL of the server you want to add.
4. Click *Save*.
