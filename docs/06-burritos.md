# Case 6 — San Diego Burrito Ratings

**Dataset:** 237 rows · crowd-sourced burrito reviews
**Sheets:** `Burrito Pivot` · `Burrito Pivot 2`

## Q1. Compare average ratings for Tortilla, Temp, Fillings, Synergy and Wrap Quality by location.

![Q1](img/06-burritos/q1.png)

## Q2. Applying a value filter for more than 2 ratings, how many locations qualify?

19 locations. The source data contains case variants of the same restaurant, such as "Taco Stand" and "Taco stand", and three spellings of "Lolita's Taco Shop". PivotTables match text without regard to case and merge them, so a case-sensitive tool returns 21 groups from the same data.

![Q2](img/06-burritos/q2.png)

## Q3. Create a calculated field that correctly averages the five scores by location.

`Average Total Score = ((Tortilla + Temp + Fillings + Synergy + Wrap Quality) / 5) / # Reviews`

The division by `# Reviews` is what keeps the average correct once rows are aggregated, since Excel evaluates the field against the sum of each source field.

![Q3](img/06-burritos/q3.png)

## Q4. Showing Average Total Score as a Rank, which location with more than 2 reviews ranks #7?

Rigoberto's Taco Shop, with 3.85.

![Q4](img/06-burritos/q4.png)

## Q5. Adding a color scale and sorting descending, which location has the lowest score? And the highest?

The lowest is Goody's with 1.97 and the highest is Los Tacos with 4.08. Goody's is an outlier, more than a full point below the next location.

![Q5](img/06-burritos/q5.png)

## Q6. How closely does Average Total Score align with Yelp Rating?

The two fields follow a similar direction, but not closely. The correlation is 0.59. The clearest mismatch is Goody's, with 1.97 on the component scores against 3.5 on Yelp.

![Q6](img/06-burritos/q6.png)

---

[← All cases](../README.md)
