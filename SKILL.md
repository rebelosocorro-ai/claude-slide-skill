---
name: slide-skill
description: Turns meeting notes or a meeting summary into a VP-ready leadership deck, built through the Gamma connector in the Meridian brand (navy and amber, Inter, "Meridian - Confidential" footer). Enforces a fixed 10-section slide spine, 8-12 slides, assertion headlines with numbers, evidence on every slide, and strict density limits. Use this skill whenever the user pastes or uploads meeting notes, a meeting summary, a QBR or business review, a status update or a performance readout and wants a deck, slides, a presentation or a "leadership update" from it, even if they do not mention Gamma, Meridian or the word "brief". Also use when the user asks to turn discussion notes into something for a VP, senior leadership or executives.
---

# Slide Skill

Convert meeting notes into a brief, then build a senior-leadership deck from that brief in Gamma. Every deck must meet the same quality standard and carry the same Meridian brand, so the output is consistent no matter who runs the skill or what the notes look like.

## Why the rules are strict

A VP reads the title of each slide and decides in seconds whether to read more. So the deck has to work as a story told by titles alone: each title is a claim with a number, each slide has one point, and the evidence sits underneath. Vague lines ("results improved") and padded slides waste that attention. When in doubt, cut.

## Input

Meeting notes or a summary containing numbers, names and dates. Accept pasted text, an uploaded file, or a transcript.

If the notes are too thin to support the spine (no numbers at all, no owners, no outcome), say so in one or two lines, list what is missing, and ask for it before building. Otherwise proceed and flag gaps inside the deck (see "Missing data").

## Workflow

1. **Extract.** Read the notes and pull out: period covered, every metric with its actual, target and prior-period value, named owners, dates, root causes, decisions needed. Use only what is in the notes.
2. **Compute deltas.** For each metric that has a target or prior period, calculate the gap in absolute terms and in %. Show your arithmetic in the brief so it can be checked. Never round in a way that changes the story.
3. **Map to the spine.** Assign content to the sections below. Skip a section only if the notes truly contain nothing for it.
4. **Write the brief** in the format under "Brief format". Show it to the user.
5. **Build in Gamma** unless the user asked for the brief only (see "Building in Gamma").
6. **Return** the Gamma link plus a short list of anything flagged as missing or assumed.

## The slide spine

Use this order. Each section is normally one slide.

| # | Section | What goes on it |
|---|---------|-----------------|
| 1 | Title slide | Deck title, date, presenter line, tagline |
| 2 | The Bottom Line | The verdict in 3 bullets max, up front |
| 3 | Context | What this deck covers, in 1-2 lines |
| 4 | Results vs. Target | Headline numbers, each against target or prior period, with the delta |
| 5 | What's Working / What's Not | Each point stated as a claim |
| 6 | Why | Root causes |
| 7 | Actions & Owners | What we are doing, who owns it, by when |
| 8 | Asks | Decisions or help needed from leadership |
| 9 | Next Steps & Timeline | Sequenced steps with dates |
| 10 | Summary | A table of owners and deadlines |

**Skipping.** Skip a section only when the notes have nothing for it (for example, no asks were raised). Never invent content to fill a section, and never leave an empty slide.

**Splitting and merging.** Results vs. Target may need 2 slides if there are many metrics, and What's Working / What's Not is two slides when both sides have substantial evidence (one idea per slide). If the total would pass 12, merge in this order: fold Context into the Bottom Line slide as a single subline, then combine Next Steps into Actions & Owners, then trim Results to the 3-4 metrics that matter most.

## Deck-quality standards

Apply all of these to every deck.

1. **8-12 slides. Never more than 12.** If content is thin, consolidate rather than pad.
2. **One idea per slide.** If a slide needs "and" to describe its point, split it or cut one half.
3. **Assertion headlines.** The title states the takeaway as a claim with the number in it. Topic labels are not allowed.
   - Yes: "SMB conversion fell from 34% to 22% in Q1"
   - No: "SMB Numbers"
   - Apply this to every slide including Context and Asks, e.g. "We need two decisions by 15 May to protect the Q2 target" rather than "Asks". The title slide's deck title should also be a claim where the notes support one; otherwise a plain descriptive title is fine.
4. **Evidence on every slide.** Each claim is backed by a specific number or name from the notes. Write "churn fell 3.1 points to 8.4%", not "churn improved".
5. **Density limits.** Maximum 5 bullets per slide. Maximum about 12 words per bullet. No paragraphs. Favour white space. The Bottom Line has at most 3 bullets.
6. **Tone.** Written for a VP: direct, decision-first, no hedging ("we think", "it seems"), no filler.
7. **Data framing.** Always show a metric against its target or prior period and state the delta, e.g. "1.97Cr vs 2.4Cr target: 18% miss". Keep the currency and units the notes use (INR, Cr, lakh, %, points). State whether a % change is relative or in percentage points.
8. **No filler slides.** No "Thank you", "Questions?", agenda slides, or section dividers.
9. **Missing data is flagged, never invented.** See below.

### Missing data

If a number the slide needs is not in the notes (no target, no prior period, no owner, no date), do not estimate it. Write the slide with a visible placeholder in the form `[DATA NEEDED: Q1 target for enterprise pipeline]`, mark it in amber, and list every placeholder in the brief and in your final message. If a whole slide would be placeholders, drop the slide.

If the notes contradict themselves (two different figures for the same metric), use neither silently. Flag it as `[CHECK: notes show both 22% and 24%]`.

## Meridian brand

Fixed for every deck. Do not ask the user to choose.

| Element | Setting |
|---------|---------|
| Company | Meridian |
| Primary colour | Deep navy `#1B2A4A`: titles, structure, table headers, lines |
| Accent colour | Warm amber `#E8A33D`: key numbers, takeaways, placeholders only |
| Background | White or very light grey; no dark full-bleed backgrounds except optionally the title slide in navy |
| Body text | Navy or dark grey on white; never amber text for long passages |
| Font | Inter (clean, modern sans-serif); fall back to the closest sans-serif available |
| Footer | "Meridian - Confidential" on every slide, including the title slide |
| Title-slide tagline | "Clarity. Momentum. Results." |
| Look | Minimal, executive, lots of white space, not playful |

Amber is for emphasis, so use it sparingly: the one number per slide that matters most, or the delta. If everything is amber, nothing stands out.

**Imagery.** No stock photos, clip art, emojis or decorative illustration. Use simple charts, tables and large numbers instead. A chart is worth including only when it shows a metric against target or a trend across 3 or more periods; otherwise use a table or a big-number callout.

## Brief format

Produce the brief in this structure. It is both the thing the user reviews and the source for the Gamma input.

```
DECK BRIEF
Title: [assertion-style deck title]
Date: [date from notes, else today's date in DD Month YYYY]
Presenter line: [name and role from notes; else "[DATA NEEDED: presenter]"]
Tagline: Clarity. Momentum. Results.
Audience: VP / senior leadership
Slide count: [n] (8-12)

DELTA CHECK
[metric]: actual vs target/prior = delta (arithmetic)

SLIDES
1. Title slide
   Title: ...
2. The Bottom Line
   Title: [claim with number]
   - bullet (max 3)
3. [Section]
   Title: [claim with number]
   - bullets (max 5, ~12 words each)
   Visual: [big number / table / chart type, if any]
...

FLAGS
- [DATA NEEDED / CHECK items, or "None"]
- Assumptions made: [or "None"]
```

### Worked example (one slide)

Notes say: "SMB conversion was 22% this quarter, down from 34% last quarter. Target was 30%. Main driver was the new pricing page launched 3 March."

```
4. Results vs. Target
   Title: SMB conversion fell from 34% to 22% in Q1, 8 points below target
   - Q1 actual: 22% vs 30% target (-8 points)
   - Prior quarter: 34% (-12 points, 35% relative drop)
   - Enterprise and mid-market: [DATA NEEDED: conversion vs target]
   Visual: big-number callout "22%" in amber, target and prior in navy beneath
```

## Building in Gamma

The Gamma tools are deferred, so load them first with `tool_search` (for example, query "Gamma generate presentation") and read the parameter names it returns. Do not guess parameter names. Then:

1. Call Gamma's generate tool for a **presentation** (not document or webpage), with the slide count set to the number of slides in the brief.
2. Pass the brief's slide content as the input text and tell Gamma to **preserve** it as written rather than rewriting or expanding it. Gamma's own rewriting tends to add bullets, drop numbers and soften headlines, which breaks the standards above.
3. Put the brand and style instructions in the additional-instructions field (template below). Use whichever of these Gamma's schema supports: a theme, footer or header-footer settings, text and image options, card dimensions. Set image sources to none or minimal.
4. If the schema lets you set the footer directly, set it to "Meridian - Confidential". If not, rely on the instruction text and check the result.
5. If a saved Meridian theme exists in the user's Gamma workspace, use it. Check with Gamma's theme listing tool and look for a theme named Meridian. Otherwise choose the closest clean navy and white theme and rely on the instruction text for colours. Gamma may not accept arbitrary hex codes through the connector, so tell the user once, briefly, if the colours come out approximate and suggest saving a Meridian custom theme in Gamma so future decks match exactly.
6. After generation, poll the status tool until the deck is ready, then share the link.
7. Check the result against the checklist below as far as the tool output lets you. If Gamma returned something you cannot inspect (only a link), say that you could not verify the visual output and ask the user to check footer, colours and slide count.

### Instruction template for Gamma

Fill in the bracketed parts and send this as the style and layout instruction:

```
Build a [n]-slide executive presentation for Meridian senior leadership. Use the slide text exactly as provided: do not add, reword, expand or remove content, and do not add slides.

BRAND
- Company: Meridian
- Primary colour: deep navy #1B2A4A for titles, table headers and structural elements
- Accent colour: warm amber #E8A33D, used only to highlight the single key number or takeaway on a slide, and for [DATA NEEDED] placeholders
- Font: Inter, or the closest clean modern sans-serif
- Footer on every slide, including the title slide: "Meridian - Confidential"
- Title slide shows the tagline: "Clarity. Momentum. Results."
- Look: minimal, executive, white background, generous white space. Not playful.

LAYOUT
- One idea per slide. Slide titles are full-sentence claims; keep them to two lines at most.
- No stock photos, clip art, icons, emojis or decorative imagery.
- Use big-number callouts, simple tables or clean charts only where specified.
- Never exceed 5 bullets on a slide. No paragraphs.
- No "Thank you", "Questions", agenda or divider slides.
- Do not shrink text below readable size to fit content.
```

## Pre-flight checklist

Run this before building and again on the result. Fix any failure rather than reporting it.

- [ ] 8-12 slides, and no section padded to fill the spine
- [ ] Slides follow the spine order
- [ ] Every title is a claim containing a number or a name, not a topic label
- [ ] Every claim has a figure or name taken from the notes
- [ ] Every metric has a target or prior period and a stated delta
- [ ] Max 5 bullets per slide, about 12 words each, no paragraphs
- [ ] Bottom Line has 3 bullets or fewer and sits at slide 2
- [ ] No filler slides
- [ ] Nothing invented: missing data is flagged with [DATA NEEDED]
- [ ] Actions slide has an owner and date for each action
- [ ] Summary slide is a table of owners and deadlines
- [ ] Navy for structure, amber for emphasis only, Inter, footer on every slide, tagline on slide 1

## Final message to the user

Keep it short:

1. The Gamma link (or the brief, if the user asked for the brief only).
2. Slide count and one line on the verdict the deck leads with.
3. The flags: each [DATA NEEDED] or [CHECK] item, so the user can supply them and rebuild.
4. Any brand limitation encountered (for example, approximate colours).

Do not recap the whole deck or describe the process.

## Edge cases

- **Notes cover several topics or teams.** Build one deck around the single decision-relevant story. Ask the user which one if it is genuinely unclear; otherwise pick the one with the most numbers and say so.
- **No results, only discussion or decisions.** Drop Results vs. Target and lead the Bottom Line with the decision made. Keep to 8 slides or more by giving Why and Actions their own space; if that still falls short, tell the user the notes are too thin for a leadership deck and offer a one-page summary instead.
- **User asks for more than 12 slides, or an appendix.** Keep to 12 and say why. Offer to put the extra detail in a separate backup document.
- **User asks to change the brand for one deck.** Follow the request for that deck and note it, but do not alter this skill's defaults.
- **Notes are in a language other than English.** Write the deck in the language of the notes unless asked otherwise; keep the tagline and footer exactly as specified.
- **Confidential content.** The footer already marks the deck confidential. Do not add names or figures that are not in the notes, and do not paste personal data beyond what leadership needs.
