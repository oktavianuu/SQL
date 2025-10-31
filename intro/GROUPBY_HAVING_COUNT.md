#### GROUP BY, HAVING AND COUNT
`GROUP BY` takes the name of one or more columns, and treats all rows with the same value in that column as a single group when we apply aggregate functions like `COUNT()`. `HAVING` is used in combination with `GROUP BY` to ignore groups that don't meet certain criteria.

**Example: Which Hacker News comments generated the most discussion?¶**
The Hacker News dataset contains information on stories and comments from the Hacker News social networking site.
We'll work with the full table and begin by printing the first few rows.

```python
from google.cloud import bigquery

# Create a "Client" object
client = bigquery.Client()

# Construct a reference to the "hacker_news" dataset
dataset_ref = client.dataset("hacker_news", project="bigquery-public-data")

# API request - fetch the dataset
dataset = client.get_dataset(dataset_ref)

# Construct a reference to the "full" table
table_ref = dataset_ref.table("full")

# API request - fetch the table
table = client.get_table(table_ref)

# Preview the first five lines of the table
client.list_rows(table, max_results=5).to_dataframe()
```

