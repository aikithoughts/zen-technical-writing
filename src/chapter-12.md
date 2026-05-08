# Chapter 12: The Weighted Rubric {#chapter-12:-the-weighted-rubric}

One of my pet peeves around technical writing relates to the challenges around when you should engage with a technical writer, or even think about technical documentation. Often, when I bring this matter up, folks rightfully assume its because I’m annoyed that, once again, documentation has been left to the very last minute. I admit that’s annoying—but it’s a situation that can happen to a lot of engineering-adjacent disciplines. But what makes this a pet peeve for me is that we—technical writers—haven’t done a great job of explaining to teams when they should think about their project’s documentation.

At a prior company, this situation was causing no end of stress for everyone—writers, engineers, product managers, and so on. To try and help, I built a rubric that teams could use to figure out if they were ready for production-ready content. I thought I’d share a revised version of that rubric here, along with some guidance about how to use it.

## Dave’s documentation rubric {#dave’s-documentation-rubric}

The rubric is pretty basic. There are four categories. In each category, you score your project—be it a release, a feature, or whatever—on a scale of 1 to 4\.

| Rubric | 1 | 2 | 3 | 4 |
| :---- | :---- | :---- | :---- | :---- |
| Use cases | Use cases are unknown or unclear. Timeline to clarify use cases is to be determined. | Some use cases are known, but ambiguity remains. It may be weeks or months before use cases are fully established. | Most uses cases are known and little ambiguity remains. Timeline to get additional clarity is measured in days and weeks. | Use cases are clear and unambiguous. |
| Deadlines | Deadline is unknown, as is when the deadline will be established. | Deadline is known but highly tentative. | Deadline is established but there may still be factors that change the date. | Deadline is firmly established and there are few, if any, risks that the date will change. |
| Code stability | Code is under heavy development and is highly unstable. | Code is under significant development. A few features might be stable, but there’s still a lot more work to be done. | Code is mostly stable. Some additional work is still in flight, but you can at least run and test the code from a user’s perspective. | Code is stable and testable. Only remaining work relates to bug fixes, performance enhancements, and other changes that don’t affect overall functionality. |
| Subject Matter Expert Availability | No subject matter expert available (usually because they’re busy writing the code). | Subject matter expert may be available, but most of their time is still spent on building the feature or figuring out user needs. | Subject matter expert is available to answer questions and provide clear guidance on intended use of the feature or product. | Subject matter expert is available to answer questions, provide guidance, collaborate on code samples, and provide technical reviews of content. |

## Interpreting the rubric {#interpreting-the-rubric}

To me, this rubric helps teams quickly figure out if they’re ready for production content. When I used a previous version of this rubric, I provided this guidance for scoring:

| Score | Meaning |
| :---- | :---- |
| 16 | The product is built and ready to ship. Chances are, you’re shipping within days. Depending on the size of the project, you might have waited too long to think about documentation. |
| 12-15 | Most of the product is ready for documentation. The combination of use case clarity, code stability, and subject matter expertise are at a point where creating production content is efficient. |
| 8-11 | There’s probably still too much ambiguity to think heavily about production content. However, there are other options. See Content Prep. |
| \<8 | Great to think about what the user journeys should be, but too soon to think about production content yet. Again, see Content Prep. |

## Content prep {#content-prep}

One of the benefits of this rubric is that you should be able to quickly determine if a given project is ready for production content or not. But what if your project isn’t ready? What if your project scores an 8, for example?

In those cases, it’s been my experience that the biggest issues revolve around code stability and subject matter expert availability. The codebase is still in flux—engineers are still figuring stuff out. And those engineers usually end up being the subject matter experts. It’s tremendously difficult—maybe impossible\!—to explain something while you’re creating it.

However, there’s still an opportunity to think about other content work:

* It might be a good time to think about the information architecture. Where will the content live in our documentation set?  
* It may be a good time to clarify who the intended audiences are for the product. The content author can then spend some time learning more about the needs of that audience and plan on how to create content in the most accessible way possible.  
* There may be concepts that we’ll need to explain to users to help ensure their success, and it may be possible to write those conceptual topics ahead of time.

In many cases, there’s almost always content work that can help get the team ready for production content, or help get production content ready faster.

## Just the beginning {#just-the-beginning}

The rubric I’ve shared here is based on my own experience. It’s proven helpful to teams, providing them a bit more clarity about when to start thinking about documentation and engage with a technical writer. That said, it’s just my own interpretation of how I look at projects, and I’m sure there are many other viewpoints that are just as valid. But I think having some way of measuring and tracking where your project is at can help ensure that we efficiently create documentation that helps users succeed with our products.