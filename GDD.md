# Game Design Document: Coin Cascade

## Game Title & Genre
**Title:** Coin Cascade
**Genre:** Idle / Physics Clicker

## Core Mechanic
Drop balls from the top of a Plinko-style peg board — they bounce off pegs and land in scoring buckets at the bottom. Earn coins based on where balls land, spend coins on upgrades that multiply earnings, unlock new ball types, and automate drops for idle progression.

## Why This Concept?
- **Idle/clicker games dominate CrazyGames trending** (Monster Merge, AFK Dungeon, Idle Dangers)
- **Physics-based visuals are inherently satisfying** — watching balls bounce is mesmerizing with zero explanation needed
- **Zero onboarding required** — tap/click to drop a ball, watch it bounce, collect coins. Instantly understandable.
- **Perfect mobile fit** — single tap interaction, portrait or landscape compatible
- **Not a direct clone** — Plinko mechanics + idle tycoon progression + upgrade meta-game is a unique combination on the platform
- **Technically achievable** as a single-file HTML5 game with custom lightweight physics

## Progression / Retention Loop

### Short Loop (per drop, ~2-5 seconds):
1. Player drops a ball
2. Ball bounces off pegs with satisfying physics
3. Ball lands in a scoring bucket (1x, 2x, 5x, 10x, 50x)
4. Coins are awarded with visual celebration
5. Repeat

### Medium Loop (per session, ~3-10 minutes):
1. Accumulate coins from drops
2. Purchase upgrades from the shop:
   - **Multi-ball:** Drop 2, 3, 5+ balls at once
   - **Auto-drop:** Balls drop automatically (idle mechanic)
   - **Better pegs:** Golden pegs that multiply points
   - **Special balls:** Fire ball (burns through pegs for bonus), Heavy ball (guaranteed bottom row), Ghost ball (phases through for random path)
   - **Board upgrades:** More scoring buckets, higher multipliers
3. Unlock new board layouts (each with unique peg arrangements)
4. Watch rewarded ads for 2x coin boost or instant ball refill

### Long Loop (across sessions, days/weeks):
1. Prestige system — reset progress for permanent multipliers
2. Unlock cosmetic themes (neon, retro, space, ocean)
3. Achievement system with milestone rewards
4. Daily bonus wheel spin
5. "Almost unlocked" teasers to encourage return

## Target Session Length
- **Quick session:** 2-3 minutes (a few manual drops, collect idle earnings)
- **Engaged session:** 10-15 minutes (active upgrading and watching cascades)
- **Deep session:** 30+ minutes (pushing for prestige, unlocking new boards)

## Tech Stack: Pure Canvas/JS (Single HTML File)

### Justification:
1. **Minimal file size** — entire game in one HTML file, well under 1MB. Far below the 20MB mobile threshold.
2. **Zero dependencies** — no CDN calls, no framework loading. Instant startup.
3. **Custom physics = custom feel** — the "bounciness" and satisfaction of the ball physics is THE core experience. Custom implementation allows precise tuning of gravity, restitution, and collision response for maximum juice.
4. **Full control over rendering** — Canvas 2D is more than sufficient for 2D circles bouncing off 2D circles. No need for Phaser's overhead.
5. **Performance** — lightweight custom code will hit 60fps easily on Chromebooks (4GB RAM target).

### Technical approach:
- Simple circle-vs-circle and circle-vs-line collision detection
- Verlet integration for physics (stable, simple)
- Canvas 2D rendering with requestAnimationFrame
- CSS-based UI overlays for shop/menus
- Web Audio API for procedural sound effects
- CrazyGames SDK loaded via script tag
- All in a single `index.html` file

## Why This Will Work on CrazyGames Specifically

| CrazyGames Success Factor | How Coin Cascade Delivers |
|---|---|
| Instant fun (< 5 sec) | Drop ball → watch bounce → get coins. No tutorial needed. |
| Max 1 click to gameplay | Game board IS the first screen. Tap anywhere to start. |
| Mobile-friendly | Single tap mechanic, responsive layout |
| Retention metrics | Idle progression brings players back, upgrade treadmill keeps them playing |
| Ad integration | Natural breaks: between board unlocks, after prestige, rewarded ads for 2x boost |
| Small file size | Single HTML file, < 1MB, loads in < 1 second |
| Visual appeal | Particle trails, screen shake, color-coded multipliers, satisfying physics |
| Progression depth | Upgrades → new balls → new boards → prestige → cosmetics |
