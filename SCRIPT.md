# Workshop Script · Claude Code for Business

**Total runtime:** ~90 min · 25 slides · ASB · April 2026

Speaker notes per slide. Italics = stage directions. **Bold** = hit hard. Times are approximate.

---

## Slide 1 · Title (1 min)

*Stand still, let the room settle. Don't start until it's quiet.*

> "Good morning. I'm Sharan. I graduated from this school in 2018. What I want to do in the next ninety minutes is something very specific: not talk about AI, not show you tools you'll forget next week. **Teach you to build the tools your actual job needs.** No engineering background. No code. By the end, everyone in this room will have one working on their laptop. Let's go."

*Click to slide 2.*

---

## Slide 2 · About me (2 min)

> "Quick thirty seconds on why I'm the one up here. I was in these exact seats, Class of 2018. After ASB: AirAsia, senior PM. MIT Sloan for the MSMS. Amazon on the Ads Science and ML team. Co-founded a healthtech startup. Head of Product at Roshn, a Saudi real estate group, led the digital transformation. Today I'm co-founder and CPO of Lumif.ai, where we're automating insurance compliance for subcontractor-heavy industries."

> "The reason I'm telling you this is not the resume. It's this line, right here." *Point to the right panel.* "**Everything I'll show you today is what I actually use.** Not a demo. Not a prototype. This is the system I open every morning to run Lumif.ai. By the end, you'll have the first version of a skill built for *your* work."

*Transition: "Let me show you what that looks like. No slides for a few minutes. Watch."*

---

## Slide 3 · Demo 1 · Legal Reviewer (4 min · LIVE)

*This is a cold open. Skip over reading the slide. Flip to terminal.*

> "Every one of you deals with contracts. NDAs. Vendor agreements. Offer letters. Most people don't read them. Fewer still can tell what's normal from what's a trap. Watch."

*Drop a contract PDF. Run the skill. While Claude works, narrate:*

- "Notice: no upload. No web tool. The PDF is on my disk. Claude reads it there."
- "It already knows I'm a buyer, not a vendor. Memory. Told it once, months ago."
- "The output is going to be a file. A one-page brief. Markdown. I'll share it with my lawyer."

*When the file appears, open it. Read the first two bullets out loud.*

> "That took about ninety seconds. The first time I needed this, it took me two hours to read, research, and write. Now, every contract I touch runs through this."

*Back to deck.*

---

## Slide 4 · That wasn't a chat window (2 min)

> "So what did you just see? Let's be precise. Because most of you, when you hear 'AI,' picture ChatGPT. A chat window. That's not what that was."

*Left card:*
> "A chatbot lives behind a chat window. It answers questions. It can't reach your files. Can't drive your browser. Can't run while you're asleep. And critically, **it can't be packaged and shared as a recipe.**"

*Right card:*
> "Claude Code does work. It reads files. Runs tools. Remembers preferences. Produces real deliverables on disk in the shape you asked for. And the thing that made it do all of that was a **skill.** Thirty-eight lines of plain English in a file."

*Pause. Then callout:*

> "That skill is the primitive of this entire talk. Everything else is just how you write one, share one, and stack them to collapse the work you keep redoing."

---

## Slide 5 · Why now (2 min)

> "Fair question: why now? Why not two years ago? I want to walk you through four years in thirty seconds."

- "**2022.** ChatGPT goes mainstream. Smart, bounded, sealed off from your actual work."
- "**2024.** Prompt chaining, early tool use. First real workflows. Still fragile. Still needed engineers."
- "**2025.** Agents. Memory. MCP. Models can plan, act, observe, iterate. Pipelines start to work reliably."
- "**2026.** Skills. Anyone who can write a paragraph can teach an agent a job. **That's today. That's this room.**"

*Callout:*
> "You're not early to AI. You're early to using it properly. That's a different thing."

---

## Slide 6 · The ladder (2 min)

> "One mental model and we move on. Four rungs. Each one includes the rung below and adds one new power."

- "**Rung one: LLM chat.** Question in, answer out. ChatGPT tab."
- "**Rung two: workflow.** Step, step, step. Zapier with AI bolted on."
- "**Rung three: agent.** Plan, act, observe. Repeat until done. Claude Code, right here."
- "**Rung four: skill.** An agent plus an expertise file becomes a specialist."

> "Barry Zhang at Anthropic puts it cleanest: '**Agents are models using tools in a loop.**' Add a skill, and that loop has expertise."

---

## Slide 7 · A skill is a folder (2 min)

> "I'm going to demystify this hard. Because when people hear 'skill,' they picture code, deployments, infrastructure. It's none of that."

> "**A skill is a folder. With markdown in it.** That's the whole thing." *Let it breathe.*

*Point at the tree:*
> "This is the entire Legal Reviewer skill on my machine. One SKILL.md, thirty-eight lines. A couple of example files. That's it. **You can read it. You can edit it. You can send it to a friend like a recipe.**"

---

## Slide 8 · Anatomy (2 min)

> "Let's open SKILL.md. Two sections, always."

*Point at code:*
- "**Frontmatter** — metadata at the top. Name and description. That's how Claude decides *when* to use this skill."
- "**Body** — plain-English instructions. Treat it like a note to a smart new hire on their first day. Tell them what the job is, the steps, the tone, where to save the output."

*Callout:*
> "If you can write a paragraph explaining how you do your job, **you can write a skill.** That's the bar."

---

## Slide 9 · The context stack (2 min)

> "Before we get to demo two, one more piece. Because writing a good skill requires understanding what Claude already knows about you. Three files. Loaded automatically, every session. None of them are code."

- "**CLAUDE.md** — your standing rules. How you want Claude to work. 'Bullet points by default. Save to this folder.'"
- "**memory/\*.md** — your history. Facts Claude has learned. Grows every session. 'User is a buyer. Prefers bullets. Active on a vendor selection.'"
- "**skills/{name}/SKILL.md** — your playbooks. Recipes for specific jobs."

*Callout:*
> "The first two teach Claude **you**. Skills teach it **jobs.** Every skill you build stands on both."

---

## Slide 10 · Matrix + onboarding (2 min)

> "Two ways to feel this. First — the Matrix. Humor me."

*Play video. Don't talk over it.*

> "Kung fu takes years. Neo loads a file. He opens his eyes: 'I know kung fu.' **That is what a skill is.** You don't train the model. You hand it a file, and it has the expertise."

*Right side, more grounded:*
> "Anthropic puts it less dramatically: **'Building a skill is like putting together an onboarding guide for a new hire.'** Same idea, suit-and-tie version. Contract to review, Claude knows contracts. Deck to build, Claude knows slides. Your specific job? That's what you'll write today."

---

## Slide 11 · Andrew Chen (1 min)

> "One more frame before we build. This is from last week. Andrew Chen, general partner at a16z. I'll read the circled bit."

> "'We'll soon view coding the way we view using spreadsheets today: **a commonplace skill every white-collar worker is expected to have.**'"

> "His timeline: under eighteen months. Every job description."

*Close line:*
> "Excel made everyone an analyst. Claude Code makes everyone a builder. **If you're not building, you're the person still doing the job by hand while your colleague runs a skill.**"

---

## Slide 12 · Demo 2 · PPT (3 min · LIVE)

> "Okay. Demo two. Different domain. Same pattern."

> "Setup: sixty minutes before a pitch. Ten slides needed. Normally: research, outline, design, build. Three hours."

*Run the skill. Take a topic from the room if you can.*

> "Three things to watch:"
- "This is a skill **someone else built.** The pptx skill. Claude loaded it automatically the moment it saw 'deck.'"
- "Content and design, together. Claude decides what goes where, in what order, with which chart type."
- "Not a preview. A real .pptx. Opens in PowerPoint or Keynote. Edit, send, done."

*When the file opens — stop talking. Let them see it.*

---

## Slide 13 · Demo 3 · GTM (4 min · LIVE)

*Switch to dark slide. Signal: this one matters.*

> "Demo three. The one I actually use every day to run Lumif.ai."

> "I'm a founder. Sales is half my job. Finding the right person at the right company, researching them, drafting a note that doesn't sound like spam. Thirty minutes per prospect, pre-Claude."

*Run the skill.*

> "Watch the pipeline. One command. I describe my ideal customer. The skill finds three real people, researches each, drafts a personalized email plus a LinkedIn note, logs to my CRM. **Six tools, one skill, one command.** Each arrow you'll see is a Claude decision, not a human step."

*When it's done:*
> "Important disclosure." *Point at warn box.* "What I just ran targets a market I don't sell into. Real people, real public data, but no one I'd ever pitch. **Real outreach gets human review before any send. Always.**"

---

## Slide 14 · Pause (1 min)

*Step back from the laptop. Look at the room.*

> "Let's land. Three demos. Three jobs done. Lawyer work. Slide work. Salesperson work."

> "Each skill: a short file. No code, no deployment."

> "Each one: built once, runs forever."

*Lean in:*
> "Now imagine thirty of those. **For everything you do twice.** That's what we're here to teach."

---

## Slide 15 · Rate limits (3 min)

*Tone shift: serious.*

> "Before we build, one slide you need to take seriously. **Power comes with rate limits.**"

*Hands-up:*
> "Quick show of hands — who's been rate-limited or flagged by LinkedIn, Gmail, or a CRM?" *Wait. Some hands will go up.*

> "Automation amplifies. Cross a ceiling and you get flagged, suspended, or banned. Permanently. This table is not a guideline. It's the line."

*Skim top to bottom. Hit the LinkedIn row hard.*

> "LinkedIn: twenty to twenty-five connection requests a day. You can ban your account forever in one afternoon of being too eager. Don't."

*Callout, read all three:*
> "**One. Never auto-send to a real human without human review.** Two. Respect captchas — they exist for a reason. Three. The skill is your assistant, not your replacement."

---

## Slide 16 · Why a terminal (2 min)

> "Last question before we build. You're about to open a terminal. A lot of you don't live there. Fair question: why?"

*Left card:*
> "Claude Code runs in your terminal. Mac, Windows, Linux. **Full agent power** — every tool, every hook, every pipeline, sub-agents, scheduled runs. It's unfamiliar for the first thirty minutes. Then it's not."

*Right card:*
> "There's also Cowork. Same Claude, same skills, but click-and-type. Lives in the Claude Desktop app. Launched January 2026. Part of Pro and Max plans. Gentler on-ramp, lower ceiling."

*Callout:*
> "Today, we're in the terminal. Push through the first half hour. Once this workshop is over, go explore Cowork on your own as a lighter alternative for your day-to-day. **But for the next sixty minutes, we're on the most powerful version.**"

---

## Slide 17 · Build intro (1 min)

*Energy up.*

> "Your turn. We're building **Job Hunt Copilot.**"

> "Paste any job URL. You get back a tailored resume, a personalized cold email, a LinkedIn note, research on the hiring manager, and a row added to your tracker."

*Left card:*
> "Why this one? Two reasons. One, it works on every job site. Two, and this is the real reason — you'll reuse this exact pattern for everything. URL in, memory, tailored files out. That's half your recurring work."

*Right card:*
> "Finish early? Card 8. Build Meeting Prep Copilot in a single paste. Same architecture, different domain. Proves the pattern generalizes."

---

## Slide 18 · The outcome (2 min)

> "Before we start, let me show you what's going to exist on your laptop in thirty minutes."

*Left pre:*
> "The skill itself — one SKILL.md file. Plus your saved preferences in memory. **Resume once, tone preferences once.** Never type those again."

*Right pre:*
> "For every job you run it on, a folder. Job description, tailored resume, cold email draft, LinkedIn note, hiring manager research. And the tracker spreadsheet grows by one row."

*Callout:*
> "**Everything is a file.** You can edit, share, version-control, or attach it to an application. No chat history to lose. No app to depend on."

---

## Slide 19 · Cards 1 to 3 (setup + 10 min of building)

> "Sixty-second setup. Three things."

- "One. Terminal open, type `claude`, hit enter."
- "Two. Open the prompt cards page in a new tab. Link is on the slide."
- "Three. Have a real job URL ready. Any job. LinkedIn, a company careers page, doesn't matter."

> "Now — Cards 1 through 3."

- "**Card 1 · Create.** Paste it in. Claude will write SKILL.md. When it's done, open the file. Read it. **That file is your skill.** Nothing else."
- "**Card 2 · Memory.** Teach it your resume. Paste Card 2. Claude will ask once, save it, and never ask again."
- "**Card 3 · Run.** Paste a real job URL. Watch the pipeline run. Ninety seconds to three minutes."

*Stage direction: circulate. Help people past their terminals. This is where the room splits into the fast and slow.*

---

## Slide 20 · Cards 4 and 5 (8 min of building)

> "You have a working skill. Two more cards to make it yours."

- "**Card 4 · Refine.** Lock in your voice. Save tone preferences so every future run follows them. **This is the moment skills compound.** After five jobs, drafts feel like they came from your hand, not Claude's."
- "**Card 5 · Verify.** Ask Claude to show you everything it created. SKILL.md path, saved resume, tone preferences, each output folder, the tracker. **If you see all of it, you've built a working skill.**"

*Callout:*
> "Tomorrow, on the next job you find, you only paste Card 3 with a new URL. The skill does the rest."

*Stage direction: when ~80% of room has done Card 5, move on.*

---

## Slide 21 · The reveal (3 min)

> "Pens down. Everyone look up."

> "What you just built is **version one.** Here's version three. Same skill, a weekend of work. Now it also does this:"

- "**Browser auto-fill.** For Lever and Greenhouse, opens the apply page, pre-fills everything. You review, you click submit."
- "**Batch mode.** Paste ten URLs. Skill fans out in parallel via sub-agents. One consolidated tracker."
- "**Follow-up scheduler.** Every outreach logged. Reminds you at day five and day twelve. Drafts the follow-up notes when the time comes."
- "**Calendar integration.** Recruiter replies with slots? Parses the email, checks your calendar via MCP, drafts a reply with availability."

*Callout:*
> "**None of this is hard.** Same pattern, applied four more times. You can do this by Sunday night."

---

## Slide 22 · Best practices (2 min)

> "Four things I've learned the hard way. The kind of thing you only learn by breaking something."

- "**One. Always review before sending.** Drafts to file. Human eyes before any human reads it."
- "**Two. Save preferences as you discover them.** When Claude does something you want every time, say so out loud. The memory file is your training data."
- "**Three. Think like your agent.** When it misfires, ask: what did Claude actually *see* in its context? Its mistakes make sense from inside its view."
- "**Four. Outputs are files. Always.** Don't let work disappear into chat history. Every skill saves a deliverable to disk."

*Warn card, louder:*
> "One rule above all rules: **Never store secrets** — API keys, passwords, financial credentials — in skill files, memory files, or anything that could end up on someone else's screen."

---

## Slide 23 · What to build next (2 min)

> "You'll leave with Job Hunt Copilot. Here are five more I'd build this weekend if I were you."

*Walk the six cards briskly, one line each:*
- "**Meeting Prep.** Paste a calendar invite, get a 1-page brief."
- "**Case Study Analyzer.** Drop a case PDF, get the frameworks and the cold-call questions."
- "**Personal CRM.** Every person you've met, with notes. Searchable forever."
- "**Industry Tracker.** Weekly roundup of your industry, cited. Runs on a schedule."
- "**Coffee Chat Follow-up.** One command after every networking event. Thank-you, LinkedIn note, CRM entry."

*The pattern card:*
> "And this is the meta-recipe. **Notice yourself doing the same thing twice. Describe it in plain English. Make it a skill. Refine over a week. Done.**"

---

## Slide 24 · Resources (1 min)

> "A few links so nothing is lost when you leave this room."

- "claude.ai/code — install Claude Code."
- "docs.claude.com — everything."
- "The two Anthropic engineering posts — 'Building Effective Agents' and 'Equipping Agents for the Real World.' Both excellent. Read them this weekend."

> "All the materials from today — this deck, the nine prompt cards, links — live here." *Point at URL.*

> "**sharan0516.github.io/asb-workshop** · password `ASB2026`."

*Dark card, voice warmer:*
> "My ask. If you build something cool with this — a skill that saves you hours every week — **tell me about it.** Email me. I'll read every reply and send back a critique plus ideas to extend it. No filter, no form. Direct."

---

## Slide 25 · Q&A (rest of time)

> "Questions? Then go build something for the boring task you did this week."

*Pause. Let a hand go up.*

**Likely questions to prepare for:**
1. *"How much does Claude Code cost?"* — Pro plan, $20/month. Max for heavier use. Same account as Claude.ai.
2. *"Can I use this for [industry / regulated data]?"* — Data goes to Anthropic's API. Check your company's policy. Enterprise tier has tighter controls.
3. *"How do I share a skill with my team?"* — It's just a folder. Git repo, Google Drive, email. Anyone who drops it in their `~/.claude/skills/` gets the same skill.
4. *"Will skills still work in a year?"* — Yes. Plain markdown doesn't break. The agent gets better; the skill stays.
5. *"What if I don't have a technical background?"* — You just built one. That's the answer.

*Close:*
> "Thank you, ASB. Kuala Lumpur. April 2026. Go build."

---

## Delivery cheat sheet

- **Don't read the slides.** They're for them, not you. Look up.
- **The three demos are the anchors.** If a demo fails, laugh, narrate the failure (it's instructive), and move on. Do not get stuck.
- **Time check at slide 14.** You should be ~30 min in. If you're behind, trim slide 5 (timeline) next pass.
- **Time check at slide 17.** Build section starts here — ~30 min. Protect it. Let everything after it shrink.
- **Energy map:** calm opening (1-2), curious (3-11), showcase (12-14), serious (15), practical (16-20), fun reveal (21), warm close (22-25).
- **The one line they should remember:** *"If you can write a paragraph explaining how you do your job, you can write a skill."* Repeat it at least twice.
