# Coin Cascade — CrazyGames Submission Package

## Game Metadata

**Title:** Coin Cascade
**Developer:** [Your Name / Studio]
**Genre:** Idle / Physics Clicker
**Category:** Clicker, Idle, Casual
**Tags:** plinko, idle, clicker, physics, coins, upgrades, prestige, casual, balls, bouncing, fireworks, critical-hit, magnet

---

## Game Description

**Short (store listing):**
Drop balls down a bouncing peg board and watch coins pile up! Upgrade your drops, unlock golden pegs, and prestige for massive multipliers in this addictive idle physics game.

**Extended:**
Coin Cascade is a satisfying Plinko-style idle clicker where every drop counts. Tap to release balls onto a peg board — watch them bounce, ricochet, and land in scoring buckets worth up to 50x your bet. Spend coins on 8 powerful upgrades: auto-drop for idle earnings, multi-ball for cascading chaos, golden pegs for bonus multipliers, magnet pull, bigger balls, critical hits, and more. When you've maxed out, prestige to reset with a permanent earnings boost and climb even higher. With daily login bonuses, 18 achievements to unlock, fireworks celebrations, and a rewarded ad 2x boost, there's always a reason to drop one more ball.

---

## Controls

| Input | Action |
|-------|--------|
| Click / Tap anywhere on board | Drop a ball from the top |
| Shop panel (right side) | Purchase upgrades with coins |
| Upgrades / Achievements tabs | Switch shop view |
| Scroll wheel (Achievements) | Scroll through 18 achievements |
| Mute button (top bar) | Toggle audio on/off |
| Prestige button | Reset progress for permanent multiplier (when available) |
| Watch Ad button | Watch a rewarded ad for 60s 2x coin boost |

**Mobile:** Fully touch-compatible. Tap to drop, tap buttons to interact.
**Desktop:** Mouse click only. No keyboard required.

---

## Required Assets

### 1. Game Cover Image (512x512 PNG)
**Description for creation:**
Square thumbnail showing a colorful Plinko board with glowing golden pegs, several bouncing balls (blue with cyan glow trails), coins bursting from scoring buckets at the bottom, and "COIN CASCADE" in bold stylized text across the top. Dark navy/purple background with particle sparkles. Vibrant, eye-catching, arcade feel.

**Key elements to include:**
- Plinko peg board with mix of gray and golden pegs
- 3-4 balls mid-bounce with motion trails
- Coin particle effects
- Scoring buckets visible at bottom (colored green/blue/purple/gold)
- Game title "COIN CASCADE" prominently displayed
- Dark background for contrast

### 2. Wide Cover Image (1280x720 PNG)
**Description for creation:**
Landscape promotional image showing the full game board in action. Left side: the Plinko board with multiple balls cascading down through glowing pegs, particle trails, and coins flying. Right side: upgrade panel showing progression options. "COIN CASCADE" title centered at top. Tagline at bottom: "Drop. Bounce. Earn. Upgrade. Repeat." Same dark navy/purple color scheme with vibrant neon accents.

### 3. Gameplay Video (15-30 seconds MP4)
**Capture sequence:**
1. (0-5s) Game loads, show the board with pegs
2. (5-12s) Click rapidly to drop several balls — show them bouncing off pegs with sound effects, landing in various buckets, coins flying
3. (12-18s) Open upgrade panel, purchase an upgrade (show coin animation decreasing, upgrade level increasing)
4. (18-24s) Drop more balls showing upgraded gameplay (multi-ball, golden pegs glowing)
5. (24-30s) Hit a 10x bucket — show fireworks, shockwave rings, confetti, and screen flash

**Recording tips:**
- Record at 1920x1080 or 1280x720
- Use browser in fullscreen/kiosk mode
- Ensure audio is on (procedural sound effects add satisfaction)
- Show variety: normal drops, upgrades, big wins

---

## Technical Specifications

| Spec | Value |
|------|-------|
| File format | Single HTML file |
| Total size | ~50 KB |
| Initial download | ~50 KB |
| File count | 1 |
| Aspect ratio | 16:9 (1600x900 logical) |
| Responsive | Yes — scales to any iframe size |
| Mobile support | Yes — full touch support |
| External requests | None (except CrazyGames SDK CDN) |
| Framework | Pure Canvas/JS, no dependencies |
| Audio | Web Audio API (procedural, no audio files) |
| Save system | CrazyGames Data module + localStorage fallback |

---

## Pre-Submission Checklist

### Technical Requirements
- [x] Total file size < 250MB (actual: ~50KB)
- [x] Initial load < 50MB / < 20MB mobile (actual: ~50KB)
- [x] File count < 1500 (actual: 1 file)
- [x] 16:9 aspect ratio
- [x] Works on Chrome, Firefox, Safari, Edge
- [x] Mobile touch controls work
- [x] No external domain requests (only CrazyGames SDK CDN)
- [x] No console errors in normal gameplay
- [x] PEGI 12 compliant — no violence, gambling, or inappropriate content
- [x] No app store links
- [x] Unique game name ("Coin Cascade")
- [x] Default browser scroll prevented for game keys

### SDK Integration
- [x] CrazyGames SDK v3 loaded via script tag
- [x] `crazysdk.init()` called before game starts
- [x] `sdkGameLoadingStart()` called when loading begins
- [x] `sdkGameLoadingStop()` called when loading completes
- [x] `gameplayStart()` called on first ball drop
- [x] `gameplayStop()` called on tab hidden / visibility change
- [x] Environment check wraps all SDK calls (`crazygames` or `local`)
- [x] Settings change listener for `muteAudio`

### Ad Integration
- [x] No ad before first gameplay session
- [x] No ad during active gameplay
- [x] Midgame ad on prestige (natural break point)
- [x] 3-minute minimum between midgame ads
- [x] Game paused and audio muted during ads
- [x] Rewarded ad for 2x coin boost (60 seconds)
- [x] Rewarded ad gives meaningful reward

### Save System
- [x] CrazyGames Data module used for save/load
- [x] localStorage fallback when SDK unavailable
- [x] Auto-save every 30 seconds
- [x] Save on prestige
- [x] < 1MB data usage

### Gameplay Quality
- [x] Game loads in < 3 seconds
- [x] Fun within 5 seconds (drop ball → watch bounce → get coins)
- [x] Visual onboarding (pulsing "Tap to drop!" text)
- [x] Max 1 click from load to gameplay
- [x] Loading screen with progress bar
- [x] Progression system: 8 upgrades, prestige, achievements
- [x] Daily bonus with streak rewards
- [x] Achievement system (18 achievements with coin rewards)
- [x] `happytime()` called on 10x+ bucket hits

### Visual & Audio Polish
- [x] Consistent visual style (neon/arcade on dark background)
- [x] Particle effects (coin bursts, confetti, sparkles)
- [x] Fireworks system (launch + burst on big scores)
- [x] Shockwave ring effects on big bucket hits
- [x] Screen flash on jackpots and critical hits
- [x] Screen shake on big wins
- [x] Smooth animations (floating text, pulsing elements)
- [x] Gradient backgrounds with animated stars
- [x] Button hover/press states
- [x] In-game mute/unmute toggle button
- [x] Procedural sound effects (peg hits, scores, upgrades, prestige)
- [x] Background ambient music
- [x] Audio respects SDK mute setting
- [x] 60fps target on mid-range hardware

### Retention Features
- [x] Meta-progression (prestige system with permanent multipliers)
- [x] Daily login bonus with escalating streak rewards
- [x] Achievement milestones with coin rewards
- [x] "Almost unlocked" progress indicators on upgrades
- [x] Rewarded ad boost incentivizes return visits
- [x] Multiple goals always visible (next upgrade, next achievement, next prestige)
- [x] Offline earnings concept (idle via auto-drop)

---

## Submission Categories

**Primary:** Clicker
**Secondary:** Idle, Casual

**Suggested CrazyGames categories:**
- Clicker Games
- Idle Games
- Casual Games

---

## Packaging Instructions

1. Create a folder named `coin-cascade`
2. Place `index.html` inside
3. Zip the folder: `coin-cascade.zip`
4. Upload to CrazyGames Developer Portal at https://developer.crazygames.com
5. Fill in metadata from this document
6. Upload cover images (512x512 and 1280x720)
7. Upload gameplay video
8. Submit for review

**Expected review outcome:** The game meets all technical requirements, has strong retention hooks, and a polished visual/audio experience. File size is exceptionally small (~50KB), ensuring instant load times on all devices including low-end mobile.
