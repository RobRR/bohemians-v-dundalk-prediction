# Match preview: Bohemians v Dundalk

When Bohemians and Dundalk last met at Dalymount Park in the League of Ireland's Premier Division on Friday, 20 March 2026, the game ended in a 1-1 draw. 

Interestingly, the Dixon-Coles model predicts another 1-1 draw as being the most likely outcome when the sides renew acquaintances at the Phibsborough venue on Friday, 19 June 2026 (8pm; live *Virgin Media Three*).

---

### Key insight ### 
Even the most likely outcome (11.7%) is not that likely. The Dixon-Coles model treats goal scoring as a random process governed by a Poisson distribution, adjusted for team strengths. In a low-scoring sport like football, a single goal can define the outcome of the game, as matches average only two to three goals in total.

Because a single goal makes up such a huge part of the final score, one lucky or unlucky moment can completely change who wins. This makes football incredibly unpredictable. The model mathematically reflects this variance by spreading out its probabilities, meaning the most likely outcome still has a low chance of occurring.

---

### Model mechanics & visuals
*The accompanying chart shows the respective goal distributions for both sides and the Dixon-Coles correct score matrix:* 

![Bohemians vs Dundalk Prediction](bohs_dundalk_prediction_2026.png)

## Overcoming the independence limitation

A baseline independent Poisson model struggles with low-scoring football matches because it assumes team scores are entirely independent. To fix this, a Dixon-Coles parameter ($\rho$) adjusts the lowest scorelines:

* 📈 **Inflates 0-0 and 1-1:** Accounts for the real-world tendency of low-scoring matches to end in draws more often than pure randomness predicts.
* 📉 **Deflates 1-0 and 0-1:** Corrects the standard Poisson model's tendency to overstate narrow, single-goal victories.


*This fix only changes low-scoring games. If either team scores two or more goals, the score is not affected.*

---

### Odds & market probability analysis

Based on the probabilities derived from the Dixon-Coles model, Bohemians are the favourites to win. However, a comparison with the market reveals significant bookmaker overround.

| Outcome | Fair odds (model) | Implied probability (model) | Paddy Power odds | Implied probability (market) |
| :--- | :---: | :---: | :---: | :---: |
| **Bohemians win** | 2.07 | 48.31% | 1.80 | 55.56% |
| **Dundalk win** | 3.83 | 26.11% | 3.70 | 27.03% |
| **Draw** | 3.93 | 25.45% | 3.70 | 27.03% |
| **Total book** | — | **100%** | — | **109.62%** |

#### Market takeaway
Paddy Power’s total book stands at 109.62%, meaning they have built a sizeable overround of 9.62% into this specific market. Efficiently-priced markets with heavy overrounds are mathematically unbeatable over the long term. Consequently, there is no positive expected value (+EV) in backing Bohemians.

---

### 📋 Note on model parameters
A time-decay factor was intentionally omitted from this run. Because the 2026 League of Ireland season only kicked off in February – with just 101 of the 180 total games played to date – the sample size is fresh enough that artificially discounting early-season data would introduce unnecessary noise rather than predictive signal.
