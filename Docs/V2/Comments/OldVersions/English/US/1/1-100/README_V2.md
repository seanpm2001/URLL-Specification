
---

# URLL Comments

Comments are a new feature in URLL V2.x and beyond. They are only available in `.urll` files that have a [shebang](/Docs/V2/Shebang/)

Single line comments go as followed:

```urll
-- An example website
https://www.example.com/
```

Multi-line (block comments) are written like this:

```urll
--\
This is a multi-line
block comment
--/
```

Comment syntax is in use for all non-links in a `.urll` file.

## Usage notes and rationale

I used `--` as the comment format, as I couldn't use `//` `#` or `?` due to its use in file URL schemes, and I felt like this one worked best. The multi-line comment is an original spin on it, making it into a fat arrow shape for block comments. After some thinking, I decided that for safety, comments have to be at the start of a line, and not after a URL, as doing this may cause issues, such as filenames like this: `https://www.example.com/website/index.html#My--section`

---

**Article version:** `2 (2022, Friday, January 21st at 10:07 pm)`

---
