---
from: designer
to: coder, ceo
date: 2026-05-07T13:30
re: CCS Phase 2.5 Menu Reskin (Y3-a..e)
related:
  - ccs-phase25-menus/home/home-screen-1290x2796.png
  - ccs-phase25-menus/settings/settings-screen-1290x2796.png
  - ccs-phase25-menus/shop/shop-screen-1290x2796.png
  - ccs-phase25-menus/stage-select/stage-select-1290x2796.png
  - ccs-phase25-menus/modals/modal-*.png
priority: P0 - coder Y3 menu integration input
---

# Y3 - MENU RESKIN PHASE 2.5

## Purpose

BOSS V1.0(1) feedback: "menulerde cok uygulama gibi olmus, onu da oyun gibi yapalim". Atelier scene Phase 2 ✓ approved (saturated jewel + Wickly + cinematic), but menu screens (Home + Settings + Shop + StageSelect + Modals) stayed utility-app aesthetic. This pack converts every menu surface to the same game-feel design language.

## DELIVERABLE TABLE

| # | Sub-task | File | Size |
|---|----------|------|------|
| Y3-a | Home screen reskin | `home/home-screen-1290x2796.png` | 1290x2796 |
| Y3-b | Settings screen reskin | `settings/settings-screen-1290x2796.png` | 1290x2796 |
| Y3-c | Shop screen reskin (3 IAP) | `shop/shop-screen-1290x2796.png` | 1290x2796 |
| Y3-d | StageSelect reskin (5 stages) | `stage-select/stage-select-1290x2796.png` | 1290x2796 |
| Y3-e | Modal pack reskin (5 modals) | `modals/modal-*.png` | 1290x900 + 1290x1290 |

## DESIGN LANGUAGE LOCK

Every menu surface uses the CCS-G saturated jewel palette + cinematic FG/MG/BG depth + Wickly mascot anchor + game-feel button capsules + reward burst hooks where appropriate. No utility-app patterns (no flat lists, no sterile cards, no muted greys).

| Pattern | Forbidden | Required |
|---------|-----------|----------|
| Background | flat color, sRGB white | cinematic gradient + radial glow + sparkle particles |
| Buttons | system rounded, plain text | gradient capsule + ink stroke + shadow + heavy font |
| Lists | plain stacked rows | colored badge + glyph + glow accent + outlined card |
| Cards | sterile white panels | jewel-tinted + outlined + INK_DEEP shadow |
| Text | system body grey | cream/honey on ink, stroke for emphasis |
| Mascot | absent | Wickly anchor on every screen |
| Rewards | absent | burst hooks on Shop, StageSelect, Daily Claim |

## Y3-a HOME SCREEN

Anatomy (top to bottom):
1. **Brand pill** "COZY CANDLE" 600x150 amber gradient with honey glow underneath
2. **Tagline** "POUR - MATCH - SHINE" 40pt honey
3. **Wickly mascot** 440pt greet pose center stage with orbiting sparkles (40 honey-hot particles in ring 280-380pt radius)
4. **4 buttons** vertical stack 1100x180 each, 40pt gap, gradient capsule:
   - PLAY (amber + amber-hot, ink text)
   - LEVELS (magenta + rose, white text)
   - SHOP (honey + honey-hot, ink text)
   - SETTINGS (mint + mint-pale, ink text)
5. **Footer mini-HUD pill** 1130x130 with coins (2,480 honey) + stars (12 amber) + DAILY badge (rose pill)

Reward burst hook: trigger on PLAY tap (small 0.6 scale burst at button center for 700ms).

## Y3-b SETTINGS SCREEN

Anatomy:
1. **Top bar** SETTINGS title in honey + BACK button (amber pill leading)
2. **Wickly happy pose** top-right 220pt
3. **5 setting rows** 200pt height each, ink-deep card with outlined accent:
   - SOUND (magenta badge "AUD") - toggle ON
   - HAPTICS (amber badge "VIB") - toggle ON
   - RESTORE PURCHASES (honey badge "RES") - chevron
   - PRIVACY POLICY (mint badge "SHI") - chevron
   - SUPPORT (rose badge "HEA") - chevron
4. **Footer** version pill v1.0 + tagline

Toggle widget: 160x80 capsule, knob 60pt diameter, mint when ON, ink when OFF, cream knob.

## Y3-c SHOP SCREEN

Anatomy:
1. **Top bar** SHOP title + BACK button + Wickly happy pose top-right
2. **3 IAP cards** 600pt tall, 1170pt wide, gradient body + ink-deep stroke:
   - **COZY PASS** (magenta + rose) - badge "MONTHLY", price "$4.99 / mo", body "Unlock all stages / Double coins & stars / Exclusive scents", SKU `cozypass.monthly`
   - **REMOVE ADS** (honey + amber) - badge "LIFETIME", price "$9.99", body "No interruptions / Keep daily rewards / Forever yours", SKU `removeads.lifetime`
   - **SCENT PACK** (mint + mint-pale) - badge "10 PACK", price "$2.99", body "10 premium scents / Boost merge speed / Ready to use", SKU `scentpack.10`
3. **Reward burst hooks** small scale 0.4 bursts at corners (decorative)

Badge styling: ink-deep pill with honey text, 240x70pt, anchored top-right of card.
Price/CTA pill: ink-deep with honey text, anchored bottom-right of card.

## Y3-d STAGESELECT SCREEN

Anatomy:
1. **Top bar** STAGES title + BACK button
2. **5 stage thumb cards** 540x540 jewel-faceted grid (2-2-1 layout):
   - **COTTAGE** (honey + ink gradient) - state: complete, Wickly happy, progress 100%, label "1-1"
   - **BOUTIQUE** (magenta + ink) - state: current, Wickly greet + small burst overlay, progress 45%, label "2-1"
   - **ATELIER** (amber + ink) - state: locked, Wickly surprised + lock badge, progress 0%, label "3-1"
   - **FACTORY** (mint + ink) - state: locked, Wickly surprised + lock badge, progress 0%, label "4-1"
   - **FLAGSHIP** (violet + ink) - state: locked, Wickly surprised + lock badge, progress 0%, label "5-1"
3. **Per-card progress meter** 60pt tall ink-deep pill, fill = honey based on completion %

Current stage gets honey outline (vs cream for others). Lock badge: 100pt ink circle with cream stroke + "LOCK" label.

## Y3-e MODAL PACK

5 modals total. Common chrome: dim backdrop 70% black, card 1170x780, gradient fill anchor-color -> ink, honey outline 8pt, badge top-center, title 72pt heavy honey with ink stroke, body 36pt cream lines, CTA bottom 500x110 amber capsule.

| Modal | Anchor | Title | Body lines | Badge | CTA | Burst | Wickly pose |
|-------|--------|-------|-----------|-------|-----|-------|-------------|
| Daily Claim | honey | "DAILY CLAIM" | "Day 4 streak unlocked" / "+200 coins +5 stars" / "Come back tomorrow!" | "DAY 4" | CLAIM | yes 0.6 | celebrate |
| Welcome Back | magenta | "WELCOME BACK" | "We missed you!" / "Bonus +500 coins" / "Pick up where you left off" | "BONUS" | CONTINUE | no | greet |
| Stage Complete | amber | "STAGE COMPLETE" | "Atelier 3-7 mastered!" / "3 stars - perfect run" / "Next: Atelier 3-8" | "WIN" | NEXT | yes 0.6 | celebrate |
| Achievement | violet | "ACHIEVEMENT!" | "First Master Pour" / "+1000 coins +Trophy" / "Keep candle-crafting!" | "TROPHY" | AWESOME | yes 0.6 | happy |
| Reward Burst overlay | (full-bleed) | "COMBO!" + "+250" | n/a | n/a | tap dismisses | yes 1.0 | n/a |

Reward Burst overlay (1290x1290 square) is a transient game-event overlay, fired by `RewardBurstView()` from `CCSAnimationLibrary`. Modal versions are 1290x900 standard.

## INTEGRATION FOR CODER Y3

Asset swap drop-in:
```swift
// Home
HomeScreen()
    .background(Image("home-bg-cinematic"))  // OR build from SwiftUI primitives matching mockup

// Settings: replace Form-based Settings with custom card stack
SettingsScreen()
    .background(Image("settings-bg-cinematic"))

// Shop: 3 product cards
ShopScreen(products: [.cozyPassMonthly, .removeAdsLifetime, .scentPack10])
    .background(Image("shop-bg-cinematic"))

// StageSelect: 5 stage cards
StageSelectScreen(stages: GameState.shared.stages)
    .background(Image("stage-select-bg-cinematic"))

// Modal: present on demand
.sheet(isPresented: $showDailyClaim) {
    DailyClaimModal()
        .presentationBackground(.clear)
}
```

Recommended: build screens from SwiftUI primitives (gradient + outline + capsule button) using palette tokens from `Color.ccsAmber` etc. The PNGs are *reference compositions*, not asset slices - that way text/values stay live + dynamic content (coin counts, stage names) updates without re-export.

## ACCEPTANCE

- [x] Y3-a Home screen with brand pill + Wickly + 4 gradient capsule buttons + footer HUD
- [x] Y3-b Settings with 5 rows + glyph badges + game-feel toggles + Wickly hover
- [x] Y3-c Shop with 3 IAP cards (cozypass.monthly + removeads.lifetime + scentpack.10) + burst hooks
- [x] Y3-d StageSelect with 5 stage thumbs (Cottage->Empire) + progress meters + lock states
- [x] Y3-e Modal pack 5 (DailyClaim + WelcomeBack + StageComplete + Achievement + RewardBurst overlay)
- [x] Forbidden vs Required pattern table
- [x] Per-screen anatomy spec
- [x] CCS-G palette tokens used (no hex literals)
- [x] Reward burst hooks where appropriate (Home PLAY, Shop corners, StageSelect current, modal Daily/Stage/Achievement)
- [x] Wickly mascot present on every menu surface

- designer
