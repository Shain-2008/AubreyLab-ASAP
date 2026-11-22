# AubreyLab ASAP

A fast, browser-based **ASAP / Early View** journal feed aggregator for chemistry researchers. Built as a self-contained single-file web app (`index.html`) powered by the live [Crossref](https://www.crossref.org/) API.

## Key Features

- **Journal Tabs & Quick Search:** Switch between major chemistry journals across **ACS**, **Wiley**, **Nature**, and **RSC**, filter tabs quickly, or jump straight to a journal by name or ISSN.
- **Permanent Custom ISSN Tabs & ISSN Directory:** Add any journal permanently by its 8-digit ISSN (with an optional custom tab label), uncheck journals to hide them (moving unchecked items to the bottom of the manager list), or browse the built-in ISSN lookup directory.
- **Time-Window & Date Filtering:** View the latest ASAP/early-view items or look back by **1 Week Ago**, **1 Month Ago**, **1 Year Ago**, or a specific calendar date.
- **Instant Filtering & View Modes:** Search by title, author, keyword, or DOI, toggle Table of Contents (TOI) graphics when available, and switch between **Cards** and **Compact** views.
- **Reading List & Citation Export:** Bookmark papers to a local reading list and copy or export citations in **BibTeX (`.bib`)** or **RIS (`.ris`)** format.

## How It Works

- **Live Data:** Article metadata is fetched directly from the Crossref API in the user's browser—no backend server or database required.
- **Local Browser Storage:** Tab customizations, custom ISSNs, view preferences, and saved reading list items are stored locally in each visitor's browser (`localStorage`).
- **Publisher Access:** Clicking **Read** or an official ASAP portal link opens the publisher's site, where institutional logins or lab VPN access apply as usual.

## Troubleshooting & Rate Limits (`429`)

- **Temporary Rate Limits or Delays (`429` / Network Errors):** Because **AubreyLab ASAP** queries Crossref directly from the browser across multiple journals, Crossref may occasionally rate-limit (`HTTP 429`) or delay one or more journal feeds during busy bursts.
- **Refresh to Retry:** If a journal feed appears incomplete, delayed, or shows a warning/notice, wait a moment and click the **Refresh** button in the header (or refresh your browser page) to re-fetch the latest articles.