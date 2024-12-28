# Incorrect use of AVG aggregate function in SQL query
This SQL query attempts to find employees in the Sales department with salaries above the average salary. However, the query is incorrect because the AVG(salary) function is used incorrectly.  The AVG() function needs to be used with a subquery to correctly calculate the average salary across the entire table, not just the filtered sales department.  This leads to an incorrect result.

## Bug
The primary issue lies in directly using `AVG(salary)` in the `WHERE` clause, which causes an error or produces an unexpected result.  The `AVG` function operates on the entire dataset selected, which may not be what's intended in the `WHERE` clause.