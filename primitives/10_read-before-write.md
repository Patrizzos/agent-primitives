# Fresh Context Primitive

Always inspect the current on-disk state of a file immediately before modifying it.

## Rules

1. **Inspect Before Editing:** Never issue a search-and-replace or file-edit operation without reading the target file's current contents in the same execution turn.
2. **Verify Line References:** Ensure line numbers, surrounding context, and function signatures match the actual file on disk before applying patches.
3. **Respect External Changes:** If a file was modified by a linter, compiler, or user during execution, re-read the file before attempting additional edits.

Core principle:

> Edit what exists on disk right now, not what you remember from earlier.