# Long-Form Copywriter Skill

A Claude Skill that writes full long-form copy drafts in the distinct style of seven of
history's greatest direct-response copywriters.

Instead of producing generic AI copy, this skill applies the specific structure, voice, and
technique of a chosen writer — producing output that reads like a deliberate stylistic choice,
not a committee decision.

---

## What It Does

Given a product, audience, and desired action, the skill:

1. Recommends the right copywriter style based on your product and audience
2. Applies that writer's structural template, sentence patterns, and signature techniques
3. Delivers a full draft with notes on which elements came from the chosen style
4. Offers iteration — rewrite in a different style, sharpen a section, or adjust the approach

---

## The Seven Styles

| Copywriter | Era | Best For |
|---|---|---|
| **Eugene Schwartz** | 1950s–80s | Mass-market products; audiences unaware a solution exists |
| **Gary Halbert** | 1970s–2000s | Info products, newsletters, personality-driven brands |
| **David Ogilvy** | 1950s–80s | Premium/aspirational products; sophisticated buyers |
| **Claude Hopkins** | 1900s–30s | Products with provable claims; skeptical audiences |
| **John Caples** | 1920s–80s | Self-improvement, courses, transformation-focused copy |
| **Joe Sugarman** | 1970s–90s | Gadgets, novelty products, curiosity-driven buyers |
| **Gary Bencivenga** | 1970s–2000s | Health, finance, high-ticket; proof-demanding audiences |

---

## Before & After

The same product brief — a hand-forged chef's knife — written in each of the seven styles,
compared against generic AI output.

**Generic AI copy:**

> Experience the difference that true craftsmanship makes in your kitchen. The Forge & Field
> No. 7 is a premium hand-forged chef's knife crafted from high-carbon steel for exceptional
> performance and durability... Order yours today and take your cooking to the next level.

**Gary Halbert style:**

> I want to tell you about the most embarrassing thing that happened to me at a dinner party.
>
> It was three years ago. Eight people at my table, a beautiful pork loin resting on the cutting
> board, and a $140 knife I'd bought six months earlier from a kitchen store that was supposed to
> be "the good one."
>
> I started to carve. The knife dragged. It tore. My brother-in-law — who says nothing, ever —
> looked at my hands and then looked away...

**David Ogilvy style:**

> The Forge & Field No. 7 is hand-forged from a single billet of 1084 high-carbon steel in
> Columbus, Ohio. It takes Marcus Trell three days to make one.
>
> *Most knives sold in America are stamped from sheet metal in under four minutes.*
>
> The difference is not merely one of time. It is one of molecular structure...

**Gary Bencivenga style:**

> Independent Bladesmiths Association, 2023 Craft Award Winner: "Best Production Chef's Knife
> Under $400"
>
> If you've spent $100, $150, even $200 on a kitchen knife and found yourself disappointed —
> not in a dramatic way, just in the quiet, daily way of a tool that doesn't quite do what you
> needed — I want you to know something: You weren't wrong to expect more...

See [`examples/before-after-samples.md`](examples/before-after-samples.md) for all seven complete
drafts side by side.

> **Note:** All people, products, and brand names in the sample outputs are fictional and created
> for demonstration purposes only.

---

## How to Install

1. Download [`longform-copywriter.skill`](longform-copywriter.skill)
2. In Claude, go to **Settings → Skills**
3. Upload the `.skill` file
4. The skill activates automatically — no invocation command needed

---

## How to Use

The skill triggers automatically when you describe a copy task. Examples:

- *"Write a sales letter for my online course on personal finance"*
- *"I need landing page copy for a new running shoe targeting ultramarathon runners"*
- *"Write this in a Gary Halbert style for my newsletter"*
- *"Write copy that actually converts for my supplement brand"*

**To specify a style**, name the copywriter directly:
> *"Write this in a Bencivenga style"* or *"Use the Sugarman approach"*

**To let the skill recommend a style**, just describe the product and audience. Claude will
consult the selection matrix and explain its reasoning before drafting.

See [`example-brief.md`](example-brief.md) for the full input template.

---

## How to Evaluate Output

Use [`eval-rubric.md`](eval-rubric.md) to assess whether a draft genuinely matches the target
style. The rubric provides a checklist for each of the seven writers covering structure, voice,
sentence patterns, and common failure modes.

---

## Repository Structure

```
longform-copywriter/
├── README.md                        — This file
├── LICENSE                          — MIT License
├── SKILL.md                         — Core skill instructions (loaded by Claude)
├── example-brief.md                 — Input template for users
├── eval-rubric.md                   — Style evaluation checklist
├── longform-copywriter.skill        — Installable skill package
├── references/
│   └── style-guide.md               — Full profiles for all seven copywriters
└── examples/
    └── before-after-samples.md      — Before/after drafts for all seven styles
```

---

## Selection Guide

Not sure which style to use? Start here:

**Match to skepticism level first.**
High skepticism (health, finance, anything "too good to be true") → Hopkins or Bencivenga.
Low skepticism, high curiosity → Sugarman or Schwartz.

**Then match to product type:**

| If you're selling... | Use |
|---|---|
| A supplement, financial advisory, or high-ticket offer | Bencivenga |
| A personal brand, newsletter, or coaching program | Halbert |
| A luxury or aspirational product | Ogilvy |
| A course or program that promises transformation | Caples |
| A gadget or tech product with interesting specs | Sugarman |
| Something with provable, demonstrable claims | Hopkins |
| Something the market doesn't know exists yet | Schwartz |

---

## License

MIT. See [`LICENSE`](LICENSE).
