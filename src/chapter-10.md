# Chapter 10: On Meaning {#chapter-10:-on-meaning}

For content to have any quality, it has to have meaning for its intended user.

This seems obvious, almost trivially true. Of course documentation needs to be meaningful to users. But meaning in technical writing is more complex and fragile than most people realize. Content can be perfectly accurate, strategically complete, efficiently concise, easily discoverable, and rigorously consistent—and still fail completely if it doesn't connect to what users are actually trying to accomplish.

Meaning isn't just about having relevant information. It's about creating content that resonates with users' mental models, supports their workflows, and helps them make progress toward their goals. Without meaning, all the other characteristics of quality become irrelevant.

I've seen this failure of meaning countless times: API documentation that meticulously describes every parameter but doesn't explain when you'd use the API. Tutorials that walk through every step of a process but never clarify what problem the process solves. Reference guides that comprehensively catalog features but don't connect those features to user outcomes.

The cruel irony is that teams often create meaningless content while believing they're being user-focused. They conduct user research, gather requirements, and carefully document what users asked for. But they miss the deeper layer of meaning that connects information to purpose.

## The Difference Between Information and Meaning {#the-difference-between-information-and-meaning}

Information is what your product does. Meaning is why it matters to your users.

Consider these two approaches to documenting the same authentication feature:  
Information-focused: "The authenticate() method accepts a username string and password string as parameters and returns a boolean value indicating success or failure."

Meaning-focused: "Before users can access protected resources in your application, you need to verify their identity. The authenticate() method takes their login credentials and confirms whether they should be granted access."

Both are accurate. The first is more technically precise. But the second creates meaning by connecting the technical capability to the user's broader goal of controlling access to their application.  
The information-focused approach treats documentation as a catalog of capabilities. The meaning-focused approach treats documentation as a bridge between capabilities and accomplishments.

This distinction becomes critical as systems grow more complex. Users can memorize information about individual features, but they need meaning to understand how those features work together to solve their problems.

## The Three Levels of Meaning {#the-three-levels-of-meaning}

Meaning in technical documentation operates at three interconnected levels: task-level, workflow-level, and strategic-level. Understanding these levels helps explain why some documentation feels immediately useful while other documentation requires users to do significant translation work.

### Task-Level Meaning {#task-level-meaning}

At the most granular level, meaning connects individual actions to immediate outcomes. When you document a specific API call, configuration setting, or user interface element, task-level meaning answers the question: "What does this accomplish?"

Poor task-level meaning sounds like this: "Set the retry\_count parameter to control retries." This tells users what the parameter does but not why they'd want to control retries or how to decide what value to use.

Strong task-level meaning sounds like this: "Set retry\_count to 3 to automatically recover from temporary network failures without overwhelming your servers with repeated requests." This connects the technical action to a meaningful outcome users care about.

Task-level meaning requires understanding not just what your product does, but what problems that functionality solves for users. It requires connecting features to outcomes that matter in users' contexts.

### Workflow-Level Meaning {#workflow-level-meaning}

The second level connects individual tasks to larger workflows that users are trying to complete. This is where many documentation sets struggle, because it requires understanding how users actually work, not just how your product works.

Workflow-level meaning answers questions like: "When would I use this?" and "What do I do next?" It acknowledges that users don't invoke features in isolation—they're following sequences of actions to accomplish larger goals.

I learned the importance of workflow-level meaning during my time documenting AWS architecture patterns. Individual services like EC2 and RDS were well-documented at the task level—users could learn how to launch instances or create databases. But users struggling to architect complete applications needed to understand how these services connected to support real-world workflows.

The breakthrough came when we started organizing content around workflow patterns: "Building a scalable web application," "Processing batch data reliably," "Implementing disaster recovery." Each pattern showed how multiple services worked together to solve a complete problem, not just how each service worked individually.

This workflow-level meaning transformed our documentation from a collection of service manuals into guidance for accomplishing business goals.

### Strategic-Level Meaning {#strategic-level-meaning}

The highest level of meaning connects workflows to business outcomes and strategic objectives. This level answers the question: "Why does this matter to my organization?"

Strategic-level meaning is often overlooked in technical documentation because it seems "too high-level" or "too business-focused." But for decision-makers evaluating tools and approaches, this level of meaning is crucial.

When Stripe documents their payment processing capabilities, they don't just explain how to charge credit cards (task-level) or how to build a checkout flow (workflow-level). They connect these capabilities to business outcomes like reducing cart abandonment, expanding to international markets, and maintaining PCI compliance (strategic-level).

This strategic meaning helps users understand not just what they can build with Stripe, but why they should invest time and resources in building it.

## The User Journey Connection {#the-user-journey-connection}

Meaningful content aligns with how users actually discover, evaluate, and use your product. This requires understanding user journeys not just within your documentation, but within their broader context of solving problems and accomplishing goals.

Most documentation fails at meaning because it's organized around product capabilities rather than user journeys. Teams create content that mirrors their internal organization—separate sections for each feature, organized by the team that built them—rather than content that matches how users approach problems.

I experienced this challenge firsthand while working on Angular documentation. The framework had dozens of features: components, services, directives, pipes, routing, HTTP clients, testing utilities, and more. The natural inclination was to document each feature thoroughly in its own section.  
But users weren't trying to learn about Angular features in isolation. They were trying to build applications. Their journey started with problems like "I need to display dynamic data" or "I need to handle user input" or "I need to make API calls."

We discovered that meaningful documentation needed to start with these user problems and then explain how Angular's features solved them. Instead of a section called "HTTP Client" with comprehensive coverage of every method and option, we created content organized around user needs: "Fetching data from APIs," "Handling loading states," "Managing authentication tokens."

This shift from feature-focused to journey-focused organization dramatically improved the meaning our documentation provided to users.

## The Context Problem {#the-context-problem}

One of the biggest threats to meaningful content is what I call the context problem: teams create documentation that makes sense within their context but loses meaning when users encounter it in different contexts.

This happens because teams know too much about their own product. They understand the assumptions, background knowledge, and workflow patterns that make their content meaningful. Users approaching the same content without that context struggle to extract meaning from it.

Consider this common example: "Configure your webhook endpoint to handle payment notifications." To the team that wrote this, the meaning is clear—they understand what webhooks are, why payment notifications matter, and what "handling" them entails. To a user who's never worked with webhooks before, this instruction is meaningless without additional context.

The context problem becomes more severe as organizations scale. Different teams develop different contexts and assumptions. What seems obviously meaningful to the team building a feature may be incomprehensible to users (or even to other teams within the same company).

The solution isn't to provide exhaustive context for every piece of content—that would make documentation overwhelming and inefficient. Instead, it's to understand which contextual knowledge is essential for meaning and which is optional for your specific users.

## Testing for Meaning {#testing-for-meaning}

Unlike the other characteristics of quality, meaning can't be evaluated purely through analytical review. You can audit content for Accuracy, Completeness, or Consistency, but Meaning requires observing how real users interact with real content in real contexts.

The good news is that you don't need massive user research studies to test for meaning. Jakob Nielsen's research showed that testing with just 5 users can identify 85% of usability problems, and similar principles apply to content meaning. The most striking truth is that zero users give zero insights. As soon as you collect data from a single test user, your insights shoot up and you have already learned almost a third of all there is to know about whether your content creates meaning for users.

For testing content meaning specifically, you can get valuable insights by observing 5-8 users attempt to apply what they've learned from your documentation. The key questions are: Can they successfully use the information to accomplish their goals? Do they understand not just what to do, but why they're doing it? Can they adapt the guidance to their specific context, or can they only repeat the exact steps you provided?

### AI as a Meaning Test {#ai-as-a-meaning-test}

There's also a surprisingly effective technique using AI tools to test whether your content has clear meaning. Here's how it works:

1. **Write your documentation** as you normally would  
2. **Write a separate summary** of what you think the main purpose and key takeaways of that documentation should be  
3. **Ask an AI tool to summarize your documentation** without showing it your intended summary  
4. **Compare the two summaries** \- either manually or by asking the AI to compare them

If the AI's summary aligns with your intended purpose and takeaways, there's a good chance your content successfully conveys meaning. If the summaries diverge significantly, it often indicates that your content isn't clearly connecting information to purpose.

This technique works because AI tools are reasonably good at extracting apparent meaning from text, but they're not good at inferring meaning that isn't explicitly present. If an AI can identify the same key purposes and takeaways that you intended, it suggests that those meanings are clearly embedded in your content rather than just existing in your head.

The AI technique isn't a replacement for user testing, but it's a useful preliminary check that can help you identify meaning problems before you invest time in user research. It's particularly helpful for quickly testing multiple drafts or revisions to see which version more clearly conveys your intended meaning.

## When Meaning Conflicts with Other Characteristics {#when-meaning-conflicts-with-other-characteristics}

Sometimes creating meaningful content requires trade-offs with other aspects of quality. Meaning might require more explanation than pure conciseness would suggest. It might require organizing content in ways that feel less complete from a feature-coverage perspective. It might require inconsistency in how deeply different topics are covered.

These trade-offs can be uncomfortable for teams used to optimizing for other characteristics. But meaning should usually win these conflicts, because meaningless content can't achieve its purpose regardless of how well it performs on other dimensions.

I learned this lesson during a project documenting complex data processing workflows. The most accurate and complete approach would have been to document each processing step in isolation, with comprehensive coverage of all options and configurations. But this approach would have made it nearly impossible for users to understand how the steps connected to solve their actual data problems.

Instead, we organized the content around common data processing scenarios: cleaning customer data, aggregating sales metrics, preparing data for machine learning. Each scenario was less comprehensive than a complete feature reference would have been, but far more meaningful to users trying to accomplish specific goals.

The result was documentation that sacrificed some theoretical completeness to gain practical meaning. Users could successfully apply what they learned because they understood not just how to use individual features, but why those features mattered in their context.

## Building Meaning Systematically {#building-meaning-systematically}

Creating meaningful content requires intentional design and ongoing attention. It's not something that emerges naturally from accurate, complete information.

Start with User Goals: Before documenting features, understand what users are trying to accomplish. What problems are they solving? What outcomes do they need to achieve? How does your product fit into their broader workflows?

Connect Features to Outcomes: For every capability you document, explicitly connect it to user benefits. Don't just explain what a feature does—explain why users would want that outcome.  
Provide Context Appropriately: Identify what background knowledge users need to extract meaning from your content. Provide essential context upfront, but don't overwhelm users with information they don't need for their specific goals.

Test with Real Users: Regularly validate that users can extract meaning from your content by observing them attempt to apply what they've learned. Look for gaps between what you think you've communicated and what users actually understand.

Maintain Connection to Purpose: As products evolve and expand, regularly review whether your content still connects clearly to user purposes. Feature additions and changes can gradually erode the meaning of existing content.

## The Foundation of Quality {#the-foundation-of-quality}

Meaning serves as the foundation for all other aspects of content quality. Accurate information that doesn't connect to user goals is meaningless precision. Complete coverage that doesn't help users accomplish anything is meaningless comprehensiveness. Concise writing that doesn't serve user purposes is meaningless efficiency.

But when content has strong meaning—when it clearly connects to what users are trying to accomplish—the other characteristics of quality become powerful amplifiers of that meaning. Accuracy ensures that the meaningful connections you've created are reliable. Completeness ensures that users can follow meaningful paths to completion. Conciseness ensures that meaning isn't buried under unnecessary information. Discoverability ensures that users can find meaningful content when they need it. Consistency ensures that meaning remains reliable across different contexts.

Without meaning, technical writing becomes merely technical information. With meaning, it becomes a tool that empowers users to solve problems and accomplish goals. And that transformation is what quality in technical writing is ultimately about.