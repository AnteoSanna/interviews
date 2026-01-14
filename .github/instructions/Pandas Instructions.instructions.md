---
applyTo: '**'
---
Provide project context and coding guidelines that AI should follow when generating code, answering questions, or reviewing changes.

When working with Pandas in this project, please adhere to the following guidelines:

- When importing Pandas, always use the alias `pd`:
  ```python
  import pandas as pd
  ```
- Use vectorized operations and built-in Pandas functions for data manipulation instead of iterating over DataFrame rows with loops.

- Prefer using method chaining for readability when performing multiple operations on a DataFrame. For example:
  ```python
  df = (df
        .dropna()
        .assign(new_col=lambda x: x['existing_col'] * 2)
        .sort_values(by='new_col'))
  ```

- commment your code to explain complex operations, especially when performing data transformation or aggregations. 
- When merging or joining DataFrames, explicitly specify the type of join (e.g., inner, outer, left, right) to avoid ambiguity.