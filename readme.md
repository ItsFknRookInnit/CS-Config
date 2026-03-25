# Cybers Structures Pro Configurator

A high-performance, live-syncing web utility designed for ARK: Survival Ascended server administrators. This tool simplifies the management of the **Cybers Structures** mod configuration by providing a professional-grade interface to generate `GameUserSettings.ini` deltas.

## 🚀 Live Data Sync
Unlike static configuration tools, this app uses a **Live Sync Engine**. It fetches real-time data directly from the [Official Cybers Structures Configuration Spreadsheet](https://docs.google.com/spreadsheets/d/1-gRdLIO918EoxvcQvJBLWmbY8_BbfjFsuKS3whcMDbs/). 

When the mod creator adds new structures or changes default values, this app updates automatically without requiring a code redeploy.

## ✨ Key Features
* **Pro Tier UI**: A dark-mode, streamlined interface optimized for desktop management.
* **Intelligent Parsing**: Automatically categorizes over 100+ structures (from Air Conditioners to Vivariums) into organized, searchable sections.
* **Pinned Global Settings**: The `GLOBAL` configuration block is pinned to the top for immediate access, with all other categories sorted alphabetically.
* **Delta Generation**: The output only shows values you have changed, keeping your `.ini` files clean and preventing unnecessary overrides.
* **Real-time Tooltips**: Hover over any setting name to see the official description and constraints (Min/Max/Usage) pulled directly from the mod documentation.
* **Validation Logic**: Includes automatic type detection for Booleans (toggles), Numbers (sliders/inputs), and Strings (text fields).

---

## 📖 How-To Guide

### 1. Loading the Configurator
Simply open the `index.html` file in any modern web browser. The app will immediately display a loading spinner while it fetches the latest parameters from the Master Spreadsheet.

### 2. Finding Settings
* **Browse**: Use the category headers to find specific structures. Click a header to expand or collapse that section.
* **Search**: Use the search bar at the top right to filter by key name (e.g., typing "Range" will show all distance-related settings across all structures).
* **Bulk Actions**: Use "Expand All" to see everything at once or "Collapse All" to tidy up your view.

### 3. Adjusting Values
* **Toggles**: Click the switch for true/false settings.
* **Sliders**: Move the slider for quick adjustments. The app automatically calculates a "Pro" range based on the default value.
* **Precise Input**: For exact numbers, type directly into the numerical input box next to the slider.

### 4. Deploying to Your Server
1.  Look at the **Final INI (Changes Only)** panel on the right.
2.  Once you are satisfied with your changes, click **Copy Output**.
3.  Access your server files (via FTP or your Game Panel like Nitrado/G-Portal).
4.  Open `GameUserSettings.ini`.
5.  Find the `[CybersStructures]` header. If it doesn't exist, create it at the bottom of the file.
6.  Paste your copied code block directly under that header.
7.  Save the file and restart your server.

---

## 🛠 Technical Details
* **Framework**: Tailwind CSS (via CDN)
* **Data Source**: Google Visualization API (JSONP)
* **Deployment**: This is a single-file application. No server-side processing is required; it runs entirely in the client's browser.

## ⚖ License
This tool is provided for use with the Cybers Structures mod. ARK: Survival Ascended is a trademark of Studio Wildcard.