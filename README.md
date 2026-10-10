<!-- Generated: README.md and assets/ are built by github-profile/ in the portfolio repo (python3 build.py && python3 readme.py). Edit the source there, not this file. -->

<picture><source media="(prefers-color-scheme: dark)" srcset="assets/hero-dark.svg"><img alt="Full-stack engineer and founder. I build the product. And everything behind it. I turn complex problems into software people use and pay for, from native iOS apps to AI-powered creator tools and the agent tools that help me build them. Under the caption &quot;Real products. Every layer.&quot;: a DeckDrop generation demo for the topic &quot;AI tools for your next idea&quot; with a row of example carousel slides, the Dosely iPhone app's dashboard with demo data, and a card reading &quot;Built with my own tools: Explore the agent infrastructure&quot;." src="assets/hero-light.svg" width="100%"></picture>

<p>
<a href="https://calendly.com/aboulnasrsherif/30min"><picture><source media="(prefers-color-scheme: dark)" srcset="assets/btn-call-dark.svg"><img alt="Schedule a call" src="assets/btn-call-light.svg" height="44"></picture></a>&nbsp;
<a href="mailto:aboulnasrsherif@gmail.com"><picture><source media="(prefers-color-scheme: dark)" srcset="assets/btn-email-dark.svg"><img alt="Email" src="assets/btn-email-light.svg" height="44"></picture></a>&nbsp;
<a href="https://linkedin.com/in/sherif-aboulnasr"><picture><source media="(prefers-color-scheme: dark)" srcset="assets/btn-linkedin-dark.svg"><img alt="LinkedIn" src="assets/btn-linkedin-light.svg" height="44"></picture></a>
</p>

<br>

<picture><source media="(prefers-color-scheme: dark)" srcset="assets/proof-dark.svg"><img alt="Built. Shipped. Operated. October 2026 snapshot: $130K+ app revenue, 100K+ App Store downloads, 4 iOS apps shipped." src="assets/proof-light.svg" width="100%"></picture>

<br>
<br>

<picture><source media="(prefers-color-scheme: dark)" srcset="assets/head-work-dark.svg"><img alt="Selected work. The idea is only the beginning. Different products. Different kinds of challenge. A closer look at the product, the decisions, and the systems underneath." src="assets/head-work-light.svg" width="100%"></picture>

<br>

<a href="https://apps.apple.com/us/app/dosely-peptide-tracker/id6759814549"><picture><source media="(prefers-color-scheme: dark)" srcset="assets/dosely-dark.svg"><img alt="Dosely, native iOS. Complex routines. A calmer daily ritual. 100K+ downloads, $130K+ revenue. Built with SwiftUI, Supabase and RevenueCat. An iPhone shows the app with demo data, cycling through three screens named by a control below it: Today, the daily dashboard with doses due and an active protocol (A clear starting point for the day); Inventory, the My Fridge view of vials and amounts left (Inventory that stays connected to the routine); and Protocols, the stack view with a concentration chart and compounds (The detail behind an active protocol)." src="assets/dosely-light.svg" width="100%"></picture></a>

Schedules, vial inventory, calculations, and reminders in one native app. I built the SwiftUI experience and the systems behind it, with a cache-first architecture that keeps the daily workflow close at hand.

<p>
<a href="https://apps.apple.com/us/app/dosely-peptide-tracker/id6759814549"><picture><source media="(prefers-color-scheme: dark)" srcset="assets/btn-appstore-dark.svg"><img alt="View on App Store" src="assets/btn-appstore-light.svg" height="44"></picture></a>&nbsp;
<a href="https://dosely.cc"><picture><source media="(prefers-color-scheme: dark)" srcset="assets/btn-product-dark.svg"><img alt="Product site" src="assets/btn-product-light.svg" height="44"></picture></a>
</p>

<details>
<summary><b>Inside the build</b>&nbsp;&nbsp;Designing the architecture around the daily experience.</summary>
<br>

**My role.** Sole engineer at EFN Group. Native app, data layer, subscription integration, release, and production maintenance.

**The challenge.** Logging a dose affects a schedule, an inventory, and an ongoing protocol. These connected tasks should feel like one coherent routine, even when the network is unreliable.

**The decision.** After production experience with shared state, I moved toward singleton-free, cache-first repositories. Screens read local data first while the backend handles persistence and sync.

**The tradeoff.** Local responsiveness makes synchronization and state ownership more important. Explicit repositories give each screen a clear data boundary and make those responsibilities easier to follow.

<picture><source media="(prefers-color-scheme: dark)" srcset="assets/dosely-arch-dark.svg"><img alt="Diagram: A native interface with a local-first data path. Four steps left to right: SwiftUI screens (Daily tasks and inventory), then Repositories (Explicit state ownership), then Local cache (Read without a network wait), then Backend sync (Persistence and account data)." src="assets/dosely-arch-light.svg" width="100%"></picture>

**In production.** A subscription app with camera-assisted vial entry, cycle planning, and a compound library. The October 2026 portfolio snapshot records 100K+ downloads and $130K+ revenue.

</details>

<br>
<br>

<a href="https://www.deckdrop.co/"><picture><source media="(prefers-color-scheme: dark)" srcset="assets/deckdrop-dark.svg"><img alt="DeckDrop, Creator tools &amp; AI: a topic becomes a finished carousel. A generation demo shows the topic 'AI tools for your next idea' for TikTok, 5 slides, with the status 'Your carousel is ready' and 5 / 5. Five slides: 'AI tools. Real ideas.' (the hook), 'Write it with Cursor.' (build the idea), 'Give it a voice.' with ElevenLabs (tell the story), 'Follow your curiosity.' with Perplexity (find the context), and 'Now make something.' (make it yours). Caption: One topic. Five editable slides. Below: 5 supported platforms, layers and undo / redo, brand kits and team libraries; built with Next.js, OpenAI, Satori and Sharp." src="assets/deckdrop-light.svg" width="100%"></picture></a>

Turn a topic, article, or PDF into social slides you can make your own. I built DeckDrop with AI-assisted drafting, a visual editor, reusable brand kits, and exports sized for five platforms.

<p>
<a href="https://www.deckdrop.co/"><picture><source media="(prefers-color-scheme: dark)" srcset="assets/btn-deckdrop-dark.svg"><img alt="Visit DeckDrop" src="assets/btn-deckdrop-light.svg" height="44"></picture></a>
</p>

<details>
<summary><b>Inside the build</b>&nbsp;&nbsp;Keeping AI output editable, exportable, and dependable.</summary>
<br>

**My role.** Product engineering across generation, the visual editor, server rendering, saved drafts, and subscription credits.

**The challenge.** A generated image locks in the design too early. Creators need to rewrite a hook, move a text layer, change a background, and adapt the same idea to another platform.

**The decision.** The pipeline returns structured slide content and editable state. The editor adds layers, undo/redo, and autosave. Each slide renders on the server with Satori, Resvg, and Sharp; the browser packages the results into a ZIP.

**The production details.** Generation involves model calls, image sourcing, and rendering. Server-side credit checks gate each paid operation, failed work triggers a refund, and compressed image payloads keep responses within serverless limits.

<picture><source media="(prefers-color-scheme: dark)" srcset="assets/deckdrop-flow-dark.svg"><img alt="From source material to a post-ready deck, in four steps: Topic, URL, or PDF (source material and brand voice); Generate a draft (slide copy and background images); Edit the details (text, layers, layout, and style); Render &amp; export (platform-sized slides in a ZIP)." src="assets/deckdrop-flow-light.svg" width="100%"></picture>

**A complete creator workflow.** Drafting, editing, saved brand styles, shared libraries, and downloadable slides for TikTok, Instagram, Reddit, LinkedIn, and X.

</details>

<br>
<br>

<picture><source media="(prefers-color-scheme: dark)" srcset="assets/codexflow-dark.svg"><img alt="The toolkit. The tools behind the work. Better products start with better tools. This is the infrastructure I built to make agent-assisted engineering more dependable. Agent orchestration: codex-flow. Parallel work that survives interruption. A workflow engine for coordinating CLI agents, validating their output, and picking up where a run left off. An illustrative walkthrough titled 'A code review, orchestrated' shows a Review workflow that branches into three review tasks: Concurrency &amp; resume, Child processes, and CLI &amp; rendering. It cycles through five steps. Queue: all three queued. Run: all three running in parallel. Interrupt: two complete, CLI rendering interrupted. Resume: the two completed reviews are reused from cache and only CLI rendering runs again. Collect: all three results, two cached and one complete. Plain Node.js. Zero npm dependencies. Based on a real review workflow; states are illustrative." src="assets/codexflow-light.svg" width="100%"></picture>

<details>
<summary><b>Inside the build</b>&nbsp;&nbsp;The hard part is what happens after something fails.</summary>
<br>

**A code review, orchestrated.**

1. **Queue three independent reviews.** This example queues reviews of concurrency and resume behavior, child processes, and CLI rendering. Each task has its own scope.
2. **Run the reviews in parallel.** The three independent tasks are running. The workflow coordinates their work and collects each result as it finishes.
3. **One task is interrupted.** Two reviews have completed. The CLI rendering review fails in this example, leaving that task unfinished while the completed results remain available.
4. **Resume the unfinished task.** The completed reviews are reused from cache. Only the unfinished CLI rendering review runs again.
5. **Collect all three results.** The remaining review completes. The workflow now has all three outputs, including the two results retained from the earlier run.

**The challenge.** A long agent run can fail after useful work has already finished. Starting over wastes that work; blindly continuing can reuse results that no longer apply.

**The decision.** I built an append-only event journal and content-addressed resume cache. Unchanged successful calls can replay their validated results. Failed calls run again.

**The boundary.** Recovery also means managing process trees, protecting concurrent resume operations, and preserving output during worktree cleanup. When dependent state changes, a fresh run keeps the assumptions explicit.

**Built for my workflow.** JavaScript orchestration, configurable concurrency, schema-validated outputs, and optional worktree isolation.

</details>

<br>

<p>
<picture><source media="(prefers-color-scheme: dark)" srcset="assets/tool-beam-dark.svg"><img alt="Beam: Point at an element. Give an agent context." src="assets/tool-beam-light.svg" width="50%"></picture><a href="https://github.com/Sherif-Aboulnasr/agent-memory-vault"><picture><source media="(prefers-color-scheme: dark)" srcset="assets/tool-memory-dark.svg"><img alt="Agent memory: Useful context, across sessions. Links to its GitHub repository." src="assets/tool-memory-light.svg" width="50%"></picture></a><br>
<a href="https://github.com/Sherif-Aboulnasr/Agent-Screen-Capture-MCP"><picture><source media="(prefers-color-scheme: dark)" srcset="assets/tool-capture-dark.svg"><img alt="Screen-capture MCP: A visual feedback loop for agents. Links to its GitHub repository." src="assets/tool-capture-light.svg" width="50%"></picture></a><a href="https://github.com/Sherif-Aboulnasr/voicetotext"><picture><source media="(prefers-color-scheme: dark)" srcset="assets/tool-voice-dark.svg"><img alt="VoiceToText: Offline dictation, one hotkey away. Links to its GitHub repository." src="assets/tool-voice-light.svg" width="50%"></picture></a><br>
<picture><source media="(prefers-color-scheme: dark)" srcset="assets/tool-handoffs-dark.svg"><img alt="Image handoffs: From a written brief to ready-to-use assets." src="assets/tool-handoffs-light.svg" width="50%"></picture><a href="https://github.com/Sherif-Aboulnasr?tab=repositories"><picture><source media="(prefers-color-scheme: dark)" srcset="assets/tool-repos-dark.svg"><img alt="Public repositories: github.com/Sherif-Aboulnasr. Links to the repositories tab." src="assets/tool-repos-light.svg" width="50%"></picture></a>
</p>

<details>
<summary><b>What each tool does</b></summary>
<br>

**Beam.** A browser extension and local bridge that connect a selected UI element to a coding session in the right repository. The dev-server port identifies the project directory.

**Agent memory.** Persistent memory built around linked knowledge graphs, automated regrouping, and two-layer recall, so project context can outlast an individual agent session. [Repository](https://github.com/Sherif-Aboulnasr/agent-memory-vault)

**Screen-capture MCP.** A draggable, click-through overlay defines a screen region that an MCP server captures on demand. Agents can inspect the interface before and after a change. [Repository](https://github.com/Sherif-Aboulnasr/Agent-Screen-Capture-MCP)

**VoiceToText.** Push-to-talk dictation for macOS using local Whisper.cpp transcription. Hold a hotkey, speak, release, and the text is pasted into the focused application. [Repository](https://github.com/Sherif-Aboulnasr/voicetotext)

**Image handoffs.** Self-contained Markdown briefs coordinate image generation across background agents. Original assets stay separate from the compressed copies shipped in a project.

</details>

<br>
<br>

<picture><source media="(prefers-color-scheme: dark)" srcset="assets/head-workshop-dark.svg"><img alt="More from the workshop. Different problems. The same attention to detail. More shipped apps, each with its own engineering challenge." src="assets/head-workshop-light.svg" width="100%"></picture>

<br>

<a href="https://apps.apple.com/us/app/pingr-tcg-restock-alerts/id6778630259"><picture><source media="(prefers-color-scheme: dark)" srcset="assets/app-pingr-dark.svg"><img alt="Pingr, real-time alerts. TCG restock alerts with a Realtime-to-push handoff and server-enforced subscription access. Three App Store screenshots: the App Store preview with the restock feed, the restock feed with store links and phone alerts, and the news feed with trading card market updates." src="assets/app-pingr-light.svg" width="100%"></picture></a>

[App Store](https://apps.apple.com/us/app/pingr-tcg-restock-alerts/id6778630259) &nbsp;·&nbsp; [pingr.live](https://pingr.live)

<br>

<a href="https://apps.apple.com/us/app/umaps-urbex/id6789791291"><picture><source media="(prefers-color-scheme: dark)" srcset="assets/app-umaps-dark.svg"><img alt="uMaps, maps &amp; community. Urban exploration built on PostGIS, with approximate public locations and server-gated precise coordinates. Three App Store screenshots: the App Store preview with the urban exploration map, the map with location categories and points of interest, and the profile showing reputation and progress toward unlocking exact locations." src="assets/app-umaps-light.svg" width="100%"></picture></a>

[App Store](https://apps.apple.com/us/app/umaps-urbex/id6789791291) &nbsp;·&nbsp; [umaps.xyz](https://umaps.xyz)

<br>

<a href="https://apps.apple.com/us/app/stepsy-walk-to-unlock/id6760950247"><picture><source media="(prefers-color-scheme: dark)" srcset="assets/app-stepsy-dark.svg"><img alt="Stepsy, health &amp; screen time. Screen time earned by walking. HealthKit, Family Controls, and four app extensions connect the experience. Three App Store screenshots: the App Store preview showing steps earned toward screen time, the dashboard with earned screen time, streaks and app blocking, and weekly statistics with steps, goal progress and streak." src="assets/app-stepsy-light.svg" width="100%"></picture></a>

[App Store](https://apps.apple.com/us/app/stepsy-walk-to-unlock/id6760950247) &nbsp;·&nbsp; [stepsy.fit](https://stepsy.fit)

<br>

<picture><source media="(prefers-color-scheme: dark)" srcset="assets/app-dashfit-dark.svg"><img alt="On the workbench: Dashfit, in development. An on-device motion game: your steps, jumps, and squats control a three-lane runner. Built with SwiftUI, SpriteKit, and Vision body-pose tracking." src="assets/app-dashfit-light.svg" width="100%"></picture>

<br>
<br>

<picture><source media="(prefers-color-scheme: dark)" srcset="assets/head-about-dark.svg"><img alt="A little about me. Curious about the details. Responsible for the whole. I’m an engineer who likes staying close to the problem, and to the people using what I build." src="assets/head-about-light.svg" width="100%"></picture>

I co-founded EFN Group. My work spans the interface, the data model, the payment flow, and the production issue that only shows up after launch.

That range shapes how I work: understand the domain, make the important decisions explicit, and keep improving the product after it ships. I bring that same ownership to the teams and people I work with.

<picture><source media="(prefers-color-scheme: dark)" srcset="assets/about-facts-dark.svg"><img alt="Background facts. Building: EFN Group, consumer apps, creator tools, and agent infrastructure. Foundation: Computer Engineering, Florida State University, BS 2025. Research: Data Analytics &amp; AI, graduate study and NLP research at FGCU. Working in: TypeScript, Swift, Python, PostgreSQL, React, SwiftUI, and Node.js." src="assets/about-facts-light.svg" width="100%"></picture>

<picture><source media="(prefers-color-scheme: dark)" srcset="assets/analytical-dark.svg"><img alt="The analytical side: research, data systems, and a foundation in embedded engineering. Cross-product analytics, Microsoft Fabric / Power BI. NLP &amp; research design, Python / FGCU. Embedded motor control, C / MSP432." src="assets/analytical-light.svg" width="100%"></picture>

<details>
<summary><b>More on the analytical side</b></summary>
<br>

**Cross-product analytics.** A three-layer warehouse consolidating product data from PostgreSQL backends, with automated quality checks and a dashboard of users, revenue, and engagement.

**NLP & research design.** A pipeline classifying 600+ research abstracts across eight emotion categories. Separate gamification-in-finance research included a 53-item survey distributed to 200+ respondents.

**Embedded motor control.** Led a four-person FSU capstone team building PID motor control and a data-acquisition pipeline for RPM, torque, and current.

</details>

<br>
<br>

<picture><source media="(prefers-color-scheme: dark)" srcset="assets/contact-dark.svg"><img alt="Have a good problem? Let’s build something that matters. Open to engineering roles and thoughtful collaborations." src="assets/contact-light.svg" width="100%"></picture>

<p>
<a href="https://calendly.com/aboulnasrsherif/30min"><picture><source media="(prefers-color-scheme: dark)" srcset="assets/btn-call-dark.svg"><img alt="Schedule a call" src="assets/btn-call-light.svg" height="44"></picture></a>&nbsp;
<a href="mailto:aboulnasrsherif@gmail.com"><picture><source media="(prefers-color-scheme: dark)" srcset="assets/btn-email-dark.svg"><img alt="Email" src="assets/btn-email-light.svg" height="44"></picture></a>&nbsp;
<a href="https://linkedin.com/in/sherif-aboulnasr"><picture><source media="(prefers-color-scheme: dark)" srcset="assets/btn-linkedin-dark.svg"><img alt="LinkedIn" src="assets/btn-linkedin-light.svg" height="44"></picture></a>
</p>
