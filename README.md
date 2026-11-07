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

## Goalie distribution and pause broadcast update (November 2026)
- Fixed goalie outlets: release after a save now gives the puck appropriate velocity, a safer starting position, and temporary re-glove protection.
- Prevented the goalie crease AI from applying the same movement twice in a single frame.
- Rebuilt the pause interface with the current score, teams, period and time, accessible controls, and a responsive grid of actions.
- Expanded the animated arena jumbotron with layered crowd spectators and a new section-wide fan cam.
- Retained the professional menu logo, hockey card designs, improved ice, and other gameplay updates.

## Multiplayer playoff tournament (November 2026)

**How to create a playoff with friends**
1. Choose **PLAY ONLINE → HOST A GAME**.
2. Set mode to **Playoff Tournament**, choose **2 players** or **4 players**, enter your player name, and choose your team.
3. Click **GENERATE INVITE CODE** and share the code or invite link with the other entrants.
4. Each guest opens **JOIN WITH CODE**, enters a player name, selects an available team, and joins the same lobby. Names and team selections appear in the shared lobby. Every participant must use a different team.
5. When the lobby is full, the host clicks **START TOURNAMENT**. In the 4-player tournament the first two games are semifinals and the winners meet in the final. Each knockout match is one game with sudden-death overtime if tied. The champion appears after the final.
6. Everyone stays connected throughout. The host's machine runs each match, including when two guests face each other; non-playing entrants spectate the live broadcast. Later games start automatically after an 8-second results screen.

**Important limitations**
- The original 1v1 **Quick Match** and **Playoff Series** modes remain available. Playoff Tournament is a separate mode, limited to 2 or 4 total participants including the host.
- This is **live peer-to-peer multiplayer**, not a persistent hosted league. The host must stay online with the tab open throughout the tournament. Closing the host tab ends the session. New players cannot join after the tournament starts. Disconnected players may forfeit.
- Uses the existing PeerJS public signaling service and WebRTC. Connectivity depends on network conditions; strict NAT/firewall configurations may prevent connections. No dedicated relay/TURN server is included.
- Same-browser testing is available by appending `?local=1` to the page URL, then opening several tabs and joining via the code. A local broadcast connection is not a substitute for real multi-device testing.
- Existing online play stays unpaused; camera/audio and gameplay are generated on the host, with spectators receiving game snapshots.

**Validation:** JavaScript syntax passes Node.js, and a simulated four-player tournament logic test confirmed lobby joins, team uniqueness, guest controls, semifinals, final, and champion advancement. Full browser/WebRTC testing could not be completed in the build environment because browser navigation was blocked by administrator policy. Test a live 2-player and 4-player tournament on separate devices before using it for an event.

## Crowd visibility & arcade fight props (November 2026)

- **Front-row crowd corrected:** Near-side spectators now render after the rink in a carefully clipped foreground layer. Their faces stay visible below the glass instead of being hidden behind board panels; the back spectator row draws before the front row.
- **Randomized fight variety:** Brawls can feature a soft foam folding chair, oversized inflatable bat, ribbon streamer, pool noodle, or squeaky toy mallet. These are short slapstick animations, with comic sound captions. They are visual-only and do not change health, damage, collision or scoring.
- **Multiplayer sync:** Active fight props and their animation timing are carried in the host's match snapshots for visiting players and spectators.
- **Previous features kept:** Main menu, professional logo, cards, goalie outlet passing, pause jumbotron, and playoff tournament lobby.
