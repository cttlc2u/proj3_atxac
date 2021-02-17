# Part 3: Soccer Data

*Introductory - Intermediate level SQL*

---

## Setup

Download the [SQLite database](https://www.kaggle.com/hugomathien/soccer/download). *Note: You may be asked to log in, or "continue and download".* Unpack the ZIP file into your working directory (i.e., wherever you'd like to complete this challenge set). There should be a *database.sqlite* file.

As with Part II, you can check the schema:

```python
import pandas as pd
import sqlite3

conn = sqlite3.connect('database.sqlite')

query = "SELECT * FROM sqlite_master"

df_schema = pd.read_sql_query(query, conn)

df_schema.tbl_name.unique()
```

---

Please complete this exercise using sqlite3 (the soccer data, above) and your Jupyter notebook.

1. Which team scored the most points when playing at home?
Team 8633 scored the most points when playing at home.

2. Did this team also score the most points when playing away?
No, Team 8634 outscored them for most point when playing away.

3. How many matches resulted in a tie?
6596 games resulted in a tie.

4. How many players have Smith for their last name? How many have 'smith' anywhere in their name?
18 players have Smith for their last name, and it's still 18 when searching anywhere in their name.

5. What was the median tie score? Use the value determined in the previous question for the number of tie games. *Hint:* PostgreSQL does not have a median function. Instead, think about the steps required to calculate a median and use the [`WITH`](https://www.postgresql.org/docs/8.4/static/queries-with.html) command to store stepwise results as a table and then operate on these results. 
The median tie score was 1-1.

6. What percentage of players prefer their left or right foot? *Hint:* Calculate either the right or left foot, whichever is easier based on how you setup the problem.
24% of players prefer their left foot.
