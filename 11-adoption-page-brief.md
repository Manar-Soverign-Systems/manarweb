# Doc 11. Adoption Page Brief
## Full Content and Build Spec for the Dedicated Page

**Slug decision.** `/adoption.html`. Considered `/ai-adoption.html` for the search phrase, rejected: the site's page names are single clean words (about, industries, security), the title tag carries the search phrase instead, and internal consistency outranks a marginal slug signal.

**Metadata.**
- Title: `AI Adoption in Pakistan | Manar`
- Meta description: `Most AI pilots fail because the AI was generic, rented, and cloud bound. Manar runs adoption the other way: trained on your data, owned on your hardware, measured before acceptance, operated by your staff.`
- OG title: `Adoption, on your ground` · OG description: same as meta · og:image, locale, twitter tags: inherit site defaults.

**Navigation.** Add to the Pages menu and both footers between Site Read and About. Label: Adoption.

**Build notes for the IDE.** Reuse existing components only: the numbered belief block style for the failure causes, the five step methodology strip style for the path, the chip row style for the What arrives section, the two card Related footer, the standard contact CTA. No new component types. Statistic attributions render as small muted text directly under each figure, same treatment as existing fine print. The page carries exactly three statistics per the evidence file rules; do not add more anywhere on it.

---

## Draft copy (verbatim, follows all Manar copy constraints)

### Hero
Eyebrow: `Adoption`
H1: `Everyone bought AI. Few were changed by it.`
Subline: `The record on generic AI adoption is now public, and it is poor. Not because the intelligence is weak, but because of how it was adopted: generic, rented, cloud bound, and gone when the consultants left. Manar runs adoption the other way.`
Buttons: `Start with a Site Read` → /site-read.html · `Open a conversation` → /contact.html

### Section: The record
Header: `What the studies found`
Lead: `Three findings, from three independent sources, describe the same failure.`

Stat block 1: `95%`
Line: `of enterprise generative AI pilots returned nothing measurable. The authors' diagnosis was not model quality. Generic tools do not learn the operation they are dropped into.`
Attribution: `MIT, The GenAI Divide: State of AI in Business, 2025`

Stat block 2: `42%`
Line: `of companies abandoned most of their AI initiatives before production, up from 17 percent a year earlier. The obstacles they named most: cost, data privacy, and security.`
Attribution: `S&P Global Market Intelligence survey, 2025`

Stat block 3: `280x`
Line: `is how far the cost of generic AI intelligence fell in eighteen months. What everyone can rent for pennies is an advantage to no one.`
Attribution: `Stanford HAI, AI Index Report, 2025`

Closing line: `Read together: adoption is failing while the technology is succeeding. The failure is in the approach, and its causes are now known.`

### Section: Why adoption fails
Header: `Four causes. Four reversals.`
Intro: `Across the published research, the same causes repeat. Manar's method was built against each of them.`

01 · `It was generic.`
`A tool trained on the world in general knows nothing about your operation in particular, and it cannot learn it. Manar starts from a registered model and trains it on your data until it knows your conditions. Specific beats general. Always.`

02 · `It was rented.`
`A subscription builds no asset. When it ends, nothing remains on your books but the invoices. A Manar deployment is owned from handover: the model, the hardware, and the growing record of your own operation.`

03 · `It assumed the cloud.`
`The most cited obstacles in the abandonment data were cost, data privacy, and security. All three are properties of sending your data to someone else's computer. Manar's systems run inside your walls, offline if required, so the obstacle is removed rather than managed.`

04 · `It left with the consultants.`
`Advice departs. Capability stays. A Manar engagement is complete only when your own staff operate the system without Manar in the room, and it keeps learning your operation after we leave.`

### Section: The Adoption Path
Header: `Five stages. One direction.`
Intro: `Adoption at Manar is a defined path, not an open engagement. Each stage ends in something you can see, hold, or measure.`

`01 Site Read` · `A paid, scoped reading of your site: what runs, what sits unread, which registered model reads it first, and on what hardware. You receive a written finding either way.`
`02 First Deployment` · `Before work begins, we agree what will be measured and what number means acceptance. Then one registered model is trained on your data and installed on hardware you own. It is accepted when it meets the number, not when it is installed.`
`03 Handover` · `Your staff are trained on the running system. The stage is complete when they operate it without Manar in the room, demonstrated, not promised.`
`04 Registry Expansion` · `A new kind of work gets a model trained for it, on the same ground, reading what your systems already produce. Nothing is rebuilt from nothing.`
`05 Compound` · `The system retrains as your record grows. Accuracy on your conditions deepens with every month it runs, a record no later competitor can shortcut.`

Link: `How Manar builds →` /methodology.html

### Section: What arrives
Header: `Adoption that arrives in a box.`
Body: `Manar deployments are hardware and software together. Stage one specifies the machine. Stage two arrives with it installed. Stage three hands you the keys. What remains on your site when the engagement closes: hardware you own, sized to the job. A registered model trained on your data. Your staff, trained and operating. A number, measured on your own conditions, that the system met before you accepted it.`
Chips: `Hardware you own · A model that knows your ground · Staff who run it · A number it had to meet`

### Section: The national direction
Header: `Inside the national direction`
Body: `Pakistan's first National AI Policy, approved in July 2025, calls for local AI products, sectoral transformation, secure and ethical deployment, and one million trained professionals by 2030. Manar's work sits inside that direction: local products, deployed in Pakistani institutions, operated by Pakistani staff trained on the systems they own.`
Link: `Manar and the National AI Policy →` /policy.html

### Section: Before you ask (FAQ, page local)
Q: `We already tried AI and it did not stick. Why would this be different?`
A: `Then you are exactly who this path was designed for, and what you saw has now been measured across thousands of organizations. The pilots that failed were generic, rented, and cloud bound. This path reverses each of those properties, and stage two does not complete until the system meets a number we agree on your conditions before work begins.`

Q: `Is this consulting?`
A: `No. Every adoption engagement ends in a deployed, owned, measured system or it does not happen. Advice without deployment is not what Manar sells.`

Q: `What does adoption cost?`
A: `It begins with a Site Read, which is scoped and priced as a defined engagement. Deployment is priced on the finding, sized to what your operation actually needs.`

Q: `Who owns everything at the end?`
A: `You do. The model, the hardware it runs on, and every byte of the record it builds. Nothing is licensed back and nothing depends on Manar continuing to exist for your system to keep working.`

### Closing CTA
Header: `Open a conversation.`
Line: `Tell us what you run and what sits unread. We will tell you where adoption starts on your ground, and reply within two working days.`
Button: `Send inquiry →` /contact.html

### Related footer
Card 1: `Related · Site Read · Stage one of the path.` → /site-read.html
Card 2: `Related · Security and Data · Why nothing leaves.` → /security.html

---

## Copy compliance checklist (IDE verifies before commit)
- [ ] No em dashes anywhere on the page
- [ ] No hyphens in prose (identifiers, slugs, and file names excepted)
- [ ] Exactly three statistics, each with source and year, matching doc 10 approved phrasings
- [ ] No competitor or lab named, no client named, no endorsement implied in the policy section
- [ ] Ownership FAQ answer consistent word for word in spirit with the homepage FAQ answer
- [ ] All internal links resolve; page added to sitemap and nav in the same commit
