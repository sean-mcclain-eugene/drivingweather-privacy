---
layout: default
title: Driving Weather Privacy Policy
permalink: /
---

# Privacy Policy for Driving Weather

**Effective date:** October 6, 2026

This policy covers the Android app **Driving Weather** (package `com.drivingweather.app`), made by Sean McClain ("I", "me"). It explains what information the app uses, where that information goes, and the choices you have.

## The short version

- Driving Weather is **free and non-commercial**. It has no ads, no in-app purchases, no subscriptions, **no accounts, no analytics, and no tracking**.
- **I don't run a server.** The app doesn't send your information to me, and I don't receive, store, sell, or monetize it.
- To plan a trip, the app sends the places you enter or choose, and your current location if you choose to use it, **directly from your phone** to the third-party map, routing, and weather services listed below. They need this information to return directions, town names, forecasts, and alerts.
- The app uses your location **only while you're using it**, and **only when you tap "Use current location."** It never uses location in the background.
- The app saves no trip history on your phone. A trip PDF is created only when you ask for one, and you choose where to send it.

## Information the app uses

### Places you type or choose
When you type in the Start, Stop, or End fields, the text you've typed so far (for example "New Y" while typing "New York") goes to **Open-Meteo's geocoding service** so the app can suggest matching places. Once you pick places and plan a trip, their coordinates go to the routing and weather services below.

### Your location (optional)
If you tap **"Use current location"**, Android asks whether to allow location access. You can allow **precise** or **approximate** location, or deny it.

- If you allow it, the app gets your device's location **once**, through Google Play services' location service on your phone, and uses it as your trip's starting point.
- To show a place name instead of raw coordinates, the app sends that location to **OpenStreetMap Nominatim**. Because it becomes your trip's start, it is also used in the trip requests below: routing, weather, the map image in the PDF, and "Open in Google Maps".
- The app **doesn't** track you, keep watching your location, use location in the background, or save your location history.
- If you deny permission, you can still type a start place. To change your choice later, go to Android **Settings → Apps → Driving Weather → Permissions → Location**.

### Trip details
To work out the forecast for the hour you'll pass each town, the app uses your departure date and time, your stops, and any layover hours. It sends the trip dates to Open-Meteo and the departure time to Google's Directions service when Google routing is used. Layover hours are only used on your phone.

### Technical information every internet request includes
Like any app that goes online, each request reveals your device's **IP address** to the service receiving it. The app also sends a fixed app identifier (a "User-Agent" with the app's name and a developer contact email address), which some services require. This identifier is the same for every user and contains nothing about you.

### Information the app does not collect
No name, email address, phone number, contacts, photos, files, account details, payment information, advertising ID, or usage analytics.

## Third-party services the app talks to

Your phone connects to these services directly, over encrypted HTTPS connections. Each one handles what it receives under its own privacy policy and terms, which I don't control. Some keep server logs. For example, Open-Meteo says its logs may include coordinates and are deleted after 90 days.

| Service | What it does in the app | What it receives | Policies |
|---|---|---|---|
| **Open-Meteo Geocoding API** (`geocoding-api.open-meteo.com`, OpenMeteo GmbH, Switzerland) | Place suggestions and place lookup | The text you type in the Start, Stop, and End fields | [Terms & privacy](https://open-meteo.com/en/terms) · [Data license (CC BY 4.0)](https://open-meteo.com/en/license) |
| **Open-Meteo Forecast API** (`api.open-meteo.com`) | Hourly forecasts for each weather zone on your route | Coordinates of points along your route; trip dates | Same as above |
| **Open-Meteo Historical Weather API** (`archive-api.open-meteo.com`) | Past weather, used only if you plan a trip for a date that has already passed | Coordinates of points along your route; trip dates | Same as above |
| **OpenStreetMap Nominatim** (`nominatim.openstreetmap.org`, run by the OpenStreetMap Foundation) | Town names along your route, and a name for your current location | Coordinates of points along your route, and your current location if you use that feature | [OSMF Privacy Policy](https://osmfoundation.org/wiki/Privacy_Policy) · [Nominatim Usage Policy](https://operations.osmfoundation.org/policies/nominatim/) · [OSMF Terms of Use](https://osmfoundation.org/wiki/Terms_of_Use) |
| **Google Directions API** (`maps.googleapis.com`, Google LLC) | Driving directions (the app's main routing service) | Coordinates of your start, stops, and destination; your departure time | [Google Privacy Policy](https://policies.google.com/privacy) · [Google Maps/Google Earth Additional Terms of Service](https://maps.google.com/help/terms_maps/) |
| **OSRM public routing server** (`router.project-osrm.org`, run by FOSSGIS e.V., Germany) | Backup driving directions, used only when Google's Directions service isn't available | Coordinates of your start, stops, and destination | [FOSSGIS privacy policy (German)](https://www.fossgis.de/datenschutzerklärung) · [Usage terms](https://www.fossgis.de/arbeitsgruppen/osm-server/nutzungsbedingungen/) |
| **U.S. National Weather Service** (`api.weather.gov`, NOAA) | Active weather alerts along U.S. routes | Only the **two-letter codes of the U.S. states** your route crosses (worked out on your phone). No coordinates, place names, or other trip details. | [NWS privacy policy](https://www.weather.gov/privacy) · [NWS disclaimer](https://www.weather.gov/disclaimer) |
| **Google Maps SDK for Android** (Google LLC) | The in-app map | The map areas you view, plus technical data the SDK collects on its own for Google: device model and OS version, SDK version, crash information, IP address, a pseudonymous Maps SDK identifier, and map interactions such as panning and zooming. Your route line and markers are drawn on your phone. | [Google Privacy Policy](https://policies.google.com/privacy) · [Google Maps/Google Earth Additional Terms of Service](https://maps.google.com/help/terms_maps/) |
| **Google Static Maps API** (`maps.googleapis.com`) | The map image in an exported trip PDF, only when you tap Export PDF | Your route line (simplified) and the coordinates of your start, stops, and destination | Same as Google above |
| **Google Play services location** (on your device) | Gets your device's location when you tap "Use current location" | Handled by Android and Google Play services according to your device's location settings | [Google Privacy Policy](https://policies.google.com/privacy) |

**"Open in Google Maps"**: if you tap this, the app passes your trip's start, stop, and destination coordinates to the Google Maps app, or to your web browser if Google Maps isn't installed. From then on, Google's [Privacy Policy](https://policies.google.com/privacy) and [Maps terms](https://maps.google.com/help/terms_maps/) apply.

I don't sell your information, share it for advertising, or make money from it. Information goes to the services above only so the app can do what you asked.

## What is stored on your phone, and how to delete it

- **Trips aren't saved.** The current trip lives in the app's memory and disappears when the app is closed by you or by Android.
- **PDF export:** when you tap **Export PDF**, the app creates a trip PDF in its private cache folder (`drivingweather-trip.pdf`, replaced by each new export). The PDF includes your start, stops, and destination (which may include coordinates if a place name couldn't be found), the route summary, weather by zone, and a map image. Android's share sheet then opens, and **you choose** which app (if any) receives the PDF. Once shared, the copy is handled by that app or recipient.
- **To delete everything the app stores:** go to **Settings → Apps → Driving Weather → Storage → Clear storage / Clear cache**, or uninstall the app.
- **Information held by third parties:** I don't have any of your information, so I can't access or delete it, and the app has no deletion-request process. To ask a third-party service about data in its logs, contact that service through its privacy policy above.

## Children

Driving Weather is a trip-planning tool for drivers. It isn't directed at children under 13, and I don't knowingly collect personal information from children.

## Security

All of the app's network connections use HTTPS (encrypted in transit). Because I don't operate a server or keep user data, I hold no store of your information that could be breached. No method of transmission or storage is completely secure, though, and each third-party service is responsible for protecting the data it receives.

## Weather and safety note

Forecasts, alerts, routes, and arrival times come from third-party sources and may be inaccurate, incomplete, or out of date. Don't rely on the app as your only source of safety information, and don't use the app while driving.

## Changes to this policy

If the app's data practices change, I'll update this page and its effective date. For significant changes, I'll also mention it in the app's release notes on Google Play.

## Contact

Questions about this policy or the app: [mcclain.sean.appdev@gmail.com](mailto:mcclain.sean.appdev@gmail.com)
