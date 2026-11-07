# Snowboy Hockey

A retro 5v5 arcade ice hockey game that runs entirely in your browser. No install, no build step, no server code: it is one `index.html` file.

**Play:** `https://YOUR-USERNAME.github.io/snowboy-hockey/` (after you finish the steps below)

## Animation upgrade (November 2026)
- Dynamic skate weight shifts and stride bobbing, including regular, small and big skaters.
- Articulated stick-grip hands, puck-handling shoulder shifts and moving blades.
- Fight footwork, circling, two synchronized strikes per combo, recoil, dodges and an animated glove layer over sprite artwork.
- All changes run locally in the browser; no installation or external rendering service required.

## Features
- 5v5 arcade hockey with Small, Regular and Big player types, fights, hits, spins and slapshots
- Easy / Normal / Hard difficulty (camera view)
- Line and team editor, hockey cards, Zamboni race betting at intermissions
- Online play with a friend (peer-to-peer, no server needed)
- Jumbotron fan cams and lounge music on the pause screen
- If you walk away, the CPU plays for you until you move the mouse

## Controls
| Key / mouse | Action |
|---|---|
| W A S D / arrows | Skate |
| Left click | Shoot (hold to charge) / body check |
| Right click | Pass / poke check |
| Space | Spin-o-rama |
| E | Switch skater |
| Shift | Block |
| 1-4 | Change lines |
| T | Toggle CPU tactic |
| Z | Cycle difficulty |
| Esc | Pause |
| M | Mute |

## Put it online with GitHub Pages (free, about 2 minutes)
1. Sign in at <https://github.com> and click **New repository**. Name it `snowboy-hockey`, keep it **Public**, and click **Create repository**.
2. Click **uploading an existing file**, drag in **all the files from this folder** (`index.html`, `README.md`, `.nojekyll`, `LICENSE`), and click **Commit changes**.
   - If your computer hides files that start with a dot, `.nojekyll` is optional. The game works without it.
3. Open **Settings > Pages**. Under **Build and deployment**, set **Source** to **Deploy from a branch**, choose branch **main** and folder **/ (root)**, then click **Save**.
4. Wait a minute, then refresh the Pages screen. Your game link appears at the top. Open it on any computer, phone or tablet.

To update the game later, upload a new `index.html` over the old one (**Add file > Upload files**).

## Notes
- The game needs a modern browser (Chrome, Edge, Firefox or Safari). A mouse and keyboard work best.
- Sound starts after your first click, which is a normal browser rule.
- Your settings (difficulty, volume, teams) are saved in your own browser.
- Online play uses the free public PeerJS service. If it is ever down, play offline instead.
- The pixel font loads from Google Fonts. Without internet the game still works with a fallback font.

## Main menu redesign (November 2026)

- Two-column, rink-inspired home screen: prominent match-up and Play Match area with a separate game-modes panel.
- Resized, responsive controls and mobile-friendly vertically stacked layout, without shrinking the entire menu.
- Existing buttons, team editor, online mode, cards, period selector, difficulty selector and keyboard shortcut IDs are preserved.
- Keyboard instructions remain available in a collapsible **How to Play** section.
- Accessibility updates include visible keyboard focus and reduced-motion support.

The gameplay animation enhancements in the prior upgrade are retained. Browser gameplay validation is recommended after deployment.

## Ice, player proportions and skating upgrade (November 7, 2026)

- Rebalanced skater body dimensions and collision radii for more natural proportions compared with the 1560×800 arena.
- Updated ice shading with subtly alternating resurfacer lanes, gentle frosty edge illumination, improved skate scratches and fine crystalline highlights.
- Added real-time skate edge marks underneath moving players.
- Player steering now blends toward the requested direction with quick acceleration, softer coasting, and a limited turn rate, creating more convincing skating without changing key bindings.
- Increased lateral stick movement when carrying the puck.
- Previous main-menu redesign, skating/fight animation upgrade, game modes and controls are preserved.

Validation: JavaScript syntax checked with Node.js. Full interactive gameplay was not validated in a browser in the build environment.
