
---

# URLL V2.0

I came up with the new specification for URLL Version 2 today, as a part of making the format more useful, and easier to read. It is backwards and forwards compatible with all versions of the URLL file specification.

Version 2 and onward require the use of a [shebang](/Docs/V2/Shebang/), which was also introduced in version 2. Some of the new features include:

[shebang/hashpling support](/Docs/V2/Shebang/)

[trusted revision count support](/Docs/V2/Revision-Control/)

[Single and multi-line comments](/Docs/V2/Comments/)

[Shortcut paths](/Docs/V2/Shortcut-Path/)

The documents can be viewed separately through the above links. The documentation is also copied below for if you want to keep reading here.

---

## URLL Shebang

Shebangs are a new feature in URLL V2.x and beyond. They are required for certain features, including:

- [x] Anything that isn't a link, which includes

- - [x] Shortcut path

- - [x] Revision count

- - [x] Comments

A version 2 shebang looks like this:

```urll
--URLL-version=2;
```

Like other shebangs, it goes at the top of the file. It must be on either line 1 or 2.

## URLL Shortcut path

Shortcut paths are a new feature in URLL V2.x and beyond. They are only available in `.urll` files that have a [shebang](/Docs/V2/Shebang/)

A version 2 shortcut path looks like this:

```urll
--URLL:"///home/<username>/Desktop/MyList1.urll";
```

For repositories, or linking from the root of a directory system, it can be written like this:

```urll
--URLL:"/<FolderName>/MyList1.urll";
```

It is an extra feature.

## URLL Trusted Revision path

Trusted revisions are a new feature in URLL V2.x and beyond. They are only available in `.urll` files that have a [shebang](/Docs/V2/Shebang/)

The term `trusted` is used, as anyone can write any version number they want to it. It is up to the users to decide whether the revision count is correct, and also to show copies of past revisions.

A revision counter looks like this:

```urll
--Revision: 1;
```

The number 0, along with negative numbers are not allowed in the revision counter. However, labeling with letters is fine:

```urll
--Revision: 2A;
```

There can only be 1 revision line per file. It is an extra feature.

## URLL Comments

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

---

**Article version:** `1 (2022, Friday, January 21st at 7:37 pm)`

---

<!-- 
()
!-->
