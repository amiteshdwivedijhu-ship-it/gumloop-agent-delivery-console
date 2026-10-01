# GOAL.md - Gumloop (2-hour build)


## Standing rules (keep in every GOAL.md)

### Prototype, not demo-as-deliverable
Build a working prototype Ami can walk through in 90 seconds. The deliverable is the prototype. The 90-second demo is only how Ami presents that prototype. Do not treat a demo as the thing you ship.

### UI observation (mandatory)
Public sources only: website screenshots, demo videos (with timestamps), product tours, docs, help center, app-store screenshots, changelog images. Never sign up, create accounts, or log in.

Every GOAL.md must include `## Their UI` before Acceptance criteria, with subsections in this order:
1. Sources
2. Layout
3. Visual style
4. Tone of UI copy
5. The exact screen where my proposed improvement would live
6. Build instruction (match their visual style and terminology so the prototype looks like a feature inside their product)

Be honest: if only marketing illustrations are visible, say "marketing UI only" and infer carefully. If no UI is publicly visible, say so, describe what can be inferred from docs, and default to a clean neutral style.

Writing: simple English. No em dashes or en dashes.

### Phone / mobile UX (mandatory for the prototype)
- Include a proper viewport meta tag so the layout respects phone width.
- Design mobile-first for about 375px width (stack everything vertically).
- No horizontal scroll at phone width.
- Touch-friendly primary actions (about 44px min height / tap target).
- Readable type on a phone (comfortable body size, clear hierarchy).
- No overlays, sticky bars, or modal chrome that clips content or blocks CTAs.
- Good mobile UX overall: one-column flow, large CTAs, thumb-reachable primary actions.

## Role this GOAL targets
- **Open role (LOCKED):** Forward Deployed Agentic Engineer
- JD: https://jobs.ashbyhq.com/gumloop/f5b326dc-99b0-4a4f-bad4-b3ba54b32d2e
- Careers board: https://www.gumloop.com/careers (Ashby)
- Location: San Francisco Office or Vancouver Office. On-site (JD). Travel up to ~30% to customer sites.
- Comp (public): $175K to $265K + equity (Ashby; multiple ranges)
- Core job (from JD): One of Gumloop's first FDEs. Embed with enterprise customers post-contract. Own technical delivery discovery → deployment. Scope high-value AI opportunities with operators and executives. Map processes, connect systems, structure data. Build/test/deploy/iterate Gumloop agents. Measure success by adoption and business impact. Partner with Customer Success and Education for ownership handoff. Turn deployments into reusable patterns and Product/Eng feedback.
- Bar notes: ~4+ years technical, shipping agents or connected systems past prototype. CS/math/SWE/DS foundation. Enterprise deployment / process mapping. Comfort with JSON, JavaScript, Git, MCPs. Clear communication. Judgment under ambiguity. Bonus: consulting/PS, prior FDE/SE, agent tooling / MCP / production LLM workflows.
- Sponsorship: JD silent on visa. Confirm early. Do not treat silence as a yes or a no.

## Company brief (8th-grade English)
Gumloop is the multiplayer AI agent builder. Anyone at a company can build, share, and optimize agents with any model and any integration; IT keeps control of data, access, and spend. Product pieces: Agents, Triggers, Skills, Artifacts, connectors / MCP servers, CLI, Chrome extension. Public customers named on JD/site narrative include Gusto, Ramp, Shopify, Samsara, Instacart, Opendoor. Funding claim on JD: over $70M from Benchmark, First Round, YC, Nexus. Docs: docs.gumloop.com. Product: gumloop.com.

## /goal
Build a working **Enterprise Agent Delivery Console** for Gumloop FDAE: load a synthetic post-sale enterprise engagement (process to automate, systems to connect, success metric), show an agent delivery packet (process map, MCP/connectors, skills, trigger, data shape) with cited readiness chips, let Ami choose a human gate (Deploy agent / Need data access / Iterate skills / Escalate to Product), then show adoption impact (runs succeeded, hours saved, owners enabled). Prove Ami can productize execution-first agent delivery in the customer environment, not a toy flowchart. Ami must walk through this prototype in 90 seconds.

**Hard product rule:** Do NOT center the hero on a Rubric Lens strip, pass/fail spreadsheet, or graded eval table. Thin readiness chips are OK as secondary UI only. The hero is engagement stub → agent delivery packet → human gate → adoption impact.

## Live demo
- Status: built, deployed, and verified at phone width
- Link: https://amiteshdwivedijhu-ship-it.github.io/gumloop-agent-delivery-console/
- What it is: Gumloop-styled Enterprise Agent Delivery Console (process + systems → delivery packet → Deploy / Need data access / Iterate skills / Escalate → adoption impact)

## Scope (fits 2 hours)
- Synthetic inputs only (no real Gumloop workspace, never sign in, never create account, never call Gumloop API).
- 1 primary path: synthetic RevOps "CRM update from call notes" process → delivery packet cites HubSpot MCP + Slack trigger + skill → Ami taps Deploy agent → status Live, adoption impact improves.
- Optional second path: customer data silo / missing OAuth → Need data access with listed connectors.
- Optional third path: agent runs but quality low → Iterate skills; or Escalate to Product when platform gap blocks reliability.
- Console must show: engagement stub, delivery chips, gates (~44px), one-line adoption impact.
- Out of scope: live MCP OAuth, real customer data, signed-in Gumloop, Rubric Lens hero, full template marketplace clone, outreach.

## Reuse first
- Reuse citation + human gate craft from https://amiteshdwivedijhu-ship-it.github.io/ mapped to Deploy agent / Need data access / Iterate skills / Escalate to Product.
- Do NOT force Rubric Lens. Do not pitch Ellipsis as a Gumloop customer.
- Vocabulary to prefer: Gumloop, agents, triggers, skills, artifacts, MCP, connectors, Company Brain, Deploy agent, Need data access, Iterate skills, adoption, business impact. Avoid: scorecard-as-hero, Rubric Lens, generic "AI magic".

## Their UI

**Honesty note:** Public sources = gumloop.com (product, use cases, integrations, handbook links), docs.gumloop.com. Sign in exists; never use. No public FDE delivery console observed. Prototype is **inferred field delivery surface**. Say when inferred.

### Sources
- Homepage / product: https://www.gumloop.com/
- Docs: https://docs.gumloop.com/
- Handbook: https://www.gumloop.com/handbook
- FDAE JD: https://jobs.ashbyhq.com/gumloop/f5b326dc-99b0-4a4f-bad4-b3ba54b32d2e

### Layout
- Marketing: agent builder multiplayer positioning, use-case grids, integration/MCP lists.
- Inferred prototype: top = customer process; center = delivery packet; bottom = gates + adoption impact.

### Visual style
- Colors: Gumloop leans modern colorful / soft gradients with clear cards (marketing). Prefer light clean console with a bold primary Deploy CTA (purple or brand accent if visible publicly; else neutral blue-violet).
- Typography: friendly sans.
- Density: medium. Process + connectors, not a Zapier node spaghetti hero.
- Mode: light.

### Tone of UI copy
- Field delivery: process map, MCP, skill, trigger, Deploy agent, Need data access, Iterate skills, adoption.
- Practical, operator-friendly, executive-safe summaries.

### The exact screen where my proposed improvement would live
- An inferred **post-contract delivery** console the FDAE uses from discovery to first production agent run, before CS/Education take ownership. Matches JD.

### Build instruction
- Match Gumloop: light cards, connector chips, skill/trigger labels, large Deploy / Need data access / Iterate / Escalate CTAs.
- Phone UX mandatory.
- Rejected: Rubric Lens hero; empty node graph with no gate.

## Acceptance criteria (must work when Ami demos the prototype in 90 seconds)
1. Load synthetic engagement → show process stub and at least 3 delivery chips (connector/MCP, skill, trigger or data shape).
2. Human gate: Deploy agent, Need data access, Iterate skills, or Escalate to Product. CTAs ~44px.
3. Deploy path updates status to Live and shows adoption impact improving.
4. Optional need-data path lists missing access and keeps deploy blocked.
5. Hero is Enterprise Agent Delivery Console, not Rubric Lens.
6. Phone-width UX mandatory.
7. ~90 second walkthrough.

## What the 90-second walkthrough proves about THEIR problem
Gumloop wants enterprises running real agents on their stack with IT control, and early FDEs own discovery-to-deployment impact (https://www.gumloop.com/ ; JD). This prototype shows Ami can ship the delivery surface that turns a process into connected agents, a clear gate, and adoption metrics.

## TIMEBOX
If not ready at 2 hours: LIGHT pitch = citation + gate craft + 2 mapping lines to FDAE and Enterprise Agent Delivery Console. No Rubric Lens.
