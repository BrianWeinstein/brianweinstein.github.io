---
title: "Moving beyond the Net Promoter Score"
author: "Brian Weinstein"
date: "2018-01-24"
# weight: 1
aliases: ["/posts/20180124-moving-beyond-the-net-promoter-score"] # alias url / permalink

tags: ["data", "product", "metrics", "ux", "research", "surveys", "design"]
categories: ["data"]

draft: false

showToc: false
TocOpen: false

hidemeta: false
disableShare: true

cover:
#     image: "/images/nps-header.jpeg"
#     alt: "<alt text>"
#     caption: "<text>"
#     relative: false

comments: false
---



### _A guide to building a more meaningful metric_

###### _originally published on_ [_Medium_](https://bweinstein.medium.com/moving-beyond-the-net-promoter-score-9b560f3767ba?source=friends_link&sk=bd16145b78737841c82e37e67b540f05)




---

![](/images/nps-header.jpeg)

The Net Promoter Score is a widely-used survey question that companies use to measure customer satisfaction, loyalty, and growth.

Proponents of NPS are drawn to it because it’s a single number that appears — on the surface, at least — to be linked to some significant indicators of performance. NPS a bad measure of success, though. It uses a poorly phrased question, a response scale that’s entirely too big, and an absurd method of calculation.

There are other metrics you can use that will be more accurate, more interpretable, and much more predictive of satisfaction, loyalty, or growth.

# Background

The standard Net Promoter Score (NPS) question asks, “How likely is it that you would recommend [company X] to a friend or colleague?” Respondents are given a scale ranging from 0–10, with 0 labeled with “Not at all likely,” and 10 labeled with “Extremely likely.”

![](/images/nps-standard.png)

Under the NPS methodology, respondents who submit a 9 or 10 are considered “promoters,” 7 or 8 are considered “passives”, and 0–6 are considered “detractors.”

The Net Promoter Score for a group of respondents is defined as the percentage of respondents who are promoters minus the percentage of respondents who are detractors.

NPS = (# of promoters - # of detractors) / (total # of respondents)

# Origin

NPS was originally proposed in a December 2003 [Harvard Business Review (HBR) article](https://hbr.org/2003/12/the-one-number-you-need-to-grow) by Fred Reichheld, a director at the Bain & Company management consultancy. Reichheld proposed the score as a “loyalty” metric, which he defines as the “willingness of someone… to make an investment or personal sacrifice in order to strengthen a relationship.”

Reichheld tested eight survey questions among 4,000 consumers, and tracked these consumers’ future purchases and referrals. He then measured the link between the survey responses and actual purchase and referral behaviors.

The NPS question — “How likely is it that you would recommend [company X] to a friend or colleague?” — was the 1st- or 2nd- most predictive question in 11 of Reichheld’s 14 case studies, showing “the strongest statistical correlation with repeat purchases or referrals.”

Reichheld chose a 0-to-10 scale, where 10 meant “extremely likely” to recommend and 0 meant “not at all likely.” He claimed that this scale was

1. “simple and unambiguous,”
2. “divide[s] customers into practical groups deserving different… organizational responses,”
3. was “intuitive to customers when they assign grades,” and
4. was intuitive “to employees and partners responsible for interpreting the results and taking action.”

I disagree with all of these. More on that below.

Reichheld then grouped the 11-point scale into the three clusters: promoters, passives, and detractors. In his analysis, Reichheld found a strong correlation between companies’ net-promoter figures and their revenue growth rates.

_I highly recommend reading [the original article](https://hbr.org/2003/12/the-one-number-you-need-to-grow) with a critical eye: It’s full of anecdotes and correlations that Reichheld frames as causal relationships. Every few paragraphs he attempts to argue that NPS is superior over some alternative measurement in terms of assessing loyalty, growth, etc.; but fails to sufficiently justify his claims._

# Why do companies use NPS?

NPS is popular. I mean _very_ popular. Tons of companies ask customers the NPS question, and many use it to measure and assess their performance.

![](/images/nps-expedia.png)

![](/images/nps-adobe.png)

![](/images/nps-glossier.png)

Proponents of NPS are drawn to it because it’s a single number that appears — on the surface, at least — to be linked to some significant KPIs. It’s also easy to measure and produces a statistic that changes easily over time.

If you’re trying to get your organization to be more data-driven, then NPS is certainly better than nothing.

# Why you shouldn’t use NPS

Now that we’ve gotten that out of the way, it’s time to discuss the many, many shortcomings of NPS. The phrasing of the NPS question, the measurement scale it uses, and method of calculation all go against the basic principles of survey sciences.

## Question

The NPS question asks a respondent to rate the likelihood of a hypothetical future; but strong, reliable survey questions ask respondents about their past behaviors, which tend to be much more predictive than forward-looking hypotheticals. “Do you plan to begin a diet in the next 6 weeks?”, for example, is a very different question from “Did you begin a diet in the last 6 weeks?” The NPS question forces the respondent to predict an ideal, future self, as opposed to reporting on their actualized behaviors.

The [HBR article](https://hbr.org/2003/12/the-one-number-you-need-to-grow) also claims that the NPS question measures loyalty and growth. In reality, though, it fails to ask about either, and isn’t necessarily what users of NPS are attempting to measure. In many cases, survey questions should be phrased to directly measure the quantity of interest.

An NPS-like question asking about actualized behavior would look more like, “In the last 6 weeks, have you referred [company X] to a friend or colleague?”

Reichheld promotes the NPS question as the most accurate one in predicting revenue growth rate. Proponents of NPS often fail to realize, however, that the NPS question was the most accurate _from a set of 8 poorly phrased options_ in Reichheld’s study. In Reichheld’s findings, the NPS question wasn’t even the most accurate predictor in all industries: In database software and computer systems, for example, other questions were stronger predictors of revenue growth rate.

## Scale

Responses collected from a large, 11-point scale are extremely noisy, and meaningful changes in ratings are hard to detect. On the NPS scale, the difference between a “6” and a “7” isn’t clear in the survey analysis, and the lack of labels on the intermediate (i.e., non-extreme) choices also make the distinction very subjective to respondents. The NPS scale is poorly calibrated, and so are the responses.

A better scale would use a 3-option Yes/Maybe/No system or a similar scale with 5 options. For any survey question, the response scale and number of options should be crafted to the individual question, and an 11-option scale is likely _always_ too big.

## Method of calculation

The method of calculation is one of the stranger aspects of the NPS.

The bucketing methodology that groups respondents into Promoters, Passives, and Detractors ends up hiding some improvements and exaggerating others. Even if respondents were able to make meaningful distinctions between a “5” and a “6”, or between a “4” and a “5”, the bucketing method categorizes all of these into the “Detractor” group, and these changes aren’t reflected in the score. An extreme example is when a company with all “0” ratings improves to having all “6” ratings: this is a huge improvement, but the NPS methodology makes it so the score doesn’t change at all. Some changes are also exaggerated by the method of calculation: the distinction between a “6” (detractor) and a “7” (passive), or between an “8” (passive) and a “9” (promoter) is exaggerated by the bucketing methodology.

The method of calculation — subtracting the percentage of detractor respondents from the percentage of promoter respondents — also produces a metric that’s difficult to interpret and hides important information. All three of the following response sets, for example, produce an NPS of +60:

![](/images/nps-multiples.png)

# Finding an alternative measurement

## NPS alternatives

The most commonly used alternatives to NPS entail a rephrasing of the question and usage of a smaller scale.

If you’re truly trying to measure growth or word-of-mouth promotion, I highly recommend Netflix’s retrospective phrasing of an NPS-style question. In its early days, Netflix asked subscribers, “In the last 6 weeks, did you recommend us to a friend or family member?” and gave respondents only a Yes/No scale to respond. Netflix also paired this with another question: they asked _new_ subscribers, “Were you recommended to us by a friend or family member?”

![](/images/nps-alt-netflix.png)

Other companies, like Vox Media’s [Polygon](https://www.polygon.com/), use a similar phrasing of the question with binary response options.

![](/images/nps-alt-polygon.png)

These are both significant improvements over the standard NPS question and scale.

YouTube has a version that deviates less from the standard NPS question and scale, but still makes some significant improvements: They keep the standard NPS question, but instead use a smaller, labeled scale.

![](/images/nps-alt-youtube.png)

## Some alternatives that are even better

In any survey, the quantity you’re trying to measure should dictate both the question you ask and the scale you use. The questions and scales you design to measure growth, loyalty, satisfaction, etc. should each be customized for a given use case. A few examples for different measurements are outlined below.

- **Growth:** In the last 3 months, have you recommended [company X] to a friend, colleague, or family member? [Yes/No]
- **Loyalty:** In the last 6 weeks, have you considered [canceling your subscription, switching to another provider, etc.]? [Yes/No]
- **Satisfaction:** How satisfied are you with [company X]? [1 (Very dissatisfied), 2 (Dissatisfied), 3 (Neither), 4 (Satisfied), 5 (Very satisfied)]

# What to do now

1. Identify what you’re trying to measure and write an appropriate question. If you want to measure word-of-mouth promotion or estimate future growth, then the “Growth” question above would be a good start. Measuring customer loyalty or customer satisfaction require entirely different questions, so make sure to ask about the thing you’re trying to measure.
2. Pick a reasonable scale for your question. 3- or 5-option satisfaction scales, and a Yes/No binary scale all capture accurate information and are easy for respondents to select from in a response.
3. Use a simple, logical method of calculation. If your response scale has 5 or fewer options, then it’s easy enough to report on the entire response distribution. If you need to have a single number to use in further analysis, then you might like a [top-box](https://measuringu.com/top-box/) or top-two-box percentage. You could also use the average of the numeric-encoded values, although you lose some information this way.

Whatever you do, pick something simpler and more interpretable than NPS.

# Additional reading and references

- [Net Promoter Score Considered Harmful](https://blog.usejournal.com/net-promoter-score-considered-harmful-and-what-ux-professionals-can-do-about-it-fe7a132f4430) by [Jared M. Spool](https://medium.com/u/b90ef6212176)
- [On Surveys](https://medium.com/mule-design/on-surveys-5a73dda5e9a0) by [Erika Hall](https://medium.com/u/d75bd682e04f)
- [Measuring the WeWork Member Experience](https://medium.com/@tsharon/measuring-the-wework-member-experience-dca7312857a2) by [Tomer Sharon](https://medium.com/u/45a23fe91a81)
