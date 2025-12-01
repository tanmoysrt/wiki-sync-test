---
route: atabase-analyzer
allow_guest: 1
published: 1
---

This tool can help you analyze storage usage of your database and find performance issues in the database as well.

## How to access the tool ?
Visit frappecloud.com/dashboard and check the sidebar. From Sidebar > Dev Tools > DB Analyzer, you can acccess the tool.

Or, you can simply visit - https://frappecloud.com/dashboard/database-analyzer

![](/files/Screenshot%20from%202025-05-30%2018-06-52.png)

## Storage Breakdown

If you want to check disk usage by every table in your database, you can click on the `Storage Bar`

![](/files/shapes%20at%2025-05-30%2018.41.11.png)

You can then view usage by each table

![](/files/Screenshot%20from%202025-05-30%2018-07-06.png)

## Database Processes

If you want to view all the active database queries, you can view them from the same page and even kill the query if it's stuck.

![](/files/Screenshot%20from%202025-05-30%2018-08-50.png)

## Slow Queries

Slow queries usually affect the performance of your site. You can find all the information about slow queries.

![](/files/Screenshot%20from%202025-05-30%2018-09-10.png)

## Time Consuming Queries

Sometimes there are queries that execute very fast but run very frequently and, in total, consume a lot of your database's CPU time.

These queries don't always affect database performance, but the results can help you further optimize your code.

![](/files/Screenshot%20from%202025-05-30%2018-09-20.png)

## Full Table Scan Queries

If queries lack indexing or have issues, they can cause full table scans, which hurt your database performance the most.

You can find these kinds of queries and optimize them for better performance.

![](/files/Screenshot%20from%202025-05-30%2018-09-27.png)


## Index Analysis

Other than that, you can click on `Suggest Indexes`, and the system will try to analyze slow queries and provide suggestions based on that.


![](/files/Screenshot%20from%202025-05-30%2018-09-49.png)