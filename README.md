# Steam Store Linker (Humble & Fanatical)

A Tampermonkey Userscript that enhances **Humble Bundle** and **Fanatical** store pages by adding Steam store links, ownership status, wishlist indicators, bundle statistics, and other useful game info.

## Features

- **Multi-Site Support**: Works on Humble Bundle and Fanatical.
- **Steam Integration**: Adds a direct link to the Steam store page for games found in bundles.
- **Visual Status Icons**:
    - **Owned**: Games you own are marked with a green checkmark check and grayed out.
    - **Wishlist**: Games on your wishlist are marked with a blue heart and highlighted.
    - **Ignored**: Games you have ignored on Steam are marked with a red cross.
- **Advanced Info**:
    - **Steam Deck / ProtonDB**: Shows a colored circle indicating Linux/Deck compatibility (Platinum, Gold, Silver, Bronze, Borked) via ProtonDB.
    - **Trading Cards**: Displays a blue card icon if the game drops Steam Trading Cards.
    - **Content Type**: Distinguishes between base games, **DLCs** (yellow icon), and **Soundtracks** (note icon).
    - **Steam User Rating**: Displays the percentage of positive user reviews from Steam.
- **Stats Panel**: A floating panel shows a summary of the current page (Total, Owned, Missing, etc.).
- **Smart Tooltips**: Hover over the Steam icon to see the game's **Cover Art** and full title.

## Installation

1. Install [Tampermonkey](https://www.tampermonkey.net/) extension for your browser.
2. [Click this link to install the script](https://raw.githubusercontent.com/gbzret4d/steam-store-linker/main/steam_store_linker.user.js).
3. Confirm the installation in Tampermonkey.

## Updates
The script will automatically check for updates via Tampermonkey.
You can also manually update by clicking the installation link again or checking for updates in the Tampermonkey dashboard.

## Usage

1.  **Login**: Make sure you are logged into [Steam](https://store.steampowered.com/) in the same browser context.
2.  **Visit**: Go to any supported store page:
    - [Humble Bundle](https://www.humblebundle.com/)
    - [Fanatical](https://www.fanatical.com/)
3.  **Permissions**: The script will ask for permission to access:
    - `store.steampowered.com` (for ownership/search)
    - `www.protondb.com` (for Steam Deck status)
    - **Allow these** to enable full functionality.
4.  **Enjoy**: The stats panel will appear, and game cards will be enriched with Steam data.

## How it works

- **Site Adapters**: Uses modular adapters to find game titles on different websites.
- **Data Sources**:
    - **Steam UserData**: Fetches your owned/wishlisted games from Steam's dynamic store API.
    - **Steam Search**: Finds the correct Steam App ID by game name.
    - **Steam AppDetails**: Fetches secondary info like Trading Cards and DLC type.
    - **ProtonDB API**: Fetches the current Linux/Deck compatibility tier.
- **Caching**: Results are cached in Tampermonkey storage to respect API rate limits and speed up subsequent page loads.

## Author

**gbzret4d**

## Disclaimer

This script is not affiliated with Humble Bundle, Fanatical, Valve, or ProtonDB. Use at your own risk.
