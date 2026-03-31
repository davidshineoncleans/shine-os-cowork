# SHINE OS — Design Decisions & Context

Parent: [[CLAUDE]]
Related: [[TASKS]] · [[LIMITATIONS]] · [[USE_CASES]]

> This file records the key design decisions made during the creation of SHINE OS,
> with the reasoning behind each.

---

## Origin

SHINE OS was extracted from the SHINE Agent Mesh — a live AI operating system built by David Caldicott for Shine On Cleans, a UK cleaning service. The full SHINE system includes n8n workflow automation, Supabase data layer, and Retell voice agents. SHINE OS is the Claude Cowork layer of that system, genericised for public release.

Contact: David Caldicott · hello@shineon.world · shineon.world

---

## Key Decisions

### 1. Name: SHINE OS (not "SHINE Agent Mesh")

**Decision:** The public repo is called SHINE OS, not SHINE Agent Mesh.

**Reason:** "Agent Mesh" refers specifically to the n8n automation layer. That layer is not included in this release. "SHINE OS" correctly describes what this is: an operating system for running your business with AI.

---

### 2. Include n8n + Supabase in the vision from day one

**Decision:** SHINE OS documents the full three-layer stack even though only the Cowork layer ships now.

**Reason:** Users should understand what they're building toward. The no-stack version is more compelling when you can see what it grows into.

---

### 3. License: CC0 1.0 Universal (Public Domain)

**Decision:** CC0. No attribution required by law.

**Reason:** Maximum adoption. The contact line in `CLAUDE.md` ensures David's name is present in every running install as a practical embedding.

---

### 4. One folder, no Cowork Projects

**Decision:** SHINE OS assumes everything lives in a single selected folder.

**Reason:** Simpler to explain, simpler to set up, covers most use cases.

---

### 5. The setup wizard (/shine-setup) is the core product

**Decision:** The `shine-setup` skill is the primary differentiator, not the folder structure.

**Reason:** Anyone can clone a folder structure. The setup wizard customises everything for the user's specific business. That first session experience is what converts users.

---

### 6. n8n Onboarding Agent (planned, not yet built)

**Decision:** The full onboarding vision: landing page → form → n8n provisions tables → generates custom CLAUDE.md → emails setup package.

**Status:** Not yet built.

---

### 7. Control Panel App

**Decision:** Include a self-contained HTML control panel in the setup package.

**Status:** Not yet built. Planned as part of the n8n onboarding session.

---

### 8. TikTok as primary distribution channel

**Decision:** First marketing push via short TikTok videos, positioned as "free, no catch."

**Honest framing:** "This is the thinking layer, not the automation layer." Don't overpromise.

---

### 9. What the repo is NOT selling

**Key distinction:** This is not selling SHINE On Cleans methodology. The cleaning business specifics are stripped. What's released is the general operating model: session conventions, agent structure, task tracking, knowledge graph.

---

## Open Questions

- Repo naming: `shine-os` vs `shineon` vs `shine-agent-mesh`
- One-click plugin install timing
- Control panel design: HTML file or Lovable-hosted?
- Pricing for paid tiers
