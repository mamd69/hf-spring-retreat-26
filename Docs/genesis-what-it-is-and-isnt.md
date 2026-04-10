# HeroForge Genesis: Definitive Internal Reference

**Sources**: Call with Natasha Beauvais (March 6, 2026), Call with Katrina Skinner (March 10, 2026), Post-call follow-up email (March 10-11, 2026)

**Context**: "HeroForge Genesis" is the rebrand of "ruvector." Mark Allen (physician turned AI entrepreneur) describes and demos the platform across two calls to different audiences. This document synthesizes everything stated across both calls into a single authoritative reference.

---

## 1. What Genesis IS

### The Core Vision

Genesis is described as "sci-fi happening today" -- an **operating system for a business**. It is a platform that takes any business from its current state to an optimized future state by combining the most powerful AI models with proprietary orchestration and knowledge engine technologies.

It is not merely an analysis tool. Genesis analyzes, plans, builds, deploys, monitors, and -- critically -- **self-improves**. Mark positions it as the convergence of several cutting-edge AI technologies brought together into a single integrated platform that can be run behind a firewall, on a laptop, using open-source components and a $200/month Claude Max subscription.

The vision extends beyond any single industry. Mark demonstrates it across orthodontics (Nexadental), hospital medical coding (Good Samaritan Hospital), real estate investment (Vermont inn/sober living), and frames it as applicable to any business including pediatric practices, marketing agencies, and financial services.

Mark's framing: "Things that take a hundred people a year to do... some of the things you can do were impossible to do, flat out impossible. Couldn't even do them at all. And now you can do them in a weekend."

### The Methodology (The 4-Step Process)

Genesis follows a defined methodology that Mark presents consistently across both calls:

**Step 1 -- Import and Digitize**: Upload all business documents, data, and institutional knowledge into the Genesis knowledge base. This can begin with existing business documents or even "a seed of an idea, of a new business idea." The data should be reasonably clean; Mark estimates 1-2 weeks maximum for data cleaning, and AI assists in that process. Large unwieldy files can be excluded in favor of the "voluminous stuff" that the system processes well.

**Step 2 -- Research and Augment**: The AI goes out and researches industry best practices, competitor analysis, benchmarks, industry groups, and unicorns in the space. All of this external knowledge is brought into the knowledge base to augment the proprietary business data. In the Nexadental example, this meant ingesting the American Association of Orthodontists (AAO) best practices plus proprietary industry databases (processed through AI before being added, to respect data licensing). In the hospital coding example, this meant downloading 600,000+ ICD code records plus all CMS rules, regulations, and severity guidelines.

**Step 3 -- Analyze and Plan**: The AI compares the business's current state against industry best practices and identifies gaps, revenue leakage, and improvement opportunities. A critical innovation here: the system is also pointed back at its own capabilities -- "using the crazy stuff that's in this platform, how would you envision a concierge-based medical practice to exist 10 years in the future." This produces ideas that go beyond current best practice to future-state possibilities. The analysis includes:
- Monte Carlo simulations across different scenarios (patient flow, staffing, doctor count, growth constraints)
- Value-versus-effort prioritization of all identified improvements
- Phased deployment roadmaps
- Financial modeling (described as better than $100K investment bank models)

Mark emphasizes that the user's domain expertise is essential during this phase: "You've been practicing pediatrics and building businesses... you're going to say this makes sense, this doesn't."

**Step 4 -- Build and Deploy**: A swarm of AI agents actually builds out the solutions -- software, automations, workflows, dashboards, AI assistants, websites, marketing materials. This is not a plan that gets handed to a human development team. The agents build it, test it (including browser-based front-end testing with computer vision), and the human reviews the output. Monitoring is included as an ongoing component: KPIs are tracked, dashboards are updated nightly, and the system self-optimizes over time.

### The Technology Stack

**Foundation Model**: Claude / Claude Code (primarily Claude Opus 4.6 for building and planning). Other models can be used for production applications depending on the problem, including more efficient models and local models. Claude Code is described as "the world's most powerful software development agent" and also "a framework to build agents in general."

**Agentic Orchestration**: Approximately 60 specialized development agents that support all aspects of the software development lifecycle. These are distinct from the production/business agents that get deployed for the client's operations. Examples of development agents include:
- Front-end developer (web apps)
- Front-end developer (iOS mobile)
- Front-end developer (Android mobile)
- QA agents (programmatic code testing)
- Browser automation agents (fill forms, press buttons, test with computer vision)
- GitHub/source control agents
- Back-end development agents
- Planning and analysis agents
- AI orchestration agents (coordinate the other agents)

Up to 20 agents can run simultaneously. The orchestration is AI-driven, not human-driven -- "that swarm is orchestrated by an AI agent, not by you." Claude just released "agent teams" publicly that do "a fraction" of what Genesis has been doing for six months.

For production/business use, different agents are built: a front desk agent that converses with patients and books appointments, a lead-booking agent, a coding optimization agent, etc. These are the agents that run in the client's business after deployment.

**The Knowledge Engine (RAG+)**: This is the core technical differentiator Mark explains in depth across both calls. It combines three database technologies:

1. **Vector Database** -- Supports semantic similarity search. When a user asks about "PTO policy," it matches results about "vacation policy" or "days off." This is the standard RAG approach.

2. **Graph Database** -- Supports hierarchical and relationship-based traversals. This handles structured knowledge where relationships between entities matter (e.g., ICD codes, organizational hierarchies, coding rules).

3. **Graph Neural Network (GNN)** -- This is what Mark identifies as the key differentiator. Unlike the vector and graph databases, the GNN **learns from interactions**. The AI models (Claude, GPT) do not learn -- "the model itself doesn't learn at all." The vector and graph databases get smarter only as you feed them more data. But the GNN learns and optimizes autonomously based on goals.

The knowledge engine is described as "infinitely scalable for all intents and purposes" with "extremely low latency." It is shared across all agents as a common brain. This solves the context window limitation: individual agents cannot read all of a business's documents in a single session, but when the documents are in the shared knowledge base, all agents can access all knowledge effectively, "as if it had an unlimited context window."

In the hospital coding example, the knowledge base contained 300,000+ records. In the orthodontic example, it combined proprietary practice data with AAO best practices and industry databases.

**Browser Automation**: A relatively new capability (only a couple of months old at the time of the calls). Agents can interact with web UIs like a human would -- filling out forms, entering data, pressing buttons. Combined with computer vision, agents can evaluate design quality, test user flows, and feed errors back into the development cycle. This is part of the agent swarm's overnight build-and-test workflow.

**Advanced Technologies (from Katrina call)**: Mark describes several additional capabilities developed by his core technical partner (referred to as "Roov"):

- **RoovView**: Wi-Fi-based sensing that can detect heartbeat, respiratory rate, and even brain patterns through walls. Uses $2 Wi-Fi chips connected via USB. Can sense a broader spectrum than standard Wi-Fi. Applications include hospital room monitoring, elderly care, baby monitoring -- without the privacy concerns of visual cameras.

- **Federated Brain**: The shared knowledge base (RAG) made distributable across multiple computers, "like a blockchain." This enables shared memory across a distributed network of systems. Includes 97% compression of the knowledge base while improving retrieval speed.

- **Quantum-Inspired Computing**: Quantum computing principles applied to regular hardware. Not actual quantum hardware, but quantum algorithms running on conventional systems. Mark describes this as "complete sci-fi" that is "way up here" and he is still learning how to apply it to business problems.

### What Genesis Produces (Concrete Outputs)

Based on demonstrations and descriptions across both calls:

**Business Intelligence and Assessment**
- Practice IQ reports: comprehensive business assessment scored against industry benchmarks (described as equivalent to a $100,000 consulting engagement, sold for $3,000). Includes practice scoring, trend analysis, gap identification, phased deployment plans, and detailed breakdowns by business area (lead response, case acceptance, patient retention, collections, engagement).
- Inside IQ dashboards: pull data nightly from billing/practice management systems and present financial and operational metrics in a friendly interface (new patients, case acceptance rates, accounts receivable, schedule efficiency, period comparisons, origin-of-starts tracking).
- Financial models: 33-tab spreadsheets with assumptions, scenario dashboards, investor return calculations, and accompanying plain-language guides. Mark states these are "better than financial models that I've paid a hundred thousand dollars for."

**AI Assistants and Agents**
- Dr. Eve: a conversational AI assistant that has access to the Practice IQ report and can discuss findings, answer questions, and provide prioritized recommendations. Available as both voice and text interface.
- Lead IQ: an AI phone/lead agent that instantly calls back leads, follows up with text and email, answers the phone (configurable -- third ring, all the time, phone tree). Operates 24/7. Embeddable as a website widget and connectable to existing phone systems.
- Front desk agents: conversational agents for patient booking and schedule management.

**Marketing and Sales Materials**
- Websites (fully generated, including content and imagery)
- Investor decks and one-pagers
- Customized sales outreach emails (e.g., identifying the 50 most ideal buyers for a property and generating personalized emails to each)
- Sales tools with prospect identification and tracking
- Comprehensive guides with glossaries

**Operational Automation**
- Medical coding optimization (combining clinical reasoning models with complete coding knowledge to identify optimal legal/ethical coding, including automated physician attestation workflows). Demonstrated 10-15% revenue improvement at a $90 million hospital.
- API integrations with practice management systems, EHRs, QuickBooks
- Nightly data synchronization and reporting
- Automated lead response and follow-up workflows

### The Self-Learning Capability

This is what Mark calls "the sci-fi element" and returns to repeatedly in both calls. The explanation is consistent:

The AI models (Claude Opus 4.6, GPT 5.3, etc.) do not learn. They are born smart after a $100M+ training investment but fundamentally have no memory and cannot learn from interactions. Chatbots create the illusion of learning through vector databases that store session history, but the underlying model remains static.

The Genesis knowledge engine, specifically the Graph Neural Network component, actually learns and improves from interactions. Mark's primary example: a lead-booking agent that converts 30% of inbound leads. You can set a goal -- "improve yourself based on how well you're booking appointments" -- and the GNN will analyze all the data from interactions and autonomously optimize toward that goal. The agent gets better over time without human intervention.

Mark frames this as fundamentally different from chatbots or workflow automation: "This is totally sci-fi stuff. That's fundamentally what the graph neural network does."

---

## 2. What Genesis is NOT

Based on explicit statements and clear implications across both calls:

**NOT just a chatbot or ChatGPT wrapper.** It is an entire orchestration platform with 60+ specialized agents, a three-layer knowledge engine (vector DB + graph DB + GNN), browser automation, and AI-driven coordination. The chatbot is one small output of the platform, not the platform itself.

**NOT a static knowledge base.** The vector and graph databases are static repositories that get smarter only when fed more data. But the GNN layer learns autonomously from interactions. This dynamic learning capability is the core differentiator.

**NOT N8N or simple workflow automation.** Mark explicitly states: "We don't use N8N here... N8N is a fast path, but it has both cost and scalability limitations. This is ultimately a better solution." Genesis builds its own automations rather than relying on third-party workflow tools.

**NOT something that requires massive hardware.** Runs on a laptop. Requires a Claude Max account ($200/month). The rest of the stack is open source. Mark tells Natasha's team: "You don't even need a fancy one... you're using a lot of processing power of cloud servers to do stuff. You don't need crazy processing power."

**NOT a do-it-for-you black box.** It is interactive and requires domain expertise from the user. Mark is emphatic: "I don't know your business... AI also hallucinates. It doesn't understand a lot unless you ask the questions right, unless you ground it properly." The user reviews plans, validates findings, provides corrections, and directs priorities. Mark explicitly moved away from "we'll do it for you" to "we'll do it with you."

**NOT limited to one industry.** Demonstrated across orthodontics, hospital medical coding, real estate/sober living investment, and discussed for application to pediatric practices, family medicine, marketing, and financial services. The methodology is industry-agnostic; the knowledge base is what makes it industry-specific.

**NOT just for tech people.** Designed with UIs for non-technical users (Practice IQ dashboard, Inside IQ, Lead IQ widget, Dr. Eve conversational AI). Mark acknowledges: "Most people, they need a UI." Claude Code is the power-user interface; the platform generates friendly UIs for everyone else. Allison (a non-technical mastermind member) is cited as proof: "I've never coded anything in my life... it made it accessible for someone non-technical like me to use."

**NOT a replacement for domain knowledge.** The AI hallucinates. It needs human validation. It may not understand why something does not make sense in a specific clinical or business context. The practitioner's experience is essential for reviewing and directing the AI's output.

**NOT data-dependent on perfect inputs.** Data cleaning takes 1-2 weeks maximum. AI can help clean the data. Big files that do not work well can be excluded. The system handles data from multiple sources in varying states of quality.

**NOT necessarily expensive to run.** The open-source stack means the graph database alone "would cost what they charge" if purchased commercially. Claude Max is $200/month. The platform runs on commodity hardware. This contrasts sharply with enterprise AI platforms that require significant infrastructure investment.

---

## 3. How Genesis Was Described Differently to Each Audience

### To Natasha Beauvais (March 6, 2026)

**Audience context**: Existing client and mastermind member. Owns Northern Virginia Family Practice (NVFP) with her team (David as IT/operations consultant, Ned as head of finance, Tiffany as team member). Some AI familiarity from mastermind participation. Has an older EMR (EMDs) and has been learning AI tools for a couple of months.

**Presentation approach**:
- Led with the detailed technical explanation of how RAG works (vector database, graph database, GNN), explaining each layer from first principles because David (the IT consultant) asked clarifying questions
- Showed three diverse examples (Nexadental orthodontic SaaS, Good Samaritan Hospital coding optimization, Vermont inn/sober living real estate package) to demonstrate breadth of application
- Focused practical conversation on applying Genesis specifically to NVFP -- discussed EMR integration challenges, HIPAA compliance approaches (de-identification vs. BAA with cloud providers), data cleaning timelines, and a phased implementation starting with non-HIPAA areas like marketing and financial analysis
- Discussed HIPAA compliance in substantial depth (de-identification scripts, Google Cloud Platform BAA, HIPAA-compliant tools like GenSpark, enterprise Claude licensing)
- Proposed a $10K/month consulting engagement with a 3-month initial commitment, framing it as "analysis and planning with some prototyping" that produces handover-ready deliverables
- Tone was collaborative and educational -- teaching David and Ned the technology while demonstrating practical applications to Natasha's specific problems
- Acknowledged the alternative DIY path: "We're teaching people the technology and methodology in the spring retreat... do you want to do something better and faster with the top experts, or do you want to have your own team do it and save some money?"

### To Katrina Skinner (March 10, 2026)

**Audience context**: New contact, introduced through Beyara/Wing mastermind. CEO and founder of Fairhope Pediatrics plus Women in Pediatrics and Pediatric CEO (coaching/community for pediatric practice owners). Attended Latie and Kenji's Prosperity Conference where Mark spoke. AI user but self-described limited knowledge. Potential partner for reaching pediatric practice owner audience.

**Presentation approach**:
- Led with his background and credibility story (MD who got into AI early, sold one company, lost money on biotech, back in AI for three years, the exponential improvement of AI models)
- Focused on business outcomes and methodology rather than deep technical architecture -- explained RAG conceptually ("a shared brain") without going into vector vs. graph database detail
- Emphasized the venture studio partnership model heavily -- positioned Katrina's "Pediatric CEO software" idea (merging financial and quality metrics) as exactly the kind of industry problem suited for a joint SaaS product
- Showed the Nexadental demo as the primary example of what a venture studio partnership produces, then briefly mentioned the hospital coding case
- Mentioned advanced technologies (RoovView Wi-Fi sensing, federated brain, quantum-inspired computing) to establish the frontier of what is possible and create excitement about the platform's trajectory
- Played the Puerto Rico retreat video to showcase the community experience and culture
- Positioned multiple on-ramps: mastermind ($15K/year or $2K/month), retreats ($6K with discounts), AI Bootcamp for Physicians, AI Physician Collective (slower pace), and the venture studio for SaaS product development
- Proposed an affiliate partnership ($1,500 per mastermind sign-up) and guest speaking to her Pediatric CEO cohort
- Tone was sales/partnership-oriented -- building excitement, establishing credibility, creating a vision of what they could build together

### What Stayed Consistent Across Both Calls

- The 4-step methodology (import, research, analyze, build) was presented identically
- Nexadental was the primary case study in both calls, with the same metrics and demos shown
- Hospital coding was the secondary example in both calls, with the same framing of "up to three times reimbursement for the exact same patient"
- The explanation that "models don't learn, but our knowledge engine does" was articulated consistently
- HIPAA compliance was confirmed as a capability in both calls
- Open-source stack plus Claude foundation was stated in both calls
- The swarm/agent orchestration concept (60 agents, 20 running simultaneously, AI-orchestrated) was described consistently
- The "value versus effort" prioritization framework for implementation decisions
- The acknowledgment that AI hallucinates and requires human domain expertise for validation
- The financial model capability was referenced in both calls (better than $100K investment bank models)
- The framing that competitors exist for individual pieces but not the integrated platform

---

## 4. Genesis vs. The Market (Competitive Positioning)

Based on Mark's comments across both calls, Genesis occupies a unique market position:

**Against point solutions**: Competitors exist for individual capabilities -- voice AI for answering phones (Mark mentions "two other competitors" when they built Nexadental's phone agent), workflow automation tools, business intelligence dashboards. But Genesis is not competing on any single feature. It is the integrated platform that produces all of these as outputs of a unified methodology. Mark explicitly chose not to compete on the phone agent feature: "I don't want to compete on a feature."

**Against N8N and workflow automation**: Mark positions N8N as a "fast path" with "cost and scalability limitations." Genesis builds its own automations directly rather than relying on a third-party workflow engine. The implication is that N8N introduces dependencies, per-execution costs, and architectural constraints that Genesis avoids.

**Against Claude's own agent teams**: Claude/Anthropic released "agent teams" approximately 2-3 weeks before the Katrina call. Mark notes this does "a fraction" of what Genesis has been doing for six months. This positions Genesis as significantly ahead of even the AI providers' own multi-agent offerings.

**Against management consulting**: Practice IQ is explicitly positioned against traditional consulting engagements: "The industry consultants do this and it costs about $100,000... we charge $3,000 for it." The AI-generated financial models are compared favorably to those produced by investment banks ("better than financial models that I've paid a hundred thousand dollars for").

**Against enterprise AI platforms**: Genesis runs on open-source technology on commodity hardware. The graph database alone, if purchased commercially, "would cost what they charge" for the entire service. Claude Max is $200/month. This dramatically undercuts enterprise pricing while delivering comparable or superior capability.

**The GNN learning capability as unique differentiator**: Mark repeatedly emphasizes that the self-learning graph neural network is what separates Genesis from everything else. Standard RAG implementations (which most competitors use) store and retrieve knowledge but do not learn. The GNN's ability to autonomously optimize toward goals is framed as genuinely novel.

**Bootstrapped vs. VC-funded**: Mark explicitly describes moving away from the traditional VC-funded company-building approach: "I used to build them with a bunch of venture capital and it took time to build products. Now we bootstrap them because it's so fast and easy to create an AI native company." VC funding is reserved for when product-market fit is established and a dedicated team needs to be hired.

---

## 5. The Genesis Business Model

Genesis is monetized through multiple channels targeting different client segments and engagement levels:

### Education and Community

- **HeroForge Mastermind Pro**: $15,000/year (annual) or $1,997/month. Rolling enrollment. Includes weekly lessons with workshops, weekly office hours, quarterly retreat discounts (two $2,500 discounts per year for annual members), on-demand foundations course, and access to the Genesis platform and methodology. A 10% discount is available for Beyara/Wing members (code BEYARAVIP).

- **Quarterly Retreats**: $6,000 per retreat (all-inclusive: accommodations, activities, meals). Discounts for annual mastermind members. Guests welcome ($2,500 if participating in programming). Three nights of intensive teaching, coaching, and building. Spring 2026 in San Diego, summer 2026 likely Norway or Finland, fall 2026 at Killington, Vermont property.

- **AI Bootcamp for Physicians**: Six-week course in partnership with Peter Kim. One lesson per week, one workshop per week, office hours. First cohort completed, second starting April 2026. Recommended time commitment of a couple hours per week minimum.

- **AI Physician Collective**: A slower-paced alternative to the mastermind, jointly created with Peter Kim. For those who want to learn but cannot keep up with the mastermind's weekly pace of cutting-edge content.

### Direct Consulting

- **Consulting engagement**: $10,000/month, 3-month minimum recommended (described in Natasha call). Includes regular meetings, teaching, collaborative building, analysis and planning of the client's business, prototyping, and handover of deliverables. After the initial engagement, ongoing development can continue at the same budget or be scoped separately for larger projects.

### SaaS Products (Industry-Specific)

- **Practice IQ**: Business assessment report. $3,000 per report. Highly automated process: connect to PMS, extract data, identify missing information, dynamically generate a supplemental form, generate the report. Potential to become free as a lead generator.

- **Lead IQ**: AI phone/lead agent. Answers phone, follows up on leads via call/text/email. Operates 24/7. Pricing not explicitly stated in the calls.

- **Inside IQ**: Real-time operational dashboard pulling nightly from billing systems. Pricing not explicitly stated in the calls.

### Venture Studio

- **Partnership model**: For clients with industry problems that could become SaaS products. Mark's team acts as the technology partner, the client provides domain expertise. One full-time developer plus Mark's oversight, weekly meetings with the client. The orthodontic partnership with Nick Kim (Nexadental) is the first and primary example. Builds for the client's own business and simultaneously for the industry as a sellable product.

### Affiliate Program

- **Mastermind referrals**: $1,500 per sign-up credited to the affiliate. Discussed with Katrina as a way to monetize her audience (Pediatric CEO community, Women in Pediatrics). Also mentioned extending to AI Bootcamp affiliate tracking.

---

## 6. Open Questions and Gaps

The following remain unclear, unresolved, or insufficiently detailed across both calls:

**Technical Implementation Details**
- Specific GNN architecture, training methodology, and how it interfaces with the vector and graph databases in practice
- How the "federated brain" works operationally for business clients (described conceptually as "like a blockchain" with "97% compression" but no implementation details)
- What "quantum-inspired computing on regular hardware" means in concrete terms and what business applications it enables today
- How the 60 development agents are configured, versioned, and maintained as the underlying models evolve

**Deployment and Operations**
- Exact timeline from initial knowledge base build to production deployment of a full solution (the 12-16 week timeline shown on slides was not discussed in detail)
- Scalability metrics: how many concurrent users, how many businesses can be served simultaneously, infrastructure requirements at scale
- How multi-tenant data isolation works when the platform is deployed as a SaaS (each client has their own knowledge base, but how is this managed?)
- Disaster recovery, backup, and data durability for the knowledge engine
- How model updates (new Claude versions) are incorporated without disrupting running production systems

**Regulatory and Compliance**
- Whether any formal HIPAA audit or certification has been completed, or if compliance is self-assessed based on following HIPAA practices
- SOC 2 or other security compliance certifications
- How the BAA chain works in practice (client -> HeroForge -> Google Cloud Platform -> model provider)
- Data retention and deletion policies, particularly for de-identified data

**Product and Pricing**
- Pricing for Lead IQ and Inside IQ as standalone SaaS products
- Pricing and structure for the venture studio partnership (equity split, IP ownership, ongoing revenue sharing)
- How Practice IQ scoring benchmarks are validated against actual industry data (the AAO data is referenced, but the scoring methodology is not detailed)
- Product roadmap: what comes after Practice IQ, Lead IQ, and Inside IQ

**Business Model**
- Revenue and client metrics (number of mastermind members, number of consulting clients, number of Nexadental customers)
- Team size and composition beyond Mark and the core developer ("Roov")
- How the platform's capabilities scale as the client base grows -- is each deployment a significant manual effort, or is it approaching self-service?
- Long-term defensibility: if the underlying models keep improving and Claude releases more agent capabilities natively, how does Genesis maintain its advantage?

**From the Natasha Call Specifically**
- NVFP next steps were left at "we have some other work to do internally before we would get into it"
- The EMR integration question (EMDs) was acknowledged but not resolved
- Whether the $10K/month engagement was accepted or is still under consideration

**From the Katrina Call Specifically**
- Whether Katrina will join the mastermind and/or attend the San Diego retreat (follow-up email suggests strong interest with intent to bring friends)
- Timeline and terms for the Pediatric CEO SaaS venture studio partnership
- Details of the speaking engagement to her May cohort
- Whether the affiliate partnership for AI Bootcamp was set up (Mark said he'd "talk to Peter about it")

---

*Document compiled from primary source transcripts and correspondence. All quotes are from Mark Allen unless otherwise attributed. Intended for internal reference only.*
