# Most Days, web app prototype

Live at https://most-days-app.vercel.app · Code at https://github.com/aloonia/most-days

A single-page web app of the phase-one flows: the happy path, Change it, Can't today, and the swim journey with honest watch sync. It installs on an iPhone home screen with its own icon and opens full screen.

## What's in the folder

- `index.html`: the whole app (HTML, CSS and JavaScript in one file)
- `manifest.webmanifest`: tells phones the app's name, colours and icon
- `icons/`: the app icon in the sizes iPhone and Android need
- `photos/`: black-and-white photos from Unsplash (free licence)

## Try it on your Mac

```bash
cd ~/Desktop/Project/most-days-app && python3 -m http.server 8765
```

Then open http://localhost:8765 in a browser. On a wide screen it shows inside a phone frame.

## Try it on your iPhone, same Wi-Fi, nothing published

1. On the Mac, run: `python3 -m http.server 8765 --bind 0.0.0.0` inside this folder.
2. Find the Mac's address: System Settings, Wi-Fi, Details, IP address (for example 192.168.1.20).
3. On the iPhone, open Safari and go to `http://192.168.1.20:8765`.
4. Tap Share, then Add to Home Screen. The Most Days icon appears and opens full screen.

This only works while the Mac is on and on the same Wi-Fi.

## Put it online for a portfolio (free)

Any static host works, because this is just files. Two easy options:

- **Netlify Drop:** go to app.netlify.com/drop and drag this folder in. You get a public https link. A free account keeps it online.
- **GitHub Pages:** push the folder to a GitHub repository and turn on Pages in the repository settings.

Then open the link on the iPhone, tap Share, Add to Home Screen.

## Demo links for presenting

Add these to the end of the link to jump straight to a screen:

Open the plain link to go through everything from the splash screen: intro, setup, building your week, then day one. Progress is saved on the device. "Start over" in the You tab resets it, and `?reset=1` clears everything.

Jump straight to a moment:

- `?demo=day1&screen=today`: a first-time Home on day one, with the wedding nudge
- `?demo=day7&screen=today`: week two, with the calendar clash and the air-quality nudge
- `?demo=day7&screen=change`: Change it, with “Early start tomorrow” picked
- `?demo=day1&screen=cant`: Can't today, with Saturday blocked by the wedding
- `?demo=day7&screen=swimsync`: the swim sync that miscounts lengths
- `?demo=day7&screen=calendar`, `screen=plan`, `screen=why`, `screen=you`
- `?screen=onb`: setup from the first question
- `?sync=two`, `?sync=off` or `?sync=nothing`: change what the watch sends when you tap I did it

## What's simulated

Calendar reading, Strava sync and suggestions are scripted for the demo. The real links are the YouTube Music playlist, Add to Google Calendar, WhatsApp, and the phone's share sheet.

## Icons

Phosphor Icons (MIT licence), loaded from unpkg. They need an internet connection.

## Photo credits (Unsplash)

Jorgen Hendriksen, Mathias Reding, Nikita Pishchugin, Oscar Söderlund, Yevgeniy Mironov, Zhu Liang, Jorge Romero, Bj Pearce, Artiom Vallat, Corey Young.
