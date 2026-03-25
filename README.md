# Cybers Structures Pro Configurator

A high performance, live syncing web utility designed for ARK: Survival Ascended server administrators. This tool simplifies the management of the Cybers Structures mod configuration by providing a professional grade interface to import, edit, and generate `GameUserSettings.ini` deltas.

---

## 🚀 Live Data Sync

Unlike static configuration tools, this application uses a **Live Sync Engine**. It fetches real time data directly from the **Official Cybers Structures Configuration Spreadsheet**.

When the mod creator adds new structures or changes default values, this application updates automatically without requiring a code redeploy.

---

## ✨ Key Features

| Feature | Description |
|---|---|
| **Smart INI Import** | Upload your existing server configuration file. The application will instantly parse your file, locate your custom settings, and update the visual interface to match your server state. |
| **Pro Tier UI** | A dark mode, streamlined interface optimised for both desktop management and mobile devices. |
| **Intelligent Parsing** | Automatically categorises over 100 structures into organised, searchable sections. All categories load collapsed by default to keep your workspace clean. |
| **Delta Generation** | The output only shows values you have explicitly changed. This keeps your server files clean and prevents unnecessary overrides. |
| **Instant Reset** | A dedicated button to clear your workspace and revert all values to their official defaults. |
| **Live Tooltips** | Hover over any setting name to see the official description and constraints pulled directly from the mod documentation. |

---

## 📖 Usage Guide

### 1. Loading the Configurator

Simply open the `index.html` file in any modern web browser. The app will display a loading spinner while it fetches the latest parameters from the Master Database.

### 2. Importing Existing Settings *(Optional but Recommended)*

1. Click the **Import** button at the top of the screen.
2. Select your current `GameUserSettings.ini` or `.txt` backup file.
3. The tool will process the file locally, find the `[CybersStructures]` block, and apply your custom settings to the visual sliders and toggles.

> A notification toast will confirm how many settings were successfully matched.

### 3. Finding and Adjusting Settings

- **Browse** — Use the category headers to find specific structures. Click a header to expand or collapse that section.
- **Search** — Use the search bar at the top right to filter by key name.
- **Adjust:**
  - Click the switch for boolean toggles (`true` or `false`).
  - Move the slider for quick adjustments on numeric values.
  - Type directly into the input box for precise numerical control or string values.

### 4. Deploying to Your Server

1. Look at the **Live INI Delta** panel.
2. Once you are satisfied with your changes, click **Copy INI**.
3. Access your server files via FTP or your web host game panel.
4. Open `GameUserSettings.ini`.
5. Find the `[CybersStructures]` header. If it does not exist, create it at the bottom of the file.
6. Paste your copied code block directly under that header, replacing any old values.
7. Save the file and restart your server.

---

## 🛠 Technical Details

| Property | Detail |
|---|---|
| **Framework** | Tailwind CSS via CDN |
| **Data Source** | Google Visualization API JSONP |
| **Security** | INI import uses the browser-native `FileReader` API. Configuration files are processed entirely on your local machine and are never uploaded to any external server. |
| **Deployment** | Single file application — no backend processing required. |

---

## ⚖ License

This tool is provided for use with the Cybers Structures mod. ARK: Survival Ascended is a trademark of Studio Wildcard.
