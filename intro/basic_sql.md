**ORDER BY**
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

**NOTE**: `ORDER BY` also works on text, not only `int` so it can be applied to columns that contain text.

