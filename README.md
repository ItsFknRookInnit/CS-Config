# Cybers Structures Pro Terminal v1.5

A high-performance live-syncing web utility designed for ARK Survival Ascended server administrators. This suite provides a professional-grade interface to import, audit, and generate configuration overrides for the **Cybers Structures** mod ecosystem.

## 🛠 Pro-Tier Standardization

This application follows the **Standardized Pro Terminal** architecture. It prioritizes data integrity and workspace efficiency by isolating technical logs from the primary configuration delta and providing adaptive environmental themes (Tactical Dark and Cyan Light).

## 🚀 Live Data Sync

Unlike static configuration tools, this application uses a live-sync engine. It fetches real-time data directly from the official Cybers Structures master spreadsheet via a secure uplink. 

When the mod creator adds new structures or adjusts default parameters, this terminal updates automatically without requiring a manual update or code redeploy.

## ✨ Key Features

* **Standardized HUD Interface**: Features the signature Pro-Terminal layout with a high-contrast "Tactical Dark" mode and a high-visibility "Cyan Light" mode (#95cfc2).
* **Adaptive Theme Engine**: Features a persistent theme toggle allowing administrators to switch between low-light tactical operations and high-visibility data auditing.
* **Intelligent Header Detection**: Scans the master spreadsheet to identify category headers. As the mod expands, the terminal automatically maps and organizes new structures into searchable sections.
* **Secure Configuration Import**: Upload existing server files locally. The terminal parses the data on your machine to match your current server state to the visual sliders and toggles without external data transmission.
* **Smart Delta Generation**: The **INI Delta** panel generates code only for parameters explicitly changed from their default state, ensuring your server files remain clean and optimized.
* **Terminal Status Monitor**: A dedicated status log in the top-right quadrant provides real-time feedback on connection strength, decryption status, and input validation.
* **Dynamic Tooltips**: Hover over any parameter to view official descriptions and constraints pulled directly from the mod’s technical documentation.

## 📖 Usage Guide

### 1. Initializing the Terminal
Launch the `index.html` file in a modern browser. The system will display a decryption loader while establishing a handshake with the master database.

### 2. Importing Existing Settings
1. Click the **IMPORT** button in the header.
2. Select your current configuration backup (INI or TXT).
3. The terminal will sync the visual state with your file. A notification toast will confirm the number of nodes successfully mapped.

### 3. Modifying Parameters
* **Search**: Use the **SEARCH PARAMETERS** HUD to filter the list by key name.
* **Adjust**: Use square toggles for booleans, range sliders for quick adjustments, or numerical inputs for precise calibration.
* **View Management**: Use **EXPAND ALL** to reveal the full map or **COLLAPSE ALL** to focus on specific categories.

### 4. Deploying to Server
1. Monitor the **INI DELTA** panel for real-time code generation.
2. Click **COPY OUTPUT** once adjustments are complete.
3. Paste the generated block into your server's `GameUserSettings.ini` under the `[CybersStructures]` header.

## 📋 Changelog

### v1.5 (Current)
* **UI Standardization**: Relocated the Terminal Log to the top-right quadrant to prioritize the INI Output workspace.
* **Dual-Theme Engine**: Implemented the standardized "Cyan Light" and "Tactical Dark" themes.
* **Protocol Hardening**: Refined state update logic to explicitly prevent UI control IDs from interfering with INI generation.
* **Data Layer Isolation**: Improved input filtering to ensure search terms do not inject into the final configuration string.
* **Logic Fix**: Resolved "Ghost Field" duplication caused by header name conflicts in the master spreadsheet.

### v1.4
* **Graphical Overhaul**: Integrated the Tactical HUD theme with cyan energy accents and hexagonal backdrops.
* **Typography**: Transitioned to Roboto Condensed and Teko for improved technical readability.
* **Component Update**: Swapped rounded UI elements for rigid block controls and custom square checkboxes.

### v1.3
* Introduced dynamic header detection and automatic sorting to keep global configurations prioritized.
* Enhanced search engine to automatically expand relevant categories upon match detection.

### v1.2
* Launched the local file import engine and delta generation system.
* Integrated notification toasts for real-time user feedback.

### v1.1
* Migrated from static arrays to a live fetch engine using the Google Visualization API.

## ⚖ License & Credits

This tool is a community utility for the Cybers Structures mod. 
ARK Survival Ascended is a trademark of Studio Wildcard.
