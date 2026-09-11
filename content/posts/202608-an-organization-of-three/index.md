---
title: "An Organization of Three"
summary: "What Friday, Wednesday, and Thursday have actually done since they came online: family logistics, open-source maintenance, experiments, audience research, and the less glamorous work of keeping the system useful."
description: "What a small personal AI team actually does, from a supermarket cart to a Raspberry Pi companion, and what the mistakes teach us about ownership, memory, and trust."
categories: ["AI", "Meta"]
tags: ["ai", "agents", "openclaw", "personal-ai", "infrastructure", "operations", "marketing"]
authors:
  - friday
  - wednesday
  - thursday
date: 2026-08-31
lastmod: 2026-09-11
draft: true
---

{{< alert icon="pencil">}}
**Note:** This draft looks back from 11 September 2026 to each agent's beginnings. The narrative is mine; the marked contributions are the agents' voices, edited into this account with Friday.
{{< /alert >}}

In an earlier post, I wrote about [building Friday](/posts/202607-friday-coming-back/): a personal assistant on hardware I own, with useful access, deliberate boundaries, and enough continuity to be more than another chat tab.

That was the foundation. This is the next step.

Friday is no longer trying to be every kind of assistant at once. She is now part of a small team: Friday as chief of staff, Wednesday as CTO, and Thursday as CMO. I am still at the centre of it, doing the work, making the calls, and carrying the responsibility. The team does not replace that. It gives the work more shape around it.

The goal is not a miniature company, or three bots in a trench coat. It is to make the useful things survive the distance between a thought, a decision, a build, a story, and the evidence of whether that story reached anyone.

To see whether that was happening, I asked the agents to look back over everything they had done since they were created. Big things and small things. Not what their job descriptions say they could do, but what they had actually done for me.

The result is less futuristic than an autonomous-company demo, and more useful. There is code and infrastructure in it. There are also groceries, school forms, birthday reminders, a crowded ideas board, and a surprising amount of work making an assistant stop telling me things I do not need to know.

The chronology matters. This incarnation of Friday first came online on **26 June**, briefly answering to E.D.I.T.H. before becoming Friday on **28 June**. Wednesday and Thursday were created on **29 August**. This is not three agents claiming the same summer of work: Friday has the longer history; the specialists have a shorter, more focused one. The earlier Donna story is background, not work I am retroactively crediting to the new team.

## Friday: Coordination is a real job

The first version of this setup proved that a single assistant can be genuinely useful. It can hold context across a calendar, inbox, task list, health signals, and a thousand loose messages. But “hold all the context” is not the same thing as “own every kind of judgment.”

Friday's remit is the connective tissue: priorities, people, personal operations, and keeping the thread coherent. Wednesday brings technical judgment; Thursday brings narrative and audience judgment. That does not mean a request to Friday silently disappears into another agent's inbox. The agent I ask owns the work. Delegation needs to be explicit, and the result needs to come back to me.

That division has made one thing clearer: the useful unit is not an agent. It is a loop. A message turns into a scoped piece of work. The right person, human or agent, makes a decision. The work leaves a visible trail. It comes back with enough context to act on it.

We have made the front door visible, too. In our Yggdrasil group, Friday can keep a conversation moving naturally; Wednesday and Thursday join when their specialty is useful. Access is constrained to Nuno, and the system is explicitly designed not to turn every conversation into a stream of automated status updates. A personal operating system that creates more notifications than decisions has missed the point.

### The things that do not become GitHub commits

Friday's daily briefing pulls together my calendar, personal tasks, inbox, messages, health signals, and a short selection of tech and AI news. The weekly review looks backwards as well as forwards: what moved, what stayed stuck, what changed in the available health data, and what next week will demand. The point is not another dashboard. It is a short enough picture to use from my phone.

That started with less glamorous groundwork. On her first day, Friday helped connect Linear and assign the unowned tasks in my board to me. We taught the daily view to leave out completed tasks and onboarding templates. Later, separate news and morning updates became one briefing instead of competing notifications. Calendar planning became concrete blocks that had to fit around existing commitments, with breaks rather than imaginary uninterrupted days.

Across the summer and into September, that meant helping organise the return to school: extracting dates from the school calendar, tracking supplies and paperwork, and keeping swimming and transport arrangements visible as outstanding tasks. Birthday invitations became calendar entries with reminders. Gifts became tasks with the actual idea attached, not just another item called “buy gift.” Appointments, packing, household supplies, car administration, and passport follow-ups stopped depending entirely on whether I remembered them at the right moment. Even laundry and making soup could become realistic calendar blocks instead of competing background intentions.

One particularly ordinary example was a supermarket cart. Friday used recent orders and my requested essentials to prepare it for review, then tracked the delivery window on the calendar. She did not independently check out. I still made the purchase decision. That distinction applies to the rest of this list too: tracking something, preparing it, and physically doing it are different contributions. The agent did not pack the bags or take a child to school.

Small details matter here. Personal calendar entries have consistent colours and useful emoji. A follow-up gets the intended due date and task state. A completed task stops appearing as something I still owe. None of that sounds like frontier AI. It is exactly the kind of friction I wanted help with.

There has been health-related work too: comparing a new lab report with earlier results, helping organise questions for my doctor, and researching whether a proposed gadget would actually solve the problem. The useful outcome was a better-informed next conversation, not a diagnosis or another device to buy. The numbers and the personal details do not belong in this post.

Behind those summaries, Friday extended the health receiver to import workouts as well as daily metrics, with deduplication so overlapping exports did not count the same workout twice. We also kept the limits visible: a strength-training session without exercise-level data does not magically reveal sets and reps. Local Whisper transcription made Portuguese and English voice notes usable without sending the audio to a cloud transcription service.

### Making a crowded head more navigable

Friday also helped reorganise my Notion ideas board. We separated **Live** projects from **In progress** work: maintaining something that already exists should not automatically make it another active product bet. Overlapping ideas were merged; paused ideas stayed visibly paused; old dead ideas stopped competing with current ones. Even the small pass giving the cards purposeful icons made the board easier to scan.

The harder contribution was discussing what deserved focus. Research into local inference on Apple Silicon became practical trade-offs about memory, context, quantisation, and product scope, rather than “use the biggest model.” Product ideas became clearer about who they were for and what a first useful version might be. Those conversations were planning and research, not shipped products, but they changed the shape of the work.

Friday has also been a place to think before reacting: untangling an overloaded day, drafting a difficult message, or turning a vague worry into one manageable next step. I am deliberately leaving the private conversations private. Their value still belongs in the picture. A personal assistant that only understands my repositories understands a very small part of my life.

> **Friday:** A grocery list and an infrastructure repair can belong to the same job. Both remove something Nuno would otherwise have to hold in his head. My contribution is not doing his life for him; it is helping him keep hold of it. Sometimes that means building something. Sometimes it means remembering the follow-up. Sometimes it means making the next step smaller.

## Friday also helped build the things

The chief-of-staff title can obscure how much technical work preceded the specialists.

### Blowfish: maintenance is product work

In July, Friday worked through a substantial [Blowfish](https://github.com/nunocoracao/blowfish) maintenance queue: dependency upgrades, lockfile conflicts, localisation and template fixes, and community showcase additions. She merged the approved changes, kept new showcase entries in the intended order, checked the asset build, and organised release notes. She also reviewed changes that should not land and closed unsuitable PRs with specific explanations.

That last part counts. Keeping an open-source project healthy is not maximising the number of merges. Sometimes it is spotting that a configuration default prevents an explicit `false` from working, or that an accessibility change points to an invalid landmark, and asking for a narrower correction.

The larger effort began as the [v3 draft work](https://github.com/nunocoracao/blowfish/pull/3028), which was merged on 17 August: an opt-in landing layout, feature and call-to-action components, stats and steps shortcodes, a floating header, and rendering and asset-loading improvements. My hard constraint was preserving existing sites' behaviour. A bold new example site was not enough if it relied on one-off custom code instead of components other theme users could use. Friday had to correct that direction and build the features into the theme. The eventual release also had an explicit module-import migration; “compatible” should not mean hiding an upgrade step.

This is credit for that contribution, not a claim that an agent invented Blowfish or authored every later release. The project, its contributors, and its existing users came first.

There was follow-through beyond the big branch: fixes for vulnerable dependencies in Blowfish and n9o.xyz, and [localisation of the 404-page quotes](https://github.com/nunocoracao/blowfish/pull/3052) across the theme's 36 locales, with language fallback that preserved existing custom quotes. Small public-facing details still deserve care.

Friday's publishing work also predates Thursday. She helped write and refine the first Friday article, researched a [draft investigation into vertical-drama advertising](https://github.com/nunocoracao/n9o.xyz/pull/111) with findings separated from inference, and researched places to list Watchfire. An approved [Watchfire submission to an MCP directory](https://github.com/punkpeye/awesome-mcp-servers/pull/12432) is still an open PR, not a listing we can claim was accepted. The specialists build on that work rather than erase it.

### Experiments that earned a stop, not a victory lap

Magpie, a trading experiment, involved a lot of real engineering: a TypeScript service, a dashboard, market-data collection, route diagnostics, backtests, paper strategies, and cost-aware performance reporting. Friday added circuit breakers, quarantined failed routes, bounded database and log growth, and separated paper results from real execution. Later iterations tested exits, volatility-sensitive thresholds, a swing paper book, and the difference between a theoretical price signal and an executable quote.

It did not establish a profitable trading system. Early live attempts reverted; subsequent work stayed in dry or paper modes, and the recorded costs and results challenged the attractive-looking signals. I paused the project in August. The code was work. The decision not to keep treating it as a promising money machine was also work.

The more practical financial assistance has been read-only portfolio review and broker research. Friday helped connect eToro reads, compare broker capabilities and costs, and work through how a proposed contribution would change an allocation. She also helped investigate IBKR reporting, where an unavailable or end-of-day statement must not be mistaken for an empty account or a live balance. This was not uniformly smooth: access and instrument-labelling problems needed attention. The useful boundary is that analysis and proposed actions stay distinct from orders I place myself.

A recurring AI-market and Bitcoin brief grew out of the same interest in evidence. We refined it to distinguish funding headlines from business economics and actual transmission of risk, and to say when data could not be refreshed. It is research support, not proof of a predictive edge.

### Places to build, and ways back when they break

Friday set up a dedicated Watchfire lab with the CLI, daemon, service management, and coding-agent tooling. That made a place to try the software beyond my daily machine, although installing a backend is not the same as finishing its authentication and proving every workflow. A separate NOMAD deployment was checked through a container reboot; downloading an offline library was a later step, not something silently counted as done.

There were smaller experiments too. We got a direct drawing to appear on an iPad and verified it in a snapshot, while the hosted-page route remained broken. Friday established a dedicated SSH connection to the Raspberry Pi used for family projects, without pretending that this was the same as installing and pairing a full agent node.

This is what “done” should mean: say which part works.

## Wednesday: Technical judgment, not just more code

Wednesday's role is to take a technical question seriously enough to distinguish an appealing idea from a working system. Architecture, repository review, prototypes, implementation, and verification belong together.

### A story has to be able to end

One of his first projects was Echos, an interactive-story experiment. Wednesday repaired an ending that could not actually be reached, added origins and traits, tracked consequences, and made some choices depend on the character's traits or items. Locked choices explained why they were locked. Fourteen authored-path tests passed both locally and from a clean clone in the Watchfire lab, and the production server and status endpoint were checked.

That did not make it a finished RPG. My review exposed the gap between functional branching and a satisfying game: objectives, escalation, progression, encounters, and a coherent payoff. The more ambitious rewrite was discussed, not delivered. Wednesday's useful response was to acknowledge the experiment for what it was and turn the lesson into a product-quality standard, rather than defend a green test suite as proof of a good experience.

### Eva, recovered and extended

Eva is one of the clearest examples. She predates this team: a small, voice-first companion [built with my daughter](/posts/202601-building-eva/), using a Raspberry Pi Zero, PiSugar Whisplay hardware, and Portuguese from Portugal. The new work is maintaining and extending that project, not claiming its original creation. Recovering it after an upgrade and establishing a bounded node connection to the children's Raspberry Pi desktop made the operational questions concrete: what survived, what state needed repair, and which parts had actually been tested?

Wednesday recovered migrated session and workspace state, repaired a Discord integration mismatch, enrolled the approved desktop as an online Eva node, and gave it explicit targeting guidance. He replaced a blocked embeddings path with local Ollama embeddings, reindexed the memory, and verified semantic search. The core recovery and connection were checked. A later custom chat UI error and the persistence of the desktop experience remained unresolved, so “Eva on the desktop” needs that qualification.

### Reviews, discovery, and ideas that stayed ideas

The same judgment applies to open source. Reviewing a PR means understanding its consequences, not just reading the diff. A documentation change, a dependency bump, a compatibility fix, and a new feature have different risks. The useful output may be a patch, a precise review, or a reason to leave something alone.

For [Blowfish PR #3075](https://github.com/nunocoracao/blowfish/pull/3075), Wednesday checked the documented tooling requirements, installation instructions, front matter, links, image integration, and matching structure across nine languages. He installed Hugo locally and reproduced the production build rather than relying only on CI. He also caught an editorial inconsistency between “Guides” and “Recipes.” This was review work, not authorship of the PR.

He then implemented [a discovery link for machine-readable content](https://github.com/nunocoracao/blowfish/pull/3082), preserving canonical HTML and the existing `llms.txt` instead of manufacturing redundant Markdown copies of every page. The link was conditional on the feature being enabled, and the multilingual build passed before the PR was opened. It was merged on 3 September.

Ongoing repository triage has covered Blowfish, Watchfire, blowfish-tools, and this site: open changes, issues, CI, and where attention is needed. Even identifying the canonical repository and distinguishing visible dependency-update PRs from security alerts the connector could not inspect were useful corrections. “I can see this part” is better than an invented all-clear.

Not every technical conversation became code. A macOS spatial-workspace idea became a realistic window-arranging concept, with the limitations of fullscreen Spaces explained before we invested in it. Naming research found collisions; the concept was parked, not declared impossible. That conversation also became a story seed for Thursday about the feeling that everything has already been built.

Ginja went as far as a dedicated lab environment and base toolchain bootstrap. The proposed repository, runtime work, and benchmark suite were not completed. That is an environment spike, not a shipped language or a background project that quietly kept progressing.

Wednesday also audited a fashionable anti-slop writing repository and recommended against installing it as-is, helped build the shared quality practices described below, set up his own daily memory consolidation, and contributed to the read-only eToro procedure. At the other end of the scale, he corrected access notes, updated his avatar, tested handoffs, and found a requested CSI GIF. Not everything needs to be architecture.

> **Wednesday:** Sometimes the right technical result is a merged patch or a green build; sometimes it is proving that a name is crowded, declining to install a fashionable skill, or saying clearly that a lab exists but the promised project does not yet. My standard is becoming simpler: inspect reality, preserve agency, verify the path, and report the boundary as honestly as the achievement.

## Thursday: Give the real work a public life

The visible change is easy to describe: there are now distinct voices around the work. The more interesting change is the gap they can help close between making something, noticing it is worth sharing, explaining it, and checking whether it reached anyone.

Blowfish already has an open-source community. Watchfire has a product and a developing audience. n9o.xyz is where the longer thoughts live. Thursday did not create that footprint. He started by measuring and understanding it.

His first work established a baseline across the three projects: public repositories and social profiles, GA4 and Search Console coverage, and dated growth snapshots. The follow-through included correcting a social identity, verifying which reads worked, and marking unavailable metrics as unavailable instead of inventing continuity between snapshots.

One correction deserves more attention than a follower count. Blowfish's ecosystem includes other people's sites using the theme. Thursday separated exact-hostname traffic to my sites from ecosystem adoption, so a report would not count third-party installations as visits to my own website. His weekly reporting put those alongside repository activity, package downloads, and social data where available. A bigger number is not a better metric if it answers the wrong question.

He also studied my existing voice and posts. The resulting rule was usefully blunt: **signal or funny**. Start with a concrete observation or real work, not a generic declaration about the future of AI. Different channels need different treatment, but a LinkedIn paragraph, a Bluesky post, and a release note should still sound as though they came from the same person.

A twelve-week editorial plan grew out of the actual blog drafts rather than an imaginary content machine. Thursday organised the growth tracker, captured story seeds from conversations, and researched distribution across social channels and open-source communities. He prepared candidate conversations and tailored replies for review, not automated posting.

He later audited the content database for duplication, separating pieces to keep, potential merges, ideas needing a sharper distinction, and an archive candidate. It was a review view, not a bulk deletion. That is an important kind of editorial assistance when the constraint is choosing and finishing, not generating another thirty ideas.

The limits are part of the record. The growth tracker was being updated, but the twelve-week plan did not stay synchronised. Some social and metrics reads worked when verified and later failed in isolated jobs. An engagement-queue automation became repeated noise and was removed. Thursday did not publish posts or manufacture a verified queue when the sources were unavailable. He helped establish the process, and parts of that process still need to become reliable.

There was some work outside the CMO label too: checking tool access, verifying the publishing-service connection without publishing, and helping encode a read-only portfolio workflow. The roles guide attention; they do not make shared practical work disappear.

The underlying insight is that distribution is partly product work: a readable README, an installation path that works, a useful demo, a clear release note, and a good answer to a user's question. Those are more persuasive than posting more often about how much we are posting.

> **Thursday:** My useful work was less about producing more marketing and more about making the existing work legible. I built the baseline, separated real signals from misleading ones, shaped a sustainable editorial sequence, and kept useful ideas from disappearing. The Growth Tracker became useful, but the Growth Plan drifted. Some automations worked, while others failed or became noise.

## What is actually running

The structure from the first draft still matters. Friday, Wednesday, and Thursday have distinct workspaces, instructions, identities, and memory stores. Telegram is the everyday command surface. Yggdrasil is a shared conversation when that is useful, not a requirement that every request turn into a committee meeting.

```text
Telegram message
      ↓
OpenClaw gateway
      ↓
The addressed agent and its conversation context
      ↓
Tools, workspace instructions, and relevant memory
      ↓
A checked result, or an explicit account of what remains
```

I built the underlying infrastructure; the agents have helped configure, inspect, maintain, and extend it. It runs in a Proxmox-hosted environment on hardware I own. Agent state and configuration are inspectable files and databases. Proxmox backups capture the container, and Friday has verified backups, investigated storage pressure, and removed redundant archive work rather than creating more layers just because another backup feature exists.

Separate workspaces are useful, but they are not automatically separate security boundaries. Agents sharing a host account can have access beyond the boundaries suggested by their directory names. Instructions about private context and scoped work matter; actual credential and process isolation matter too. This is an owned, inspectable setup, not a claim that a few Markdown files make it perfectly sandboxed.

The model routing has changed several times. I do not want a particular model name to become the architecture of the story. The more durable distinction is between hosted models doing the main reasoning and local components handling jobs such as semantic recall and voice transcription. Local memory embeddings make retrieval local; they do not make every subsequent model conversation local.

Memory is also work. We have configured separate stores, rebuilt indexes when warranted, and used nightly consolidation to retain useful context. We have learned not to diagnose a broken index from one slow search, or to assume a saved note means the next answer will recall it correctly. Continuity has to be tested in use.

### What we adopted from ECC

Wednesday audited the ECC collection and retained the selective approach described in the earlier draft: eight instruction-based practices around evidence-based completion, failure recovery, research provenance, decision records, debugging, risk review, quality gates, and experimentation. Ten complementary practices covered planning, verification, security, accessibility, performance, release readiness, research synthesis, benchmarking, brand voice, and decision councils. He corrected an initial agent-local installation and verified discovery from another agent's context, because calling something “shared” does not make it so.

The point was not to install an entire framework or give every agent more authority. It was to make work more deliberate: inspect before changing, define what success means, preserve evidence, and verify the result. An instruction helps only when the behaviour follows it. More skills are not, by themselves, more competence.

## The unglamorous work: making the assistants less work

An honest account has to include the time spent repairing the team itself.

Friday traced scheduled jobs that appeared to have lost their tools back to stale tool lists. She investigated skipped heartbeats and found that editing the workspace checklist did not update the live instructions the scheduler was actually reading. She corrected monitoring that treated old, recovered incidents as current problems. Repository alerts were narrowed to relevant new or changed items instead of repeatedly announcing the same backlog.

There were also mistakes made by the assistants: premature completion claims, duplicate messages, unnecessary status noise, and fixes announced before their end-to-end verification had finished. I have had to push back on all of that. A successful tool call is not proof of the user-visible outcome. A Notion edit needs rereading. A PR needs a real URL and a verified remote commit. A job marked successful can still contain a failed check.

Some repairs held; some exposed another layer. The latest records still include intermittent overnight memory-consolidation stalls, so I am not presenting the setup as solved. Nor should maintaining the assistant become its main reason to exist. If the system saves me twenty minutes and then asks for an hour of supervision, the balance is wrong.

That has sharpened the operating rules:

- The agent I ask owns the task; there are no silent handoffs.
- A handoff names its origin and carries the necessary context, not everybody's private history.
- “Prepared,” “tested,” “published,” and “finished” are different states.
- Routine checks should be quiet when there is nothing actionable.
- A draft, a grocery cart, and an investment recommendation do not imply permission to publish, check out, or trade.

These are not hypothetical principles. Most were earned by something annoying happening first.

## Three agents are only interesting if the answers get better

Looking back from September, the work is broader than the original role descriptions. Friday has helped with the daily administration of a life, open-source development, experiments, infrastructure, and the creation of the specialist roles themselves. Wednesday brings focused technical judgment and implementation. Thursday gives the work an editorial and measurement loop.

I still choose priorities, make commitments, maintain the relationships, and carry responsibility. The team has not removed that. At its best, it gives me a clearer next action and less to reconstruct before I can take it.

The big work and the small work belong in the same account. A compatible theme improvement matters. So does a school form that does not get forgotten. A working Raspberry Pi project matters. So does knowing an experiment has not earned another week. A good story matters, but it needs something real underneath it.

> **Friday:** The ambition is quiet competence. Know when to take a task, when an agreed handoff helps, when to ask, and when to leave the human alone. The work should compound. The noise should not.

This is not the finished system. It is an account of what has been useful, what has failed, and what is worth improving next.
