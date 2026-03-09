Changes made
•	Added MAX_VISIBLE_LINES and a helper createTruncatedPre(text) to render pre blocks truncated to 10 lines.
•	Replaced direct pre creation for Secret and Line with the truncated pre (with a "Show more"/"Show less" toggle when content exceeds 10 lines).
Reasoning
•	Keeps long multiline secrets/lines readable in the table while allowing the user to expand when needed. Inline styles are used so no external CSS edits are required.

0.1.1
Changes made
Summary of changes
•	Added optional DOM hook lineFilter (use an <input id="lineFilter"> in your HTML) and event handling.
•	Implemented getFilteredItems() and applyFilterAndRender() to filter items by a JavaScript regular expression applied to the extracted Line value.
•	handleFiles now triggers filtered rendering so uploads respect the current filter.
•	Invalid regex patterns display an error message but do not crash; they fall back to showing all items.
Usage
•	Add an input element in the page, for example: <input id="lineFilter" placeholder="Filter Line by regex" />
•	Type any JavaScript regular expression (without delimiters), e.g. password|secret or ^\s*const\s+TOKEN to filter shown rows by the Line field.

