# Chapter 4: A personal reckoning  {#chapter-4:-a-personal-reckoning}

I joined Google as a Technical Writer, which was technically a step down (level-wise) from previous roles. After about a year, I decided to try for promotion. I worked with my manager to put together my justification—what we called a 'promotion packet'—a comprehensive document listing my accomplishments, links to content I created, and testimonials from colleagues. Then I waited.

I didn't get the promotion.

That stung, but it's hardly unusual. Most people don't get promoted their first time through. I listened to the feedback, put together an action plan with my manager, and prepared to try again six months later.

I was declined again.

This time, it hurt worse. Not just because I had done what I thought the committee had asked, but because of the reason they gave me: "We have concerns about his writing quality."

As you read this, I hope you have to imagine what I must have felt. There I was, at one of the top companies in the world, and I was being told my writing quality wasn't good enough. If that was the case, why was I still employed? Why hadn't they moved me to exit? Even more baffling, my performance reviews were great\! By one measurement, I wasn't doing well, but by another I was doing great.

I would like to say that I handled this feedback well. But I didn't. I spent a good half year being angry and upset. Don't do that. It neither helps you nor those around you.

When I finally moved into more of a growth mindset, I made a decision. If my writing wasn't of high enough quality, then I was going to fix that. And to fix that, I needed information. Specifically, I needed to know: How did we define content quality?

## The Search for Standards {#the-search-for-standards}

I thought I would find an easy, or at least well-defined answer. After all, I was at Google, a company that prided itself on making data-driven decisions. Surely we had data that indicated when content was of high quality and when it wasn't. We certainly have such mechanisms for code. When you submit code into a repository—for those unfamiliar with the process, I'm basically saying when you save the code so it can be used in a production environment—that code has to go through all sorts of tests. We have all sorts of ways of measuring if the code is functioning correctly, if it's doing the right things in the right ways. Most companies even have coding guidelines that cover the subtle nuances of software engineering that are harder to measure—things like how to declare variables, method names, and so on.

But technical writing doesn't have such mechanisms. There isn't an easy way of determining if a conceptual topic actually explains its concepts effectively, or if a how-to guide actually helps a user perform a given task. Depending on how you create your API documentation, you might not have an easy way of determining if a method does what it says it does.

There are some ways where you can get a few insights into this question of content quality. You can add widgets to your pages so people can give it a thumbs up or a thumbs down, even asking probing questions if a user is unhappy. Such widgets can give you some information, but they suffer from Negative Review Bias, which is a term used to describe how people who are unhappy with something are more motivated to share their unhappiness than those who are satisfied.

You can use page analytics, which include metrics such as bounce rates and pageviews. But those are also difficult to parse. A high bounce rate usually means that users are visiting the page and then leaving quickly. That would seem bad. But what if the topic is a landing page, with the purpose of leading users to the content they actually need? In that case, having a high bounce rate might be good—you don't want your customers spending a lot of time on a page trying to find the right link. A page with low pageviews might be seen as low quality. But maybe it's a page that's about a specific feature—one that, although not used often, is crucial to those who need it? Or, what if your potential user base for your content simply isn't as large as another documentation set? For example, I remember working on the Angular documentation. At the time, I was on a team that focused on internal developers. Angular was an outlier in that it was used internally, but was also open source, so it was used by millions of external developers. Looking at the numbers, my content was viewed by ten times the number of people than some of the content my teammates worked on. That didn't make their content lower quality—it meant that they had a smaller audience.

And you can conduct user research studies. These studies probably give you the most accurate insights into your content quality. You can actually sit with your users and see how they use your content, where it excels and where it falls short. But these studies take time and they take skilled professionals who know how to conduct them scientifically. Most technical writers aren't lucky enough to have access to a user experience team who can help conduct these studies.

I quickly found that we didn't have a clear idea of what content quality actually meant. We knew that some content was of higher quality than others, but we couldn't necessarily articulate why.

## Why This Matters {#why-this-matters-1}

This is a big problem for several reasons. One of them is obvious: if everything around you is able to be measured, but your own work is not, how can you articulate your value to the team and the company? I think this issue alone is why a lot of product teams distrust or discount the value that technical writing brings. Software engineers and product managers all have ways of measuring the impact of their work, but have no idea if the quality of their product's documentation even matters. And if they don't know if it matters, then it's understandable that they might underappreciate its value. That may be one reason why technical writers often experience variations of the following conversation:

Product team: "We need docs\!"

Technical Writer: "Sure\! When?"

Product team: "We shipped yesterday\!"

Another reason why the lack of clarity around content quality causes problems: there aren't enough technical writers to handle all the documentation needs. Every company I've worked at—from Microsoft to Amazon to Google to Stripe—has never had enough technical writers. That's often meant that some product teams have to write their own documentation. But how can they do that when we can't articulate what quality documentation is? Imagine being asked to build a house, but not having access to any building codes or instructions. You'd have no way of knowing if the house you built was safe, let alone stable. We ask product teams to own their documentation all the time. And most have the best intentions when it comes to creating that content. But, if I can paraphrase Jeff Bezos for a moment, intentions don't matter—mechanisms do. Customers don't care if you meant well when you wrote your documentation; they only care if the content tells them what they need to know, when they need to know it.

And speaking of customers, that's the third reason why being unable to define content quality is such a problem. If we can't define it, we risk creating subpar customer experiences. Poor documentation might be overlooked if the product is simple or intuitive enough, but as systems get increasingly complex, you need quality documentation for customers to succeed. No matter who your customer is, they're coming to you because you're helping them solve a problem. If they can't figure out how you solve that problem for them, you're not helping them, you're hindering them.

Technical writers contribute to this evaluation challenge too. We're well-intentioned but often struggle to articulate why we write the way we do or what we need to create good content. When product teams ask how long documentation will take, or why we need certain information, many of us give vague answers about "understanding the user journey" or "ensuring content flows well." We can assess whether we're ready to write, but we can't systematically evaluate whether what we've written is actually good.

## The AI Complication {#the-ai-complication}

You'd think with the proliferation of AI and large language models, this issue of content quality would fix itself. Just have the AI write everything\! But it's not that simple—and in some cases, adding AI makes things worse.

With the introduction of large language models and generative AI, we have the opportunity to measure and improve content quality. In fact, while I was at Stripe (which, admittedly, was at the beginning of a lot of the AI innovations that are going on today) we decided to focus our energies on what we thought AI could do best: determine if the code examples in our documentation were functional—or at least, syntactically correct.

This idea was great in theory, but in practice it proved more difficult. When you document code in a tutorial, for example, you don't always show all of the code at once. Sometimes you build out the example one snippet at a time. But it's hard for AI to know that a snippet is part of a larger example. So we'd get a lot of errors about undeclared variables or undefined functions, when in fact they were defined earlier in the tutorial. The number of false positives in our tests made identifying real issues challenging—save for more obvious errors, such as a missing semicolon. And even if the code example was correct, that didn't mean the documentation around that code was accurate.

There's another reason why AI can be problematic when it comes to documentation and content quality. These models are only as good as the data on which they're trained. How do you know if that data represents good documentation? You can run tests to see if code works, but we have had decades of writing content without a strong definition of content quality nor decent ways of measuring that quality. But we all know about documentation that absolutely fails to meet customer expectations. Simply put, we're asking the models to be experts on a subject and giving those models questionable data on which to make decisions and analysis.

I'll be more blunt: We've spent decades de-prioritizing documentation, and now we want AI to write that documentation for us.

## An Attempt at a Solution {#an-attempt-at-a-solution}

As I continued to try to understand what content quality was while I was at Google, I had the opportunity to reflect on my career. It was then I realized that, while I had worked with amazing editors and writers across companies like Microsoft, Amazon, and Stripe, we had never really established a framework to discuss content quality. Every team had informal ways of recognizing good writing—we could point to examples we liked or disliked—but we couldn't systematically explain why one piece of documentation worked better than another.

I started thinking that such a framework could be transformative. It would bring technical writing closer to other software engineering disciplines in terms of metrics and measurement, giving us the language to articulate our value and process. We could use it to help product teams understand what they should think about when they needed to write their own content, moving beyond vague requests for "good docs" to specific, actionable guidance. Most importantly, we could better ensure that the products we created and the software we shipped was genuinely helpful to our customers.

A part of me thinks: "Who am I to determine what content quality is?" The best answer I can give you is: "I'm no more and no less qualified than anyone else who has spent their career writing technical content. But I know we have to do better than a definition that amounts to 'we know it when we see it.'" My promotion experience had forced me to think systematically about what makes writing work, and I'd seen firsthand how the absence of clear criteria hurt writers, our teams, and our customers. The status quo isn't good enough.

The rest of this book is my attempt to fix that. You might read my words and agree. And you might read them and think I'm full of it. That's not the point. If you read the rest of this book and come away just thinking about what content quality means, and understanding why it's important, I've done what I set out to do.

So let's get to it.