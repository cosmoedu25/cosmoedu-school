# CosmoeduVenture Design System

## Sources

This design system was built from the following sources:
- **GitHub repo**: https://github.com/cosmoedu25/cosmoedu-school — main landing page codebase (HTML/CSS/JS)
- **Figma**: https://www.figma.com/design/36YQTS3tSaftfKnD9RGBPP/%EC%A0%9C%EB%AA%A9-%EC%97%86%EC%9D%8C (limited access — images exported)
- **Live site**: https://school.cosmoedu.co.kr — public landing page & brochure assets

---

## Company Overview

**코스모에듀벤처(CosmoeduVenture)** is a Korean edtech company providing AI & coding education curriculum, platform, and rental eduware for schools, academies, and alternative schools.

**Products:**
1. **Landing page** (`index.html`) — B2B marketing site targeting school administrators & education centers
2. **Alternative school page** (`alternative.css`) — dark-themed AI-focused landing for alternative/progressive schools
3. **Platform** (`platform.html`) — SaaS learning management + curriculum delivery platform screenshots
4. **Brochure** (`브로셔.html`) — 8-page A4 print brochure for consultations/sales
5. **Curriculum page** (`curriculum.html`) — detailed program/course listing

**Core offer:** "플랫폼 + 수업 + 렌탈" — Platform subscription + remote/in-person teaching + device rental (all-in-one)

---

## CONTENT FUNDAMENTALS

### Tone & Voice
- **Language**: Korean (한국어) primary; English tool names (Scratch, Python, ZEP, Vibe Coding) kept in Roman
- **Register**: Professional yet warm — speaks to education administrators and teachers, not students
- **POV**: Company speaks in first person (저희, 코스모에듀), addresses readers as 교육기관/선생님/학교
- **Casing**: Sentence case in Korean; tool/brand names capitalized (Python, App Inventor)
- **Emoji**: Not used in primary copy; occasional icon characters (✦) as design accents

### Headline patterns
- Bold promises: "이것 하나면 AI 코딩교육이 됩니다"
- Problem/solution pairs: "강사가 없어도, 장비가 없어도 — 지금 시작할 수 있습니다"
- Numbered features: "① 이것 하나면 ② 수업 그대로 ③ 모든 것이 한 곳에"

### Copy examples
- "교육현장에서 하기 어려운 수업, 코스모에듀가 함께합니다"
- "학년·수준별 커리큘럼이 이미 준비되어 있어 기획 없이 바로 시작합니다"
- "작품이 클라우드에 자동 저장되고 따로 정리 없이 포트폴리오로 쌓입니다"

### Content structure
- Section chip/badge first (e.g. "CLASS FEATURES") → H2 title → subtitle → content
- Stats/numbers used sparingly (20명 수업, 5대부터, 주1회)
- CTAs: "무료 상담 신청하기", "지금 시작하기" (action-oriented, low-friction)

---

## VISUAL FOUNDATIONS

### Colors
Two palettes — **Light (B2B landing)** and **Dark (alternative/AI-focused)**:

**Light palette**
| Token | Value | Use |
|---|---|---|
| `--blue` | `#2563EB` | Primary brand, CTAs, links |
| `--blue-d` | `#1D4ED8` | Hover states |
| `--blue-l` | `#3B82F6` | Tints, accents |
| `--cyan` | `#0891B2` | Secondary accent |
| `--purple` | `#7C3AED` | Tertiary accent |
| `--green` | `#059669` | Success, tags |
| `--amber` | `#D97706` | Warning, vacation, highlights |
| `--text` | `#0F172A` | Primary text |
| `--muted` | `#64748B` | Secondary text |
| `--bg` | `#F8FAFC` | Page background |
| `--bg2` | `#EFF6FF` | Alt section background |

**Dark palette (alternative)**
| Token | Value |
|---|---|
| `--alt-bg` | `#0A0F1E` |
| `--alt-card` | `#111827` |
| `--alt-blue` | `#3B82F6` |
| `--alt-cyan` | `#06B6D4` |
| `--alt-purple` | `#8B5CF6` |

### Typography
- **Primary font**: `'Segoe UI', 'Malgun Gothic', sans-serif` — clean, widely available on Windows/Korean systems
- **Preferred upgrade**: Pretendard or Noto Sans KR
- **Weight system**: 400 (body), 600 (semibold), 700 (bold), 800/900 (display/hero)
- **Headline style**: Very tight leading (1.13–1.2), max-width clamp (`clamp(2rem, 4.5vw, 3.2rem)`)
- **Gradient text**: Used on hero and key section titles — blue→cyan→purple linear-gradient with `-webkit-background-clip:text`

### Backgrounds & Imagery
- Light pages: soft `#F8FAFC` with `#EFF6FF` alternating sections
- Subtle radial gradient blobs in hero (opacity ~0.07)
- Full-bleed photos: classroom shots, student work screenshots
- Dark page: pure `#0A0F1E` with card backgrounds `#111827`
- No heavy texture or patterns; clean flat surfaces

### Cards
- `border-radius: 12–20px`; white background; `box-shadow: 0 5px 15px rgba(0,0,0,.10)`
- Hover: `translateY(-4px)` + shadow increase
- Border: `1px solid rgba(15,23,42,.10)` (light) or `rgba(59,130,246,.2)` (dark)

### Buttons
- **Primary**: `linear-gradient(135deg, #2563EB, #0891B2)` + white text + `box-shadow`
- **Outline**: transparent bg + `1.5px solid border` → hover: blue border + tint bg
- **Border-radius**: same as card radius (12px)
- **Hover state**: `translateY(-2px)` + deeper shadow

### Section Labels / Chips
- Small ALL-CAPS badge above section titles
- Cyan color on light, cyan on dark
- `background: rgba(8,145,178,.08)`, `border: 1px solid rgba(8,145,178,.25)`, `border-radius: 100px`
- Letter-spacing: `0.15em`

### Animation & Motion
- Transitions: `0.28–0.3s ease` throughout
- Hero badge: pulsing dot `2s infinite`
- Entrance animations: `fadeInUp` (0.8–1.2s staggered) on hero elements
- No heavy parallax or scroll-based animations

### Layout Rules
- Max-width: `1160px` (main), `1200px` (alternative)
- Fixed header with backdrop-filter blur
- Grid: CSS Grid with `auto-fit / minmax(300px, 1fr)` for responsive card grids
- Section padding: `80px 0` (light), `6rem 0` (alternative)

### Corner Radii
- Cards: `12–20px`
- Buttons: `12px` (var --r)
- Chips/badges: `100px` (pill)
- Small elements: `6–8px`

### Shadows
- Light: `0 5px 15px rgba(0,0,0,.10)`
- Medium: `0 8px 30px rgba(37,99,235,.12)`
- Glow (dark theme): `0 0 24px rgba(59,130,246,.25)`

---

## ICONOGRAPHY

### Icon system
- **Font Awesome 6.4** (`fas`, `far`, `fab`) loaded via CDN
- `https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css`
- No custom icon font; no SVG sprite
- Icons used inline as `<i class="fas fa-..."></i>` within buttons, cards, list items

### Common icons in use
- `fa-robot` — AI
- `fa-code` / `fa-laptop-code` — coding
- `fa-brain` — computational thinking
- `fa-graduation-cap` — education
- `fa-chalkboard-teacher` — teacher
- `fa-chart-line` — learning tracking
- `fa-cloud` — cloud storage
- `fa-certificate` — certification
- `fa-phone` / `fa-envelope` — contact

### Logo files
See `assets/` directory:
- `cosmoedu_logo_black.png` — horizontal wordmark (dark text, 1024×180)
- `cosmoedu_logo_white.png` — horizontal wordmark (white text, 1024×180)
- `logo_circle.png` — circular favicon/icon version
- `logo.png` — square logo (48×48 or similar)
- `logo_36.png` — small square logo (36×36)

### Emoji usage
- **Not used** in main copy
- `✦` (decorative star) used as a section micro-accent in brochure
- Numbers ①②③ used as list design elements

---

## File Index

```
/
├── colors_and_type.css        — Design tokens (colors, type, spacing, shadow)
├── styles.css                 — Root CSS entry point (@imports all css/)
├── README.md                  — This file
├── SKILL.md                   — Claude Code skill manifest
├── 브로셔.html                 — 8-page A4 print brochure
├── index.html                 — Main B2B landing page
├── platform.html              — Platform feature showcase
├── curriculum.html            — Curriculum/program listing
│
├── css/                       — Component stylesheets
│   ├── style.css              — Master import file
│   ├── alternative.css        — Dark AI-theme page styles
│   ├── header.css             — Fixed header
│   ├── footer.css             — Footer
│   ├── programs.css           — Program/course cards
│   ├── about.css              — About section
│   ├── career.css             — Career/진로 page
│   ├── teacher.css            — Teacher training page
│   └── popup.css              — Contact form popup
│
├── assets/                    — Brand assets (logos, images)
│   ├── cosmoedu_logo_black.png
│   ├── cosmoedu_logo_white.png
│   ├── logo_circle.png
│   ├── AI_CLASS.png
│   └── hero_img.jpg
│
├── img/                       — Site images (platform screenshots, mentor photos)
└── uploads/                   — User-uploaded student work photos
```

---

## UI Kits

- `ui_kits/landing/index.html` — B2B landing page UI kit (header, hero, features, pricing, CTA)
- `ui_kits/alternative/index.html` — Dark AI-theme landing for alternative schools

---

## Notes for Designers & Developers

1. **Google Font recommendation**: Replace `'Segoe UI', 'Malgun Gothic'` with **Pretendard** for consistent Korean typography across platforms.
2. **Variables**: Core CSS vars defined in `colors_and_type.css`. Individual CSS files also define their own locals (e.g. `alternative.css` has `--alt-*` vars).
3. **Brochure**: `브로셔.html` is a self-contained print document (A4 × 8 pages, no external dependencies beyond Font Awesome CDN + local img/).
4. **Image slots**: `image-slot.js` provides drag-and-drop placeholder slots for user-uploaded images in the brochure.
