---
title: "In defense of “nothing interesting”"
author: "Brian Weinstein"
date: "2020-02-19"
# weight: 1
aliases: ["/writing/20200219-in-defense-of-nothing-interesting"] # alias url / permalink

tags: ["data", "data science", "research", "analysis", "questions"]
categories: ["data"]

draft: false

showToc: false
TocOpen: false

hidemeta: false
disableShare: true

# cover:
#     image: "/images/kpis-dudley-metrics.gif"
#     alt: "<alt text>"
#     caption: "<text>"
#     relative: false

comments: false
---



### _A tribute to useful, but less interesting research findings_

###### _originally published on_ [_Medium_](https://towardsdatascience.com/in-defense-of-nothing-interesting-577b47b198da?source=friends_link&sk=1ce03345fd14ca451d3988057025bade)




---

> A tribute to useful, but less interesting research findings

A few years ago as a Data Scientist I was presenting to co-workers an analysis I’d been working on. The presentation went fine and the work was well-received, but I could tell the group was a little underwhelmed. Towards the end of the presentation, one co-worker asked, “Did you find anything that surprised you? Anything we didn’t already know?”

I had uncovered some new information, but most of what I’d found was well-aligned with what we already thought to be true. Still, I understood their sentiment. Any Data Scientist or Researcher will tell you that the most common thing we find when analyzing a dataset is… nothing interesting. It happens constantly. Many of our findings corroborate what we and our business partners already thought to be true, even when we’ve asked the right question. This can be frustrating for Data Scientists, Researchers, and our partners, but finding “nothing interesting” is *very* different from finding “nothing useful,” and I’m a strong believer that finding nothing interesting after asking the right question is still worthy of celebration.

# The Utility-Interest plane

Before diving in, I want to emphasize the difference between a result being _interesting_ and a result being _useful_. All analytical results (and the questions that spawned them) will fall somewhere in the Utility-Interest plane.

![](/images/nothing-interesting-plane.png)

**A.** Useful results that are also interesting are the holy grail. Findings from these analyses drum up tons of excitement with stakeholders and have the potential to create a huge impact.

**B.** Useful results that aren’t too interesting are less exciting, but are equally valuable! These are the only types of uninteresting results that are still defensible (the main topic of this post!). Useful, yet uninteresting results often arise when evaluating a hypothesis that everyone had assumed to be true, or when tackling a question that’d been answered through other methods in the past.

**C.** Useless results that aren’t very interesting are just a poor use of time. These come from asking the wrong question, and a question to which everyone already knew the answer. These won’t gain much traction with stakeholders, and the primary downside is just wasting your own time.

**D.** Useless, but interesting results are dangerous. Very dangerous! Useless, yet interesting results arise when finding an exciting answer to the wrong question. Stakeholders can latch onto these findings and invest their own time into addressing a topic that should be lower priority.

By finding “nothing interesting” in the data (i.e., a result in quadrant B) and presenting it to your stakeholders, you’re able to make decisions with more confidence, ask meaningful follow-up questions, and increase stakeholders’ trust in using data in the future.

# Knowing when your intuition is right is just as important as knowing when it’s wrong

Asking a question of the data means you’re unsure about something: maybe a course of action to take, the reason behind something happening, or something else. Exploring a dataset and finding no surprises just means that, in this case, your intuition wasn’t too far off.

Even when you and your business partners have some intuition about a problem area, evaluating your hypotheses with data will let you know, without a doubt, if your hypotheses were true. Knowing when you’re right is just as important as knowing when you’re not, and by evaluating your hypotheses you’ve learned to either maintain or change course.

# Asking meaningful follow-ups

Assuming you asked a worthwhile question of the data, finding “nothing interesting” will help inform what questions you should ask in the future. Any useful finding — whether interesting or not — gives you more confidence in the problem area and refines your area of focus, helping you to ask better questions going forward.

# Reinforcing confidence in data

Findings that contradict our intuition can be hard to accept — especially when the findings tell us that not only was our intuition wrong, but that our actions or plans were too. By finding and presenting “nothing interesting,” you help build trust between your stakeholders and the data, making it easier for them to accept information from you in the future, especially when it’s counter to some of their beliefs.

# What to do now

**Ask the right questions of your data.** Of course, the points above only hold true if you’ve asked the right question in the first place. Poor questions can sometimes lead to interesting answers, but the usefulness of these answers will be limited. My favorite way to refine a research question is to brainstorm with a cross-functional group of stakeholders (plus with this approach, you get stakeholder buy-in at the same time).

**Celebrate “nothing interesting.”** A finding doesn’t have to be interesting in order to be useful. Next time you find “nothing interesting,” remember to celebrate it.

---

### Further reading

For resources on asking good questions, I really like [Asking Great Questions as a Data Scientist](https://datamovesme.com/2019/03/02/asking-great-questions-as-a-data-scientist/) by [Kristen Kehrer](https://medium.com/u/8be51bb10c2f), and [How to solve a business problem using data](https://www.littlemissdata.com/blog/businessproblem) by [Laura Ellis](https://twitter.com/LittleMissData/). (Please let me know if you have any others!)
