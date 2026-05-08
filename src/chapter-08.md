# Chapter 8: On Discoverability {#chapter-8:-on-discoverability}

In my twenty-five years of writing technical documentation and thinking about how users actually consume information, there is one metaphor that continues to persist, over and over again: the book metaphor. If you look at any documentation set, they all have a left navigation that outlines the contents of the documentation just like you would with a book. There's an introduction, a number of chapters organized in logical sequence, and an underlying assumption—whether acknowledged or not—that users will read the content in that order, from start to finish.

That's not how people read technical documentation.

The book metaphor made sense when documentation was literally printed in books, when users had to flip through pages sequentially to find information. But in our digital world of search engines and AI assistants, where users can land on any page from any search query, this linear thinking actively works against user success.

The reality is that any topic might be the first topic a user reads, and any topic might be the last. Users don't start at your carefully crafted introduction and work their way through your logical progression. They arrive at your content through Google searches, AI queries, colleague recommendations, and support ticket links. They jump between topics based on immediate needs, not your intended narrative flow.

When we think about putting documentation systems together—because they are systems, not books—we need to acknowledge how users actually discover and navigate content.

## Beyond Content Types {#beyond-content-types}

The traditional approach to documentation organization focuses on content types: reference materials, API documentation, conceptual overviews, tutorials, and troubleshooting guides, just to name a few. This approach assumes that users think in terms of content types—that they wake up in the morning and decide, "Today I need to read some conceptual material."

Users don't think this way. They think in terms of goals and problems: "I need to integrate payments into my application" or "Why is my API call failing?" They don't care whether the answer comes from a reference page, a tutorial, or a troubleshooting guide—they just want to accomplish their objective.

The best documentation sets don't restrict themselves to artificial content-type boundaries. Stripe's API documentation exemplifies this approach beautifully. They didn't limit their API reference to just describing objects and methods. They included comprehensive coverage of authentication workflows, checkout processes, webhook handling, and error management—topics that traditional thinking would categorize as "conceptual" or "tutorial" content that doesn't "belong" in an API reference.

This works because Stripe organized their documentation around user workflows rather than internal content taxonomies. When developers are implementing payment processing, they need to understand both the specific API calls and the broader context of how those calls fit into secure transaction flows. Stripe's documentation serves both needs in one coherent experience rather than forcing users to jump between different content types to piece together a complete understanding.

## The Sherpa Approach {#the-sherpa-approach}

Great documentation doesn't just respond to user queries—it acts like a sherpa or guide. It's there to get you where you want to go, but also to help you discover interesting and valuable things along the way that you might not have known to look for.

A good sherpa doesn't just follow your exact instructions to get from point A to point B. They help you understand the terrain, point out important landmarks, suggest better routes based on current conditions, and alert you to opportunities or hazards you might not be aware of. They're proactive guides who enhance your journey rather than reactive responders who only answer direct questions.

Traditional documentation is more like basic signposts. It points you toward the specific destination you asked about, but it doesn't help you discover that you're asking the wrong question, or that there's a better route you haven't considered, or that there's a related destination that would solve your broader problem more elegantly.

But implementing the sherpa approach requires careful balance and respect for user intentions. There's a tension between guiding users toward valuable discoveries and respecting their immediate goals and cognitive load.

## Respecting User Time and Intent {#respecting-user-time-and-intent}

The first principle of discoverable documentation is respecting your users' time and intentions. Users aren't typically on a journey to find something new and exciting—they're trying to get something specific done, often under pressure or time constraints.

I learned this lesson clearly during my time at Stripe, where we faced constant pressure from product teams who wanted to promote beta features and new capabilities in our documentation. These teams were acting with good intentions—they wanted to share innovative solutions that could genuinely help users. But those users weren't browsing for innovations. They were trying to implement payment processing, resolve integration issues, or meet project deadlines.

Adding promotional content or feature callouts to task-focused documentation creates cognitive overhead that interferes with user success. It's like a sherpa asking if you want to climb Kilimanjaro instead when you're focused on reaching Everest base camp before dark. Kilimanjaro might be a genuinely rewarding expedition, but it's not what you signed up for and it doesn't help you accomplish your immediate goal.

This doesn't mean never exposing users to new capabilities—it means being strategic about when and how you do it. The key is understanding the difference between users who are in exploration mode versus execution mode, and designing your content experience accordingly.

## Orientation and Self-Triage {#orientation-and-self-triage}

Since any topic might be a user's first encounter with your documentation, every piece of content needs to help users quickly determine whether they're in the right place. This is like calling a support line and reaching the wrong department—a good support center quickly helps you identify where you actually need to be and gets you there efficiently.

Effective content orientation happens upfront, usually in the first paragraph or section. There's a simple pattern you can use to implement this approach consistently. For every topic, create a three-sentence introduction: The first sentence explains why the content matters—what value or outcome it provides. The second sentence describes what the topic will specifically cover. The third sentence offers links to related topics in case the user realizes they're in the wrong place.

Good orientation also includes contextual information about prerequisites, scope, and related topics. If a user needs to complete other setup steps first, or if the content assumes familiarity with certain concepts, that should be clear from the beginning. Similarly, if there are alternative approaches or more appropriate starting points for their specific situation, those should be signposted early.

However, be careful not to create prerequisite chains that frustrate users. I've encountered documentation sets where I had to navigate through three levels of prerequisites before I could access the topic I actually wanted to read. Good orientation mentions essential prerequisites without creating a maze of dependencies that prevents users from reaching their goals.

This upfront investment in orientation saves time for both users who are in the right place (they can proceed with confidence) and users who are in the wrong place (they can redirect their efforts quickly rather than getting lost in irrelevant content).

## No Dead Ends {#no-dead-ends}

One of my fundamental rules for documentation structure is that no topic should ever be a dead end. Every piece of content should give users logical places to go next, should they choose to continue their journey.

This principle flows naturally from thinking like your users. After completing a tutorial, users might want to learn more about the API calls they just implemented, or they might want to add additional features to what they built, or they might want to understand how to troubleshoot common issues. After reading a reference page, they might want to see practical examples of implementation, or understand how that feature fits into larger workflows.

Designing for logical next steps requires understanding user progression patterns and common workflow sequences. It also helps identify unintended gaps in your content—if you can't think of appropriate next steps for a topic, that might indicate missing content that would serve your users.

The "no dead ends" principle doesn't mean overwhelming users with every possible option. It means providing 2-3 thoughtful suggestions that represent the most common and valuable paths forward from that specific content. These suggestions should be based on actual user behavior and feedback rather than assumptions about what users might find interesting.

## The Information Architecture Problem {#the-information-architecture-problem}

Despite the importance of user-centric organization, information architecture remains crucial even in an age of search and AI-powered content discovery. I've seen many documentation sets—Angular was one example when I worked on it several years ago, though it has improved since—where the categories of content simply didn't make sense. They were generic, poorly defined, and worst of all, there was often content that didn't fit into any of the established buckets.

To this day, when I see a section of documentation labeled "Advanced Topics," I know what that really means: "We didn't know where to put this information, so we shoved it here." Advanced Topics is the kitchen junk drawer of documentation—a catch-all category that serves no one well.

The broader problem is relying on complexity-based categories at all. Terms like "Fundamentals," "Intermediate," and "Advanced" are meaningless without user context. What's fundamental to a database administrator is radically different from what's fundamental to an application developer. What Stripe considers basic payment processing might be incredibly advanced for someone who's never handled financial transactions before.

These vague labels are actually a symptom of not understanding your users well enough. Effective information architecture uses categories that describe actual user goals and contexts: "Setting up authentication," "Handling payment failures," "Multi-party transactions," "Compliance requirements." These labels help users identify relevant content based on what they're trying to accomplish rather than forcing them to guess which arbitrary complexity level matches their needs.

## The Garage Cleanout Process {#the-garage-cleanout-process}

When I work with teams on information architecture, I often use the typical garage that you'd find anywhere in the United States as a metaphor. In the US, people store all sorts of things in their garages—tools, holiday decorations, sports equipment, old furniture, boxes of miscellaneous items. So much accumulates that many people can't even park their cars in their garages anymore.

Sooner or later, a homeowner decides they need to clean their garage out. This process has two essential steps. First, you pull everything out and ask yourself: "Do I actually need this? Why?" You ruthlessly get rid of things that aren't important or useful anymore. Second, when you put things back, you organize them not only so you know where everything is, but so there's room for additional items as you acquire them.

The same principle applies to documentation. Review everything in your current information architecture and honestly assess whether it's still helpful to users. You can determine helpfulness partially through user feedback and analytics, but you can also evaluate it by observing how often content gets updated and maintained. Content that consistently falls behind or gets ignored probably isn't serving an important user need.

When you rebuild your content system, look at your product roadmap and planned releases. Can you quickly identify where future content would fit in your new information architecture? If you can't immediately see where new features or capabilities would belong, your IA needs more work.

This is a continuous process, not a one-time project. Every couple of years, you should review your documentation and clean out the garage. Products evolve, user needs change, and content that was once valuable may become obsolete or redundant.

## The Development Analogy {#the-development-analogy}

When working with developer audiences, I often explain information architecture problems using programming concepts they already understand. Just as novice developers might create a "helper" class that seems logical initially but quickly becomes a dumping ground for unrelated properties and methods, documentation teams create categories like "Advanced Topics" that seem reasonable but become incoherent grab bags over time.

Both problems stem from taking the easy categorization path instead of doing the harder work of understanding actual relationships and usage patterns. It's much easier to create an "Advanced Topics" category than to figure out why certain content doesn't fit your existing structure, or whether your structure needs to evolve to accommodate new types of content.

Like helper classes, these vague documentation categories seem harmless at first. "Advanced Topics" might start with 2-3 legitimately complex pieces of content. But over time, anything that doesn't obviously fit elsewhere gets tossed there, until it becomes an incoherent collection that serves no user need effectively.

The maintenance problems parallel programming as well. Helper classes become harder to refactor over time because dependencies become unclear and interconnected. Similarly, the longer you let content accumulate in vague organizational buckets, the harder it becomes to reorganize properly because you lose track of user relationships and workflow connections.

## The Roadmap Test {#the-roadmap-test}

I mentioned earlier that, when cleaning out your garage, you should not only remove what you don't need, but think about what you might need in the future. For documentation, I call this the Roadmap Test. Look at your product's planned features and releases for the next 12-18 months. For each new capability or enhancement, ask yourself: "Where would documentation for this feature belong in our current IA? Can I identify the logical location immediately, or would I be tempted to create a new top-level category or throw it into a miscellaneous section?"

If you constantly struggle to place future content in your existing structure, that's a strong signal that your IA is organized around your current product state rather than user workflows and goals. Good information architecture should be flexible enough to accommodate product evolution without requiring constant restructuring.

The roadmap test also helps you identify emerging content themes that might warrant new organizational approaches. If you notice that several upcoming features all relate to a specific user workflow or use case that isn't well-represented in your current structure, that might indicate an opportunity to reorganize around that user journey.

And just as you don't clean out your garage only once, you should continuously examine your information architecture. The roadmap test isn't a one-time evaluation—it's an ongoing practice that helps you stay ahead of organizational problems before they become entrenched.

## Discoverability in the Age of AI {#discoverability-in-the-age-of-ai}

Even as users increasingly find content through AI queries rather than browsing hierarchical navigation, underlying information architecture remains crucial. AI systems need to understand the relationships between concepts, the logical progression of user workflows, and the context in which different pieces of content are most valuable.

Well-structured information architecture actually enhances AI-powered discovery by providing clear semantic relationships that help AI systems surface the most relevant content for specific queries. When your IA is organized around user goals and workflows, AI tools can better match user intent with appropriate content, even when users don't know exactly what they're looking for.

The sherpa principle becomes even more important in AI-mediated discovery. When users ask an AI assistant for help, they want guidance that goes beyond just answering their immediate question—they want to understand the broader context, learn about related concepts that might be relevant, and discover solutions they hadn't considered.

## Building for Discovery {#building-for-discovery}

Effective discoverability requires thinking systematically about user journeys while designing for the reality that users will enter and exit your content at unpredictable points. This means:

**Every topic must be able to act as an entry point** into the rest of the documentation set while connecting meaningfully to the broader system. Users should be able to understand and act on the content regardless of where they came from or what they read previously.

**Navigation should reflect user workflows** rather than internal product organization. Categories and labels should match how users think about their work, not how your company organizes its feature development.

**Content relationships should be explicit** rather than assumed. If topics build on each other or relate to common workflows, those connections should be clearly surfaced through strategic linking, contextual suggestions, and logical progression cues.

**Discovery should be progressive** rather than overwhelming. Instead of presenting users with every possible option, focus on the 2-3 most valuable next steps based on common usage patterns and user feedback.

The goal isn't to control how users navigate your content—it's to support their natural discovery patterns while gently guiding them toward information that will help them succeed. Like a good sherpa, effective documentation gets users where they want to go while helping them discover valuable things they didn't know they needed.