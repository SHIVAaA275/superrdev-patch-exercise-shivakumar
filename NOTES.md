# Patch Notes

## Summary
- Fixed the status filter SQL condition in `TaskRepository`.
- Fixed frontend loading/error handling in `useTasks`.
- Reset pagination when search or status changes.
- Removed the artificial `Thread.sleep()` delay from `TaskController`.

## Not Changed
- Did not change the Oracle SQL reference file because the application uses H2 locally and the actual repository query was fixed.
- Did not make larger refactors to keep the patch focused.

## Biggest Remaining Risk
- Pagination currently loads all matching tasks before selecting the requested page, which may not scale well for a large dataset.

## Tools / AI
- Used VS Code, PowerShell, Git, browser/API testing, and AI assistance for debugging and understanding the changes.
- Tested the fixes locally after making the changes.