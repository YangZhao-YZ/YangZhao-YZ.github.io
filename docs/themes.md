# Site themes

The navigation shows a compact palette icon and “Theme” label. Opening its native
dropdown reveals Northeastern, Illinois, and Cyberpunk. Northeastern remains the
default. Internal keys remain `neu`, `uiuc`, and `cyberpunk`, so existing selections
persist between pages and visits using `hb-theme-pack` in local storage. The control's
tooltip identifies the current theme, and keyboard/screen-reader behavior remains native.

## Cyberpunk website direction

The design follows the official website's alternating acid-yellow and black
sections, condensed headlines, cyan framing, and cracked horizontal separators.
The navigation floats over the page. Its page links, search, and theme picker form a connected group
with complementary notched seams, a clipped lower-left corner on the first item,
and a clipped upper-right corner on the theme picker. The active/hovered control is cyan;
other controls share translucent black fills and the same height. On mobile,
search, theme, and the menu toggle form a joined strip; the expanded menu uses two
joined pairs. The logo retains its individual chip.
Standalone controls use a square upper-left corner, a small rectangular notch
at the center of the left edge, and a clipped lower-right corner. The Download CV
button uses a larger notch and an inset outline, with a cyan hover/focus state.
It sits over a black profile section: a compact portrait, name, and social links
on the left, with the biography and CV button on the right.
Education stays in stacked rows on yellow, news on black, and stacked publication
rows on yellow. Subtle cyan dot grids fade across the black section backgrounds.
On mobile the profile and biography stack within the same section.

Featured publication figures sit on inset white canvases inside dark frames with
cyan corner brackets. The frame separates the white figures from the yellow
section background. Figures retain their original colors and fit without cropping
or hover zoom; the frame moves above the publication text on mobile.

The separator uses a local SVG mask with long flat runs, irregular triangular
notches, small negative-space cuts, and detached barcode-like marks. Its minimum
rendered width preserves these fine details on mobile rather than compressing
the entire pattern. The first edge belongs to the top of the profile section
and scrolls away with that section, independently of the floating navigation.
Black-to-yellow transitions mirror the edge horizontally.

The portrait uses the original photo in full color, with no filters, glitch
layers, scan lines, or hover animation. Its cyan angular frame remains.
Reduced-motion preferences disable animation and transitions.

Education and experience logos sit directly on their cards, inside thin yellow
corner brackets. The Cyberpunk theme recolors the existing logos yellow using SVG
filters; detailed crests and images containing white use an ink treatment that
preserves internal detail and removes white backgrounds. The badges are static.
The school themes retain their original full-color logos and filled circular badges.

### Typography

The official site uses Refinery 25 and Blender Pro. This implementation uses
self-hosted Teko (headlines) and Rajdhani (interface/body text) as open-source
alternatives; these are not the exact commercial typefaces or the game's logo.
Fonts are loaded only when used by the Cyberpunk preset. The WOFF files were
converted from the upstream Google Fonts TTF distribution, retaining all glyphs.
Licenses and source information are in `static/fonts/cyberpunk/`.

### Visual references

- [Official Cyberpunk website](https://www.cyberpunk.net/us/en/)
- [Cyber Kit by Matt Walker](https://www.figma.com/community/file/921630016386632325/cyber-kit): channel displacement, sliced lettering, and fine cyan frames. The navigation button group is a CSS adaptation of its grouped-button design, based on the user-provided close-up, resized for navigation and arranged as two pairs on mobile, under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).
- [Cyberpunk 2077 Concept UI Redesign by Sajid](https://www.figma.com/community/file/1014971564349982506/cyberpunk-2077-concept-ui-redesign-freebie): angular framing and detailed section separators. `static/media/cyberpunk/section-divider.svg` is a hand-drawn adaptation of the separator shown in the user-provided close-up, with adjusted proportions and placement, used under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).

Both Figma community pages list CC BY 4.0. The separator and button-group adaptations
are attributed above; other elements use the templates as visual references. No exported Figma
components or game artwork are bundled in the site.

## Implementation

- `assets/css/custom.css`: school themes and default visibility of alternative content.
- `assets/css/cyberpunk.css`: scoped Cyberpunk styling, fonts, layout, and glitch effects.
- `static/media/cyberpunk/section-divider.svg`: decorative mask shared by the homepage section boundaries and footer.
- `data/themes/cyberpunk.yaml`: Hugo Blox theme registration.
- `layouts/_partials/hooks/head-end/site-theme.html`: picker, persistence, and dark component mode.
- `layouts/_partials/hooks/body-end/cyberpunk-icons.html`: shared monochrome logo filters, used only by Cyberpunk card icons.
- `layouts/_partials/hbx/blocks/site-biography/block.html`: delegates the school profile to the upstream block, and renders the same two-column arrangement with Cyberpunk styling from the same author data.
- `layouts/_partials/views/featured-publication-horizontal.html`: shared publication markup and theme-specific metadata; titles and images link to each publication.

The new homepage block retains `id: section-resume-biography-3`, preserving the
school themes' existing selectors and anchors. All Cyberpunk layout rules are
scoped to `html[data-site-theme="cyberpunk"]`. Fonts are defined globally but
referenced only within that scope.

The default is `hugoblox.theme.school` in `config/_default/params.yaml` (the legacy
key accepts `cyberpunk` too). Saved visitor preferences take priority.

## Preview

Run `pnpm dev` for the Hugo preview. Run `pnpm build` to generate the production
site and Pagefind index. Serve `public/` with a static server to verify search.
Check all presets, refresh/navigation persistence, publication pages, experience
cards, and mobile navigation. GitHub Pages publishes pushes to `main`; development
stays on `dev` until the changes are ready to merge.
