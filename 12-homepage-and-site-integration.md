# Doc 12. Homepage and Sitewide Integration
## The Exact Edit List for the IDE

**Rule for this whole document:** edits ship as one coherent commit set, page changes and nav changes together, so no interim state shows a link to a page that does not exist or a page no nav reaches. The eight versus nine sector drift happened because edits shipped separately; this list exists so that does not repeat.

---

## 1. Navigation and footers (all pages)

Add `Adoption` → /adoption.html to the Pages menu and to the footer Platform column, positioned after Industries and before How Manar Builds. Rationale: the footer Platform column reads as the offer in sequence (what sectors, how adopted, how built, what models, how secured).

## 2. Homepage edits

### 2.1 Hero (minimal touch)
Keep the H1 and subline untouched; they are the brand. Change only the third hero button: `Open roles` becomes `How adoption works` → /adoption.html. Careers remains one click away in the header and footer; the hero's three slots should carry the commercial sequence: Site Read, the thesis, adoption. If Farabi prefers keeping Open roles while hiring is active, add nothing and rely on section 2.3's link instead; do not grow the hero to four buttons.

### 2.2 The premise block (one sentence added)
In the existing premise copy ("Generic AI is available to everyone, which is precisely why it is the advantage of no one..."), append one sentence at the end:
`Stanford's AI Index measured the same conclusion: the cost of generic intelligence fell 280 fold in eighteen months. What everyone can rent is an advantage to no one.`
Attribution style: the source name is inside the sentence, no footnote apparatus. This is the homepage's single statistic. The homepage carries exactly one; the other two live on the adoption page. Do not add a stat strip to the homepage; restraint is the brand and the record section belongs to the dedicated page.

### 2.3 New homepage section: The adoption record (compact)
Placement: directly after What we believe, before Where it fits. Uses the existing two column text block style, no new components.

Eyebrow: `The record`
Header: `Adoption is failing. The causes are known.`
Body: `The public record on generic AI adoption is now measured: most pilots return nothing, abandonment is rising, and the obstacles organizations name most are cost, data privacy, and security. Not one of these is a property of the intelligence. All of them are properties of how it was adopted: generic, rented, and cloud bound. Manar runs adoption the other way, in five stages, ending in a system you own, run by your staff, that met a number before you accepted it.`
Link: `The Adoption Path →` /adoption.html

Note: this section deliberately carries zero digits. The claims are directional and every one is backed on the adoption page with source and year. This keeps the homepage's register calm while the dedicated page carries the evidence.

### 2.4 What we believe (add the fifth belief)
Append after belief 04, same numbered style:
`05` · `Adoption is a build. Not a subscription.`
`What is rented visits your operation. What is built and owned becomes part of it. Manar engagements end with assets on your books and capability in your staff, or they have not ended.`

### 2.5 Homepage FAQ (add one, keep the existing two)
Q: `We tried AI before and it did not stick. Why would this be different? +`
A: `Because what you experienced has now been measured across thousands of organizations, and the causes are known: the tools were generic, rented, and cloud bound. The Adoption Path reverses each one, and a deployment is accepted only when it meets a number agreed on your conditions before work begins. The full record is on the adoption page.`
Link within answer: /adoption.html

## 3. Site Read page
Add one sentence to the page's framing copy, near the top:
`The Site Read is stage one of the Adoption Path: the reading that decides what deploys first, on what hardware, measured by what number.`
Link the phrase Adoption Path → /adoption.html.

## 4. Methodology page (How Manar Builds)
Add a two sentence preamble above the existing 01 to 05 stages:
`These five stages are how a deployment is built. Inside a client engagement they are carried by the Adoption Path, which begins with a Site Read and ends with your staff operating a system that met its number.`
Link Adoption Path → /adoption.html. The stages themselves change nothing.

## 5. Industries page
At the existing per sector deploy CTA, adjust the line to:
`Deploy [sector] intelligence on your own hardware. Adoption starts with a Site Read.`
Both phrases link (adoption → /adoption.html, Site Read → /site-read.html). One line only; the industries page stays about sectors.

## 6. Partners page
Add one framing sentence to the intro:
`However a partnership is structured, what the partner carries to the client is the same Adoption Path: assessment, an owned deployment, a measured acceptance, and a trained staff.`
Link → /adoption.html.

## 7. Security and Data page
Add one sentence in the offline section:
`In the published abandonment data, the obstacles organizations cite most are cost, data privacy, and security. The architecture on this page is why a Manar adoption does not carry those obstacles: there is no data leaving to secure in someone else's cloud, and no per query bill.`
Attribution inline: `(S&P Global survey, 2025)` in the site's fine print style. This is the security page's single statistic.

## 8. National AI Policy page (policy.html)
Add a short section or closing paragraph:
`Adoption is where policy meets ground. The policy calls for local AI products, sectoral transformation, and a trained workforce. Every Manar engagement contributes all three on a small and concrete scale: a local product deployed in a Pakistani institution, a sector's work transformed, and named staff trained to run what they own. How that happens in practice is the Adoption Path.`
Link → /adoption.html. Claims stay at alignment of direction, never endorsement, per the evidence file rules.

## 9. About page
One sentence added where the working method is described:
`The company's frame for every engagement is adoption: not whether a model was installed, but whether the organization was changed and equipped by it.`

## 10. Careers page (light touch, optional)
The intro already says the practical part of the job is visiting a site and building for that ground. Optionally append: `That is the Adoption Path, and every role here serves a stage of it.` Skip if it reads as decoration; the careers voice is already right.

## 11. Consistency checklist (run before merge)
- [ ] Nav and footer updated on every page in the same commit set
- [ ] Sitemap.xml includes /adoption.html; meta and OG tags present per doc 11
- [ ] Statistics count: homepage one (Stanford), security page one (S&P), adoption page three; nowhere else on the site carries a number from the evidence file
- [ ] Every statistic matches its doc 10 approved phrasing, with source and year
- [ ] No em dashes and no prose hyphens introduced anywhere in these edits
- [ ] Registry counts untouched: six families, seventeen models, nine sectors appear exactly as before, since this work adds no model and no family
- [ ] FAQ page (dedicated) receives the same new question as the homepage FAQ so the two stay aligned, which was a known past drift point
- [ ] Ownership language on the adoption page agrees with the homepage FAQ ownership answer
- [ ] All new internal links resolve; no external links added anywhere by this work

## 12. Sequencing for the IDE
1. Build /adoption.html complete per doc 11.
2. Apply edits 1 through 10 in one pass.
3. Run checklist 11.
4. Farabi reviews the adoption page live on a preview, then the commit set merges as one.
