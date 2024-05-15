# TE Academy Reputation Weighted Voting Course

## Week 3 Resources
by: Octopus

Here is a list of resources that will help prepare learners for the topics of discussion in Week 3 of the TE Academy RWV Course. 

**Overview:** In Week 3, we will start making real progress towards selecting the final voting algorithm, by listing and analyzing potential approaches. This will be a lot of fun, but we have two fundamental constraints to keep in mind.
1. The fact that no voting algorithm will perform as desired in all situations.
2. The fact that the final decision and implementation needs to be done in just a few weeks. 

Students will be asked to present on a voting design that they think may work as a final candidate, and meets all the requirements needed. It's important that these voting systems be **specific** -- we should know how to implement them in a clear, step-by-step manner. 

The materials below are intended to help learners be prepared for these discussions, by emphasizing the kinds of tradeoffs that will need to be considered, and the tools that make it possible to consider these tradeoffs. 8 would encourage you to look at not only the content of these materials, 
but also the choices made in presenting and explaining the facts given. 

The goal of these materials is **not** so much the specific vote-processing algorithms being analyzed, but rather the big picture of different approaches for looking at the algorithms under consideration. There is a lot of material here, and I don't expect anyone to engage with **all** of them before Wednesday's class. 
Rather, 8 would encourage you to engage with ones that look accessible and/or interesting, so that as a community we are prepared to explore different aspects during Wednesday's session. 

### Basics 

These materials will be most useful if you are a beginner to voting systems and/or computational analysis of complex systems. 

#### Overview of Voting

* [Introduction to Weighted Voting, by mathis4u](https://www.youtube.com/watch?v=Iaxblazgb1Y) In order to achieve the requirement that TEAcademy credentials be meaningful in the final decision, it feels natural to consider assigning weights to voters based on their TE Academy NFTs (and possibly other computable aspects). 
These weights can be processed in a variety of ways and combined with other methods, but it's necessary to first understand the concepts of the most basic weihted voting systems. Some questions that might arise in our context include: is it over OK for a wallet to have veto power in our system? is it over OK for a wallet to be a dummy?
* [Five Ways Plurality Voting Fails](https://electionscience.org/voting-methods/spoiler-effect-top-5-ways-plurality-voting-fails/) 
* [To Build A Better Ballot: An Interactive Essay by Nicky Case](https://ncase.me/ballot/) This explorable explanation  allows the user to explore the outcome of different voting procedures using intuitive click-and-drag visual simulations. Highly recommended. 

#### Exploring Complex Systems
* [Safe-to-Fail Experiments, by Cultivating Leadership](https://www.youtube.com/watch?v=i_h2WJ1qNRA)
* [Introduction to Functions in Python, Part 1](https://www.youtube.com/watch?v=5YQ__J5HmGg) It's extremely helpful in many aspects of Token Engineering to be familiar with functions, from both the mathematical and computational viewpoints.
This video is part of a conversation I had with a former student on how to work with functions in Python.
* [Introduction to Functions in Python, Part 2](https://www.youtube.com/watch?v=MhUty_RdXpw) A continuation with some more approaches to functions in Python and mathematics. 

### Intermediate

Here we include a few examples of voting systems, coupled with analyses. 

* [The Top 5 Ways Plurality Voting Fails](https://electionscience.org/voting-methods/spoiler-effect-top-5-ways-plurality-voting-fails/) Plurality voting (what many people are referencing when they say "democracy") has a number of non-obvious but easily understandable drawbacks. 
This article lays out 5 clear issues with using this method. 

* [Ranked Choice Voting](https://ballotpedia.org/Ranked-choice_voting_(RCV)) A description of Ranked Choice Voting, also known as "Instant Runoff Voting". 
* [Mathematical Flaws in Ranked Choice Voting are Rare But Real](https://www.promarket.org/2023/05/03/mathematical-flaws-in-ranked-choice-voting-are-rare-but-real/) An analysis of some cases where Ranked Choice Voting does not perform in ways that one might hope. 

* [Fairness in Voting Methods](https://openstax.org/books/contemporary-mathematics/pages/11-2-fairness-in-voting-methods) This textbook section shows a variety of measurable criteria that might represent the intuitive notion of "fairness". 
It gives clear examples of how different methods can fail to meet this criteria. 

* [Electoral Systems Criteria, by Great Canadian Bagel](https://www.youtube.com/watch?v=jyZriqHQeJM) A very watchable 20 minute overview of different criteria or requirements that one might look for in a voting system. 
* [The Favorite Betrayal Criterion](https://electowiki.org/wiki/Favorite_betrayal_criterion) We would think that a voter should never have an incentive to rank their preferred choice lower than first. However, there are instances where doing so actually helps their preferred candidate win! 
* [Later-No-Harm Wikipedia Article](https://en.wikipedia.org/wiki/Later-no-harm_criterion) The Later-No-Harm Criterion is an example of a subtle mechanism that a voting system can fail. While this may not be the first thing we consider when designing our voting system, such criteria are useful for framing specific discussions. 

* [Why Approval Voting is Unworkable In Contested Elections](https://archive3.fairvote.org/research-and-analysis/blog/why-approval-voting-is-unworkable-in-contested-elections/) This article explores how approval voting and other mechanisms can be gamed by strategic voters. 

### Advanced (or Academic)

These are more formal mathematical ways that one might analyze a voting system. It's good to be thinking now about how these could be implemented in the near future. 

* [Shapley-Shubik Power Index](https://math.libretexts.org/Bookshelves/Applied_Mathematics/Math_in_Society_(Lippman)/03:_Weighted_Voting/3.05:_Calculating_Power-__Shapley-Shubik_Power_Index) The Shapley-Shubik Power Index is a popular method for determining how much power a voter ("player")
holds in a weighted voting system. 
* [Shapley-Shubik Power Index YouTube Explainer](https://www.youtube.com/watch?v=6T7g4AyMIm0) A video explaining how to 


* [Ethical Considerations on Quadratic Voting, by Ben Laurence and Itai Sher](https://ideas.repec.org/a/kap/pubcho/v172y2017i1d10.1007_s11127-017-0413-4.html) Gives an argument using economic utility theory that any vote-buying scheme will run into issues when there are inequalities of wealth. 
In addition to the result being interesting in its own right, it gives a nice example of how utility functions can be utilized in analysis of voting theory. 
