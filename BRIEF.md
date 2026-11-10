# Yoyli.dev — redesign brief

Wave's brief (2026-11-10): YoyliOS is an operating system **parents buy for their children**.
The site must be marketing — it has to sell — but not only glassmorphism and surface
design: it needs **thinking for children**. Dual audience: the parent's eye buys
(trust, control, clear price); the world that eye sees is the child's.

Built on three foundations, studied in full (see STUDY-chimney.md, STUDY-torim.md):

## From Chimly (chimney-project) — conversion & honesty
- ONE action in the whole site: **Get YoyliOS — $19**. Header, hero, after every
  major section, price block, footer.
- Sticky mobile split pill — the ONLY glass element on the page (dark navy glass,
  blur, like Chimly's): [Get YoyliOS $19] | [How it works]. Glass is an accent for
  one floating element, never the design language.
- Trust without inventions: no fake testimonials, no invented ratings. Instead:
  a "What YoyliOS is not" section (no Apple Silicon, Robo can make mistakes, you
  need a 16 GB USB stick), exact requirements, and one real human contact
  (yoylios.app@gmail.com, from the original site).
- Page = funnel: promise → what's inside → how it works (01/02/03) → fit &
  limits → FAQ that kills objections → buy → short human footer.

## From Torim (Queasy) — product depth & tokens
- Design tokens first, defined once in CSS :root (below). No random AI gradients.
- One parent decision path; every section answers ONE parent question:
  Is it safe? (facts) → What does my kid actually get? (real games by age) →
  Am I in control? (real parents panel) → Who helps them? (Robo) → How do we
  start? (3 steps) → What happens after I pay? (checklist) → What can go wrong?
  (honest limits) → How much? ($19) → Questions (FAQ).
- Every module carries real data: real game names/ages/screenshots, real system
  requirements, the real post-purchase sequence (license key → download → write
  USB → boot → create child profile). Edge states are content, not an afterthought.
- Branding comes from the product: the site font is Rubik — the font the child
  sees inside YoyliOS — and the palette is built to sit with the OS screenshots.

## Motion & 3D (Wave, 2026-11-10)
- The site is animated. No wall of static game screenshots.
- HERO: a Three.js laptop that OPENS toward the visitor when they reach it
  (scroll into view). As it opens, the screen runs a BOOT sequence like a real
  bootloader — boot logo/lines and a progress bar — and then YoyliOS itself
  comes up: the real home-screen screenshot (the image from the top of the
  original page) as the booted desktop. Tapping the laptop replays open+boot.
- GAMES section: a Three.js desk scene — monitor on a desk, keyboard, mouse,
  and a desktop tower standing beside it. The monitor screen is ALIVE: the
  games run there as an animated carousel / active game simulation (animated
  canvas texture: game art sliding, bubbles/stars moving) instead of 10 static
  pictures. Below the scene, the visitor can pick a game and the monitor
  switches to it.
- Performance rules: render each 3D scene only while it's on screen, cap pixel
  ratio, low-poly primitives, graceful static-image fallback if WebGL fails,
  respect prefers-reduced-motion.

## Games section pattern (Wave, 2026-11-10 — FINAL: the player unit)
- THREE earlier forms were rejected by Wave (mini-monitor explorer; sticky
  computer + list; fixed zone + chimney-style stacking deck — verified
  working, still "מסורבל, לא כיף" on a phone). Wave's ruling principle:
  judge it as a human on a phone — it must be watchable, simple, fun, and
  NOT take over the screen. No sticky machinery at all.
- Built form: ONE compact player card in normal flow — the existing desk
  simulation as a video-like window, a one-line "Now playing", the three
  age chips, and a swipeable thumbnail rail (scroll-snap) of the group's
  games directly under the screen. Tap a thumbnail → it plays above it.
  Total unit ≈ half a phone screen; the page flows past it naturally.
  A picked game HOLDS 20 seconds before the auto-carousel resumes.
- Devices/launcher scene framing rule (Wave): pull the camera back until
  BOTH devices are whole in frame — realistic relative sizes and a smooth
  look beat readable screen content; tablet center-back, phone in front.

## Games section pattern (Wave, 2026-11-10 — earlier iterations)
- Wave's catch: by the time a visitor scrolls down to the game buttons, the
  desk simulation has scrolled away — they tap games but can't SEE them change.
- First fix (a sticky mini-monitor mirroring the desk + age-grouped cards)
  was REJECTED by Wave on sight: two simulations stacked is wrong, the sticky
  monitor was huge, covered the cards and blocked taps.
- Wave's own spec, now built: ONE simulation only — the desk computer itself
  scrolls a little and then STICKS (sticky stage) while the options scroll
  beneath it. Beside/below it: THREE age tabs side by side (Ages 2–4 /
  5–8 / 9–12); a tab swaps the list under it to that age's games only
  (2–4: the four toddler games; 5–8: Galaxy Math Racer, Letters Adventure,
  Star Pop, Fishing Lake; 9–12: Robo Code, Time Rescue) and starts the
  group's first game on the computer. Tapping a game plays it on the
  always-visible screen.

## V2 polish pass (Wave, 2026-11-10 — after seeing the prototype)
- Higher quality everywhere: more polish, richer animations.
- 3D quality: rounded geometry instead of blocky rectangles, simulation-grade
  realism — environment lighting, soft shadows, real materials.
- NO cropped interfaces: screenshots and in-simulation screens always show the
  FULL interface (fit, never cover-crop). Wave caught the profile-picker shot
  under the animations being cut — fixed by rule, everywhere.
- Logo rebuilt as ONE lockup: David's original logo.webp is a wide robot+"Yoyli"
  image; v1 squashed it into a square AND duplicated it with HTML text. Rule:
  one logo only — a fresh SVG robot mark (David's cute purple robot, redrawn
  clean in the site's toy style) + one "YoyliOS" wordmark. Never the raw
  logo.webp in a square, never logo + repeated name beside it.
- New section: a tablet and a smartphone as 3D simulations. CRITICAL framing
  (Wave, 2026-11-10): on phone/tablet this is a FUTURE LAUNCHER — the
  "YoyliOS Launcher" for Android — NOT the operating system. The OS is PC-only.
  The section must say "coming soon / launcher" clearly; the devices show the
  launcher's world (profiles, home, Little Play) as a preview. Never imply
  YoyliOS-the-OS runs on phones or tablets.
- Device identity matters (Wave): sculpt recognizable hardware — a Samsung
  Galaxy Tab–class tablet (~12", 16:10) and a Galaxy S26 Ultra–class phone
  (boxy titanium frame, punch-hole camera) at true proportions, and the
  screens inside must be SHARP and clearly readable — pre-rendered fitted
  screens, high texture resolution, no per-frame blur.

## Backgrounds — a kindergarten wall, all the way down (Wave, 2026-11-10)
- The backgrounds are the kids' world: soft, innocent, user-friendly colors —
  like a kindergarten wall painted in gouache: a forest, hills, a house, the
  night sky. Every scroll/section brings its own drawing with it — a new cute
  scene and new characters arrive as you go down the page.
- Characters are ORIGINAL generic animals (fox, rabbit, owl, deer, cat,
  hedgehog, teddy bear, duck, butterflies). NEVER copyrighted characters —
  Wave named Winnie the Pooh only as the vibe, explicitly not to use him.
- Each section gets a pastel wash + a hand-drawn SVG scene band (hills, trees,
  its character) that reveals as the section scrolls into view, with gentle
  idle motion (drifting clouds, twinkling stars, a fluttering butterfly).
  Content always stays on top and readable; scenes are decoration, pointer-
  events off.

## Voice
Parent to parent. Short sentences. Specifics over slogans.
No AI superlatives ("revolutionary", "magical experience"). If a claim can't be
pointed at in the product, it doesn't go on the page.

## Design tokens (v1)
- --paper: #FFF8EC (warm cream) · --ink: #1C2B4A (parent navy)
- --sky: #2F9BE8 (primary) · --sun: #FFC531 (accent) · --coral: #FF6B57 (the buy action)
- --grass: #2FBF8F · --berry: #7C5CD6 (sparingly, games only)
- Cards: white, 3px solid ink border, offset hard shadow (6px 6px 0 ink),
  radius 22px — tactile "toy block" feel for the kid-facing parts; parent-trust
  sections stay calm navy-on-paper.
- Font: Rubik (product font), weights 400/700/900.
- Touch targets ≥44px. Works with no JS (FAQ = native details). Reduced motion respected.

## Facts — only from David's real site (do not invent)
- $19 one-time, lifetime license key, no subscription. Checkout: LemonSqueezy
  (link preserved from the original site).
- Ages 2–12; profiles 2–4 / 5–8 / 9–12. Works fully offline. No ads, no in-app
  purchases, no accounts, no feeds.
- Needs: 64-bit PC, 4 GB RAM min (8 recommended), 16 GB+ USB stick.
- Install paths: next to Windows / from USB / inside Windows window. Uninstaller restores the PC.
- Games Exclusive (real): ages 2–4 — Bubble Pop, Star Catcher, Shape Drop, Animal
  Surprise. Ages 5+ — Galaxy Math Racer, Letters Adventure, Robo Code, Time Rescue,
  Star Pop, Fishing Lake.
- Yoyli Learn (real, 16): Magic Clock, Fruit Market Math, Alphabet Balloons, Count
  the Critters, Colors & Shapes, Magic Memory, Magic Keyboard, Mouse Garden,
  Connect the Glow, Word Workshop, Match Party, Farm Friends, Toy Band, Magic
  Paint, Shape Puzzle, Star Maze.
- Yoyli Store: 100+ curated apps, parent approval for every install.
- Robo: offline AI buddy, homework help incl. photo of a worksheet; can make mistakes.
- School suite: writer, slides, sheets with templates. Little Play (2–4).
  Planner & sticker album. USB backup of profiles.
- Languages: English, Spanish, Hebrew.
- FAQ facts: refunds per policy; Intel Macs may work, Apple Silicon not supported;
  running from USB doesn't touch the PC; no internet needed; support by email.
