---
title: "Speaking like a president"
description: "Natural language processing on the first 2016 presidential debate"
summary: "Natural language processing on the first 2016 presidential debate"
author: "Brian Weinstein"
date: "2016-10-03"
publishedElsewhere: "Originally published on [Fouriest Series](https://fouriestseries.tumblr.com/post/151287440363/natural-language-processing-on-the-first-2016)"
# weight: 1
aliases: ["/posts/20161003-debate-nlp"] # alias url / permalink

tags: ["data", "analysis", "nlp"]
categories: ["data"]

draft: false

showToc: false
TocOpen: false

hidemeta: false
disableShare: true

cover:
     image: "/images/debate-header.png"
#     alt: "<alt text>"
#     caption: "<text>"
#     relative: false

comments: false
---


The first debate in the 2016 presidential race was held on September 26. It’s no secret that Clinton and Trump are running on drastically different platforms, but how do they compare when it comes to their speech patterns and word choice? To quantify this, I dug into the data, using the debate transcript and natural language processing.

I measured the sentiment of Clinton’s and Trump’s responses, and examined how emotional their words were throughout the debate. I also looked at each candidate’s most commonly used adjectives. Building off the work of [Alvin Chang at Vox](https://www.vox.com/debates/2016/9/27/13070616/debate-clinton-trump-not-answers/in/12771101), I was also able to examine how the speech patterns of Clinton and Trump each changed when directly responding to and when skirting the questions.

# Sentiment

Using the [Google Cloud Natural Language API](https://cloud.google.com/natural-language/), I measured the sentiment of each candidate’s answers. The [polarity](https://cloud.google.com/natural-language/docs/basics#sentiment_analysis_response_fields) of a response is a measure of how positive or negative it is, and the [magnitude](https://cloud.google.com/natural-language/docs/basics#sentiment_analysis_response_fields) indicates how much emotion the words convey. The chart below shows the polarity of each candidate’s responses, weighted by the magnitude.

![](/images/debate-sentiment.png)

Trump and Clinton matched each other’s polarity for the first half of the debate, but after his defense of stop-and-frisk around 9:50 PM, Trump’s words became much more negative.

Throughout the rest of the debate — during the questions on birtherism, cyber security, homegrown terrorism, nuclear weapons, and Clinton’s looks and stamina — Clinton became more positive and Trump more negative.

[The combination of polarity and magnitude](https://cloud.google.com/natural-language/docs/basics#interpreting_sentiment_analysis_values) gives us the best understanding of each line’s overall sentiment, and each candidate’s most positive and negative responses are posted [here](https://github.com/BrianWeinstein/presidential-debate-nlp/blob/master/quotes.md).

## Braggadocios, and other adjectives

I was also interested in the adjectives each candidate used most frequently during the debate. Using syntax analysis to extract each word’s part of speech, I identified the most-used adjectives of each candidate.

![](/images/debate-clinton-adj.png)

![](/images/debate-trump-adj.png)

## Answers vs non-answers

As [Chang](https://www.vox.com/debates/2016/9/27/13070616/debate-clinton-trump-not-answers/in/12771101) found, the candidates spent a lot of time not answering Holt’s questions — 48% of Clinton’s words and a whopping 69% of Trump’s words were used in non-answers — and using the data Chang compiled, I was able to look at how the candidate’s speech patterns differed when answering and not answering the questions.

![](/images/debate-nonanswers.png)

## Sentence subjects (“[I alone can fix it](https://www.theatlantic.com/politics/archive/2016/07/trump-rnc-speech-alone-fix-it/492557/)”)

Using part-of-speech tagging, I also identified the [subjects](https://universaldependencies.org/en/dep/nsubj.html) of each candidate’s sentences. Clinton was more inclusive in her words, but only when directly responding to questions — using the plural “we” more frequently than the singular “I” — and the the opposite was true for her when avoiding a response. Trump, on the other hand, was always more likely to use “I” over “we”.

![](/images/debate-clinton-subj.png)

![](/images/debate-trump-subj.png)

## Non-answer phrases

The words each candidate used when directly answering the questions are all, unsurprisingly, highly related to the questions Holt asked. What’s interesting here are the topics the candidates defaulted to when avoiding a response.

![](/images/debate-clinton-nonanswer.png)

![](/images/debate-trump-nonanswer.png)

---

- A handful of my findings didn’t make it into this post. If you’re interested in more, there’s some additional analysis, including multiple classification models, in the project’s [GitHub repo](https://github.com/BrianWeinstein/presidential-debate-nlp).
- The text of this article (excluding this sentence) has polarity -0.4 and magnitude 15.5, so despite my best efforts it’s leaning slightly negative.
- Many thanks to [Alvin Chang and Vox](https://www.vox.com/debates/2016/9/27/13070616/debate-clinton-trump-not-answers/in/12771101) for their permission to use their annotated transcript, and to [Kelsey Scherer](https://twitter.com/kelsa_) for designing the charts and lead image.
- Analysis was performed in R.
- Plots were generated using ggplot2, and then styled by Scherer using Sketch.
- The sentiment scores, part of speech tags, and all of the other NLP datasets can be found in the [GitHub repo](https://github.com/BrianWeinstein/presidential-debate-nlp).
