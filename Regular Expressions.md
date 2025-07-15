---
tags:
  - COMP206
---
# Regular Expressions(Regex)
### Meta-characters
- These characters have special meanings in regex:
- `.`:: Matches **any** single character except newline.
<!--SR:!2024-12-17,15,130-->
- `^`:: Anchors the match at the **start** of the string.
<!--SR:!2024-12-24,57,250-->
- `$`:: Anchors the match at the **end** of the string.
<!--SR:!2025-01-29,83,270-->
- `*`:: Matches **0 or more** of the preceding element.
<!--SR:!2024-12-26,59,250-->
- `+`:: Matches **1 or more** of the preceding element.
<!--SR:!2024-12-29,61,270-->
- `?`:: Matches **0 or 1** of the preceding element (makes it optional).
<!--SR:!2025-01-23,66,230-->

### Character Classes
- Define a set of characters to match with::in square brackets (`[]`):
<!--SR:!2024-12-12,45,230-->
`[abc]`    # Matches:: 'a', 'b', or 'c'
<!--SR:!2024-12-23,57,250-->
`[^abc]`   # Matches:: any character except 'a', 'b', or 'c'
<!--SR:!2025-03-14,104,250-->
`[0-9]`    # Matches:: any digit (same as \d)
<!--SR:!2025-02-01,93,290-->
`[a-zA-Z]` # Matches:: any letter, both uppercase and lowercase
<!--SR:!2025-01-09,69,270-->

### Predefined Character Classes
- These shortcuts represent common groups of characters:
- `\d`: Matches:: any digit (equivalent to `[0-9]`).
<!--SR:!2025-03-27,124,290-->
- `\D`: Matches:: any **non-digit**.
<!--SR:!2024-12-26,58,250-->
- `\w`: Matches:: any word character (letters, digits, and underscores).
<!--SR:!2024-12-16,52,250-->
- `\W`: Matches:: any **non-word** character.
<!--SR:!2024-12-12,49,250-->
- `\s`: Matches:: any whitespace character (spaces, tabs, newlines).
<!--SR:!2025-02-25,86,230-->
- `\S`: Matches:: any **non-whitespace** character.
<!--SR:!2025-01-23,70,230-->

### Quantifiers
- Specify the number of times a pattern should occur:

a{3}     # Matches:: exactly 3 'a's
<!--SR:!2024-12-19,54,250-->
a{2,4}   # Matches:: between 2 and 4 'a's
<!--SR:!2025-03-11,102,250-->
a{2,}    # Matches:: 2 or more 'a's
<!--SR:!2025-03-25,111,250-->
a*       # Matches 0 or more 'a's (same as a{0,})
a+       # Matches 1 or more 'a's (same as a{1,})
a?       # Matches 0 or 1 'a' (same as a{0,1})


### Anchors
- Use these to match specific positions in the string:
- `^`: Start of the string.
- `$`: End of the string.
```regex
^abc     # Matches 'abc' at the start of a string
abc$     # Matches 'abc' at the end of a string
```

### Groups and Capturing
- Use parentheses `()` to:: group patterns or to capture matched text:
<!--SR:!2024-12-08,47,250-->
```regex
(abc)    # Captures:: the sequence 'abc'
(a|b)    # Matches:: either 'a' or 'b'
```

### Escaping Special Characters
- Use a backslash (`\`) to escape meta-characters:
```regex
\.       # Matches a literal period '.'
\*       # Matches a literal asterisk '*'
```

### Lookahead and Lookbehind
- **Lookahead**: Matches a group **only if** it is followed by a certain pattern:
```regex
a(?=b)   # Matches 'a' only if it's followed by 'b'
```
- **Lookbehind**: Matches a group **only if** it is preceded by a certain pattern:
```regex
(?<=b)a  # Matches 'a' only if it's preceded by 'b'
```

### Non-Capturing Groups
- Use `(?:...)` to group expressions without capturing the match:
```regex
(?:abc)  # Groups 'abc' but does not capture it
```

### Tips
- Always use `\` to escape characters like `.`, `*`, `?`, etc., if you want to match them literally.
- Combine character classes and quantifiers for more complex patterns:
```regex
\d{3}-\d{2}-\d{4}  # Matches a social security number-like format (123-45-6789)
```