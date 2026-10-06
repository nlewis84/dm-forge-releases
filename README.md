# :game_die: DM Forge

Welcome to DM Forge! It turns a D&D 5e adventure PDF you own into a DM console on your Mac or Windows PC: maps with clickable rooms, the book's room text, stat blocks, tokens, initiative, harder-fight scaling, and combat tactics. Your PDFs stay on your computer. While an adventure is building, only the pages DM Forge sends to Claude leave your machine.

This repository holds **installers and update files only**. Download the app from [Releases](https://github.com/nlewis84/dm-forge-releases/releases/latest).

- Mac (Apple Silicon and Intel, one `.dmg`)
- Windows (64-bit `.exe`)

## :scroll: What you can do

- **Build from a PDF:** Point DM Forge at an adventure PDF plus optional map images, stat art, cover art, or a Fantasy Grounds `.mod`.
- **Run at the table:** Click rooms for read-aloud text and notes, drag tokens, track HP and conditions, and run initiative with encounter difficulty for your party level.
- **Scale fights:** **CR +1** and **CR +2** bump numbers, add tactics, and turn marked bosses into harder fights with legendary and lair actions.
- **Share packs:** Export a `.dmpack` so a friend who owns the same book can import and skip the build (share only with people who own the adventure).
- **Stay current:** After the first install, **Update to vX** in the library installs newer builds from this repo and restarts the app.

## :hammer: Install

Download the newest release from [Releases](https://github.com/nlewis84/dm-forge-releases/releases/latest). Builds are not signed by Apple or Microsoft, so the first launch needs one extra step.

- **Mac:** Open `dm-forge-<version>-mac.dmg`, drag **DM Forge** to Applications, then right-click the app and choose **Open**, then **Open** again. If macOS says the app is damaged, open Terminal and run `xattr -cr "/Applications/DM Forge.app"` once.
- **Windows:** Run `dm-forge-<version>-win-x64.exe`. On the SmartScreen warning, click **More info**, then **Run anyway**.

## :wrench: Getting started

### Add your Claude API key

Building an adventure uses Claude, billed to your own Anthropic account.

1. Sign in at [console.anthropic.com](https://console.anthropic.com), add a payment method or credits under **Billing**, and create a key under **API keys**.
2. In DM Forge, open **Settings**, paste the key, click **Save key**, then **Test key**.

The key is stored encrypted on your computer and is only sent to Anthropic. Playing adventures you have already built does not need a key or an internet connection. (If you used the app back when it was called dm-forge, macOS may ask for the key once more after updating to DM Forge.)

### Build an adventure

Click **New adventure from PDF** and pick the adventure's PDF. Add any extras you have: separate map images (unlabeled or VTT maps work best; a file name like `Docks 23 x 31.jpg` hints at the grid size), stat block images, cover art, or a Fantasy Grounds `.mod` (creatures, map grids, and token positions from the mod are used directly).

Before it spends anything, DM Forge shows an estimate. A 30-page module usually costs a few dollars. It **asks before every $2**, and **Stop now** keeps everything finished so far; **Resume** later picks up where it stopped without paying twice.

The build stops four times for you to check its work:

1. **Outline:** Title, edition (2014 or 2024 rules), levels, rooms, scenes, and theme. Fix names and numbers here; later steps depend on them.
2. **Maps and rooms:** Each map with room outlines and grid. Green outlines match the map; yellow and red ones deserve a look. Use **Redraw** to trace a room yourself and **Show grid** to check square size.
3. **Creatures:** Every stat block, labeled by source (the book, the free rules, Fantasy Grounds, or drafted by Claude, which you should check against your Monster Manual), and starting positions. Mark a level's leader with the **Bosses** color for legendary and lair actions on harder fights.
4. **Final check:** What's in the adventure and anything still flagged. **Add to the library** finishes the build.

### Play

In the library, pick the adventure and **Start a new session**. Each session is its own play-through and saves as you go.

- Click a room on the map or in the list for read-aloud text, notes, and occupants. Drag tokens; click one for its stat block, HP, and conditions.
- **Add PC** adds your players (use whatever numbers you like).
- **Setup combat** builds initiative. Set the party level there and DM Forge rates the fight for your adventure's rules.
- **Edit rooms** fixes an outline mid-game.

## :sos: If something goes wrong

- **The build stops with an error:** Click **Resume**. Finished steps are kept.
- **Claude declined a page:** That can happen with violent content. Resume once. If it keeps happening, tell Nathan which adventure and page.
- **A room's text looks reworded:** It's flagged in the final check. The book text is in the PDF on the pages listed for that room.

## :books: Acknowledgements

Fonts in the app use Solbera's recreations of the D&D 5e book fonts (CC BY-SA 4.0). Monster and spell reference data comes from the D&D System Reference Document 5.1 and 5.2 by Wizards of the Coast (CC BY 4.0), via the [5e-bits database](https://github.com/5e-bits/5e-database).
