# privacy_engineering

This is Imperial Coursework for Privacy Engineering

# Friday 31st October - Meeting Notes

Dropping rows:

- compromise utility to achieve privacy (k-anonymity)
- remove outliers/insensible rows because otherwise very hard to achieve k-anonymity
- can show benchmark before vs after to discuss tradeoffs

Equivalence classes issue:

- as long as we benchmark and show distribution before vs after

quasi-identifiers:

- keep more specific, e.g. still with income since attacker can still have access to this information
- can decrease bin sizes to help generalize more (e.g. income only useful for on-benefits fairness so only care about low vs high income, no need more bins)

_k-anonymity & l-diversity code: done by this weekend_

Report:

- follow yasminehemmat report structure
- can write report based on split work
- yukie & hs: part 1-3, part 6 evaluation
- hailey & lyn: part 4-5
- part 7 can be done by whoever finishes first

report deadline: next Wednesday

- proof read before Friday

=============================================

Meeting Agenda:

- Meeting online every Thursday morning 10am
- For anything urgent we can jump in fast call

Timeline:

- Before next Thursday get the strategy part out
- Work on test and report after next Thursday

Task Allocation:

- Hs & Yukie: Benchmark + Analyze + hashing
- Hui Xuan & Xin Yi: Suppression + Generalisation

Strategy:

1. Analyse the dataset: identify the quasi and the sensitive information, seeing if there any missing data and checkout the distribution of dataset
   1. sensitive: disease, on_benefit, malnutrition score
   2. quasi: everything except name and dob
   3. check for duplication for hashing
2. Hashing: pseudomisation => find hash function [just use pick one and justify the reason] with a salt [random string]
   1. Generate an id for each entry then hash it [why we need the id]
   2. Check if the duplication happens, if not then concat
3. Suppression => evaluation on which column is not uncessday for usecae => remove unnecessary attribute column before
   1. Drop name and dob (map into age)
4. Anonymising the data: generalising the data
   1. postcode: remove to the first two / three letters => the biggest area represent
   2. mulnitration: high or not high [into the range (based on the distribution)]
   3. Age: into brackets
   4. income: into brackets / low, middle, high
   5. Num of children: in brackets
   6. Home ownership: rent / buy (or just keep it)

benchmark: ( after each step [define the func])

1. Evaluate utility: entropy and k-anomity (find the optimal k value), L-diveristy and T-closeness
2. Evauate safety: do all the attacking (semnatic, heterogeneous attack, profiling attack)

Testing (later part):

- each user case and evaluate the usefulness (accuracy score and recall / F1 score)
  - Compare with the original data

Report => do it later

kldnl;ask jdfwe
