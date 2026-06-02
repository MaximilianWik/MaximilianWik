<!--
  ============================================================================
  MAXIMILIAN WIKSTRÖM — github profile
  ============================================================================
  Cyber-sigilism design system, ported from the Tessera project:
    ink ground · bone text · blood accents · monospace voice
  Sigils embedded in banner.svg (hero) + banner-1..5.svg (section breaks).
  ============================================================================
-->

<p align="center">
  <img src="assets/banner.svg" alt="Maximilian Wikström — full-stack, Stockholm" width="100%">
</p>

<p align="center">
  <a href="https://max-wik.com/"><img src="https://img.shields.io/badge/-MAX--WIK.COM-c41e26?style=flat-square&logoColor=white&labelColor=000000" alt="max-wik.com"></a>
  <a href="https://maximilian-wikstrom.vercel.app/"><img src="https://img.shields.io/badge/-PORTFOLIO-ece6d8?style=flat-square&labelColor=000000" alt="portfolio"></a>
  <a href="https://www.linkedin.com/in/maximilian-wikström/"><img src="https://img.shields.io/badge/-LINKEDIN-797368?style=flat-square&labelColor=000000" alt="linkedin"></a>
  <a href="https://www.instagram.com/max_wik/"><img src="https://img.shields.io/badge/-INSTAGRAM-b9b3a4?style=flat-square&labelColor=000000" alt="instagram"></a>
  <img src="https://komarev.com/ghpvc/?username=MaximilianWik&label=PROFILE+VIEWS&color=c41e26&style=flat-square" alt="profile views">
</p>

<br>

```
┌─ MANIFEST ──────────────────────────────────────────────────────────────────┐
│                                                                             │
│   I build small, opinionated web things — and the occasional desktop        │
│   oddity. React, TypeScript, Cloudflare Workers, Hono, Python, numpy.       │
│                                                                             │
│   Currently obsessed with: things that outlast their author. QR codes       │
│   verified against the ISO spec. State-switch architectures. DSP that       │
│   stays deterministic forever. Portfolios that load in under a second       │
│   on a phone in a basement.                                                 │
│                                                                             │
│   Based in Stockholm. Open to interesting work.                             │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

<p align="center"><img src="assets/banner-1.svg" width="85%" alt=""></p>

## ◆ ARTIFACTS

<table width="100%" cellspacing="0" cellpadding="0">
<tr><td valign="top" width="50%">

### [tessera](https://github.com/MaximilianWik/Tessera)
*verified-permanent QR codes*

A QR generator built for codes that get tattooed and must work for life. Encoder verified bit-for-bit against the **ISO/IEC 18004 Annex I** worked example. Every output round-tripped through three independent decoders (jsQR, zxing-js, native `BarcodeDetector`). Damage-tolerance simulated with progressive Gaussian blur. Printable archival spec sheet with full module matrix as ASCII + hex dump.

`Vanilla JS` · `Reed-Solomon` · `GF(256)` · `93 tests in CI`

**→ [live](https://tessera-neon.vercel.app/) · [tests](https://tessera-neon.vercel.app/tests.html)**

</td><td valign="top" width="50%">

### [subdermal](https://github.com/MaximilianWik/Subdermal) `// max-wik.com`
*the page behind a tattooed QR*

A React SPA on **Cloudflare Workers + Hono + D1**, with a state-switch architecture: a single number in `state.ts` selects what the page renders. State 8 is a 16,384 × 24,576 collaborative canvas — nine brushes, pinch-zoom, draft auto-save, per-browser ownership in D1, admin-token-gated moderation.

`React 19` · `Hono 4` · `Cloudflare D1` · `edge SQLite`

**→ [live](https://max-wik.com/)**

</td></tr>

<tr><td valign="top" width="50%">

### [cursed-echoes](https://github.com/MaximilianWik/CursedEchoesMiniGame)
*a gothic typing trial*

Browser typing game, Dark-Souls aesthetic. Four zones, three bosses, parry system, dodge-roll i-frames. **Three HiDPI canvases**, game state in refs (HUD ticks at 10 Hz, no per-keystroke React renders). All audio synthesized via Web Audio on demand — cathedral reverb bus, dissonant tritone drones per zone, inharmonic bell partials.

`React` · `HTML5 Canvas` · `Web Audio API`

**→ [live](https://cursedechoes.vercel.app/)**

</td><td valign="top" width="50%">

### [carpet-eater](https://github.com/MaximilianWik/Carpet-Eater)
*a desktop mouth that chews audio*

Frameless, transparent, mouth-shaped Windows app for the artist [Carpet Eater](https://soundcloud.com/carpet_eater). Drag any audio file onto it — it chews and spits a mangled version next to the original. Five DSP chains, nine pure-numpy stages, deterministic from a SHA-1 of the input file (same input → same output, forever). PyInstaller + Inno Setup, GitHub Actions CI builds EXE + installer + portable on every push.

`Python` · `PySide6` · `numpy DSP` · `ffmpeg`

</td></tr>

<tr><td valign="top" width="50%">

### [studio-panic-attack](https://github.com/MaximilianWik/Studio-Panic-Attack)
*3D scroll-driven portfolio for a designer*

Built (pro bono) for designer Ema Stoyanova. **`@react-three/fiber` + Three.js r180**, custom GLSL shaders (halftone, dither, paper, glass, metal), GSAP scroll-synced timelines. GPU-tier-adaptive: tier ≤ 1 devices get particles halved, postprocessing dropped, transmission swapped. Custom asset pipeline: 857 MB raw → ~70 MB WebP + 14 MB AVIF + LQIP placeholders.

`R3F` · `Three.js` · `GLSL` · `WebGL`

**→ [live](https://studio-panic-attack-maximilian.vercel.app/)**

</td><td valign="top" width="50%">

### [portfolio](https://github.com/MaximilianWik/PortfolioV3)
*dark-fantasy-formal personal site*

React 19 · Vite 6 · Tailwind 4 · `motion/react`. Ember-blood on ink-void, ceremonial typography, bonfire-lit hero. Heavy sections code-split via `React.lazy`. `DispersingText` runs a single `pointermove` listener + single RAF loop for the whole paragraph. JSON-LD Person + WebSite schemas for Knowledge Graph signals.

`React 19` · `Vite 6` · `Tailwind 4` · `motion`

**→ [live](https://maximilian-wikstrom.vercel.app/)**

</td></tr>
</table>

<p align="center"><img src="assets/banner-2.svg" width="85%" alt=""></p>

## ◆ STACK

```
┌─ PRIMARY ──────────────────────────────────────────────────────────────┐
│  TypeScript    React    Vite    Hono    Cloudflare Workers    Tailwind │
└────────────────────────────────────────────────────────────────────────┘
┌─ ALSO COMFORTABLE WITH ────────────────────────────────────────────────┐
│  Python    numpy    PySide6/Qt    Three.js / R3F    GLSL    Node       │
│  D1 / SQLite    Postgres    Vercel    GitHub Actions    Playwright     │
└────────────────────────────────────────────────────────────────────────┘
```

<p>
  <img src="https://skillicons.dev/icons?i=ts,react,nextjs,vite,tailwind,nodejs,python,cloudflare,vercel,github,sqlite,figma&theme=dark" alt="stack icons">
</p>

<p align="center"><img src="assets/banner-3.svg" width="85%" alt=""></p>

## ◆ TELEMETRY

<!-- Live counters via shields.io — bulletproof, always up -->
<p align="center">
  <img src="https://img.shields.io/github/followers/MaximilianWik?style=for-the-badge&label=FOLLOWERS&labelColor=000000&color=c41e26&logo=github&logoColor=ece6d8" alt="followers">
  <img src="https://img.shields.io/github/stars/MaximilianWik/Tessera?style=for-the-badge&label=TESSERA&labelColor=000000&color=c41e26&logo=github&logoColor=ece6d8" alt="tessera stars">
  <img src="https://img.shields.io/github/stars/MaximilianWik/Subdermal?style=for-the-badge&label=SUBDERMAL&labelColor=000000&color=c41e26&logo=github&logoColor=ece6d8" alt="subdermal stars">
  <img src="https://img.shields.io/github/last-commit/MaximilianWik/Subdermal?style=for-the-badge&label=LAST+COMMIT&labelColor=000000&color=ece6d8&logo=git&logoColor=c41e26" alt="last commit">
</p>

<!--
  Static stats card — generated daily by .github/workflows/profile-summary-cards.yml
  and recolored to the Tessera palette in the same workflow.
-->
<p align="center">
  <img src="profile-summary-card-output/transparent/3-stats.svg" alt="stats" width="60%">
</p>

<!-- Activity graph — different Vercel deployment from the paused stats one -->
<p align="center">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=MaximilianWik&bg_color=07070a&color=ece6d8&line=c41e26&point=ece6d8&area=true&area_color=c41e26&hide_border=true&custom_title=ACTIVITY%20%E2%80%94%20LAST%20YEAR" alt="activity graph" width="100%">
</p>

<!-- Snake animation. Generated daily by .github/workflows/snake.yml -->
<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/MaximilianWik/MaximilianWik/output/snake.svg">
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/MaximilianWik/MaximilianWik/output/snake-light.svg">
    <img src="https://raw.githubusercontent.com/MaximilianWik/MaximilianWik/output/snake.svg" alt="contribution snake animation" width="100%">
  </picture>
</p>

<p align="center"><img src="assets/banner-4.svg" width="85%" alt=""></p>

## ◆ TRANSMISSION

```
$ contact --priority high
  ↳ max.wik@icloud.com
  ↳ +46 70 736 05 15
  ↳ stockholm, se
  ↳ open to: senior frontend · full-stack · creative engineering
```

<p align="center"><img src="assets/banner-5.svg" width="85%" alt=""></p>

<p align="center">
  <sub><code>// EOF — built with care, on a ground of ink, in a font of bone, with one drop of blood.</code></sub>
</p>
