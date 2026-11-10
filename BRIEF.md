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
