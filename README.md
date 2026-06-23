# Netflix Content Analysis

An EDA project I did to practice pandas and matplotlib on a real dataset. I use Netflix a lot so I figured this would be more interesting than working on some generic sales CSV.

The main questions I tried to answer:
- Is Netflix mostly movies or TV shows (and has that ratio changed)?
- Which countries produce the most content?
- What genres dominate, and is "International" really just a workaround category?

---

## What I found

- **70% of Netflix is movies** — way higher than I expected just from browsing the app
- **US is #1 by a huge margin** (~37%), India is a distant #2 which surprised me — I expected UK
- **Content peaked in 2021** then dropped off, which lines up with Netflix's subscriber slowdown
- **South Korea has the highest TV-to-movie ratio** of any major country — K-dramas really do dominate their output
- **"International TV Shows" is the most common TV category**, which is more of a language tag than an actual genre. I think that says something about how Netflix thinks about its non-English audience

---

## Files

```
netflix-content-analysis/
├── notebooks/
│   └── netflix_analysis.ipynb   ← main analysis, start here
├── data/
│   └── netflix_titles.csv       ← dataset (~8,800 titles)
├── dashboard/
│   └── netflix_dashboard.html   ← visual summary you can open in browser
└── requirements.txt
```

---

## How to run it

```bash
git clone https://github.com/pranay-2310/netflix-content-analysis
cd netflix-content-analysis
pip install -r requirements.txt
jupyter notebook notebooks/netflix_analysis.ipynb
```

The dashboard is just a static HTML file — open it in your browser, no server needed.

---

## Tools used

- Python 3.10
- pandas, numpy
- matplotlib, seaborn
- Jupyter Notebook

---

## Limitations / things I'd do differently

The `listed_in` column has multiple genres per title separated by commas and I just took the first one — a proper analysis should explode that column. Same with `country`. I noted this in the notebook. Also the dataset has a cutoff date so it's missing newer titles.

---

## What's next

I want to extend this into a recommendation mini-project — given a movie you liked, suggest similar ones based on genre + country + rating. That'll probably be a separate repo.

---

Pranay Beemanapalli — MS Data Science  
[LinkedIn](https://linkedin.com/in/pranaybeemanapalli) · [GitHub](https://github.com/pranaybeemanapalli)
