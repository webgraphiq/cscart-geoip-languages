# GeoIP Languages for CS-Cart

**🛑 PREMIUM ADD-ON: This repository does not contain the open-source code. It serves as the official listing and documentation page for the WebGraphiq premium add-on.**

**GeoIP Languages** (Automated Local Language Suite) is a geolocation language add-on for CS-Cart and Multi-Vendor. It detects the visitor’s country from IP and switches the storefront to a mapped local language on the first visit, so copy matches the market without a manual language pick.

## [🛒 Buy & View Live Demo](https://www.webgraphiq.com/geo-ip-languages.html)

One-time license. The current price and the live demo are on the product page.

## Why store owners use it

- Show local language from the first page view — less bounce from “wrong language” friction.
- Map each installed CS-Cart language to one or more ISO country codes (for example `AT,BE,CY` for German).
- Uses the MaxMind GeoIP data CS-Cart already relies on (`fn_get_country_by_ip`).
- Unmapped or unknown countries keep the shop default / browser language.
- An explicit `sl=` in the URL, and a later manual language choice stored in the cookie, still win.
- Googlebot and empty user agents are skipped.
- No CS-Cart core file edits.

## How it works

1. The add-on reads the visitor IP and resolves the country.
2. If the request has no `sl` and no stored `cart_language` cookie, and the browser language differs from the mapped language, it switches the storefront language.
3. When the display language changes, description language follows (unless `descr_sl` is already set).
4. Otherwise CS-Cart keeps the browser or default language (fallback).
5. Clearing browser cookies is needed if you want a fresh geo-detect after testing.

## What you control

- License key on the add-on settings screen.
- **Associated country code** on Administration → Languages — comma-separated ISO codes; spaces are stripped and codes stored uppercase.
- First install can seed English (`US,GB,CA,AU`), German (`DE`), and Italian (`IT`) when those languages exist.
- Optional test IP via the installation guide (`wgip`) for storefront checks.

## Requirements

- CS-Cart or Multi-Vendor **4.12.1** or newer, including **4.21**
- PHP **8.3** or a current 8.x release used by that shop
- Installed language packs with country codes filled in for the markets you sell to

## This repository

<p align="center">
  <a href="https://www.webgraphiq.com/geo-ip-languages.html">
    <img alt="Buy and view the live demo" src="https://img.shields.io/badge/CS--Cart-Buy%20%26%20View%20Live%20Demo-28a745?style=for-the-badge&labelColor=1A365D">
  </a>
</p>

<p align="center"><strong>One-time license · local language by visitor country</strong></p>

This is the public product listing. The add-on package, license checks, and source files are not published here. After purchase, the package is readable PHP under the WebGraphiq commercial license, installed from your WebGraphiq account.

Support: [webgraphiq.com](https://www.webgraphiq.com) · webgraphiq@gmail.com

© WebGraphiq. All rights reserved. [License](https://www.webgraphiq.com/license.html)

## Other Premium CS-Cart Add-ons by WebGraphiq

More CS-Cart and Multi-Vendor add-ons are listed on the [WebGraphiq GitHub profile](https://github.com/webgraphiq).
