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

## Quadratic Credibility Voting, by [0xJade](https://github.com/0xJade) & [flocke](https://github.com/fxFlocke)

The QCV-Mechanism is designed with the intent to level up the fairness in distribution of Grants/Funding, 
while smoothing out inequalities of weight for Voter-Groups and make Voters really feel their impact on the outcome. 

It takes 2 approaches to tackle this Problems:

   **1. Combine Quadratic Funding & Quadratic Voting:**
   
      * Quadratic Funding protects the outcome against to much influence from high-weight Voters, who put all their Voting-Power on one candidate.
      * Quadratic Voting provides a much more fine grained distribution of the Grant, since the Candidate-Voting-Scores are mapped in a larger range.
      * It is represented with the following Equations:
          * $T_i(a) \in T_i$ (The VotingCredits($T_i(a)$), which are allocated to a candidate($a$), are a subset of the whole amount of VotingCredits of a Voter)
          * $QS(a) = \sum_i^n \sqrt{T_i(a)}$ (The Quadratic-Score of a Candidate, is build by the sum over all Square-Rooted Token-Credits, allocated by each voter)
          * $QV(a) = QS(a)^2$ (The Quadratic-Votes of a Candidate, is build by Squaring the Quadratic-Score)
          * In general, the QCV-Mechanism distributes the Grant/Fund according to their percentual share of Quadratic-Votes, in respect to all Quadratic-Votes.
          * For special cases like this, the Grant will be given completely to the Candidate with the highest $QV(a)$, which naturally also the highest Quadratic-Score. 

  **2. Voting-Credit allocation depending on weights:**
  
      * The amount of Voting Credits distributed, will always match exactly the Grant amount.
      * Each Voter receives a share of the Grant, that equals his share on the total weights.
      * This hopefully results in Voters really feeling the impact & power of their Voting-Rights.
      * The outcome in Grant-Distribution will not exactly match the Voted-Credits, which is needed from an Incentive-Compatability persepective.
      * Nevertheless, Voters know their upfront chance of impact, which will be bound by QF & QV rule to minimize the impact of high-weight-groupings.

      

You can find the Presentation-Slides here: https://docs.google.com/presentation/d/1MKdSUUVRQSXPU_SDV6O1fsfNEyTS2RN1oSDXPuwaZP0/edit#slide=id.g202d2d8a737_0_69

A customized Simulation-Tool to verify the Mechanism here: https://github.com/fxFlocke/votingSimulations

Additonally here is a first draw of an Implementation-Schema that can be used: https://discord.com/channels/1016433241978314913/1232416297170636961/1240336875902730270
