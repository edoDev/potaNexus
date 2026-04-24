# potaNexus
A dynamic map for POTA activations
# POTA Cartographer's Dynamic Map

A beautiful, single-file, Leaflet-powered interactive map showing **all the parks you have activated** in the Parks on the Air (POTA) program. Designed specifically for cartographers (like KD0WAN) with topographic basemaps, marker clusters, live POTA API integration, dynamic statistics, full activation logs, and a clean sidebar.

Perfect for embedding on your **QRZ.com** page, personal website, or sharing with fellow hams.

## ✨ Features (the "wow" factors)

- Fully **customizable** – just edit the config at the top of the file
- Live POTA API integration (park metadata + recent activation logs + dynamic stats)
- Beautiful modal with rich metadata, comments, agency info, grid squares, first activation, and your personal QSO stats
- Two sidebar tabs: Parks list + Chronological Timeline
- Marker clustering + 3 professional basemaps (Topographic is default – cartographers love it!)
- Responsive, modern dark theme with smooth animations
- Zero dependencies other than Leaflet (CDN-loaded)
- Single HTML file – easy to embed anywhere

## Quick Start (for non-technical users – step-by-step)

1. **Download the file**  
   Go to the GitHub repository → click the green **Code** button → **Download ZIP**.  
   Extract it and find the file named `index.html`.

2. **Customize it for YOUR callsign** (takes 30 seconds)  
   Open `index.html` in any text editor (Notepad on Windows, or my online text editor https://edodev.github.io/AdaptPad/).  
   Scroll to the top where you see this block:

   ```js
   const CONFIG = {
       myCallsign: "KD0WAN",        // ← CHANGE THIS LINE
       ...
       parks: [ ... your parks ... ]
   };

   Change "KD0WAN" to your callsign.
Replace or add your own parks in the parks array (copy the format exactly – reference, name, latitude, longitude).


3. **Test it locally**
Double-click the index.html file. It should open in your web browser and show the map.
4. **Embed on QRZ.com (or any website)**
- Copy the entire contents of index.html.
- Log into QRZ.com → Edit your page → paste the HTML into a custom HTML widget or page section.
- Save. Your beautiful map is now live on your QRZ profile!

***Troubleshooting Common Issues***
"Live POTA API unavailable" message in the modal
This is normal and usually temporary. The POTA API is public but sometimes experiences short downtime or blocks direct browser requests (CORS).

The map still works perfectly.
Click the link inside the modal to go straight to the official POTA park page.
For full live data when testing locally, you can use a free CORS-unblocker browser extension (search "CORS Unblock" in Chrome Web Store).

Map looks blank or pins are missing
Make sure you have internet (the map tiles load from the internet).
Exploring More POTA API Endpoints (for advanced users)
This map already uses two powerful endpoints:

https://api.pota.app/park/{REF} → full park metadata
https://api.pota.app/park/activations/{REF}?count=20 → recent activation log

Other useful public endpoints you can add yourself:

https://api.pota.app/spot/ → Live activator spots (great for a "current activity" overlay)
https://api.pota.app/program/parks/US → All US parks (very large – use carefully)
Add a toggleable live-spots layer in future versions!

How to Publish Your Own Version on GitHub (so others can use it)

Create a new GitHub repository (name it something like pota-my-activations-map).
Upload the index.html file.
Create a new file called README.md and paste the entire README you are reading right now (you can edit the title and description).
Enable GitHub Pages in Settings → Pages → choose the main branch.
Your map will be live at: https://YOURUSERNAME.github.io/pota-my-activations-map/

Others can now fork your repo, change the callsign and parks list, and have their own map in seconds.
Credits & License

Built with ❤️ by Grok for KD0WAN and the POTA community
Leaflet.js + MarkerCluster for the map
Data courtesy of the public POTA API (api.pota.app)
Open source – feel free to fork, improve, and share!

Questions? Open an issue on GitHub or find me on the POTA Slack / Facebook groups.
73 de your friendly neighborhood cartographer-activator!
