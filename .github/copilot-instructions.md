# Copilot / Developer Instructions

This file summarizes the repository's HTML structure, CSS hooks, and common tasks to help future contributors (or Copilot-style agents) modify the site safely.

## High-level structure
- `index.html` — Landing / "Thank you" page. Contains the primary hero, features grid, and a link to the "How to Use" page.
- `howto.html` — Usage instructions for players/DMs. Includes detailed steps for using the Pants of Ascension, with styled emphasis on key actions.
- `customize.html` — Tailoring, rune, and customization notes. Features four aesthetic options, each with placeholder images and unique cantrip chants.
- `assets/styles.css` — Central stylesheet. Contains:
  - Corporate + fantasy theming.
  - Hero full-bleed helpers.
  - Title/tab bar styles.
  - Button styles.
  - Enhanced `strong` text styling for emphasis.
  - Spacing adjustments for list items.
  - Dark mode support.
- `assets/logo.svg` — Small SVG logo used in the header.
- `.nojekyll` — Prevent Jekyll processing on GitHub Pages.

## Recent Changes
1. **Removed Lore Page**:
   - The `lore.html` file has been removed as per user request.
   - References to the "Lore & FAQ" tab have been removed from all navigation bars.

2. **Footer Updates**:
   - Standardized copyright text across all pages: `© Ascension Industries — Getting Right Up There since lore began.`

3. **Customize Page Enhancements**:
   - Grouped aesthetic options into uniform panels with placeholder images.
   - Added unique cantrip chants for each customization option.

4. **How to Use Page Improvements**:
   - Added detailed instructions for using the Pants of Ascension.
   - Styled `strong` text for better emphasis.
   - Added spacing between list items for improved readability.

5. **CSS Enhancements**:
   - Improved the active tab styling for better contrast and readability.
   - Removed underline from `strong` text to avoid confusion with hyperlinks.
   - Increased font size for `strong` text to make it more noticeable.
   - Added spacing between list items.

## Notes for Future Developers
- Placeholder images are used in `customize.html` for aesthetic options. Replace these with actual images when available.
- The dark mode toggle is implemented across all pages. Ensure any new styles are compatible with both light and dark modes.
- The `lore.html` file is currently a placeholder indicating its removal. If reintroduced, update navigation bars accordingly.
