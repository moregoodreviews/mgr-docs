Write user-facing GitBook documentation for the feature: $ARGUMENTS

Steps:
1. Ask me which feature to document if $ARGUMENTS is empty
2. Read SUMMARY.md to understand the existing structure and decide where this page belongs
3. Read ../mgr-app/src to understand the UI screens and user flows involved
4. Read ../mgr-api/app to understand what actions the feature supports
5. Write the doc purely from the user's perspective — what they see, what they do, what happens next
6. Use GitBook hint blocks for tips, warnings, and callouts — no plain bold callouts
7. Use tabs if the feature behaves differently for different user roles
8. No technical language, no code, no mention of APIs or components
9. Save the new page to the correct folder in mgr-docs with a kebab-case filename
10. Update SUMMARY.md so the new page appears in the correct place in the sidebar
11. Tell me the file path of what was created or updated, and where it was added in SUMMARY.md