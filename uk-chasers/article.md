# Who is the strongest Chaser? The latest ratings and an interactive explorer

*Data through **2026-11-20**. Last successful data check: **2026-11-26 00:27 AUS Eastern Daylight Time** (Sydney time).*

## Latest ratings at a glance

| Rank | Chaser | Rating % | Change (pp) | SE (pp) | 95% range | Appearances | Latest date |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | Anne Hegerty | 75.8 | -0.62 | 4.71 | 65.4–83.8 | 508 | 2026-09-15 |
| 2 | Paul Sinha | 73.7 | +0.01 | 5.05 | 62.7–82.4 | 479 | 2026-11-20 |
| 3 | Jenny Ryan | 73.7 | +0.08 | 4.95 | 62.9–82.2 | 287 | 2026-11-16 |
| 4 | Mark Labbett | 72.1 | -1.02 | 5.01 | 61.3–80.8 | 518 | 2026-11-18 |
| 5 | Darragh Ennis | 57.2 | +0.07 | 7.41 | 42.2–71.0 | 120 | 2026-11-17 |
| 6 | Shaun Wallace | 44.4 | +0.12 | 6.10 | 32.8–56.6 | 494 | 2026-11-19 |

**Change** is the rating movement since that Chaser's preceding appearance, in percentage points. **SE** is the approximate posterior standard deviation on the same percentage-point scale—not the standard error of a raw win percentage. The 95% ranges condition on the model settings. Each row is measured at that Chaser's latest appearance, rather than at a shared forecast date. Same-day appearances are combined into one update.

**Anne Hegerty has the highest current point estimate at 75.8%.** The next estimates are Paul Sinha (73.7%) and Jenny Ryan (73.7%). Read the intervals and sensitivity comparisons before treating the order as decisive.

## What the rating means

A win against a target of 12 and a win against a target of 24 both count as wins, but they tell us different things. These ratings adjust for the challenge faced and allow performance to change gradually.

A rating of 75 means roughly a three-in-four estimated chance of winning a **reference Final Chase against a target of 18**. It does not mean 75% question accuracy or a 75% actual career win rate. This measures Final Chase performance conditional on the target, not overall quiz knowledge or performance across every round.

Every Chaser starts with the same broad assumption. Before each result, the model predicts a win probability using their history and the target. Unexpected wins move the estimate up; unexpected losses move it down. Recent evidence can change the estimate, while older appearances still contribute. The chart starts displaying a Chaser after 20 appearances.

## The data

This snapshot contains **2406 episodes and 9624 player records**, spanning **2009-06-29 to 2026-11-20**. Records originate from [One Question Shootout's episode tables](https://onequestionshootout.xyz/episodes/series_all.htm) and [player tables](https://onequestionshootout.xyz/players/series_all.htm). The counts describe the available cache, not a guarantee that every broadcast episode is present.

| Chaser | Episodes | Win rate | Mean target |
| --- | --- | --- | --- |
| Anne Hegerty | 508 | 79.7% | 16.3 |
| Darragh Ennis | 120 | 76.7% | 15.2 |
| Jenny Ryan | 287 | 79.4% | 16.0 |
| Mark Labbett | 518 | 75.7% | 16.7 |
| Paul Sinha | 479 | 78.5% | 16.4 |
| Shaun Wallace | 494 | 71.3% | 15.3 |

The model uses the Final Chase Chaser, date, target and result. Player data support validation and the seat exploration below; Cash Builders and money do not enter the recommended rating. Unknown outcomes and invalid targets are excluded rather than invented. Airing order may differ from filming order.

**Episode 16.075 date status:** Provisional: user assigned 2024-11-02.

For episode 15.174, Zak's Cash Builder and Low and Middle offers are correctly £0; the chosen offer is labelled Low by convention. This does not affect ratings.

## Recommended settings

The published summary uses **target difficulty 0.55, annual drift 0.10, team effect 0, starting probability 0.70, starting uncertainty 1.0, reference target 18 and 95% intervals**. Weekly updates keep these settings fixed, so a changing ranking reflects new or corrected data rather than automatic retuning.

The original comparison used 885 episodes from 2018–2023 to compare 105 parameter combinations, with pre-2018 data providing history. A tiny improvement from an added team-size effect did not justify the extra assumption, so the recommendation retained zero. Among zero-team-effect candidates, these settings gave the best earlier-period log loss.

On the original 331 later episodes from 2024 through 20 November 2026, the recommended model's Brier score was 0.1228, compared with 0.1306 for the app's original defaults. A no-drift version was very close and slightly better at 0.1226. These are dated research results, not a claim that the model has been independently revalidated every week. Later-period scores were inspected during the exploratory work; this was retrospective validation, not a preregistered experiment.

## How the ratings change with the assumptions

The following table is recalculated with each data refresh. Each row changes one setting while retaining the rest of the recommendation. Values are rating percentages.

| Setting | Hegerty | Sinha | Ryan | Labbett | Ennis | Wallace |
| --- | --- | --- | --- | --- | --- | --- |
| Recommended | 75.8 | 73.7 | 73.7 | 72.1 | 57.2 | 44.4 |
| No drift | 77.2 | 75.0 | 72.4 | 75.7 | 58.0 | 47.5 |
| Faster change | 75.4 | 71.6 | 74.7 | 70.3 | 55.4 | 45.4 |
| Very fast change | 75.3 | 67.0 | 75.0 | 69.0 | 52.2 | 51.0 |
| Weaker target effect | 75.6 | 75.1 | 74.9 | 71.3 | 65.3 | 60.0 |
| Stronger target effect | 76.6 | 74.1 | 74.0 | 73.1 | 55.4 | 40.3 |
| Team effect 0.2 | 78.6 | 76.8 | 77.1 | 75.5 | 61.0 | 47.7 |

No drift: Hegerty, Labbett, Sinha, Ryan, Ennis, Wallace. Faster change: Hegerty, Ryan, Sinha, Labbett, Ennis, Wallace. Weaker target effect: Hegerty, Sinha, Ryan, Labbett, Ennis, Wallace.

**Rate of change:** zero drift preserves more of the career record. Higher drift makes the estimate more responsive to recent surprises and usually increases uncertainty about current ability. It is not a fixed rolling window.

**Target difficulty:** a stronger adjustment gives less credit for winning against a low target and is more forgiving of defeats against high targets. It can therefore change both the gaps and the order when Chasers have faced different target distributions.

**Team size:** a positive extra-finalist effect makes a given target harder to beat when more finalists are present. Target already reflects a head start and contestants' answers, so separating these effects is difficult. The recommended effect remains zero.

**Starting assumptions and history:** a shorter record leaves more influence from the prior. Restricting the range with earlier history retained merely changes the display; turning history off deliberately starts the model again. These answer different questions. Changing the minimum episode count or interval coverage affects visibility or band width, not the central fitted estimates. Changing the reference target changes the meaning of the percentage; holding the prior probability fixed also changes the prior assumption.

## Reading the results responsibly

The exact ranking is less certain than the numerical order suggests. Overlapping ranges and changes under plausible settings are reasons to avoid declaring close positions decisive. Questions, casting, pushback ability and production eras can matter in ways this model does not capture. The target also depends on contestants surviving earlier rounds, so this is not a causal estimate of intrinsic Chaser ability.

:::sidebar
## Technical sidebar

The win probability is logistic(theta − beta × (Target − reference) − gamma × (FinalistsAdjusted − 2)). FinalistsAdjusted is at least one for a Lazarus game. Theta begins Normal(logit(0.70), 1²), and its variance grows by drift² × elapsed air-date years between observations. The mean does not automatically decay.

A 401-point grid over ±8 prior standard deviations integrates the Bernoulli likelihood; posterior mean and variance define the Gaussian approximation passed to the next date. Same-day games for a Chaser are combined. Historical estimates are filtered, not smoothed using later results, although the recommended parameters were selected retrospectively.

Rating = 100 × logistic(posterior latent mean). The SE column is the posterior standard deviation of 100 × logistic(theta), numerically integrated under the propagated Gaussian posterior. It is labelled SE for readability, but is a Bayesian uncertainty measure, not a frequentist sampling standard error. The 95% endpoints transform the latent mean ±1.96 SD. They need not equal rating ±1.96 SE because the transformation is nonlinear.

Uncertainty excludes parameter selection, model misspecification and errors in the data. The bands are pointwise rather than simultaneous, and do not give direct probabilities of rank differences. Change is a descriptive difference between successive post-update estimates, not a significance test.

The original grid compared beta in {0.15, 0.25, 0.35, 0.45, 0.55, 0.65, 0.80}, drift in {0, 0.10, 0.20, 0.40, 0.60}, and gamma in {−0.20, 0, 0.20}. The grid was expanded when its first best target coefficient hit the boundary. Simplicity was an analyst judgement: the unrestricted earlier-period best log loss was 0.385663, versus 0.386162 for the selected zero-team-effect model.

Predictive Brier score is mean squared probability error; log loss penalises confident mistakes. The explorer computes both before each observation updates the model, integrating over ability uncertainty. They are not proof of interval calibration. Repeatedly tuning on the same evaluation period overfits.

Background: Leonhard Knorr-Held, [Dynamic Rating of Sports Teams](https://epub.ub.uni-muenchen.de/1490/1/paper_98.pdf), revised 1999. This is a simpler custom implementation, not a reproduction of that paper.
:::end

## Interactive ratings explorer

Use the controls below to reproduce the published settings or explore alternatives. The downloadable HTML contains the data and calculations and works without an R server.

:::explorer
