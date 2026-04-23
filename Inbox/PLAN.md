  # Responsive Mobile Pass for iFolder

  ## Summary

  Make the existing single-file app responsive down to 280px wide without changing the desktop interaction model or
  breaking the core editor flow. Keep the current stacked mobile layout, but reduce density on narrow screens and
  introduce mobile-only collapse behavior for the two heaviest editor sections: Overlay and Symbols.

  ## Implementation Changes

  - Preserve the current desktop/tablet behavior above 720px.
  - Keep the current stacked layout below 1000px, but refine phone behavior at three tiers:
      - <= 720px: enable phone layout rules and mobile-only collapsible cards for Overlay and Symbols.
      - <= 420px: switch dense action rows to one-column layout, reduce page/card padding, tighten title spacing, and
        simplify control density.
      - <= 320px: apply ultra-compact rules so the UI still fits cleanly at 280px without horizontal overflow.
  - Rework mobile layout density in index.html CSS:
      - Reduce masthead padding/gap and make the title size fluid with clamp(...).
      - Tighten .app, .card, .upload-zone, .text-input, .symbol-search, and slider spacing for phone widths.
      - Convert .export-row and .project-row from side-by-side flex rows to stacked rows on <= 420px.
      - Stack the Browser Slot label/select vertically on <= 420px.
      - Keep the 3 small slot buttons in one row until <= 320px, then stack them vertically.
      - Let .toggle-cluster in the File Color card wrap or compress on ultra-narrow screens so the toggle never crowds
        the title.
      - Keep color cards stacked on phones and allow .color-tools to wrap if needed at the smallest widths.
  - Make Overlay and Symbols collapsible on phones only:
      - Add title-row toggle buttons with chevrons, aria-expanded, and aria-controls.
      - Wrap each card body in a dedicated collapsible content container.
      - On widths <= 720px, default Symbols to collapsed.
      - On widths <= 720px, default Overlay to collapsed, but auto-expand it whenever an overlay exists or is created
        so adjustment controls remain discoverable.
      - On widths > 720px, force both sections expanded and hide the collapse affordance.
  - Improve the Symbols card specifically for phone widths:
      - Change the category chips from a tall wrapping block into a horizontal scrollable chip row on <= 720px.
      - Keep the symbol grid below it; preserve search, active-state styling, and current symbol-selection behavior.
      - Retain the existing max-height cap for the grid on mobile so it does not dominate the page.
  - Keep the existing editor behavior intact:
      - No change to export logic, project persistence, autosave, overlay math, or color picker functionality.
      - No change to card ordering: preview/import/export/project stays first; color/text stays immediately visible;
        advanced tools become collapsible only on phones.

  ## Interfaces / Behavior Changes

  - No public API changes.
  - Add two mobile-only UI state controls in index.html:
      - Overlay section toggle
      - Symbols section toggle
  - Add JS state for mobile collapse mode, driven by matchMedia('(max-width: 720px)').
  - Add accessibility semantics for the new collapsible controls:
      - button
      - aria-expanded
      - aria-controls

  ## Test Plan

  - Verify at widths 280, 320, 360, 390, 768, and 1024.
  - Confirm phone widths show Overlay and Symbols collapsed by default, except Overlay auto-expands when an overlay
      - change folder/file colors
      - enter text
      - open Symbols and apply a symbol
      - adjust overlay controls
      - export PNG/SVG
      - save/load/reset project
  - Confirm tap targets remain usable and action labels no longer wrap awkwardly in export/project rows on narrow
    screens.
  - Confirm accordion controls are keyboard accessible and update aria-expanded correctly.
  - Re-run a browser pass with screenshots at 320px and 280px to verify the compact layout visually.

  ## Assumptions and Defaults

  - Keep the existing single-file architecture; all changes stay in index.html.
  - “Without breaking the main function” means preserving the current editor/export workflow and avoiding desktop
    regressions.
  - Mobile collapse applies only to Overlay and Symbols; Folder Color, File Color, and Text remain immediately
    visible.
  - The minimum supported narrow-phone target for this pass is 280px.