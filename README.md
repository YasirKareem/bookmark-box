# Bookmark Box

A Firefox bookmark manager with preview thumbnails, smart search, folder organization, and bulk maintenance tools.

> Firefox-only &nbsp;·&nbsp; Manifest V3 &nbsp;·&nbsp; All data stays on your device &nbsp;·&nbsp; No server, no tracking

---

## Screenshots

Screenshots will be added when the extension is published.
See [`screenshots/`](screenshots/) for the list of planned images.

---

## What it does

Bookmark Box replaces the default Firefox bookmark workflow with a full-featured library manager. You can save the current page, add tags and notes, capture a thumbnail, search across your entire library, scan for broken links, and export a backup — all without leaving Firefox, and without any data leaving your device.

---

## Features

**Saving and organizing**
- Save the current page with one click from the toolbar or sidebar
- Assign a folder, tags, and a note at save time
- Access your full library in a sidebar or a dedicated full-page view

**Preview thumbnails**
- Capture a screenshot of any saved page
- Bulk capture queue with progress tracking, pause, and resume
- Thumbnails stored in your browser (IndexedDB) — never uploaded

**Search and filter**
- Fast search across titles, URLs, tags, and notes
- Advanced filters: folder, tag, date range, capture status
- Sort by title, date added, or folder

**Folder and tag management**
- Create, rename, and delete folders
- Assign multiple tags to any bookmark
- Detect and merge duplicate URLs

**Maintenance tools**
- Broken-link scanner: identify dead or redirecting bookmarks
- Duplicate detector: find and clean up repeated URLs
- Empty-folder cleanup
- Trash with capacity display and one-click restore

**Import and export**
- Export your full library as a JSON backup file
- Re-import from backup with folder placement confirmation
- Merge imports without overwriting existing bookmarks

**Insights**
- Library statistics: total bookmarks, folders, tags
- Preview capture coverage
- Broken-link count summary

---

## Installation

**Once published on Firefox Add-ons (AMO):**

Installation will be available through [Firefox Add-ons](https://addons.mozilla.org). A direct link will be added here when the listing goes live.

**Manual installation (for testing):**

1. Download or clone this repository
2. Open Firefox and go to `about:debugging#/runtime/this-firefox`
3. Click **Load Temporary Add-on**
4. Select `manifest.json` from the project folder

> Temporary add-ons are removed when Firefox restarts. Use the AMO version for persistent installation.

---

## Permissions

Bookmark Box requests the minimum permissions needed to work.

| Permission | Why it is needed |
|---|---|
| `bookmarks` | Read and write your Firefox bookmarks |
| `storage` | Save app state, tags, settings, and thumbnail metadata locally on your device |
| `tabs` | Read the active tab URL and title when saving a page; required for screenshot capture |
| `clipboardWrite` | Copy a bookmark URL when you click the Copy button |
| `downloads` | Save your exported backup file to your Downloads folder |

**Optional permissions — not granted at install:**

| Permission | When it is requested |
|---|---|
| `<all_urls>` | Requested only if you use Preview Capture or Broken-Link Check. Firefox will prompt you separately before granting it. |
| `nativeMessaging` | Not used in the standard release. Listed as optional for a possible future companion component. Has no effect unless a native application is separately installed. |

For the full explanation see [PRIVACY.md](PRIVACY.md).

---

## Privacy

No data is sent to any server. No analytics. No tracking. No crash reporting.

All bookmarks, thumbnails, tags, and settings are stored on your device only. Data is never uploaded or shared without your explicit action.

See [PRIVACY.md](PRIVACY.md) for the complete statement.

---

## Support

For bug reports or questions, open an issue in this repository.

See [SUPPORT.md](SUPPORT.md) for what to include in a bug report.

---

## Requirements

- Firefox 140.0 or later
- Firefox for Android 142.0 or later

---

## License

MIT &nbsp;·&nbsp; © 2025 Yasir Kareem
