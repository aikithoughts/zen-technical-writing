# Chapter 6 (Completeness): interview notes

Raw material from a talk-it-through session on 2026-11-25. Dave's words are kept as he said them (lightly cleaned up). Claude's observations are marked separately.

## Seeds kept from the old draft (Dave's lines)

- "Teams love to create quickstarts… Teams also love to write deep technical tutorials… But if I'm being honest, they also love writing them because they get to show off… What about the content in between?"
- "If you haven't documented how to do something users want to do, the users will tell you!"

## Story: the Amazon curriculum developer interview

When I was interviewing to become a curriculum developer at Amazon (a brief foray into a world outside of technical writing), one of my interviewers asked me: "Are you an expert in cloud technologies?"

"No," I answered. "And I think being an expert is a bad idea."

"What are you talking about?" he said. "Our users expect us to be experts."

"I disagree," I said. "Our users expect us to be able to explain to them how they can get their work done. The more we become experts, the further we are from their own journey, and the harder it is for us to empathize with their situation. We don't want to be experts. We want to be far enough along the path that we can show them the way."

I realize this story is more about expertise than completeness, but the two ideas are very closely linked. You cannot document something completely without becoming an expert. And the moment you become the expert, you risk alienating those who are just beginning their journey.

## Story: GoogleSQL

When I worked on GoogleSQL, there were a lot of nuances. Every function had subtle nuances that could impact its behavior. But, 99.99% of the time, those nuances never came about. So when you document to that level of completeness, you end up wasting time, writing about things that will rarely be relevant. That doesn't mean you shouldn't write about them. It means that you need to prioritize completeness correctly.

## Completeness and consistency

Completeness is also very closely tied with another characteristic: consistency. And that's for a very simple reason. It's rare for content to be consistently complete. Too often, the easily-explained is documented fully, and the harder to explain is documented more shallowly. That happened with Angular. The easy things to explain were documented in full. Many of the harder things to explain, like change detection or content projection, were documented lightly or not at all.

(Confirmed by Dave: the well-documented basics were components, templates, data binding, event binding, and directives.)

## Weighting

When it comes to quality, completeness is something you have to weight carefully, because it's rarely going to be a full 100%.

## Story: Microsoft OGF (Outstanding, Good, Fair)

At Microsoft, working on Windows meant working on something vast. Fully documenting the API would be a nearly-impossible task. Instead, they developed a system: OGF, which stood for Outstanding, Good, and Fair. This system helped us categorize the API reference:

- **Fair.** The API is documented at a bare minimum. Classes, methods, and properties are described simply, along with signatures, expected parameters, and so on.
- **Good.** Everything in Fair, but with descriptions. What the intended purpose was for each method, etc.
- **Outstanding.** Everything in Good, but it includes examples.

Here's the thing: you don't WANT everything documented at the Outstanding level. It's a waste of time. If I have a function, `returnTimeSinceEpochInMillisecondsAsDouble`, I don't need a full description and example of what this function does. It's all right there. With this method, we could review the API and then decide which classes, properties, and methods needed to be at which level, and we could determine overall what percentage of our API reference should be in each category.

## How you decide the level

Ah. That's where things get interesting. You had to really think about the purpose of the content.

It's a lot like testing code. What tests are important, what tests are trivial? It depends on what the user journeys are that you want to support. Those user journeys determine what parts of the API, or application, or whatever, need more attention, and which ones require less attention. Then you balance that with, as I pointed out, which items are self-describing. In other words, deciding on the level of documentation is where you provide your judgment and expertise.

## Completeness is decided again with every release

Another thing that was important. The goal might be to eventually get closer to (but you'll never quite reach) 100. So it's not that you decide a level of completeness once. You decide it with every update and every release.

## Story: Stripe and AWS (where it goes wrong)

There are so many examples here. But let's look at Stripe. Stripe has amazing documentation. But they also have an incredibly broad portfolio. So you onboard at Stripe. You go through the quickstart, you figure out how to accept a payment. You're up and running!

Then what?

Well, that depends, doesn't it? What kind of business are you? Do you sell goods or services? Are you in the United States or in Europe? What types of things do you sell? What kinds of things do you do? The list is endless, and Stripe can't make those decisions for you. You're on your own. But you don't know what you don't know yet.

Another example: Migrating from an on-premises network to AWS. If you just lift and shift your network topology to AWS, you'll be paying a lot more money than you would have otherwise (or, at least, that was true in the 2010s). But migrating to AWS meant you have to actually *know* your network and your business. What kind of database system do you need? SQL? NoSQL? Something else? What kind of capacity do you need, and when? AWS can help you get up and running, but it can't tell you which services to use and how to use them effectively.

That's the content gap. At its worse, it's a case of "this is too hard to explain, so we don't bother."

## Claude's observations (not Dave's words)

- Possible opening line / thesis: "We want to be far enough along the path that we can show them the way."
- The expertise-vs-empathy idea is the established "curse of knowledge."
- The "easy things documented fully, hard things thinly" pattern may be the cause of the content void, at the level of a whole doc set. Check with Dave.
- OGF is a tiered, deliberate version of "prioritize completeness correctly," and it sets a target mix across the whole reference. It's essentially a weighted rubric applied inside one characteristic, which is a natural bridge to Chapter 12.
- Chapter 11 also opens with a job-interview story (Google). Consider where each interview story goes.
- The testing analogy will land with engineers: 100% test coverage isn't the goal either; coverage follows the journeys you need to protect.
- "Deciding on the level of documentation is where you provide your judgment and expertise" echoes Dave's Chapter 12 point (the writer must understand the docs the way an engineer understands the codebase). Judgment may be a through-line of the whole book.
- "You decide it with every update and every release" connects to Chapter 11's quality trajectory.
- Decided: use "content gap" (not "content void") throughout the book.
