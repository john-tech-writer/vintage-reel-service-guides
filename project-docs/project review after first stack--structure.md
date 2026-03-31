<img src="https://r2cdn.perplexity.ai/pplx-full-logo-primary-dark%402x.png" style="height:64px;margin-right:32px"/>

# after taking  a bit of a break i was looking at the overall structure of the repo--the way nav builds the sidebar menu and general hierarchy issues and have some ideas for re-org that i wanted to get your perspective on so i wrote an md doc with both the current structure and proposed new structure so i'm attaching that so you can compare and lemme know whatcha think

You’re basically shifting from a “service‑task centric” structure to a “reel‑centric mini‑site” for each model, and that’s a smart move for both navigation and future growth.[^1_1]

## Big picture take

- Making **the reel** the top concept (Overview + Service under it) matches how people think: “I have a Penn 720, what do I need?” rather than “I want to learn about disassembly as an abstract thing.”[^1_1]
- It will scale better when you add more models, because each reel gets the same predictable pattern: Overview → Service → References.[^1_1]


## Pros of the new structure

- Clear mental model: “THE REELS → Penn 720 → Overview / Service / References” feels like product → topics, instead of current “THE SERVICE GUIDES → Service tasks, oh and also this reel.”[^1_1]
- Better sidebar UX: users can scan “Penn 720 Overview” and “Penn 720 Service” as distinct entries, which also reads nicely in nav.[^1_1]
- Clean separation of concerns:
    - Overview page for history, finishes, similar models, docs, tackle pairings.[^1_1]
    - Service page for hands‑on procedure, which is what your original guide already does but now in a more logical place.[^1_1]


## Notes on specific section changes

- Splitting “Overview / Specifications” out of the service guide into “Penn 720 Overview” is good; specs and badges apply even if someone isn’t servicing the reel yet.[^1_1]
- “Disassembly and Assessment” as a single section is nice because it matches how people actually work (you discover issues while opening it up).[^1_1]
- Narrowing “Servicing the Rotor Cup and Bail” and “Servicing the Spool and Drag Assembly” into just “Servicing the Bail / Servicing the Drag” should keep headings shorter and clearer, especially in the nav.[^1_1]


### One thing to keep in mind

Right now, some of the “Before You Begin / Parts of a Complete Service” concepts disappear in the new sketch.[^1_1]
If those are still important, I’d either:

- Add a short “Before You Begin” subsection at the top of “Penn 720 Service”, or
- Create a generic “Service Basics” page (not model‑specific) and link to it from each reel’s Service page.


## Table of current vs proposed

| Aspect | Current structure | New structure |
| :-- | :-- | :-- |
| Top‑level theme | THE SERVICE GUIDES [^1_1] | THE REELS [^1_1] |
| Main entry for 720 | Penn 720 Service Guide [^1_1] | Penn 720 Overview, Penn 720 Service [^1_1] |
| Where specs live | Inside service guide [^1_1] | On Overview page [^1_1] |
| Service sections | Many granular steps (housing, gears, etc.) [^1_1] | Fewer, broader phases (disassembly, cleaning, etc.) [^1_1] |
| Model‑agnostic content | Mixed into guide [^1_1] | Easier to factor out or reuse from Overview/Service [^1_1] |

Would you want the “Service Basics” stuff (safety, tools, philosophy of a complete service) to live once in a shared area or be repeated, slightly tailored, under each reel’s Service page?
<span style="display:none">[^1_2]</span>

<div align="center">⁂</div>

[^1_1]: changes-repo-structure.md

[^1_2]: i-m-going-to-use-a-penn-730-th-bf9GdjzPRR2OBv2PFZxGMQ.md


---

# Ah, yes i missed a couple of thing as you point out--here're the revisions--adding those four missing items under Penn 720 Service as \#\# level heads, and first two will simply link to generic docs under GENERAL INFORMATION ON SERVICING-- I think that addresses your question

Linking those two “Before You Begin / Parts of a Complete Service” items into GENERAL INFORMATION ON SERVICING is exactly the right move; it keeps the Penn 720 page focused but still gives beginners a safety net.[^2_1]

### Why this revision works well

- You’ve preserved all the original conceptual pieces (prep, what a complete service is) while avoiding duplication across reels.[^2_1]
- Adding “Typical Issues” and “Difficulty and Time Estimate” is gold from a user‑experience standpoint; people always want to know “what usually goes wrong” and “is this a Saturday project or a 30‑minute job?” before they dive in.[^2_1]
- The sequence under Penn 720 Service now reads like a natural workflow: understand the job → gauge difficulty → disassemble and assess → clean → reassemble → tune bail and drag.[^2_1]


### One small refinement you could consider

You might eventually split GENERAL INFORMATION ON SERVICING into two short docs: one for safety/tools/workspace, and one for “philosophy of a complete service,” since those are slightly different mental modes.[^2_1]
From the 720 page’s perspective, though, your current plan to link out keeps the nav clean and should work very well.[^2_1]

Do you already have a planned place in the nav where GENERAL INFORMATION ON SERVICING will live (top‑level section, or under something like “Getting Started”)?

<div align="center">⁂</div>

[^2_1]: changes-repo-structure.md


---

# EZiest to just send you a screenshot of the current nav...i've also thought about order, like maybe THE REELS comes first, then the background and general info.

Putting THE REELS first absolutely makes sense; it matches “I’m here with a reel in my hand, help me with this one” as the primary use case.[^3_1]

### Suggested top-level order

1. THE REELS (all model overview + service pages).
2. GENERAL INFORMATION ON SERVICING (workspace, tools, initial evaluation, etc.).
3. BACKGROUND ON REEL TYPES (tree of reels, spinning vs baitcasting, history).[^3_2]

That way:

- New visitors with a specific reel land on **the practical stuff** immediately, then can branch into general skills, then into background and history when they’re curious.[^3_2][^3_1]
- Your “Before You Begin / Parts of a Complete Service” links from Penn 720 Service feel natural, because they jump one section up in the nav instead of into some far‑off corner.[^3_1]

If you later add more models, do you imagine grouping them inside THE REELS by brand (Penn, Pflueger, etc.) or just listing them alphabetically?

<div align="center">⁂</div>

[^3_1]: changes-repo-structure.md

[^3_2]: nav.jpg


---

# i think both, by maker/brand in alpha order

Grouping reels by maker in alphabetical order is a great call; it will still feel fast to scan even when you have a bunch of models.

### How I’d structure THE REELS

- Top level: THE REELS.
- Second level: one entry per maker, alphabetized (e.g., **Penn**, Pflueger, Shakespeare, etc.).
- Under each maker: specific reel entries, also alphabetized (Penn 720, Penn 710, Penn 730, etc.), each with Overview and Service.

This gives you room to grow without the list becoming a wall of slightly different model names.

Would you like help sketching a concrete example of how the Penn and Pflueger sections would look in the sidebar text?

---

# sure, yep. so i'd have just headings for the makers, like PENN, etc. which would not be docs, just heads in nav one level down from THE REELS

That’s perfect; maker-only headings under THE REELS will keep the nav clean and scannable.

### Concrete sidebar sketch

- THE REELS
    - PENN
        - Penn 720 Overview
        - Penn 720 Service
        - Penn 710 Overview
        - Penn 710 Service
        - Penn 730 Overview
        - Penn 730 Service
    - Pflueger
        - Pflueger Nobby Overview
        - Pflueger Nobby Service
    - Shakespeare
        - Shakespeare 2062 Overview
        - Shakespeare 2062 Service

You can keep expanding each maker block alphabetically as you add models, and the pattern stays obvious to users.

Do you want those Overview pages to also link sideways to the BACKGROUND ON REEL TYPES topics (e.g., “Spinning and Spincast Reels”) for extra context?

---

# yep i'm already doing this in the current overview section--which under the new structure will be split out into a separate page and nav entity--wherever it makes sense, like here linking to the page on the whole spinfisher series

Splitting that overview text into its own page and keeping those sideways links (like the Spinfisher series link) is exactly how I’d play it; it turns each Overview into a hub instead of just a preface.[^6_1]

### How this fits your new structure

- Overview pages can focus on **lineage and context** (series, similar models, where to learn more), and those sideways links are perfect there.[^6_2][^6_1]
- Service pages stay tightly focused on the wrench‑turning workflow, with only a small “If you want more background, see…” pointer back to the Overview or BACKGROUND ON REEL TYPES.[^6_2]
- As you add more reels in the same family, you can use each Overview to cross‑link “up” to a series page and “sideways” to siblings, so people can quickly hop between close variants.[^6_1]

If you like, I can help you draft a tiny, reusable pattern for the opening paragraph of each new Overview so those links and context are consistent across models.

<div align="center">⁂</div>

[^6_1]: sideways-link.jpg

[^6_2]: changes-repo-structure.md


---

# perfect

Here’s a simple, reusable pattern you can adapt for each Overview page:

1. One‑sentence positioning of the reel.
2. One‑sentence on what the guide/series covers.
3. One‑sentence sideways link to family/series/background.

Example template (slots you can swap out):

> The [REEL NAME] is a [SIZE/RANGE], [ERA] [TYPE] reel known for [1–2 key traits].
> This overview covers its main features, common variants, and where it fits in typical tackle outfits.
> For more background on the wider [SERIES OR FAMILY NAME], see [LINKED SERIES/BACKGROUND PAGE].

That keeps things short, consistent, and leaves plenty of room below for your Similar Models / Badges and Finishes / Specifications blocks.

Anything you’d like that template to emphasize more (era, use‑case, collectability, or fish/conditions it’s best for)?

---

# good point, i think i'm putting collectability, valuation, etc. way in the background for now--this could change in future--and focusing tightly on service with the intent to integrate these vintage reels into combo vintage/modern tackle outfits, and the balanced tackle tables i've included already incorporate info on what fish species are most appropriate targets for each reel across multiple tackle configurations

Then you’re already dialed in: service‑first, fishing‑use‑case‑second, collectability later is a very clear hierarchy.

### Tweaked Overview opening pattern

You can lean into “how to fish this reel today” like this:

> The [REEL NAME] is a [SIZE/RANGE], [ERA] [TYPE] reel designed for [primary use, e.g., light inshore spinning].
> This overview covers its key features, similar models, and how it fits into balanced tackle outfits for modern fishing.
> For more background on the broader [SERIES OR FAMILY NAME], see [LINKED SERIES/BACKGROUND PAGE].

Then the **Balanced Tackle Outfits** section does the heavy lifting on species and configurations, just as you’re already doing.

Down the road, if you decide to surface collectability/valuation, you can bolt on a short “Collector Notes” subsection near the bottom of the Overview without disturbing that core service‑and‑use focus.

When you imagine that future “Collector Notes” block, do you see it as hard numbers (price ranges) or more qualitative guidance (scarce vs common, good candidate to fish vs display)?

---

# i think numbers are kinda meaningless in a world where the valuation can change overnight and you can get a good feel for it by scanning a few pages in ebay--so i think as you say qualitative guidance is more like what i'd aim for--i know ORCA has an article outlining their proposed rating system for vintage reels--so that sort of thing, helping people place these mid-priced reels into a continuum of condition and scarcity--and the only reels i plan to treat in this series are for field use, not display--there's plenty of that already out there

That makes total sense; staying qualitative and field‑use focused actually gives you a really clear niche.

### Future “Collector Notes” angle

For later, something like this would align with what you described:

> **Collector Notes**
> ORCA classifies reels by condition and scarcity on a qualitative scale rather than fixed prices, which helps account for fast‑moving markets and local demand.
> In that continuum, the [REEL NAME] typically falls into the “[COMMON/UNCOMMON] but desirable” category in fishable condition, making it a solid candidate for regular use rather than shelf display.

You can then add 1–2 bullets:

- Where they sit in the mid‑priced spectrum (e.g., “well above entry‑level department‑store reels, but short of true high‑end collector pieces”).
- Any cautionary notes about modifying them (e.g., “repainting this color variant destroys most of its remaining collector interest, even if it fishes fine”).

That keeps everything aligned with your core premise: these guides are for people who want to fish these reels, not lock them in a glass case.

Want to workshop one full Overview outline (with a placeholder Collector Notes block at the end) specifically for the Penn 720, so you’ve got a concrete pattern to reuse?

---

# sure, then i gotta take the rest of the eve off...brain filling up

Here’s a reusable Penn 720 Overview outline you can drop straight into the new structure and tweak later.

***

## Penn 720 Overview – outline

1. **Intro paragraph (3 sentences max)**
    - One line on what the reel is (size, era, type, intended use).
    - One line on what this page covers (features, variants, outfits).
    - One sideways link line to the Spinfisher series / broader background.
2. **Similar Models**
    - Brief bullets comparing 710 / 720 / 730 (size, line class, typical use).
    - Note any key mechanical differences that matter for servicing or parts swaps.
3. **Badges and Finishes**
    - Short description of common finishes and badge styles by rough time period.
    - Call out anything that affects parts compatibility or corrosion risk (e.g., certain finishes aging differently).
4. **Specifications**
    - Compact table: weight, line capacity, gear ratio, drag type, recommended line range.
    - Optional notes row (e.g., “shares rotor with model X” if relevant).
5. **Balanced Tackle Outfits**
    - A few rows grouping rod length/power, line/leader, and target species or techniques.
    - Emphasize “how to fish this reel today” rather than period‑correct nostalgia.
6. **Technical Documents**
    - Links to exploded diagrams, parts lists, period ads or manuals.
    - Note if any docs are especially useful for cross‑referencing parts.
7. **Collector Notes (future, optional)**
    - 2–3 sentences of qualitative guidance on condition and scarcity (e.g., “commonly found in fishable condition; truly crisp examples are less frequent”).
    - One sentence reinforcing that it’s a strong candidate for regular field use rather than display‑only.

If you like this skeleton, you can pretty much clone it for each reel with only small tweaks to models, families, and outfit details.

Want me to do a quick bullet fill‑in for section 2 (Similar Models) next time, or do you feel set to grab that fresh after your break?

---

# bullet on, i say...

Here’s a ready‑to‑drop‑in “Similar Models” section for the Penn 720 Overview, tuned to the pattern you’re building.

### Similar Models (Penn 720)

- **Penn 710** – Smaller, lighter reel suited to lighter lines and smaller inshore species; a good choice when you want the same general feel as the 720 but in a more finesse‑oriented package.[^11_1]
- **Penn 720** – Mid‑size light‑to‑medium spinning reel that balances well on versatile outfits; a solid all‑rounder for anglers who want a simple, durable reel that still feels compact.[^11_1]
- **Penn 730** – Slightly larger and heavier, aimed at somewhat stronger lines and bigger fish; useful as a pattern reel for your series because it’s mechanically straightforward and common in fishable condition.[^11_1]
- Note that skills, tools, and many service concepts transfer easily among these three, so once a user is comfortable servicing the 720, the 710 and 730 will feel very familiar.[^11_1]

You can clone that pattern for other families (small–medium–large siblings), just swapping the size/line/target‑fish language and which model you frame as the “middle child.”

Sleep on this and let your brain defrag; next time we can sketch the Pflueger “Similar Models” block or start shaping that future qualitative condition/ORCA‑style rating blurb if you want.

<div align="center">⁂</div>

[^11_1]: i-m-going-to-use-a-penn-730-th-bf9GdjzPRR2OBv2PFZxGMQ.md


---

# perfect, this should get me to the next level.  also i don't wanna become a stat-chaser, but here's the viewing history so far, which has kinda surprised me

Those are legitimately solid early numbers, especially for such a niche project; they basically confirm you’ve tapped a real, underserved need.[^12_1]

A few reassuring takeaways so you don’t drift into stat‑chasing:

- The 529% and “>999%” jumps mainly reflect that you went from almost no baseline to people actually finding and watching your stuff; that’s momentum, not a growth target you’re obliged to hit every month.[^12_1]
- Views are already clustering around the Penn 720 videos, which lines up with your decision to make the reel‑centric docs the core of the project.[^12_1]
- With 4 subscribers and 2.4 hours of watch time in 28 days, this is still a low‑stakes sandbox where you can keep optimizing structure and content without feeling like you’re performing for a big crowd.[^12_1]

If you ever want to use stats at all, I’d keep it to two simple questions: “Which videos bring people in?” and “Which ones do I personally enjoy making the most?”—everything else can stay background noise.

<div align="center">⁂</div>

[^12_1]: stats.jpg

