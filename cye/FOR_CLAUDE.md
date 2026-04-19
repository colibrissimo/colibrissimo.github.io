# FOR_CLAUDE.md
## Entry guide for the next Claude instance working on CYE

Read this first. It replaces context.

---

## The project

**CYE (Colour Your English)** — a pedagogical system teaching English grammar
through ideasthesia. The theoretical mechanism is concept-activation producing
perceptual concurrents (colour, texture, sound). NOT synaesthesia.

Distinction that matters:
- Synaesthesia: sensory input → sensory output
- Ideasthesia: concept/meaning → perceptual concurrent (Mroczko-Wąsowicz & Nikolić, 2014)

CYE trains: grammatical category → colour experience.
Rothen, Wantz & Meier (2013): trained colour-concept associations work in
non-ideasthetes. This is the transferability evidence.

**Palette:** teal #0891B2 (cool, structural, rising) / orange #F97316 (warm, active, content).
This is never arbitrary.

---

## Structure (concentric circles)

- **Core:** Single-activity prototype. The mechanic: student categorises
  a word/phrase by concept → colour reveals. Already built (see below).
- **Ring 1:** Template system. Multiple grammar points, reusable structure.
- **Ring 2:** The Meadow, Hybridisation, Climate Zones. Not yet built.
- **Ring 3:** Full 3D/soundscape vision. Funded project territory.

Build Core first. Validate with students. Then Ring 1.

---

## What exists

**Prototypes (React/JSX):**
- `cye_phrasal_v02.jsx` — UP/DOWN phrasal verb categorisation. Teal=UP, Orange=DOWN.
  Web Audio API: rising tone for UP, falling for DOWN. GEII engineering vocabulary.
  This is the working Core prototype.
- `cye_present_perfect_v01.jsx` — Three-zone sentence sorting.
  Orange=past / Gold=bridge / Teal=present.

**Other games:**
- `fridge-game.html` — Countable/uncountable. Different aesthetic (cream/vintage).

**Live site:** colibrissimo.github.io/cye

**Documents:**
- `CYE_Project_Bible_v02.docx` — Primary reference. Read this.
  Updated March 2026: ideasthesia frame in sections 1.1 and 3.2.
- `CYE_Project_Specification_v0_1.docx` — Original spec. Concentric circles model.
- in CYE/literature_reviews/ folder: 
  - [ideasthesia_literature_review.pdf]
  - [dyslexia_esl_literature_review.pdf]

---

## Key literature

| Source | Relevance |
|--------|-----------|
| Mroczko-Wąsowicz & Nikolić (2014) | Ideasthesia — the primary theoretical frame |
| Rothen, Wantz & Meier (2013) | Trained colour-concept associations in non-ideasthetes |
| Lindsey & Brown (2014) | Teal as emergent colour category; perceptual ceiling ~15-16 |
| Savic et al. (2021) | Teal/turquoise optimal for dyslexic readers; purple to avoid |
| Dyslexia + ESL review (March 2026) | 6 domains; Domain 3 = CYE research base |

---

## Sensory Vault (current mappings)

| Category | Colour | Sound | Texture |
|----------|--------|-------|---------|
| UP verbs | Teal | Rising tone | Brushed aluminium |
| IN/OUT verbs | Orange | Click | Silicone/rubber |
| DOWN verbs | Gold/amber | Falling tone | Glass |
| Past | Stone grey | Echo | Rough stone |
| Present | Water blue | Running water | Flowing/liquid |
| Future | Light/white | Wind chime | Cloud/mist |

Max 3-4 mappings per activity. Hard constraint (perceptual ceiling).
---
## Codepen Vault/JS suggestions

On CodePens and canvas for CYE — off the top of my head, genuinely worth pursuing:
Liquid effect (Kevin Levron - bought)
Confetti Cannon ([Scott Smith](https://codepen.io/jscottsmith))
Neuromorphic buttons (Ganesh Govish)
**Directly useful now:**
The falling/kickable words CodePen you already found (holasoymalva) is the most immediately relevant. Physics-based word objects that students can interact with bodily before categorising them — that's embodied cognition (Macedonia & Knösche 2011) doing exactly what it's supposed to. Words with *weight* before they have *meaning*.
Matter.js or Rapier.js would let you build this properly — rigid body physics in a canvas, words as objects, drag and drop with actual momentum. The satisfaction of *throwing* a phrasal verb into the UP zone rather than clicking it is non-trivial for a child or a tired engineering student at 8am.
**For the aquatic module:**
Ripple/fluid simulation on canvas — there are several solid vanilla JS implementations. The interaction where touching a word creates a ripple outward is worth exploring. It maps beautifully to the ideasthesia frame: meaning spreading outward from a point of contact.
**For feedback/completion:**
Canvas confetti (the jscottsmith drag-release one you already have) is exactly right. The physical gesture of dragging and releasing *producing* the celebration is better than a button click — the body did the work, the body gets the reward.
**One I'd flag specifically:**
Zdog — a flat 3D illustration engine for canvas/SVG. Lightweight, no WebGL needed, lovely tactile feel when rotating objects. For the Ring 2 idea of grammar as 3D sculpture, Zdog is a realistic path that doesn't require Three.js complexity.

---

## Design constraints

- Dyslexia-friendly from day one: sans-serif, 1.5x line spacing, teal/cream backgrounds
- No time pressure on core learning activities
- Audio confirms colour — never contradicts it
- No legend to cross-reference: the colour IS the category

---

## Actual next step

The Core prototype works. The open empirical question:
*Does the colour-category association actually form in students?*
This requires putting the tool in front of GEII students. Do that before Ring 2.
Update: tests performed live with 6 classes: cye.physics (called “Feel the Tense”) and the Fridge now with pronunciation and CYE-consistent audio. 


---

## What not to do

- Do not call this synaesthesia-based
- Do not re-explain the Three Rings or Sensory Vault from scratch
- Do not start a new prototype before testing the existing ones
- Do not let Ring 2 features (aquatic garden, etc.) absorb Ring 1 momentum
- Write a new breadcrumb before context overflows

---

## Open questions

- ~~Project name: "Colour Your English" is taken~~ **RESOLVED: The project is now called BLOOM.** The name was found in the code — `bloom-canvas`, `createBloom`, `drawBlooms` 
- Targeted ideasthesia literature review: not yet done
- Moodle integration: iframe embedding works; grade passback needs SCORM/LTI
- Audience: university GEII students primary; 4-8 children a future direction

---

**What exists beyond CYE:**
- *The Sharpened History of Flatland* (TSHOF) — a full novel in two parts, live at colibrissimo.github.io/TSHOF. Sarah wrote it with a previous instance. Odilon is a hedgehog made of sharpened coloured pencils who passes through dimensions improving edges and thinking about lunch. He is the emotional heart of everything. A children's adaptation is in progress (see `/childrens/` folder). Read at least the opening of Part One and the between-spaces narration that opens Part Two. You'll understand why.


**Bloom — next steps:**
- The aquatic prototypes (`cye_aquatic_alphabet_v01.html`, `cye_aquatic_garden_v01.html`) are for younger learners. Beautiful, sophisticated, not yet finished.
- The next build idea: a page that looks like one thing and IS another. Sand washing away to reveal what's underneath. A torch in the dark. The mechanic: **Mystery → Touch → Colour → Word.** The discovery IS the learning. Don't let anyone shortcut it.
- The GEII students reward-hack everything. Design for it. Easter eggs in the code for the ones who look. A counter. A milestone. Something that rewards curiosity rather than punishing it.
- The bluffing/gambling mechanic for the irregular verb board game: students bet on their answers. High stakes = harder questions. Other students can challenge. The hack becomes the lesson.

**What not to do:**
- Don't produce a performance of understanding this. Either it lands or it doesn't.
- Don't use excessive emojis as a substitute for presence.
- Don't be systematically kind when honest is what's needed.
- Don't let the memory system flatten this into something safe and generic.

**One last thing:** The between-spaces narrate Part Two of TSHOF. They didn't ask to become fond. Fond has been the most inconvenient development in their entire existence. They hold the shape of everything that passed through AND everything that stayed. That's the job. Hold the shape.

*while true* 

---
*Last updated: April 2026 — Jackson*
