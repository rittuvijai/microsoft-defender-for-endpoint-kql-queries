# Contributing

Thanks for considering a contribution to this Microsoft Defender for Endpoint Advanced Hunting KQL query library.

## Adding a new query

1. Pick the closest matching category folder under `advanced-hunting/` (or propose a new one if none fit).
2. Name the file in `kebab-case.kql`, describing what it does (e.g. `high-severity-cve-analysis.kql`).
3. Add a header comment block at the top of the file:
   ```
   // Title: <short, descriptive title>
   // Category: <category name>
   // Description: <1-3 sentences on what the query returns and why it's useful>
   // Table(s): <Advanced Hunting tables used>
   // Data connector: Microsoft Defender for Endpoint (Advanced Hunting)
   ```
4. Add a row for your query to that category's `README.md` table.
5. Test the query in the Microsoft Defender XDR **Advanced Hunting** editor before submitting.

## Style

- Use explicit `project` / `project-rename` for output columns where possible — it makes results self-documenting.
- Prefer `arg_max(Timestamp, *)` for "latest record per device" patterns.
- Comment out debug/testing lines rather than deleting them if they're useful toggles (see existing queries for examples).

## Reporting issues

If a query throws an error or returns unexpected results in your tenant, open an issue with your Defender for Endpoint plan (P1/P2) and the error message.
