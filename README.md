# Elevate_Labs_Task4
Aggregation, Grouping

Interview Questions: 1.What is GROUP BY?
 `GROUP BY` collects rows that share the same value(s) into **groups** so you can apply aggregate functions (like COUNT or SUM) to each       group separately.  
  Example: `SELECT Department, COUNT(*) FROM Employees GROUP BY Department;`

2. Difference between WHERE and HAVING?
   * `WHERE` filters **rows before grouping**.  
   * `HAVING` filters **groups after aggregation**.  
   Example: `HAVING COUNT(*) > 5` keeps only groups with more than five rows.

3. How does COUNT(*) differ from COUNT(column)?
   * `COUNT(*)` counts **all rows**, including those with NULLs.  
   * `COUNT(column)` counts only rows where that column is **not NULL**.

4. Can you group by multiple columns 
   Yes. Provide a comma-separated list and SQL forms groups based on the **unique combination** of those column values.  
   Example: `GROUP BY Department, JobTitle`.

5. What is ROUND() used for
   `ROUND()` returns a number rounded to a specified number of decimal places.  
   Example: `ROUND(Salary, 2)` rounds salary to two decimals.

6. How do you find the highest salary by department  
   Group by department and use an aggregate like MAX:  
   ```sql
   SELECT Department, MAX(Salary) AS HighestSalary
   FROM Employees
   GROUP BY Department;
   
7. What is the default behavior of GROUP BY
  SQL automatically sorts groups by the grouped columns in ascending order unless you add your own ORDER BY clause.

8. Explain AVG and SUM
  AVG(column) calculates the mean (average) of non-NULL values.
  SUM(column) adds up all non-NULL values.

9.How to count distinct values
  Use COUNT(DISTINCT column) to count the number of unique non-NULL entries.
  Example: SELECT COUNT(DISTINCT Department) FROM Employees;

10. What is an aggregate function
  A function that operates on a set of rows and returns a single value per group or result set.
  Common examples: COUNT, SUM, AVG, MIN, MAX.
