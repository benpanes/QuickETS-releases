# QuickETS

A small Android home-screen widget that shows the next arrivals at an Edmonton Transit Service (ETS) stop, drawn like the orange LED boards in ETS stations.

- Pick a stop by **name** or number, or from stops near you. Each shows its direction (northbound, southbound, ...).
- It updates when you **tap its refresh icon** or open its menu, and runs nothing in the background (no service, no notification). The widget shows clock times, so they never go stale between updates.
- Tap it to see every arrival in the next 20 minutes, and filter by **route and destination** (for example, only `8 Abbottsfield`, not `8 University`).
- Transit centres with many platforms (Coliseum, Mill Woods, ...) can be shown **all together**, with the platform letter beside each arrival, or filtered to just the bays you use.
- A **two-stop commute** can switch by itself: the morning stop before noon, the stop you catch home after, with no tapping.
- Live times from ETS where available, the published timetable otherwise.
- **Delays:** late buses are red with the delay in brackets after the time, like `5:02(+10)`; early buses are yellow.
- **Follow a trip:** tap an arrival in the widget menu to see the bus's whole journey, pick a stop after yours, and follow it there. Until the bus arrives, the widget (and the watch tile) show only that trip, with when it leaves and when it reaches your destination. The destination is remembered for next time.
- **Past departures** can be listed, dimmed, in the widget menu (you choose how far back, or turn it off).
- **Maps:** tap **Show on map** on a trip to see it on a map (OpenFreeMap, built from OpenStreetMap data): the route, your stop and destination, and a bus or train icon where the vehicle is. Buses show their live position; trains (ETS publishes no live train positions) are placed along the real track from the timetable and drawn fainter, marked `estimated`. When you add a widget or swap its stop, **Show stops on a map** lets you tap a stop to choose it. **Settings > Map style** picks light, dark, follow the phone, or a plain background with no map.
- **Service alerts** from ETS for your stop and route show on the trip screen.
- **Offline mode** (Settings): nothing is fetched, and boards and trips come from the stored timetable. It can also switch on by itself whenever the phone is not on Wi-Fi.
- **Walking time** (opt-in, Settings): how long it takes to walk to the stop and when to leave for the next bus, worked out on the phone with your location.
- A **Wear OS tile** can show the same board. The watch app is a separate install and is not part of these downloads.

## Install

You need an Android phone running Android 8.0 or newer.

1. Open the **[latest release](../../releases/latest)** on your phone and download `QuickETS-<version>.apk`.
2. Open the downloaded file. Android will ask you to allow installing apps from your browser or file manager: allow it for this one install.
3. Open QuickETS, tap **Add widget to home screen** (or long-press your home screen, choose Widgets, then QuickETS), and pick your stop.

The first time you pick a stop, the app downloads ETS's timetable (about 18 MB, once). The app itself is about 14 MB (it carries the map library) and is built for 64-bit ARM phones, which is nearly every Android phone from the last several years.

### Updating

Open QuickETS, tap **Settings**, then **Check for updates**. It also looks quietly when you open it and shows a banner when a newer version exists. New versions install over the old one and keep your widgets and settings.

## Privacy

There are no accounts, no ads and no analytics. The app downloads ETS's public timetable and live feeds and checks this page for new versions. Your location is used only when you tap **Find stops near me**, or while the menu, the main screen or the trip map is open if you turn on walking time, and it never leaves your phone. Opening a map downloads map tiles from OpenFreeMap (a free service built on OpenStreetMap data), which can see your IP address and the area you are viewing (and nothing else); that is the only time the app contacts OpenFreeMap.

## Data and credits

Arrival data is published by Edmonton Transit Service through the City of Edmonton's open data program and is used under the [City of Edmonton Open Data Terms of Use](https://data.edmonton.ca/stories/s/City-of-Edmonton-Open-Data-Terms-of-Use/msh8-if28/). QuickETS is an independent project and is **not affiliated with or endorsed by the City of Edmonton or ETS**.

The lettering inside the app is the [Doto](https://github.com/oliverlalan/Doto) font, copyright 2024 The Doto Project Authors, used under the SIL Open Font License 1.1 (the licence text is also inside the app, under **Open-source licences**).

## About this repository

This repository only hosts the release builds. Each release's notes say what changed.

QuickETS is provided as is, without warranty of any kind, and is released under the MIT License (see [LICENSE](LICENSE)). Arrival times are predictions and can be wrong; don't rely on them for anything critical.
