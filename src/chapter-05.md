# Chapter 5: On Accuracy {#chapter-5:-on-accuracy}

When I think about accuracy, I think about TIMESTAMPS.

Let me explain.

One of the first projects I worked on for Google was documenting a SQL dialect. I didn't know a lot about SQL at the time, except for this famous comic from XCKD and running simple queries such as `SELECT * FROM table;`. But anything is learnable, and I set to work.

One of the data formats I needed to document was `TIMESTAMP`. Timestamp represents an absolute point in time, independent of any time zone or convention like daylight saving time. That seems like a pretty simple explanation, but there is a lot of work to make this a reality. There are timezones, conventions like daylight savings time, leap seconds—all sorts of things go into making sure that the timestamp that's stored is correct. Or, to put another way, to make it accurate.

I think the complexity of `TIMESTAMP` in SQL is very similar to the complexity of accuracy in technical documentation. You'd think it's very easy to look at a piece of content and say whether it's accurate or not, but the truth is it's not that simple:

* What's accurate for a newly-released product may not be the same as for a more mature one. 
* What's accurate for a one-person development shop may not be sufficient for an enterprise corporation
* What's accurate for a novice developer may not be accurate for an experienced one (and, interestingly enough, the reverse is also true)

Of course, accuracy is important when you think about documentation. And I'd rather have no documentation than content I know to be inaccurate. But to think about accuracy correctly, we have to use the term as a framework, not as a binary.

## Accuracy principle #1: Respect the product state

If you talk with any technical writer, they'll have a story similar to the one I'm about to tell you. I'm sharing this because I've chosen not to name the company or the product. But, to be fair, you could probably insert *any* company and *any* product, and it would likely be true.

The product I was working on was brand new. Pre-release, as it were. Often, when products are in this state, the team is focused on what they call the MVP, or Minimally Viable Product. (Lately, this has changed to MLP, or Minimally Loveable Product, but the idea is the same.) An MVP is just that: it's enough of the product that folks can see the potential. It's more than a proof of concept, which is often held together with paperclips and bubblegum. But it's not the full product yet either.

When products are in this state, things can be incredibly dynamic. Features come and go. What worked yesterday doesn't work today, and may work completely differently tomorrow. Key user journeys are added and tossed aside. All of this is totally normal. The team is in full-fledged create mode, and creating things is messy.

But often, when I'm on a product that's in this state, I don't get the same luxury. The team doesn't care what state the product is in; they want real, full-fledged documentation. I call this "asking for GA docs for beta code." And this ask creates an impossible situation: as the writer, I am being asked to document with certainty something that is inherently uncertain. It's like trying to describe an elephant when you've never seen one. And it's dark. And you're in another room. And also, no one told you there was an elephant in the first place.

That's why, one principle to consider when you're thinking about accuracy is to respect the product state. Acknowledge the fact that products and services in different lifecycle stages require fundamentally different levels of accuracy:

* Early-stage products (previews, beta releases, and so on)
might only need to be accurate for the specific scenarios and use cases the team wants to enable. The primary users are going to be early adopters, and those users expect rough edges and content gaps. It's unreasonable and unproductive to try to document every possible error condition, edge case, or integration pattern that might one day exist.

* Products that are more mature, such as those that just reached general availability, need a different level of accuracy. Now we're moving beyond early adopters and asking the larger potential user base to adopt the product. Those users will encounter more scenarios, have more demands, and need more information than those early adopters.

* Enterprise-level products require a different type of accuracy. These enterprises often want to know everything they can about the products they use. In addition, they also may have constraints like regulatory compliance that they have to consider.

When you think about accuracy, you need to think about the state of your product, and adjust your acceptance criteria accordingly.

## Accuracy principle #2: Respect the user's knowledge

When you think about the accuracy of your content, you need to consider the knowledge your user has when they're reading it.

I first started thinking about this principle when I was the lead writer for Angular. Because Angular was an open source project, I had the opportunity to directly engage with members of the community, listening to their experiences and making decisions based on what they shared.

It won't surprise you when I tell you that I found the Angular community incredibly diverse. On one end of the spectrum you had people who had been working with Angular from its very early days, who would regale you of their migration from Angular 1.0 (which became known as AngularJS) and Angular 2.0 (which turned into the Angular in use today). And on the other end of the spectrum we had people who were brand new to software development in general, let alone web development or JavaScript frameworks.

This diversity is incredible. But it's also means that creating content that's accurate is more difficult than it might first appear. A good example of this challenge is with Angular's change detection. Change detection, as the name implies, is the process in which Angular updates component values in an application. For most Angular developers, the smart thing to do is to let Angular handle change detection on its own. It's simpler and, most of the time, it does the right thing at the right times. 

But not all the time. And for some situations and applications, it makes more sense for the developer to take control of when Angular makes updates. But doing so comes at a cost: at the time I worked on Angular, this decision applied to your entire application. There wasn't a way to tell Angular: handle change detection as you see fit, except in this case.

So when I was writing about change detection, I had to decide what level of accuracy made the most sense. Should I say: "Let Angular handle it?" That would make the framework more accessible and understandable to new developers. Or do I explain change detection more fully, which would satisfy advanced developers but risk making the framework seem too complicated to adopt?

I ultimately decided to go with the first option: explain what change detection was and how Angular handled it for you. Then we planned to write a different topic that provided a deeper dive into how change detection worked. (I left the team before we could turn that topic into a reality.) The idea is that you don't have to be 100% accurate. Instead, you have to be accurate *enough* so the user can use the information you're providing.

## Accuracy principle #3: Respect the user's journey

In the previous section, I describe that, to create content that is accurate, you have to consider the user's knowledge at the time of reading. Another user aspect that you must consider is their journey.

Users read for different reasons. For technical documentation, the most common reason is to do. Users who are reading to do want to get the task done and get back to work. Accuracy, for these users, means content that 100% reflects reality, that's clear, and doesn't require them to make any more decisions than necessary.

Another reason users read is to discover. Readers in this mindset may not have a specific task they want to accomplish. They have an idea, or they're vetting an approach. These users often want more options, so they can weigh the pros and cons and make an informed decision.

Senior team members often read to influence. These are your principal engineers, your senior architects, who aren't looking for step-by-step instructions but instead are looking at how to make thoughtful decisions about how the systems are built.

Lastly, a fourth reason users read is to direct. This group is often your managers, your leadership teams, who need enough information to guide their organizations in a direction that aligns with their business goals.

As you can imagine, accuracy means something different for each of these groups. That's okay—but it means you need to understand the user journey your content is enabling so you can calibrate your definition of accuracy accordingly.

## Questions list: accuracy

When you understand the state of your product, when you respect your users' knowledge, and when you understand the journey that user is on, you can start thinking about what accuracy means for your content. When I reach this stage, I usually ask myself these questions:

* Are API names used correctly?
* Do code examples function correctly and follow current best practices?
* Is the depth of detail appropriate for the intended audience?
* Are all steps accurate and complete?
* Is the intended result of the task clearly stated and verifiable?
* Are terms defined clearly and at an appropriate level of detail?
* Are concepts explained with sufficient context?
* Is alternate text for graphics comprehensive enough to stand alone?
* Are all claims and statements backed by current data/research?

You may not need all of these questions, or you may add a few of your own, but these questions are starting point for understanding how accurate your content is.