# Chapter 6: On Completeness

> **About this draft:** Everything here is Dave's own words from our 2026-11-25 conversation, rearranged into chapter order. Anything in [square brackets] was added by Claude as connective tissue or a note: rewrite it, keep it, or cut it. Nothing here has been published.

When it comes to quality in technical writing, completeness matters. But knowing what completeness means matters even more.

When I was interviewing to become a curriculum developer at Amazon (a brief foray into a world outside of technical writing), one of my interviewers asked me: "Are you an expert in cloud technologies?"

"No," I answered. "And I think being an expert is a bad idea."

"What are you talking about?" he said. "Our users expect us to be experts."

"I disagree," I said. "Our users expect us to be able to explain to them how they can get their work done. The more we become experts, the further we are from their own journey, and the harder it is for us to empathize with their situation. We don't want to be experts. We want to be far enough along the path that we can show them the way."

I think about this story when I think about completeness. Granted, the story is *really* about expertise, but they're closely linked. You cannot document something completely without becoming an expert. And the moment you become the expert, you risk alienating those who are just beginning their journey.

[Claude: You may want one sentence here restating the Chapter 4 question for completeness: "Are you providing the information that users need to succeed in their specific workflows?"]

## Complete doesn't mean exhaustive

When I worked on GoogleSQL, I remember thinking how complicated all of it was. Remember TIMESTAMP back in Chapter 5? That was just the tip of the iceberg! Every function had subtle nuances that could impact its behavior. But, 99.99% of the time, those nuances never came about. If I had tried to document everything to that level of completeness, I'd have ended up wasting a lot of time, writing about things that would rarely become relevant. That's true in a lot of cases: to document something fully almost means writing to distraction.

## Outstanding, Good, and Fair

At Microsoft, working on Windows meant working on something vast. Fully documenting the API would be a nearly-impossible task. Instead, they developed a system: OGF, which stood for Outstanding, Good, and Fair. This system helped us categorize the API reference:

- **Fair.** The API is documented at a bare minimum. Classes, methods, and properties are described simply, along with signatures, expected parameters, and so on.
- **Good.** Everything in Fair, but with descriptions. What the intended purpose was for each method, etc.
- **Outstanding.** Everything in Good, but it includes examples.

Here's the thing: you don't WANT everything documented at the Outstanding level. It's a waste of time. If I have a function, `returnTimeSinceEpochInMillisecondsAsDouble`, I don't need a full description and example of what this function does. It's all right there. With this method, we could review the API and then decide which classes, properties, and methods needed to be at which level, and we could determine overall what percentage of our API reference should be in each category.

## Prioritizing completeness

None of this means you shouldn't write about the nuances. It means that you need to prioritize completeness correctly.

That's where things get interesting. You have to really think about the purpose of the content.

It's a lot like testing code. What tests are important, what tests are trivial? It depends on what the user journeys are that you want to support. Those user journeys determine what parts of the API, or application, or whatever, need more attention, and which ones require less attention. Then you balance that with which items are self-describing. In other words, deciding on the level of documentation is where you provide your judgment and expertise.

## Where completeness goes wrong

Completeness is very closely tied with another characteristic: consistency. And that's for a very simple reason. It's rare for content to be consistently complete. Too often, the easily-explained is documented fully, and the harder to explain is documented more shallowly. That happened with Angular. The easy things to explain, like components, templates, data binding, event binding, and directives, were documented in full. Many of the harder things to explain, like change detection or content projection, were documented lightly or not at all.

[Claude: Bridge into the old draft's lines, which were yours.]

Teams love to create quickstarts. Teams also love to write deep technical tutorials. But if I'm being honest, they also love writing them because they get to show off. What about the content in between?

Let's look at Stripe. Stripe has amazing documentation. But they also have an incredibly broad portfolio. So you onboard at Stripe. You go through the quickstart, you figure out how to accept a payment. You're up and running!

Then what?

Well, that depends, doesn't it? What kind of business are you? Do you sell goods or services? Are you in the United States or in Europe? What types of things do you sell? What kinds of things do you do? The list is endless, and Stripe can't make those decisions for you. You're on your own. But you don't know what you don't know yet.

Another example: migrating from an on-premises network to AWS. If you just lift and shift your network topology to AWS, you'll be paying a lot more money than you would have otherwise (or, at least, that was true in the 2010s). But migrating to AWS meant you have to actually *know* your network and your business. What kind of database system do you need? SQL? NoSQL? Something else? What kind of capacity do you need, and when? AWS can help you get up and running, but it can't tell you which services to use and how to use them effectively.

That's the content gap. At its worst, it's a case of "this is too hard to explain, so we don't bother."

But here's the silver lining: if you haven't documented how to do something users want to do, the users will tell you!

## Completeness is never finished

When it comes to quality, completeness is something you have to weight carefully, because it's rarely going to be a full 100%.

The goal might be to eventually get closer to (but you'll never quite reach) 100. So it's not that you decide a level of completeness once. You decide it with every update and every release.

[Claude: Possible bridge to Chapter 11's quality trajectory and Chapter 12's weighted rubric. OGF is a weighted rubric inside one characteristic.]

## Questions list: completeness

[Claude: TODO. Chapter 5 ends with a questions list. Yours to write. Candidates drawn from your words, to keep, cut, or rewrite:
- What user journeys does this content need to support?
- Which items describe themselves, and which need more?
- Is the hard material as complete as the easy material?
- What happens after the reader finishes the quickstart?
- Have you revisited your completeness decisions since the last release?]
