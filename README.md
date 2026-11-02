# Snowboy Hockey

A retro 5v5 arcade ice hockey game that runs entirely in your browser. No install, no build step, no server code: it is one `index.html` file.

**Play:** `https://YOUR-USERNAME.github.io/snowboy-hockey/` (after you finish the steps below)

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
