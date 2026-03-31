# Adding the Stack — Automation, Data, and Voice

Parent: [[CLAUDE]]

> You don't need this to get started. The framework works without it.
> Come back here when you're ready to automate.

---

## The Three Layers

### Layer 1 — Supabase (Persistent Data)

**What it adds:** Your task system, session history, and business data persist across all sessions.

**What to set up:**
- Create a free project at supabase.com
- Run the SQL migrations in `Dev/stack-setup/supabase/`
- Add your Supabase URL and anon key to your environment
- Update `Memory/glossary.md` with your project URL

**Core tables:** `tasks`, `session_reports`, `leads`, `outbound_queue`

**Time to set up:** ~1 hour

---

### Layer 2 — n8n (Workflow Automation)

**What it adds:** Your agents can trigger each other automatically.

**What to set up:**
- Create an account at n8n.io (cloud) or self-host
- Import starter workflow templates from `Dev/n8n-Workflows/`
- Connect your Supabase credentials in n8n

**Key workflows to start with:**
- `Lead_Intake` — captures new leads and creates tasks
- `Task_Dispatcher` — routes tasks to the right agent
- `Session_Logger` — writes session reports to Supabase

**Time to set up:** ~2–4 hours

---

### Layer 3 — Retell (Voice Agents)

**What it adds:** Your agents can make and receive phone calls.

**What to set up:**
- Create an account at retell.ai
- Create a new agent using the prompt from `Agents/[your-service-advisor]/PROMPT_TEMPLATE.md`
- Connect a phone number
- Set up the webhook to connect Retell events to n8n

**Requires:** Supabase + n8n already set up

**Time to set up:** ~2–3 hours

---

## Recommended Order

1. Get comfortable with the no-stack version first (at least 1–2 weeks)
2. Add Supabase when session memory starts feeling limiting
3. Add n8n when you want things to happen automatically
4. Add Retell when you're ready for AI phone calls

Don't rush the stack. The methodology works on paper first.

---

## Getting Help

hello@shineon.world — We've been through this setup. We know where the sharp edges are.
