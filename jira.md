Jira Cheat Sheet
================

## Find by Mentions of current user within the past 7 days

```sql
comment ~ currentUser() AND updatedDate >= -7d
```
