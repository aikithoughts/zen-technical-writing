# Chapter 12: The Quality Trajectory {#chapter-12:-the-quality-trajectory}

When I interviewed at Google, I was asked the following question:

“We have 6 projects that need to get done. You only have time to do 3 of them. What do you do?”

I answered without hesitation: “I do 3 of them and I make sure the people I work with understand this.”

The interviewer—a dev manager—replied: “But we need all 6 things done.”

“Are we hiring more staff—assuming there’s time to do so?” I asked.

“No.”

“Are we willing to move the deadline?”

“Can’t.”

“Well then,” I said. “We’re doing 3 things. Let’s figure out which 3 are the most important.”

“They’re all important.”

“I’m sure they are, but they’re all not equally important.” I continued. “Look, you’re a dev manager, right?”

“Yup\!”

“I’m sure the list of feature requests and bug fixes exceeds what your team can handle in a given period of time. You have to triage too.”

“Good point,” my interviewer said. We were both enjoying the conversation. “But is there any way you can do more than 3?”

This is where the conversation got interesting. To me, at least.

“Sure,” I said, after taking a moment to think. “Let’s say we have 3 months until our deadline. Each project takes 1 month to complete. That includes one week for tech reviews and testing.

“If we agree that we don’t need tech reviews or testing, then we can get 4 projects done instead of 3\. How does that sound?”

My interviewer thought for a moment. “Hm. I’m not sure I want to publish something that we haven’t reviewed.”

“It’s not my preferred way of doing things either,” I replied. “But sometimes it happens, and it’s sometimes the right call to make. But it does come at a cost, so we have to think about what the trade-offs are.”

We had to move on to other topics, but this exchange always stuck with me.

## The Iron Triangle {#the-iron-triangle}

Many of us know about the Iron Triangle for project management. If you’re not familiar with it, the triangle looks like this:

This triangle shows (or makes the case that) the quality of work is constrained by three criteria: scope, schedule, and budget. As you saw in my response to my interviewer (and I’m sure my interviewer knew where I was going with my questions), when asked when I could get something done, I asked about two of these three constraints: schedule (”Can we push out the date?”) and budget (”Can we hire more people?”).

The iron triangle isn’t a perfect analogy of quality—more on that in a moment. But it is a good way of determining how different constraints impact the quality of a given documentation project.

## A missing piece: Trajectory {#a-missing-piece:-trajectory}

One way the iron triangle isn’t perfect is that it assumes that quality is a constant, fixed state. It’s not—it has a trajectory that changes over the lifetime of the documentation. And, if you don’t pay attention to that trajectory—if you only focus on how scope, cost, and time affect a project in the immediate or near-term, you risk enabling a downward trajectory of quality that becomes increasingly difficult to recover from.

On the flip side, it is equally important to remember that you can always increase your quality trajectory. This idea is encompassed in the saying: “Don’t let perfect be the enemy of good.” It’s understandable that, for all releases, nothing will be perfect. It’s also understandable that some parts of the product will be closer to perfection than others. When it comes to documentation, I find that I need to remind myself that this is okay\! Unevenness in content quality is very normal. But this fact also reminds me that I should remain committed to equalizing the state of all the documentation—from APIs to tutorials. For example, sometimes you need to prioritize improving the documentation for an existing feature over documenting a brand new feature. Sometimes you need to be laser-focused on the API and set that cool tutorial you’re working on aside. And sometimes, you need to take a step back to make sure the whole documentation experience is working as it should.

By keeping this focus, I can help make sure that the quality trajectory of our content is always trending up.

## The documentation decay cycle {#the-documentation-decay-cycle}

Here's a pattern I've seen play out repeatedly across multiple companies: A team launches a new product or feature with great documentation. They've invested time and energy into creating comprehensive, well-organized content. Users are happy. The documentation is genuinely helpful.

Then the team moves on to the next priority. The product continues to evolve—new features get added, APIs change, workflows get optimized. But the documentation updates become sporadic. Small inaccuracies creep in. Gaps in content start to appear but don’t get addressed. The information architecture that made sense at launch becomes strained as content gets tacked on without strategic planning.

For a while, nobody notices. The core documentation still mostly works. Users can usually figure things out. Support tickets increase gradually, not dramatically.

Then the complaints reach a critical mass. Users are frustrated. Support is overwhelmed. Leadership demands action.

I experienced this firsthand early in my time at Google. Something triggered a complete documentation overhaul across Google Cloud Platform. "Code purple" refers to when hospitals stop accepting new patients to focus on critical cases—and that's exactly what we did. For months, the entire documentation team ceased any new work and focused exclusively on improving existing documentation. New templates were defined, new styles and patterns were implemented. It was a long, grueling effort, and we were all exhausted by the end of it.

I saw a similar pattern with Angular documentation. When I joined that project, we found entire sections that had been around for years but were no longer relevant or even accurate. The number of times I would ask a question about a given Angular topic, only to get the response: “How long has THAT been there? That’s not even true anymore\!” became hard to track. To address this, I implemented a rule: if you needed to update a topic, you had to review the entire topic, not just what you changed. There were simply too many instances of old or outdated content to trust that any topic was current. 

The good news: for Google Cloud Platform, some of those best practices that were defined during that code purple experience continue to benefit customers to this day. And the Angular team recently revamped their entire documentation set. But each is still an unfortunate example of what happens when an engineering organization decides to de-emphasize documentation quality for too long. And these efforts are no guarantee that the problem won’t repeat itself in the future, as the demands for more documentation for more features continues to grow.

This boom-and-bust approach to documentation quality is expensive, exhausting, and ultimately inefficient. It’s like only taking your car in for maintenance when the engine breaks down. Sure, you can do it, but regular maintenance would have everyone’s lives a lot easier. (Well, maybe the mechanic is okay with how things are, but that’s taking the analogy too far.)

## Maintaining Upward Trajectory {#maintaining-upward-trajectory}

Think about how a plane stays in the air. The engines don't fire once during takeoff and then shut off. They run continuously throughout the entire flight, providing constant thrust to keep the plane aloft. The moment the engines stop, the plane begins to descend.

Documentation works the same way. You can't achieve quality once and then stop paying attention. Quality requires continuous energy and focus. Every product update, every new feature, every API change affects your documentation's trajectory. If you're not actively maintaining and improving your content, it's decaying—even if you can't see it happening yet.

Maintaining an upward quality trajectory means always thinking about documentation. Is it accurate as the product evolves? Is it complete for the workflows users actually need? Is it still relevant, or has it been superseded by new approaches? Does it maintain consistency with newer content? Does it still connect to what users care about accomplishing?

This is where the six characteristics framework becomes essential for sustainable quality. Each characteristic degrades over time if not maintained:

* **Accuracy drifts** as products evolve. APIs change, features get deprecated, recommended practices shift. Documentation that was perfectly accurate at launch can become misleading or wrong months later.  
* **Completeness develops gaps** as new features get added. Each product release potentially creates new user workflows that need documentation. The content set that felt complete last quarter may have significant holes today.  
* **Conciseness suffers** as content accumulates. Teams add new information without removing obsolete content, leading to bloated topics that bury important information under outdated material.  
* **Discoverability breaks down** as the information architecture strains under content growth. The navigation structure that worked for 50 topics becomes unwieldy with 500 topics.  
* **Consistency fragments** as different people contribute content over time, especially if standards aren't actively maintained and reinforced.  
* **Meaning erodes** as the gap between what documentation describes and what users actually need grows wider. Content written for last year's user journeys may not serve this year's use cases.

The solution isn't occasional heroic efforts—it's continuous, sustainable attention to documentation quality. This requires:

* **Partnership with engineering:** Documentation cannot be an afterthought that happens after code is complete. Writers need to be involved in planning conversations, understand what's changing and why, and have time allocated for documentation updates in every release cycle.  
* **Regular content audits:** Systematically review existing content to identify accuracy problems, completeness gaps, and relevance issues before they compound into crisis-level problems. The rubric from Chapter 13 can help teams assess whether content is ready for production—and whether existing content is still production-ready.  
* **Deprecation policies:** Just as engineering teams deprecate old code, documentation teams need clear policies for retiring outdated content. Keeping obsolete information around creates confusion and erodes trust.  
* **Quality gates:** New content should meet the same quality standards as initial documentation. It's tempting to accept lower quality for "just one more feature" when deadlines loom, but each compromise accelerates the decay cycle.  
* **Investment in foundations:** Sometimes you need to prioritize improving the documentation for existing features over documenting brand new features. Sometimes you need to refactor your information architecture rather than adding more content to a strained structure. These foundational investments maintain trajectory even though they don't produce visible new content.

The goal is to make documentation quality a continuous practice rather than a periodic project. Small, consistent investments in maintenance prevent the decay that leads to crisis-level overhauls.

## Summing up {#summing-up}

"That interview conversation always reminds me that quality is a trajectory, not a fixed state. It reminds me that I need to balance my drive to improve the documentation experience (something that I will always consider to be of high priority) with my understanding that this experience may not always align with my team's objectives. Simultaneously, it is part of my role to ensure that the quality trajectory of our content is always trending up—through continuous attention to the six characteristics, through partnership with engineering, through regular maintenance rather than periodic heroics—making our users' lives better and their efforts more successful.