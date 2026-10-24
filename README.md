# What wins a Premier League season? (2007-08)

Match-level analysis of all 380 games of the 2007-08 Premier League season, in Python (pandas, statsmodels, SciPy, matplotlib).

## Key findings
| Question | Result |
|---|---|
| Is home advantage real? | Yes. Home teams scored 0.42 more goals per game (paired t-test p < 0.001) and won 46% of matches vs 27% for away teams. |
| Accuracy or volume? | Volume. Shot accuracy was flat (~54%) across the table, but the top four landed ~65% more shots on target per game than the relegated sides. |
| One metric for the table? | Shots-on-target difference per game explains 77% of the variation in final points (OLS, HC3 SEs, n = 20): +1 per game ≈ +7.8 points. |

The league table is rebuilt from raw results and validated against the official final standings.

## Reproduce
1. Open `PL_2007_08_Analysis.ipynb` in Google Colab.
2. Upload `2007-08.csv` (source: [football-data.co.uk](https://www.football-data.co.uk/englandm.php)).
3. Runtime → Run all.

## Limitations
One season; team-level regression on 20 observations is descriptive, not causal; shots on target ignore shot location (xG). Next: multi-season panel and a match-level Poisson goals model.
