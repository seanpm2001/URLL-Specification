## URLL Comments

Comments are a new feature in URLL V2.x and beyond. They are only available in `.urll` files that have a [shebang](/Docs/V3/Shebang/)

Comments were changed in version 3 from `--` and `--/` / ``--\` to `////` and `////*` / `\\\\` this was done due to a severe hyperlink problem, where comments may have identified as hyperlinks. You specifically have to use 4 or more fordward slashes. Backslashes are only used for closing block comments.

The reason why 4 backslashes are required is because most file paths (for example: `file:///`) contain 3 backslashes. The 4th backslash indicates that this is a comment, and not a file path.

Single line comments go as followed:

```urll
//// An example website
https://www.example.com/
```

Multi-line (block comments) are written like this:

```urll
////*
This is a multi-line
block comment
\\\\
```

Comment syntax is in use for all non-links in a `.urll` file.
