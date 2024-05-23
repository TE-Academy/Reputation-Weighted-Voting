# Voting Designs for TEA Reputation-Weighted Voting

## GroupHug, by [Joan](https://github.com/joanbp-dk)

Voting interface: A voter is asked to vote for one of the eligible candidates.

Behind the scenes each voter is seen as belonging to one or more stakeholder groups: Experts, intellectuals, active participants and the community at large. Group membership is determined based on the voter's TEA NFTs. Each stakeholder group distributes points among the candidates according to the group's own algorithm (the specifics are explained in the full description of the design). A candidate's final score is the weighted sum of points that they receive from all stakeholder groups. The winner is the candidate with the highest final score.

[Illustration](https://github.com/joanbp-dk/Repbased_voting_playground/blob/main/Voting.pdf)

[Full design](https://github.com/joanbp-dk/Repbased_voting_playground) (see the [readme.md](https://github.com/joanbp-dk/Repbased_voting_playground/blob/main/README.md) for details on how to play with the mechanism).

## Rank-and-Slide, by [Jonas](https://github.com/derjogi/)
A simple rank-us-on-a-slider interface where voters rank candidates on one slider.

Under the hood it works like this:

Each candidate has a total score available, depending on which NFTs they’ve done
When voting, each candidate starts in the middle of the slider, i.e. everyone would get the same proportion of the voters score (i.e. with 4 candidates each gets 25%)
The voter can change each candidate’s relative position, which will give the candidates more or less of the pie
The points a candidate will receive will be calculated live, so the user has feedback about their setting
The scores from all voters will be added up, the candidate with the total highest score wins.
On a draw, the tiebreaker could be which candidate has the smallest average score (e.g. a few people might have voted for candidate A with 100% of their voting power, but not many others gave cand. A a lot, whereas many voters gave candidate B just slightly above 50%, bringing that to the same total as A. Candidate B would win)

Here’s the visual diagram explaining it: https://docs.google.com/presentation/d/1Mr8U3o2A4rFQo3HgAMjrNDfHDD2v3_1EMMa_XrmDWaA/edit?usp=drive_link

I’ve got a code repository at https://github.com/derjogi/Repbased_voting_playground (forked from Joan’s repo 🙇) in which a basic version of this can be tested in a Jupyter Notebook (https://mybinder.org/v2/gh/derjogi/Repbased_voting_playground/HEAD?labpath=Playground.ipynb). There are some explanations on that file, and I’ll continue to update and improve them. Or possibly I’ll soon just merge it with other repos 🤷 

## Quadratic Credibility, by [flocke](https://github.com/fxFlocke)

TODO
