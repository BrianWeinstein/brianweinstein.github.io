---
title: "Defining meaningful metrics for product teams"
author: "Brian Weinstein"
date: "2020-12-22"
# weight: 1
aliases: ["/posts/defining-meaningful-metrics-for-product-teams"] # alias url / permalink

tags: ["data", "product", "metrics", "kpis"]
categories: ["data"]

draft: false

showToc: false
TocOpen: false

hidemeta: false
disableShare: true

# cover:
#     image: "/images/dudley-metrics.gif"
#     alt: "<alt text>"
#     caption: "<text>"
#     relative: false

comments: false
---



### _A checklist for developing better product metrics & KPIs_

###### _also published on_ [_Medium_](https://bweinstein.medium.com/defining-meaningful-metrics-for-product-teams-56576d34a684?source=friends_link&sk=0ad658b2703fce11d061f26278851618)




---

Defining clear KPIs is one of the most important things for a Product team, and (unfortunately) it’s incredibly easy to do poorly. A good metric not only helps evaluate your product’s performance, but also guides your team in building the right things to progress you toward your goal.

The framework described below is one I’ve used for a few years while working with teams that develop software products, and has been very helpful for me, my Data Science teammates, and our Product partners in measuring the success or failure of the products we build.

# Shared definitions for objectives, KPIs, & product metrics

Before diving in, let’s define a few relevant terms and how they relate to each other.

An **objective** is a description of the impact you want to have on the business. It should be qualitative, easy to understand, and somewhat obvious.

A **key performance indicator (KPI)** (aka **success metric**) is the one, top-level metric that measures if your product is driving the outcome outlined in the Objective. This is the quantifiable top-level goal of your product, and should be a more quantitative statement of your objective. This is *the* metric you use to measure the performance of your product. Your success metric should be set longer-term and the definition of it shouldn’t change very much, if at all, from quarter to quarter.

A **product metric** measures the success of a specific feature. These are lower level metrics than KPIs: product metrics are something you should monitor to make sure your feature is facilitating the user behaviors that ultimately contribute to your KPI. Product metrics are also helpful in reporting: to ensure users are making use of the feature you’ve built in the way that you intend.

A **health metric** is used to monitor the technical health of a product. These are usually more pertinent to Engineers, but important for Product leaders to monitor as well. Performance metrics include things like page load time, API response time, etc. I won’t focus on them here, but want to call out that they’re distinct from these other types of metrics.

*You may have different names for some of these concepts, but the ideas behind them should be more or less the same. What’s most important is aligning on a common vocabulary for you and your team to use when talking about these ideas.*

![Dudley Dursley uses bad metrics.](/images/dudley-metrics.gif)
(a bad metric)

# The “good metric” checklist

Since it’s so easy to come up with the wrong metric, I like to think through a few criteria while brainstorming to ensure we settle on a metric suitable to the product. The criteria below apply to both KPIs and Product Metrics.

**Specific & sensitive**: Metrics should be specific to the product or feature, and need to be explicitly and quantitatively defined. The metric should also be sensitive enough to measure the impact we expect to see.

**Robust**: To complement the **sensitivity** criteria above, we also need to make sure the metric is measuring only the effect of the product of interest, and that it isn’t reactive to things we expect to change but don’t control. Related to [internal validity](https://en.wikipedia.org/wiki/Internal_validity), we should try to avoid using a metric that can be significantly influenced by anything other than the product/feature we care about.

**Measurable**: This one is kind of obvious, but a metric must be something that we can actually measure. It’s not uncommon to ideate a bunch of “ideal” metrics that would perfectly measure the impact of your product, but end up being impossible or infeasible to really capture.

**Interpretable**: Metrics should be easy to understand and agreed upon by those whose success is measured by the metric. There’s often a tradeoff between simplicity and accuracy, and I typically err on the side of simplicity. A metric that’s hard to understand provides none of the benefits listed in the section below.

**Aligned**: Objectives, KPIs, and Product Metrics are hierarchical: every product should have an objective, a KPI that quantitatively measures progress toward achieving the objective, and then multiple product metrics to evaluate the performance of individual features. A product’s KPI should also be aligned upward with higher level company metrics. Any movement in these metrics should also be reflected in and contribute to those above them in the hierarchy.

This certainly isn’t an exhaustive list, but captures some of the most important criteria. If your metric meets all five of these conditions you should be in fairly good shape. If your metric doesn’t meet one or more of these criteria, you’ll likely need to ideate other metrics to use for your product.

# Benefits of this approach

It takes a fair amount of effort to pick the right metric, and this is why it all matters!

**Clarity of thought**: Often what seems obvious to you is not so clear to others. Defining your goals & objectives in terms of hard numbers forces you to make your personal intuition clear to your team and to others at the company.

**Opportunity for innovation**: KPIs and product metrics represent a goal, but don’t mandate the path to get there. This frees up everyone on the team to think about new ways to move the needle rather than focusing on a prescribed solution.

**Alignment on goals**: When you set your metrics, you tell your business partners what return it should expect from its investment in your team. If expectations aren’t aligned, you’re able to pivot before it becomes a problem.

**Insight for prioritization**: You can use your pre-defined KPI to compare the potential impact of a handful of projects you’re considering working on.

**Proof of success**: It’s much easier to communicate your impact on the organization when your goals are quantifiable.

**Indication of failure**: By monitoring progress toward your goals, it’s easy to correct course or sunset a product when your efforts aren’t as effective as intended.

# Notes on this framework & further reading

This is a work in progress! I’ve added to and generalized this framework over the past few years as I’ve worked with different types of teams (based on their domains, operating style, degree of data literacy, etc.), and will keep doing so in the future.

There’s a lot I don’t touch on in this article, like leading & lagging indicators, reliability, defining targets for your metrics, balancing metrics, and more. For further reading, I like:

- [Finding the metrics that matter for your product](https://www.intercom.com/blogfinding-the-metrics-that-matter-for-your-product/) by the Product & Data team at Intercom
- [How to grow product with KPIs](https://medium.com/@ilnem/growing-product-with-kpi-trees-34d91f49671b) and [How to prioritize work with KPIs](https://medium.com/@ilnem/how-to-prioritize-projects-or-the-main-product-growth-equation-9cc08da2e160) by Ilya Leyrikh
- [A framework to define your product metrics](https://uxdesign.cc/a-framework-to-define-your-product-metrics-6ca9837bfc8b) by Zandre Coetzer
- [10 tips on how to choose the right key performance indicators](https://www.romanpichler.com/blog/10-tips-how-to-choose-the-right-product-key-performance-indicators-kpis/) by Roman Pichler
