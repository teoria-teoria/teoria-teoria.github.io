# personal site brief — mateo acosta-rubio

paste this whole file into claude code as context before building. the site should feel like it was made by hand, by a person who has something to say. not a startup landing page. not a portfolio template. a page.

---

## the build

- single `index.html`
- inline css (or one `style.css`)
- vanilla js only (used once, for a live clock)
- no framework, no build step, no dependencies beyond two font CDNs
- deploys directly to github pages at `teoria-teoria.github.io`
- mobile responsive, desktop-first design
- max content width around 720px. this is an intimate page, not full-bleed

---

## the feeling

early internet but elevated. think editorial print designer who happens to know html. the site shouldn't feel like a founder pitching. it should feel like a thing someone made because they had something to say.

references the user sent:
- carlota mojica's site (tiny image on huge whitespace, metadata at the bottom)
- pioneer works s4ad page (terminal-style mono, brutalist)
- ed ruscha "thought about leaving, not moving" (red field, tiny white type)
- grace kasten dot xyz (hand-built, eccentric, alive)

shared DNA: lots of whitespace, big contrast in type sizes, mostly monochrome with one color moment, mono fonts handling structural/system text, soft fonts handling human voice.

---

## type system

two fonts. that's it.

### switzer (the human voice)
- this is mateo speaking
- always lowercase
- first person ("i", "we", never "you" addressing the visitor)
- short sentences. occasionally a little cryptic but not edgy for its own sake.
- weight range: 400 (body), 500 (emphasis), 700 (headlines)
- load from fontshare:
  ```
  https://api.fontshare.com/v2/css?f[]=switzer@400,500,600,700&display=swap
  ```

### intel one mono (the system voice)
- this is the website itself, not mateo. metadata, scaffolding, signposting.
- ALWAYS UPPERCASE
- used for: timestamps, page labels ("PAGE 1 OF 5"), section markers ("[02] CURRENT WORK"), dates, locations, status, navigation if any
- smaller than the switzer body text. it's signage, not content.
- load from google fonts:
  ```
  https://fonts.googleapis.com/css2?family=Intel+One+Mono:wght@400;500;700&display=swap
  ```

### scale guidance
- hero headline: very large, switzer, around 64-96px on desktop
- body switzer: 16-18px
- mono labels: 11-12px, with letter-spacing of about 0.08em
- big contrast between display and body. not three or four sizes in between. just big, medium, and tiny.

---

## color

- background: warm off-white, `#f5f3ee` or similar. not pure white.
- primary text: near-black, `#111` or `#1a1a1a`. not pure black.
- secondary text: medium gray, `#777` ish
- mono labels: lighter gray, `#999` ish
- accent: one red, `#d63623` or close to ruscha's red
- the red shows up ONCE or TWICE in the whole page. anchoring the letallgirls / didi section. that's its job. don't sprinkle it.

---

## structure

single scrolling page, divided into sections that feel like pages in a small book. each section gets a mono label at the top, like a chapter marker.

### header (fixed thin band at top, or sticky)
- left: `mateo acosta-rubio` in switzer, lowercase, small (around 14px)
- right: `MIAMI, FL · [LIVE CLOCK]` in intel mono, uppercase, smaller (11-12px)
- live clock updates every second, shows current time in eastern, format like `08:14:32 ET`
- thin hairline border under the header in light gray

### [01] opening
mostly empty. lots of vertical space.

intel mono label, small, top of section: `[01] WHO`

switzer, lowercase, hero size. one of these as the opener, or something close:

> "i build things for the people who actually run things."

> "i grew up running churro stores. now i build software for the people who do."

> "i'm building clave. before that, i was running stores. before that, i was in middle school selling pink hoodies."

below the hero line, smaller switzer paragraph (around 18-20px), three sentences max:

> "i'm a junior at babson and a co-founder of clave, an ai platform for franchise operators. my family has run churromania for over twenty years across ten countries. clave is the tool we wish we'd had the whole time."

then small mono at the bottom of the section: `PAGE 1 OF 5`

### [02] current work — clave
this is the main section. give it weight.

mono label: `[02] CURRENT WORK`

switzer, lowercase, large but not hero-size (maybe 32-40px):

> "clave."

then switzer body:

> "an ai platform for qsr franchise operators. it connects to everything operators already use, point of sale, labor, inventory, delivery, and turns it into specific actions. operators see a queue of proposals and act with one tap. no new dashboards. no new logins. just the next move."

> "i'm building it with my brother tadeo, our co-founder carlos, and our founding engineer valentina. our family ran the problem for two decades before we built the solution."

below the prose, a small mono block of metadata. aligned left, narrow column:

```
FOUNDED         MARCH 2025
LOCATION        MIAMI, FL
ROLE            CO-FOUNDER & COO
RAISED          $1M+
BACKED BY       BAIN CAPITAL, HUSTLE FUND,
                GEEK VENTURES, TETRAD, UNTAPPED
LINK            TRYCLAVE.AI →
```

the arrow on the last line is a real link to tryclave.ai. links underline on hover, no color change.

### [03] before this, alongside this
mono label: `[03] OTHER WORK`

three short blocks. each one: switzer paragraph + mono metadata. separated by generous whitespace, not borders.

**stuvi**

> "before clave, my brother tadeo, carlos, and i built stuvi. a studio booking marketplace for musicians. we connected over a thousand artists and studios across boston and miami before it was acquired in 2025."

```
STUVI           2023 — 2025
ROLE            CO-FOUNDER
OUTCOME         ACQUIRED BY JAMMED
```

**churromania**

> "the family business. 140+ stores, ten countries, two decades. i grew up in it and still work on product development. everything i know about operations started here."

```
CHURROMANIA     2019 — PRESENT
ROLE            PRODUCT DEVELOPMENT MANAGER
```

**letallgirls** ← this is where the red lives

> "letallgirls is a nonprofit i run alongside clave. we build offline ai education devices for communities without internet, starting in south sudan. it was founded by my friend didi ding mayen kuai, a babson freshman from bor. she passed away unexpectedly in march of 2024, a few days after we put together the first gofundme. i took over to carry her mission forward."

> "this year, letallgirls won the u.s. and north american championships at the global student entrepreneur awards. in july, i represent the u.s. at the global finals in south africa."

the words `didi ding mayen kuai` are in red (`#d63623`), inline. that's the color moment. just her name. nothing else on the page is red.

```
LETALLGIRLS     2024 — PRESENT
ROLE            EXECUTIVE DIRECTOR
PARTNERS        UNESCO, UNICEF, CARE FOUNDATION
LINK            LETALLGIRLS.ORG →
```

### [04] other things that are true
mono label: `[04] ALSO`

one tight switzer paragraph. no metadata block here. just text.

> "i was captain of my high school soccer team and we won two rings. i started designing clothes when i was twelve and ran an e-commerce brand called dirtbrokeworld until covid killed it. before that, when i was in middle school, my best friend and i sold pink hoodies in the school hallways to raise money for breast cancer awareness. our dean shut it down. a few weeks later we learned he'd been diagnosed himself. every dollar we raised went to his gofundme. that's the first time i remember caring about building things that mattered."

### [05] contact
mono label: `[05] REACH`

a clean mono block. left-aligned. each line a link where applicable.

```
EMAIL           MATEO@TRYCLAVE.AI →
LINKEDIN        /IN/MATEOACOSTARUBIO →
CLAVE           TRYCLAVE.AI →
LETALLGIRLS     LETALLGIRLS.ORG →
```

(if the user hasn't given exact urls or handles, leave placeholders and flag them to fill in.)

### footer
bottom of page. intel mono, tiny (10-11px), light gray, centered or left-aligned.

```
END OF PAGE · LAST UPDATED MAY 20, 2026 · BUILT BY HAND IN MIAMI
```

---

## interactions

keep it almost still. this isn't a tech demo.

- live clock in header, updates every second, eastern time
- links: subtle underline appears on hover. no color shift, no transform.
- no scroll animations
- no fade-ins
- no scroll-triggered anything
- it loads, it's there, it stays still

---

## copy rules (strict)

- no em dashes anywhere. use periods, commas, or "and."
- no rhetorical questions
- no startup language: never use "transforming," "revolutionizing," "disrupting," "synergy," "leverage," "ecosystem," "game-changing," "next-generation"
- never address the visitor as "you" in switzer text. switzer is mateo speaking about himself.
- intel mono can be impersonal/instructional, that's fine
- short sentences over long ones. when in doubt, cut.
- lowercase everything in switzer. uppercase everything in intel mono. no exceptions.

---

## what to leave out

- no revenue figures (no ARR, no per-store dollar amounts)
- no investor logos as images. text only.
- no client logos. text only if mentioned.
- no testimonials
- no big call-to-action button. the email at the bottom is enough.
- no dark mode toggle
- no images at all in v1. pure type. (an image can be added later if it fits.)
- no awards list. the gsea mention inside the letallgirls paragraph is enough.

---

## delivery checklist for claude code

- [ ] one `index.html`, no other files needed (or one `style.css` if cleaner)
- [ ] both fonts loaded correctly from their CDNs
- [ ] live clock works and updates
- [ ] red shows up exactly once: on `didi ding mayen kuai`
- [ ] responsive on mobile (test at 375px width)
- [ ] no console errors
- [ ] no broken links (use placeholders flagged with TODO if URLs missing)
- [ ] file is ready to commit and push to github pages

once it's built, the user will preview locally, iterate if needed, then push to `teoria-teoria.github.io`.
