# Chapter 5: On Accuracy {#chapter-5:-on-accuracy}

When most people think about accuracy in technical writing, they imagine it as a binary state: information is either accurate or it isn't. In this view, good technical writing means getting every detail exactly right, while inaccurate writing is simply failed writing. But after years of working with products at different stages of maturity—from startup MVPs to enterprise platforms serving millions of users—I've learned that accuracy is far more nuanced and strategic than that simple binary suggests.

The traditional approach to accuracy creates impossible situations. Teams demand perfect documentation for imperfect products. Writers spend weeks documenting edge cases that may never ship. Users get frustrated when reality doesn't match the comprehensive promises made in documentation. Meanwhile, the core use cases that actually matter to users get lost in a sea of theoretical completeness.

There's a better way to think about accuracy—one that's strategic, user-focused, and aligned with how products actually evolve in the real world.

## Accuracy Across Product Lifecycles {#accuracy-across-product-lifecycles}

One of the most common mistakes I see teams make is demanding what I call "GA docs for beta code." Picture this scenario: A product team is preparing to launch a new API. The engineers are still fixing critical bugs discovered in testing. Key features might be delayed to the next release. Error handling is inconsistent across endpoints. But the product manager insists that documentation must be "complete and accurate" before launch.

This creates an impossible situation: writers are asked to document with certainty something that is inherently uncertain. The resulting documentation either becomes obsolete before it's published, or it makes promises the product can't yet keep.

I've seen writers spend weeks crafting detailed explanations of features that get cut the day before launch. I've watched support teams field angry customer complaints because the documentation confidently described functionality that was still experimental. I've observed engineering teams delay product launches because they felt the documentation wasn't "accurate enough," even though the core functionality worked perfectly well.

The reality is that products and services in different lifecycle stages require fundamentally different approaches to accuracy:

Early-stage products (beta releases, version 1.0, proof-of-concepts) only need to be deeply accurate for the specific scenarios and use cases the team wants to enable. If you're launching a beta API for processing payments, you need bulletproof accuracy for the standard payment flow. But you don't need to exhaustively document every possible error condition, edge case, or integration pattern that might theoretically be possible.

Consider Stripe's early API documentation. When they were starting out, they didn't try to document every conceivable payment scenario. Instead, they focused laser-sharp accuracy on the core use case: accepting a payment. The documentation was incredibly precise about that flow—every parameter, every response, every error code that mattered for the basic transaction. But they didn't pretend to have solved every edge case in e-commerce.

Growing products (version 2.0, expanding feature sets, new user segments) need accuracy that scales with their ambitions. As your user base grows and diversifies, the range of scenarios that require accurate documentation expands. But it expands strategically, following user demand rather than theoretical completeness.

Mature products (established platforms, enterprise solutions, widely-adopted tools) need broader accuracy coverage because users will naturally try to push the boundaries of what's possible. When you're serving millions of users across thousands of different use cases, the long tail of edge cases becomes significant. But even then, not every edge case deserves the same level of documentation accuracy.

I sometimes flip the question to product teams: "Would you want beta docs for your GA product?" The answer is always no. Nobody wants their mature, stable product to feel experimental or unreliable. A customer evaluating your enterprise platform doesn't want to read documentation that hedges every statement with "this might work" or "we're still testing this."

This helps teams understand why the reverse is also problematic. Beta software with GA-level documentation promises creates expectations the product can't meet. It's not just misleading—it's strategically counterproductive.

## The Right Depth of Accuracy {#the-right-depth-of-accuracy}

The second major misconception about accuracy is that it requires exhaustive technical depth. This leads to documentation that reads like engineering specifications rather than user guides, where every implementation detail is meticulously explained whether it's relevant to the user or not.

I don't need to understand the chemical reactions in a baking recipe to successfully bake a cake. I need to know the ingredients, the proportions, the temperature, and the timing. The fact that gluten proteins form networks when hydrated and agitated might be fascinating to a food scientist, but it's not necessary information for someone who just wants to make bread.

Similarly, users don't need to understand every technical detail of how a system works to use it effectively. They need to understand the parts that affect their decisions and actions.

Consider database documentation. A developer using your database API needs to know that certain operations are atomic, but they probably don't need to understand the specific locking mechanisms that make atomicity possible. They need to know that indexes improve query performance, but they don't need to understand B-tree algorithms unless they're doing database optimization work.

The key is providing the right level of accuracy for the task at hand. This means focusing on what users need to know to accomplish their goals, not everything there is to know about the subject.

But here's where it gets tricky: different users have different depth requirements even for the same task. A database administrator setting up replication needs to understand consistency models in much more depth than an application developer writing simple queries. The same system, the same feature, but very different accuracy requirements.

I've seen technical writers get paralyzed by this variation. They try to accommodate every possible depth requirement in a single document, creating sprawling explanations that satisfy nobody. The beginner gets lost in details they don't need. The expert gets frustrated by explanations of concepts they already understand.

The solution isn't to find some middle ground that disappoints everyone equally. It's to be strategic about layering information. Start with the accuracy level that serves your primary user's immediate goals. Then provide clear paths to deeper information for users who need it.

Amazon Web Services does this well in their documentation. Their getting-started guides focus on the accuracy needed to complete basic tasks—creating resources, configuring settings, testing functionality. But they link extensively to deeper reference material, troubleshooting guides, and architectural best practices for users who need that additional depth.

The principle is simple: accurate enough to be useful, deep enough to be trustworthy, but no deeper than necessary for the immediate task.

## User-Centric Accuracy {#user-centric-accuracy}

Perhaps most importantly, accuracy is inherently user-centric. What counts as accurate depends entirely on who's using the information and what they're trying to accomplish. This seems obvious, but it's one of the most frequently violated principles in technical documentation.

Information that's perfectly accurate for a seasoned developer might be misleading or incomplete for someone new to software development. Consider this statement in API documentation: "Authentication uses standard OAuth 2.0 flow." For an experienced developer, this is accurate and sufficient—they know what OAuth 2.0 is, how it works, and what they need to implement. For a junior developer or someone new to API integration, this statement is technically accurate but practically useless. They need to understand what OAuth 2.0 means, why it's used, and what specific steps they need to take.

The same technical detail that's essential context for one audience might be distracting noise for another. A system administrator needs to know about memory usage patterns when configuring a server. An end user of the application running on that server doesn't need that information—it would just create unnecessary anxiety about performance.

This user-centric view of accuracy explains why so much technically correct documentation fails to help users accomplish their goals. The information is accurate in an abstract sense, but it's not accurate for the specific person trying to use it in a specific context.

I learned this lesson the hard way early in my career. I was documenting a complex enterprise software system, and I prided myself on getting every technical detail exactly right. The engineering team praised the documentation for its technical accuracy. But user support was still overwhelmed with questions that seemed like they should have been answered in the docs.

The problem wasn't that the documentation was inaccurate—it was that it was accurate for the wrong audience. I had optimized for technical precision rather than user success. The documentation answered questions that engineers had about the system, not questions that users had about accomplishing their work.

This means accuracy isn't just about getting the facts right—it's about getting the right facts for the right audience. It's about understanding not just what is true, but what truths matter to the people who will use this information.

Consider the difference between these two accurate descriptions of the same software feature:

Engineer-accurate: "The system implements exponential backoff with jitter for retry logic, starting with a 1-second delay and doubling until reaching a maximum of 30 seconds, with randomization to prevent thundering herd scenarios."

User-accurate: "If your upload fails, the system will automatically retry several times with increasing delays between attempts. You don't need to manually retry—just wait and the system will handle it."

Both statements are factually correct. But they're accurate for completely different audiences and use cases. The first is accurate for someone who needs to understand the implementation (perhaps to configure it or troubleshoot it). The second is accurate for someone who just needs to know what to expect when using the feature.

The best documentation often includes both levels of accuracy, but clearly separated and targeted. The user-facing explanation focuses on what the user needs to know to be successful. The implementation details are available for users who need that deeper understanding, but they don't get in the way of users who don't.

## Managing Accuracy in Practice {#managing-accuracy-in-practice}

Understanding these principles is one thing; implementing them in real organizations with real constraints is another. The most effective approach I've found is to create what I call a "content accuracy hierarchy" that aligns with how users actually discover and consume information.

The foundation of this hierarchy is focusing canonical documentation on what's established and working reliably. This is your official documentation—the content that appears in your main doc site, gets linked from your product interface, and represents what your company officially supports.

For this canonical content, accuracy standards should be high but strategically focused. Document the scenarios you want users to succeed with. Be precise about the features that are stable and supported. Don't hedge or equivocate about functionality that works reliably.

But what about newer or experimental features? What about edge cases that might work but aren't fully supported? This is where the hierarchy becomes crucial.

Let blog posts, developer advocates, community content, and experimental documentation explore the cutting edge. These content types have different expectations and allow for more uncertainty. A blog post titled "Exploring Advanced Use Cases with \[Product X\]" signals that readers are venturing into less certain territory. A developer advocate's conference talk about "bleeding edge features" sets appropriate expectations about stability and support.

This creates a clear content hierarchy: official documentation represents what the company stands behind, while other content sources can acknowledge uncertainty and explore emerging possibilities.

I've seen this work particularly well at companies like HashiCorp. Their official Terraform documentation focuses laser-sharp accuracy on core workflows and stable features. But their blog, community examples, and developer advocate content explores newer providers, experimental features, and complex architectural patterns that might not be ready for official documentation.

When documentation does need to cover less-established scenarios—and sometimes it must—the key is being transparent about the level of support. Users should understand when they're in well-supported territory versus when they're venturing into areas that might change or require troubleshooting.

Some effective ways to signal this:

Clear labeling: "Preview feature," "Beta functionality," "Advanced configuration"

Explicit support statements: "This workflow is supported by our customer success team" versus "This is a community-contributed solution"

Honest limitations: "This integration works well for datasets under 10GB" rather than claiming unlimited scalability

Update commitments: "This documentation is updated with each product release" versus "This guide was last updated in Q2 2023"

The goal isn't to make users feel uncertain about your product. It's to help them make informed decisions about which features to rely on for critical workflows and which ones to experiment with in non-production environments.

## Common Accuracy Pitfalls {#common-accuracy-pitfalls}

Even with these principles in mind, teams still make predictable mistakes when managing accuracy. Here are the patterns I see most often:

The Perfectionist Trap: Teams delay publishing documentation until they can make it "completely accurate." Meanwhile, users struggle with no documentation at all. Remember: accurate documentation about 80% of use cases is infinitely more valuable than perfect documentation that doesn't exist.

The Kitchen Sink Problem: Writers try to document every possible scenario with equal accuracy and detail. This creates overwhelming documents where critical information gets lost among edge cases. Be strategic about what deserves detailed accuracy treatment.

The Oracle Fallacy: Documentation promises more certainty than the product actually provides. This is especially common with AI/ML products, where outcomes are inherently probabilistic. Don't let your documentation make promises your product can't keep.

The Static Mindset: Teams treat accuracy as a one-time achievement rather than an ongoing process. Product features evolve, user needs change, and business priorities shift. Accuracy requires maintenance and updates, not just initial precision.

The Expert Bubble: Subject matter experts review documentation for accuracy, but they're not representative of actual users. What seems accurate and complete to an expert might be confusing or insufficient for someone less familiar with the domain.

## The Business Impact {#the-business-impact}

Companies often struggle with content accuracy because they haven't connected documentation quality to business outcomes. They see accuracy as a "nice to have" rather than a strategic necessity. But inaccurate documentation creates measurable business costs that compound over time.

Increased Support Overhead: Every inaccurate piece of documentation generates support tickets. I've tracked cases where a single misleading sentence in API documentation generated dozens of support requests per week. The cost isn't just the support team's time—it's also the engineering time required to investigate issues that turn out to be documentation problems rather than product problems.

Slower User Adoption: Users who can't trust your documentation will be hesitant to adopt new features or expand their usage of your product. They'll stick with workflows they've already figured out rather than risk encountering more documentation that doesn't match reality. This directly impacts feature adoption metrics and expansion revenue.

Frustrated User Churn: Users who repeatedly encounter inaccurate documentation develop learned helplessness. They stop trusting your content and start looking for alternative solutions. In B2B contexts, this can mean losing entire accounts over documentation quality issues.

Reduced Team Velocity: When internal documentation is inaccurate, your own teams move slower. Engineers waste time trying solutions that don't work. Product managers make decisions based on outdated information. Sales teams make promises that can't be kept. The productivity cost ripples through the entire organization.

But measuring these costs is genuinely difficult, which is why accuracy often gets deprioritized. Unlike feature development, where you can track user engagement and conversion rates, documentation accuracy has indirect and delayed impact that's harder to quantify.

The companies that do prioritize accuracy have usually learned this lesson through painful experience. They've lost customers, wasted engineering cycles, or missed market opportunities because of documentation problems. The abstract concept of "quality" became concrete when it hit their revenue or their team's productivity.

Some of the contributing factors I see most often:

Feature Shipping Pressure: Teams focus too heavily on shipping features because that's what directly generates revenue. Documentation is seen as overhead rather than an enabler of that revenue. But this creates a false economy—rushed documentation often costs more in support and user confusion than it saves in development time.

Measurement Challenges: It's very difficult to test the effectiveness of documentation in traditional product metrics. How do you know if people are using your documentation effectively? How do you measure the counterfactual—the support tickets that didn't happen because documentation was accurate? The business impact is real but often invisible to standard analytics.

Technical Depth Mismatches: Technical writers aren't always technical enough to properly assess accuracy, especially for complex developer tools or enterprise software. Some writers would bristle at me saying this, but it's true and it's important. You can't accurately document what you don't understand. This doesn't mean every technical writer needs to be a software engineer, but there needs to be sufficient technical depth somewhere in the content creation process.

The most successful teams I've worked with address these challenges head-on. They've found ways to measure documentation effectiveness (user success rates, support ticket categorization, onboarding completion metrics). They've invested in technical writers who can engage meaningfully with the products they're documenting. And they've connected documentation quality to business metrics that leadership cares about.

## Building Sustainable Accuracy {#building-sustainable-accuracy}

The goal isn't perfect accuracy—it's sustainable accuracy that serves your users and your business over time. This requires systems and processes, not just individual effort.

Establish Update Cycles: Different types of content need different accuracy maintenance schedules. API reference documentation might need updates with every release. Conceptual guides might be reviewed quarterly. Getting-started tutorials might need monthly verification. Don't treat all content the same way.

Create Feedback Loops: Build mechanisms for users to report accuracy problems, and more importantly, build processes for acting on that feedback quickly. A "report an issue" link that goes into a black hole is worse than no feedback mechanism at all.

Involve the Right People: Subject matter experts should review content for technical accuracy, but they shouldn't be the only reviewers. Include people who represent your actual user base in the review process. Their confusion often reveals accuracy problems that experts miss.

Design for Change: Accept that your product will change and design your documentation processes accordingly. This might mean focusing on principles rather than specific UI elements, or creating modular content that can be updated independently.

Track What Matters: Identify the business metrics that documentation accuracy affects—support ticket volume, feature adoption rates, user onboarding success—and track them over time. When you can connect documentation improvements to business outcomes, it becomes easier to justify continued investment.

The companies that achieve sustainable accuracy treat it as a product capability, not a content problem. They build systems, processes, and cultures that support ongoing accuracy rather than hoping it will emerge from individual effort and good intentions.