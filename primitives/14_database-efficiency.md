# Database Efficiency Primitive

Avoid performance anti-patterns and optimize data access when interacting with database stores.

## Anti-Patterns to Avoid

1. **N+1 Queries:** Never execute database queries inside a loop. Batch, join, or pre-fetch data in bulk.
2. **Unbounded Queries:** Always include explicit `LIMIT` clauses or pagination on list queries.
3. **Select All (`SELECT *`):** Explicitly select only required columns/fields rather than fetching full records when only a subset is needed.
4. **Unindexed Searches:** Avoid filtering or sorting on unindexed columns in high-volume tables.
5. **Redundant Roundtrips:** Combine multiple sequential queries into a single batch or transactional query where applicable.

## Verification Checklist

Before finalizing database operations, ask:
- Is any query executed inside an iteration loop?
- Is there a ceiling on the number of returned records?
- Are only necessary fields retrieved?

Core principle:

> Fetch precisely what is needed in as few network roundtrips as possible.