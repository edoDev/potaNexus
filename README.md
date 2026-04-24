# potaNexus

**A beautiful, dynamic, single-file interactive map for your POTA activations**

potaNexus displays **all the parks you have activated** in the Parks on the Air (POTA) program with professional cartographic styling, live POTA data, rich park details, and activation statistics.

Perfect for embedding on your **QRZ.com** page, personal website, or sharing with fellow hams. Originally built for KD0WAN (a professional cartographer).

---

## ✨ Key Features

- Single HTML file — no server or installation needed

- Live POTA API integration (park metadata, activation logs, and dynamic stats)

- Rich modal with park details, grid squares, agency info, first activation, and your personal QSO counts

- Two sidebar tabs: Parks list + Chronological Timeline

- Smart marker clustering + 3 high-quality basemaps (Topographic default)

- Modern dark theme with smooth animations

- Fully customizable for any activator

- Mobile-friendly and QRZ-ready

---

## Quick Start (Step-by-Step)

### 1. Download the Project

- Go to this GitHub repository.

- Click the green **Code** button → **Download ZIP**.

- Extract the file. You will find `index.html` inside.

### 2. Customize for Your Callsign (Takes ~1 Minute)

1. Open `index.html` in any text editor:

   - Windows: Right-click → **Open with Notepad**

   - Mac: Open with **TextEdit**

   - Recommended easy online editor: [AdaptPad](https://edodev.github.io/AdaptPad/)

2. Scroll near the top to find the `CONFIG` section.

3. Update these two parts:

```js

const CONFIG = {

    myCallsign: "YOURCALLSIGN",        // ← CHANGE THIS

    ...

    parks: [

        // Add or replace with your parks here

        { ref: "US-1751", name: "Castlewood State Park", lat: 38.5487, lng: -90.545 },

        // Add more parks following the same format

    ]

};

Important:

Keep the exact format for each park: ref, name, lat, lng.
Use decimal coordinates (you can find them on pota.app or Google Maps).
3. Test the Map Locally
Double-click the index.html file.
It should open in your web browser and display your map.
Click any park pin or list item to open the detailed modal.
4. Embed on QRZ.com (or any website)
Open index.html and copy all the content (Ctrl+A then Ctrl+C).
Log into QRZ.com → Edit your page.
Paste the code into a custom HTML section/widget.
Save. Your interactive map is now live on your QRZ profile!
Troubleshooting
"Live POTA API unavailable" appears in the modal This is common and usually temporary. The public POTA API sometimes has short outages or CORS restrictions in browsers.

The map and pins still work fine.
Use the links inside the modal to visit the official POTA park page.
Tip: While testing locally, install the free "CORS Unblock" browser extension (Chrome/Firefox) to enable live data.
Map is blank or pins are missing Make sure you have an active internet connection (map tiles load from the internet).

Need help adding parks? Open an Issue on this GitHub repo or ask in the POTA Facebook group / Slack.

Exploring the POTA API (Advanced)
potaNexus currently uses:

https://api.pota.app/park/{REF} — Full park metadata
https://api.pota.app/park/activations/{REF}?count=20 — Recent activations
Other useful endpoints:

https://api.pota.app/spot/ — Live activator spots
https://api.pota.app/program/parks/US — All US parks
Publishing Your Version on GitHub
Create a new repository (recommended name: potaNexus).
Upload index.html.
Create a file named README.md and paste this content (edit as needed).
Go to Settings → Pages → select main branch → Save.
Your map will be live at: https://YOURUSERNAME.github.io/potaNexus/
Credits & License
Built with ❤️ by Grok for KD0WAN and the POTA community.
Powered by Leaflet.js + MarkerCluster.
Data from the public POTA API.
Open Source — Fork, modify, and share freely!
73 de your friendly neighborhood cartographer-activator!

Questions or suggestions? Open an Issue on GitHub or reach out in the POTA community.

Happy activating and mapping!
