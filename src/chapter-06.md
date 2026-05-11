# Chapter 6: On Completeness {#chapter-6:-on-completeness}

> **Under development:** This chapter is still being written and may have entirely different words in it at any moment.

Ask most technical writers what makes documentation complete, and they'll give you a laundry list: comprehensive feature coverage, exhaustive API references, detailed troubleshooting guides, multiple examples for every use case. This approach treats completeness as an inventory problem—if you document everything that exists, you've achieved completeness.

But this misses the fundamental question: complete for whom, and for what purpose?

After working with dozens of product teams across different industries and maturity stages, I've learned that completeness isn't about documenting everything that's possible. It's about documenting everything that's necessary for your users to succeed in their specific contexts. And those contexts vary dramatically based on where your product is in its lifecycle, who your users are, and what they're trying to accomplish.

The traditional approach to completeness creates several predictable problems. Teams exhaust themselves trying to document every feature and edge case, often before they understand which features actually matter to users. Writers create comprehensive reference materials that nobody reads because they don't match how people actually work. Documentation becomes a reflection of the product's complexity rather than a bridge to the user's success.

There's a more strategic way to think about completeness—one that adapts to your product's reality and serves your users' actual needs.

## Completeness Across Product Maturity {#completeness-across-product-maturity}

Just as accuracy requirements change as products evolve, so does the definition of completeness. The completeness standard that makes sense for a mature enterprise platform would be wasteful and counterproductive for a startup's MVP.

For newer products, completeness means thoroughly documenting the specific scenarios that comprise your minimally viable product. These are the user journeys that you've validated, tested, and committed to supporting. Everything else is speculation.

When working on documentation for early-stage products, completeness doesn't mean documenting every possible integration or advanced workflow. It means making sure users can successfully complete the core scenarios that define your product's value proposition. Those fundamental use cases need to be documented completely and clearly. Advanced features and edge cases can wait until the product and user base mature.

This focused approach to completeness serves both users and the product team. Users get reliable guidance for the workflows that actually work well. The product team avoids over-committing to features that might change or disappear. Resources go toward perfecting the core experience rather than documenting theoretical possibilities.

As products mature and stabilize, the definition of completeness naturally expands. Your user base grows more diverse, with different skill levels and use cases. Features that were experimental become foundational. Edge cases that affected few users in the early days now impact thousands of users.

But even for mature products, completeness remains strategic rather than exhaustive. Amazon Web Services has thousands of features across hundreds of services, but their documentation doesn't try to document every possible combination and configuration. Instead, they focus completeness efforts on the workflows that drive the most user success and business value.

The key insight is that completeness should scale with your product's proven value, not its theoretical capabilities. Document completely what you know works well and supports reliably. Be more selective about scenarios that are possible but not yet proven or prioritized.

## User-Centric Completeness {#user-centric-completeness}

Completeness also varies dramatically based on who your users are and what they're trying to accomplish. What feels complete to a power user will overwhelm a beginner. What seems comprehensive to a developer might be useless to a business user. Even for highly technical documentation, completeness is ultimately about user success, not feature coverage.

Consider database documentation. For a database administrator setting up a new cluster, completeness means detailed coverage of installation, configuration, security settings, monitoring, backup procedures, and disaster recovery. Missing any of these topics leaves them unable to deploy the database safely in production.

For an application developer who just needs to store and retrieve data, completeness means clear guidance on connecting to the database, executing queries, handling errors, and managing connections efficiently. They don't need the DBA-level details about cluster configuration—including that information actually makes the documentation less complete from their perspective because it obscures what they need to know.

For a data analyst who needs to extract insights from stored data, completeness means comprehensive coverage of query syntax, functions, performance optimization, and data export options. Installation and configuration details are irrelevant to their success.

Same database, same feature set, but three completely different definitions of completeness based on user goals and contexts.

This user-centric view of completeness explains why so much technically comprehensive documentation fails to help users accomplish their actual work. The documentation covers everything about the product, but it doesn't cover everything the user needs to be successful with the product.

The most effective documentation teams I've worked with start by mapping user journeys rather than product features. They identify the key scenarios that each user type needs to complete successfully, then ensure those scenarios are documented completely from the user's perspective. Features that don't serve those core journeys get secondary treatment, regardless of how sophisticated or impressive they might be from a technical standpoint.

## The Content Void Problem {#the-content-void-problem}

Even when teams understand that completeness should be user-focused and maturity-appropriate, they often fall into a predictable pattern that creates what I call the "content void”  of documentation completeness.

Teams love to create quickstarts. These short, "hello world" topics give teams a quick adrenaline rush of writing something clearly valuable. And it's true—a good quickstart is genuinely helpful to new users. It proves that your product works and gives people confidence to explore further.

Teams also love to write deep technical tutorials. These are weighty, comprehensive topics that showcase the full power of whatever they're building. Teams love them because they demonstrate impressive capabilities and complex use cases. But if I'm being honest, they also love writing them because they get to show off their own knowledge and technical sophistication.

What about the content in between? That content frequently gets left behind, because it's harder than writing a quickstart, and nowhere near as exciting as writing an in-depth tutorial. The quickstart can be knocked out in an afternoon. The comprehensive tutorial feels like a significant accomplishment that demonstrates expertise. But the middle content requires understanding user progression, breaking down complex workflows, and creating stepping stones that aren't as flashy but are absolutely critical for user success.

So you end up with this content void for most content sets. On one side, you have quickstarts that get users started but don't help them progress. On the other side, you have in-depth tutorials that demonstrate advanced capabilities but assume massive leaps in user knowledge and confidence. And in between is a wasteland of missing content that users have to somehow navigate on their own to build their expertise.

Consider Angular documentation as an example. You might have a quickstart that shows users how to create their first component—a simple "Hello World" that displays some text and maybe handles a click event. Then you have comprehensive tutorials that walk through building a complete e-commerce application with routing, reactive forms, HTTP client integration, state management, authentication, and deployment strategies.

But what about the progression between these extremes? How do you go from displaying "Hello World" to building components that communicate with each other? How do you handle user input before you're ready for complex reactive forms? How do you make HTTP requests before building a full e-commerce checkout flow? These intermediate steps get skipped, leaving users to figure out the progression on their own.

This is why you see documentation sets that have topics like "Create your first component" that immediately jump to "Build a full-featured application with authentication, routing, and API integration." There's nothing in between to help users progress from basic component creation to sophisticated application architecture.

The gap creates several problems:

**User Abandonment:** Users complete the quickstart successfully, feel confident about the product, then hit a wall when they try to build something real. They can't bridge the gap between the simple example and the complex tutorial, so they either struggle with inadequate guidance or abandon the product entirely.

**Skewed User Progression:** The only users who successfully advance beyond the quickstart are those who already have significant expertise or unusual persistence. This creates a user base that skews toward advanced users, which can distort product priorities and feedback.

**Wasted Advanced Content:** Those impressive comprehensive tutorials often don't get used because most users never develop enough confidence and knowledge to attempt them. The content that teams are most proud of becomes least accessible to their actual user base.

But here's the silver lining: if you haven't documented how to do something users want to do, the users will tell you\! This focused approach to completeness creates a natural feedback loop where real user needs drive documentation priorities rather than theoretical feature coverage.

## Filling the Void {#filling-the-void}

One of the most effective approaches I've found for addressing the content void is to start with those in-depth tutorials that teams want to write anyway, then deliberately break them down into standalone, progressive pieces.

Take that comprehensive content management system tutorial. Instead of presenting it as a single intimidating guide, decompose it into discrete topics: database schema design, user authentication, basic CRUD operations, input validation, error handling, user authorization, automated testing, deployment considerations. Each piece should stand on its own while also serving as a building block for more complex scenarios.

This approach satisfies teams' desire to create impressive comprehensive content while solving the real problem of missing progression. Users can work through the components at their own pace, building confidence and expertise incrementally. They can also mix and match components based on their specific needs rather than following a single prescribed path.

The key is ensuring each middle-ground topic truly stands alone. It should have clear prerequisites, explicit learning objectives, and practical outcomes that users can validate. Avoid the temptation to assume knowledge from previous topics or to set up dependencies that force users through a rigid sequence.

Consider authentication and database connectivity as an example. This topic should cover everything needed to securely connect to a database and verify user credentials, including error handling for common failure scenarios. Users should be able to implement this functionality successfully without having read other topics in the series. But it should also integrate cleanly with more advanced topics like user authorization and session management.

Some teams resist this decomposition because they worry about repetition or redundancy. They don't want to explain basic concepts multiple times across different topics. But this concern misses the point—users don't read documentation linearly like a novel. They jump to topics based on immediate needs, often months apart. A little redundancy in service of standalone utility is almost always worth it.

## Identifying What's Missing {#identifying-what's-missing}

The challenge is recognizing when you have a content void problem and systematically identifying what belongs in that missing middle ground.

The most reliable diagnostic is user behavior and feedback patterns. If you see a consistent pattern where users successfully complete your getting-started content but then struggle to progress to more advanced scenarios, you probably have a gap problem. If your support team repeatedly answers questions that seem like they should be covered in documentation, those questions often point to missing middle content.

Pay attention to the questions users ask in community forums, support tickets, and sales calls. Questions that start with "I've successfully completed the quickstart, but now I need to..." or "The advanced tutorial assumes I know how to..." are clear signals of missing progression content.

Another approach is to audit your existing comprehensive tutorials with fresh eyes. Look for assumptions, leaps in complexity, or points where the tutorial suddenly introduces multiple new concepts simultaneously. These are often opportunities to extract standalone topics that bridge the gap between basic and advanced content.

Consider involving users in content gap analysis. Users who have successfully progressed from beginner to intermediate or advanced usage can provide valuable insights about what information they wish they'd had at different stages. They remember the struggle points and knowledge gaps that your expert team members may have forgotten or never experienced.

The most systematic approach is to map actual user progression paths rather than theoretical feature coverage. Track how users actually move through your product and documentation. Where do they get stuck? What workflows do they attempt after completing basic tutorials? What combinations of features do they typically use together? This behavioral data reveals the natural stepping stones that your documentation should provide.

## Sustainable Completeness {#sustainable-completeness}

Achieving and maintaining appropriate completeness requires ongoing effort and strategic thinking. It's not a one-time documentation project—it's an ongoing alignment between your content strategy and your users' evolving needs.

**Start with Core Journeys:** Instead of trying to document everything, identify the 3-5 most important user journeys for your product and ensure those are completely and clearly documented. Everything else is secondary until those core paths work well.

**Build Feedback Systems:** Create mechanisms for users to identify gaps and report completeness problems. But more importantly, build processes for acting on that feedback systematically. A "suggest improvements" link that disappears into a backlog isn't useful—you need workflows that turn user feedback into content improvements.

**Measure User Success, Not Content Volume:** Track whether users can successfully complete the workflows your documentation describes, not how many topics you've published. Completion rates, success metrics, and user progression data are better indicators of completeness than content audits.

**Design for Progression:** Explicitly plan how users will develop expertise over time. What should they learn first? What builds on previous knowledge? What are the natural next steps after each major workflow? Design your content architecture to support this progression rather than hoping it emerges naturally.

**Maintain Content Relationships:** As your product evolves, keep track of how content topics relate to each other. When you update one piece of documentation, consider what other topics might need updates to maintain consistency and completeness across the user journey.

The goal isn't perfect completeness—it's strategic completeness that serves your users' success and grows appropriately with your product's maturity and user base. Focus your completeness efforts where they have the most impact on user outcomes, and resist the temptation to document everything just because it exists.