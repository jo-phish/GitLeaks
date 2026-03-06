Changes made
•	Added MAX_VISIBLE_LINES and a helper createTruncatedPre(text) to render pre blocks truncated to 10 lines.
•	Replaced direct pre creation for Secret and Line with the truncated pre (with a "Show more"/"Show less" toggle when content exceeds 10 lines).
Reasoning
•	Keeps long multiline secrets/lines readable in the table while allowing the user to expand when needed. Inline styles are used so no external CSS edits are required.
