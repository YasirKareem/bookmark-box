# Changelog

## 1.0.5

### Improved preview image sourcing
Bookmark Box now prefers the page's own representative image when saving or re-capturing a bookmark preview. It tries, in order: Open Graph image (`og:image`), Twitter card image, JSON-LD schema image, and a hero image heuristic (large content images inside article/main/content containers). The viewport screenshot fallback is used only when none of these are available, or when the image cannot be fetched.

### Broken Links panel improvements
- Added per-row **Retry**, **Dismiss**, and **Delete** actions on failed link checks.
- Added **Retry all failed** button to recheck all timed-out or blocked bookmarks in a single scan.
- Error rows now show human-readable labels (Timed out, Network error, Certificate error, Request blocked, etc.) with the raw error message available on hover.
- Added select-all / deselect-all toggles for both broken and error sections.
- Added bulk **Delete** for selected broken links and bulk **Delete** for selected failed-check bookmarks.
- Broken link and failed-check sections now have separate selection sets and bulk bars.

### Re-capture improvement
Re-capturing a bookmark's preview also uses the metadata image pipeline before falling back to a screenshot, consistent with the Save Current Page path.

---

## 1.0.4

Initial public release under the Bookmark Box name.

- Preview thumbnail capture and storage
- Smart search, filters, and advanced search
- Folder tree navigation with expand/collapse
- Duplicate and similar-URL grouping
- Broken link scanning
- Tag management
- Trash with restore
- Import/export (JSON, HTML, ZIP)
- Insights panel
- Saved searches
- Smart Collections
- Native desktop bridge (optional)
