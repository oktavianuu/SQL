### ORDER BY
- `ORDER BY` clause used to change the order of our result, we usually put it on the last of our query. 
Example:
```sql
query = """
        SELECT ID, Name, Animal
        FROM `project_name.dataset_name`
        ORDER BY ID 
        """
```
output:
|ID|Name|Animal
|---|---|---|
|1|Harris|Rabbit|
|2|Moon|Dog|
|3|Ripley|Cat|
|4|Tom|Cat|

**NOTE**: `ORDER BY` also works on text, not only `int` so it can be applied to columns that contain text. By default, `ORDER BY` will return the result ascendingly but we can reverse it by `DESC` argument as follow:
```sql
ORDER BY column_name DESC
```

#### DATES
Dates come up very frequently in real world databases. They are stored in two ways; `DATE` or `DATETIME`.
The DATE format has the year first, then the month, and then the day. It looks like this:
`YYYY-[M]M-[D]D`
The `DATETIME` format is similar but with time added at the end. 
