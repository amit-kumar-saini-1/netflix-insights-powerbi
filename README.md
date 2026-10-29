# Netflix Insights: Power BI Dashboard

An interactive Power BI dashboard analysing Netflix movies and shows, covering
IMDb ratings, votes, runtime and release trends.

![Netflix Insights Dashboard](images/dashboard.png)

## Objective
Understand how Netflix content has changed over time and which factors, such as
type, age certification and release year, relate to audience ratings and engagement.

## Business Questions
- How have average IMDb scores changed over the years?
- Which age certifications receive the highest ratings?
- How do movies and shows compare in audience votes?
- Which movies have the most votes?
- How has the number of titles released changed over time?

## Key Insights
- Average IMDb score is **6.53** across **5,235** titles.
- Scores have declined from about **7.0 in the early 2000s to about 6.3** in recent years.
- **TV-14** and **TV-MA** titles have the highest average ratings (7.3 and 7.1).
- Movies account for about **60%** of average votes, shows about **40%**.
- Title volume grew sharply after 2010. [Note: the last year is partial]
- Most-voted titles include Inception, Forrest Gump and Django Unchained.

## Dataset
- **Size:** 5,235 titles
- **Key columns:** title, type, release year, age certification, runtime,
  IMDb score, IMDb votes

## Process
1. **Data cleaning (Power Query):** [handled nulls, fixed data types, removed duplicates]
2. **Modelling and DAX:** created measures for [average score, total titles, votes]
3. **Visualisation:** built 6 charts plus KPI cards, with slicers for Release Year and Movies vs Shows

## DAX Measures
```DAX
Avg IMDb Score = AVERAGE(Titles[imdb_score])
Total Titles = COUNTROWS(Titles)
```
[Replace with your actual measures]

## Dashboard Visuals
| Visual | Purpose |
|---|---|
| KPI cards | Total titles and average IMDb score |
| Bar chart | Average score by age certification |
| Donut chart | Average votes by type |
| Area chart | Average score by year |
| Line chart | Number of titles by year |
| Treemap | Top 5 movies by votes |
| Funnel | Average runtime by movie |

## Tools Used
Power BI Desktop, Power Query, DAX

## How to Use
1. Download `Netflix_Insights.pbix`
2. Open it in Power BI Desktop
3. Use the slicers to filter by release year and type

## Author
**Amitkumar Saini**
