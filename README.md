# Cybers Structures Pro Terminal v1.6

A high performance live syncing web utility designed for ARK Survival Ascended server administrators. This tool simplifies the management of the Cybers Structures mod configuration by providing a professional grade interface to import, edit, and generate configuration files.

## Live Data Sync

Unlike static configuration tools, this application uses a live sync engine. It fetches real time data directly from the official Cybers Structures configuration spreadsheet. 

When the mod creator adds new structures or changes default values, this application updates automatically without requiring a code redeploy.

## Key Features

*   **Tactical HUD Theme:** Completely overhauled visual style to mirror the native menus of ARK Survival Ascended. Features a custom hexagonal backdrop, cyan energy accents, blocky inputs, and condensed technical typography.
*   **Smart Configuration Import:** Upload your existing server configuration file. The application will instantly parse your file, locate your custom settings, and update the visual interface to match your server state.
*   **Delta Generation:** The output only shows values you have explicitly changed. This keeps your server files clean and prevents unnecessary overrides.
*   **Instant Reset:** A dedicated button to clear your workspace and revert all values to their official defaults.
*   **Live Tooltips:** Hover over any setting name to see the official description and constraints pulled directly from the mod documentation.

---

## Usage Guide

### 1. Loading the Terminal
Simply open the index file in any modern web browser. The app will display a decryption loader while it fetches the latest parameters from the master database. All fields and categories are automatically sorted alphabetically for easy scanning.

### 2. Importing Existing Settings
1. Click the import button at the top of the screen.
2. Select your current configuration backup file.
3. The tool will process the file locally, find the required data block, and apply your custom settings. 

> **Pro Tip:** You can click **SHOW MODIFIED** to instantly filter your view and audit your imported changes.

### 3. Finding and Adjusting Settings
*   **Browse:** Use the category headers to find specific structures. Click a header to expand or collapse that section.
*   **Search:** Use the search bar at the top right to filter by key name.
*   **Adjust:**
    *   Click the square switch for boolean toggles.
    *   Move the slider for quick adjustments on numeric values.
    *   Type directly into the input box for precise numerical control or text strings.

### 4. Deploying to Your Server
1. Look at the **INI Output** panel on the right.
2. Once you are satisfied with your changes, click **COPY**.
3. Access your server files via FTP or your web host game panel.
4. Open your `GameUserSettings.ini` file.
5. Find the `[CybersStructures]` header. If it does not exist, create it at the bottom of the file.
6. Paste your copied code block directly under that header, replacing any old values.
7. Save the file and restart your server.

---

## Technical Details

*   **Framework:** Tailwind CSS via Content Delivery Network.
*   **Data Source:** Google Visualization API JSON output.
*   **Security:** The import feature uses the browser native file reader API. Your configuration files are processed entirely on your local machine and are never uploaded to any external server.
*   **Deployment:** This is a single file application. No backend processing is required.

---

## Changelog

### v1.6 (Current)
*   **Heuristic Boolean Parsing:** Conducted a full bug sweep to identify fields lacking default values like `PropagatorDisableDinoMods`. Implemented a text scanner that reads the official mod descriptions for the words true, false, or toggle and forces the UI to render the correct checkbox control.
*   **Alphabetical Auto Sort:** Reworked the data engine to automatically sort all categories and individual config fields alphabetically. This dramatically improves visual scanning speed.
*   **Audit Mode:** Added the **SHOW MODIFIED** filter button, allowing admins to instantly collapse all untouched configs and review only the fields they have altered.

### v1.5
*   **Data Layer Isolation:** Implemented strict input filtering to prevent terminal search terms from being erroneously injected into the INI generation engine.
*   **Ghost Field Removal:** Eliminated general category duplication and ghost fields caused by header name conflicts in the master spreadsheet.
*   **Protocol Hardening:** Refined the state update logic to explicitly ignore UI control IDs during data synchronization.
*   **Tooltip Stacking Fix:** Migrated tooltips to a fixed position global layer to ensure visibility over isolated panels.

### v1.4
*   Complete Pro Tier graphical overhaul integrating a Tactical HUD theme.
*   Implemented cyan tinted glass panels and subtle hexagonal grid backgrounds.
*   Replaced standard web fonts with Roboto Condensed and Teko to mirror in game text rendering.
*   Swapped rounded inputs for rigid block controls including custom square checkboxes.
*   Updated notification toasts with technical terminology and glowing accents.

### v1.3
*   Introduced dynamic header detection logic.
*   Application now intelligently distinguishes between structure categories and individual configuration parameters directly from spreadsheet data.
*   Enhanced search engine to automatically expand relevant categories when a match is found.

### v1.2
*   Added the file import engine allowing users to upload existing text or configuration files.
*   Implemented local parsing logic to read uploaded files and extract matching values.
*   Created the delta generation system to ensure output only contains modified values.

### v1.1
*   Replaced static data arrays with a live fetch engine connecting to the Google Visualization API.

---

## License

This tool is provided for use with the Cybers Structures modification. ARK Survival Ascended is a trademark of Studio Wildcard.
