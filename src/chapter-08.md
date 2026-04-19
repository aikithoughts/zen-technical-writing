# Chapter 8: On Conciseness {#chapter-8:-on-conciseness}

When most people think about conciseness in technical writing, they imagine it as a simple editing exercise: cut unnecessary words, shorten sentences, eliminate redundancy. This approach treats conciseness as purely about brevity—fewer words equals better writing.

But conciseness isn't just about using fewer words. It's about conveying your meaning with the fewest words possible while still achieving your communication goals. And those goals extend far beyond just transmitting information—they include building trust, maintaining engagement, and respecting your reader's time and cognitive load.

The challenge is that most writers, when they try to be concise, fall into one of two traps. They either strip away so much that their writing becomes cold and mechanical, or they swing in the opposite direction and add so much personality and explanation that they bury their message in unnecessary words. Both approaches fail because they misunderstand what conciseness is really about.

While our previous discussions of accuracy and completeness operated at the content and topic level, conciseness drops us down to the section, paragraph, and sentence level. This is where the rubber meets the road in terms of user experience—where individual sentences either help or hinder comprehension, where word choices either build or erode trust, and where tone either supports or undermines your message.

## The False Economy of Extreme Brevity {#the-false-economy-of-extreme-brevity}

Consider this example of a letter thanking an aunt for a gift:

"Dear Aunt Jane,

Thank you for the sweater. It's a lovely shade of blue. I love how warm it is, and it fits perfectly. I know I'll wear it for years to come.

Love,

Dave"

Following conciseness to its extreme, you might revise this to:

"Aunt Jane:

Thank you for the sweater. It is:

* Warm

* Blue

* Well-fitting

I will wear it for at least two years.

Dave"

The second version is undeniably more concise. It uses fewer words, eliminates subjective language, and presents information more efficiently. But it's also a terrible letter. Aunt Jane isn't going to send you anything else any time soon.

This example illustrates the fundamental problem with treating conciseness as pure word reduction. The goal isn't to minimize word count—it's to maximize communication effectiveness. Sometimes that requires more words, not fewer. Sometimes personality and warmth are essential to your message, not obstacles to it.

The same principle applies to technical writing. Users aren't just trying to extract information from your documentation—they're trying to accomplish goals, solve problems, and build confidence in your product. Pure brevity can undermine these objectives just as much as excessive verbosity.

## The Three Extremes of Technical Writing Style {#the-three-extremes-of-technical-writing-style}

When it comes to conciseness in technical writing, I find it helpful to think about three distinct styles that represent different approaches to balancing brevity with communication effectiveness.

### Academic Writing {#academic-writing}

Anyone who went to high school or college knows what academic writing sounds like. It's formal, precise, and often unnecessarily complex. Interestingly enough, many of the conventions we associate with academic writing exist because, historically, academics wanted to make people work to understand what they were saying. Complexity was a feature, not a bug—it demonstrated sophistication and seriousness.

Academic writing in technical documentation sounds like this:

"In order to facilitate the implementation of the authentication mechanism, it is necessary to configure the appropriate parameters within the configuration file, ensuring that the requisite security protocols are properly instantiated before attempting to establish a connection to the remote server."

This sentence contains accurate information, but it buries simple concepts under layers of unnecessary formality. "Configure authentication settings in the config file before connecting to the server" would convey the same information more effectively.

Teams often drift toward academic writing because it feels professional and authoritative. Writers who learned formal writing in educational contexts may default to this style without realizing how it affects their readers. The problem isn't that academic writing is wrong—it's that it optimizes for perceived authority rather than user success.

### Casual Writing {#casual-writing}

On the opposite extreme, we have casual writing. This is what many novice writers default to when they want to avoid sounding academic. They've heard that technical writing should be conversational and accessible, so they swing hard in the direction of informality.

Casual writing is equally verbose but in a different way. It fails to respect the user's time by adding unnecessary personality, explanations, and conversational elements that don't serve the user's immediate goals.

Casual writing sounds like this:

"Alright, so now we're going to check out this really cool authentication function that we just wrote. It's pretty neat how it handles all the security stuff automatically\! Let's dive in and see how it does all this magic behind the scenes. Don't worry if it seems complicated at first—we'll walk through it step by step, and I promise it'll make sense by the end\!"

This style might feel friendly and approachable, but it's actually disrespectful to users who are trying to accomplish specific tasks. They don't need encouragement or entertainment—they need clear, actionable information. The chattiness becomes cognitive overhead that interferes with comprehension.

The casual approach often emerges from good intentions. Writers want to sound approachable and human rather than robotic. They've seen examples of technical writing that feels warm and engaging, and they want to replicate that connection with their readers. The desire to avoid sounding like a machine or a textbook is understandable—nobody wants their writing to feel cold or intimidating.

Some writers are genuinely skilled at using humor and personality to enhance their communication, creating content that's both informative and engaging. But developing that skill requires significant practice and careful attention to audience needs. These skilled writers understand when personality serves the message and when it becomes a distraction. They know how to add warmth without adding confusion, and they can gauge whether their voice is helping or hindering their readers' success.

Many writers attempt a casual tone without considering how their personality affects comprehension, especially for readers for whom English is a second language. Cultural references, idioms, humor, and conversational asides that feel natural to native speakers can create cognitive overhead and confusion for ESL readers who are already working harder to process technical information in their non-native language. This consideration becomes even more critical when content needs to be localized or translated—casual writing that relies heavily on cultural context or wordplay often doesn't translate well, creating additional barriers for global audiences who depend on clear, direct communication to accomplish their technical goals.

### Informal Writing: The Sweet Spot {#informal-writing:-the-sweet-spot}

Neither academic nor casual writing serves users effectively. What we want is what I call informal writing. Informal writing strips away unnecessary academic formality while still respecting the user's time and cognitive resources. It's neither pretentious nor chatty—it's direct, clear, and appropriately human.

Here's my test for informal writing: Pretend you're working with a colleague on a document. Your colleague is about to board a plane and won't have internet access during the flight. They have just a few minutes before boarding, and they need crucial information from you. How would you convey your message?

You wouldn't be formally academic—you know this person, and formality would waste precious time. You also wouldn't be excessively casual or chatty—they need to catch a flight, and joking around would be inappropriate and ineffective. Instead, you'd be clear, direct, and appropriately personal. You'd focus on what they need to know, expressed in the most efficient way possible. And you'd be supportive, because you want your colleague to be successful.

That's informal writing: respectful of the relationship, mindful of constraints, focused on effectiveness.

Applied to our authentication example, informal writing would sound like this:

"Configure your authentication settings in the config file before connecting to the server. Set the security\_protocol parameter to 'TLS' and add your API key to the credentials section."

This version is concise without being terse, clear without being condescending, and direct without being robotic. It respects the user's time while providing the information they need to succeed.

## Why Teams Fall Into These Traps {#why-teams-fall-into-these-traps}

The academic and casual extremes aren't random choices—they emerge from understandable and well-intentioned thinking.

The **Academic Trap** often catches writers whose last significant writing experience was in college. Academic writing was rewarded in educational contexts, so it feels like "good writing" even when it's counterproductive for user documentation. Writers may also believe that formal language makes them sound more professional or authoritative, especially when documenting complex technical systems.

The **Casual Trap** catches writers who want to "sound cool" or make their content more engaging. They've seen examples of successful casual writing—often from skilled writers who have developed that ability over time—and they try to replicate the style without understanding why it worked in those specific contexts. They may also be reacting against overly formal documentation they've encountered, swinging too far in the opposite direction.

It's important to note that these aren't vocational patterns. I've seen casual technical writers and overly formal developer advocates. The tendency toward one extreme or another seems to depend more on individual background and intentions than on job role.

## Recognizing Your Writing Style {#recognizing-your-writing-style}

Most writers have difficulty objectively evaluating their own tone and conciseness. We're too close to our own writing to hear how it sounds to others. Here are some practical techniques for developing awareness of your writing style:

**Read Aloud with Minimal Inflection:** Read your content out loud, but try to use as little vocal inflection as possible. Speak in a flat, monotone voice. This technique forces you to hear the actual words and sentence structure without the emotional coloring that your internal voice adds when reading silently. Academic writing will sound pretentious and unnecessarily complex. Casual writing will sound juvenile or condescending.

**Try Hostile Inflection:** As a follow-up test, try reading your content with deliberately sarcastic or hostile inflection. Quality writing should be resilient enough to survive this kind of stress test—the core message and logic should remain clear even when someone's trying to make it sound bad. If sarcastic delivery completely undermines your writing or reveals potential misinterpretations, it might indicate that your writing relies too heavily on assumed reader goodwill. This technique is particularly useful for identifying problematic word choices like "simply" or "just" that can sound condescending when read sarcastically. You don't necessarily need to change your writing based on this test, but it can help you anticipate how your content might be received and prepare you for potential reader reactions.

**Use Text-to-Speech Tools:** Screen readers and text-to-speech software provide an even more objective perspective on your writing. Hearing your content in a synthetic voice reveals patterns you might miss when reading with your own internal voice. The artificial delivery makes obvious any unnecessary complexity or chattiness that interferes with comprehension.

**Apply the Coding Analogy:** When working with developers, I often explain conciseness using programming principles they already understand. Code that is too terse becomes difficult to understand and maintain later. Code that is too verbose—using twenty lines when ten would suffice—becomes cluttered and hard to navigate. The best code is tightly written but verbose enough that it remains comprehensible and maintainable.

The same principles apply to technical writing. After all, content is essentially code that gets compiled by the human brain. Your readers need to parse your sentences, understand your logic, and execute your instructions. Unnecessary complexity creates cognitive overhead. Excessive casualness creates processing delays. Optimal writing minimizes both while maximizing comprehension and task completion.

## The Developer Perspective {#the-developer-perspective}

The coding analogy resonates particularly well with technical audiences because it reframes writing quality in terms they already understand and value.

Maintainable Code vs. Maintainable Content: Just as code needs to be maintainable by future developers (including your future self), content needs to be understandable by future readers (including users with different backgrounds and expertise levels). Academic writing creates maintenance problems because it's unnecessarily complex. Casual writing creates maintenance problems because it includes too much irrelevant information.

Performance Optimization: Developers understand that code performance matters—inefficient code wastes computational resources and creates poor user experiences. Similarly, inefficient writing wastes cognitive resources and creates poor reading experiences. Every unnecessary word, every confusing sentence structure, every irrelevant tangent is like inefficient code that slows down the user's mental processing.

Clean Code Principles: The programming concept of "clean code"—code that is easy to read, understand, and modify—applies directly to technical writing. Clean writing follows consistent patterns, uses clear variable names (in writing, this means precise word choices), eliminates redundancy, and focuses on functionality over cleverness.

However, there's an important caveat when applying coding principles to writing. Developers often follow DRY (Don't Repeat Yourself) principles when coding, but this can be problematic when applied too strictly to documentation. It often leads to attempts to "single source" content so that the same message is included in multiple topics through shared snippets or references. This creates a maintenance nightmare—when you need to change a note or explanation, how do you know how many topics are impacted? Does the updated message apply equally to all those different contexts? Unlike code, where a function serves the same purpose everywhere it's called, content often needs slight variations based on context, user type, or specific workflow. Sometimes a little redundancy in documentation is actually beneficial for user comprehension and content maintainability.

## Conciseness Beyond the Sentence Level {#conciseness-beyond-the-sentence-level}

While conciseness primarily operates at the sentence and paragraph level, the principles can influence broader content architecture decisions. When you consistently write concisely, you might discover that you need fewer topics than originally planned, or that information can be organized more efficiently.

However, these broader implications are secondary to the primary goal of sentence-level clarity. The completeness framework we discussed earlier provides better guidance for topic-level decisions. Conciseness is most valuable when applied to how you express ideas within those topics, not whether those topics should exist at all.

## Practical Application {#practical-application}

Achieving effective conciseness requires ongoing practice and attention. Here are some approaches that work consistently:

**Start with Clarity, Then Trim:** Don't try to be concise in your first draft. Focus on getting your ideas down clearly and completely, then revise for conciseness. It's easier to cut unnecessary words from clear writing than to add clarity to overly brief writing.

**Consider Your Voice and Tone:** Spend time thinking about your tone and voice. How do you want to communicate? Are you a knowledgeable advisor, a respected expert, a visionary leader? Your words construct your personality in the mind of the reader. Think about that personality and make sure your words support it. This isn't about adding unnecessary flourishes—it's about ensuring that every word choice aligns with the relationship you want to build with your readers and the role you want to play in their success.

**Test with Real Users:** The ultimate test of concise writing is whether it helps real users complete real tasks more effectively. You don't need a full user research study—talking with just a few users can yield great insights about whether your attempts at conciseness are helping or creating new barriers to comprehension.

**Consider Your Audience's Context:** Conciseness isn't just about word count—it's about respecting your reader's cognitive resources and time constraints. A user troubleshooting a production issue needs different conciseness than someone learning a new concept. Adjust your approach based on the urgency and complexity of your reader's situation.

The goal isn't to achieve some arbitrary standard of brevity. It's to find the optimal balance between efficiency and effectiveness for your specific users in their specific contexts. Sometimes that means more words, sometimes fewer, but always with intentionality about how those words serve your reader's success.