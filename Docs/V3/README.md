
---

# URLL V3.0

I came up with the new specification for URLL Version 3 in the past month. It was debated, but ultimately decided in favor of its creation.

Version 3 implements an important critical fix to the format, but breaks backwards compatibility. URLL v2 is not compatible with URLL v3, but URLL v1 is compatible with URLL v3

| Version | Compatibility with V1 | Compatibility with V2 | Compatibility with V3 |
|---|---|---|---|
| V1 | ✅️ | ✅️ | ✅️ |
| V2 | ✅️ | ✅️ | ❎️ |
| V3 | ✅️ | ❎️ | ✅️ |


Version 2 and onward require the use of a [shebang](/Docs/V2/Shebang/), which was also introduced in version 2. Some of the new features include:

However, version 3 requires [a new shebang](/Docs/V3/Shebang/) as part of the new comment format.

URLL isn't a complex format, so changes won't be too complex. All features from version 2 are changed in version 3. An additional component, known as `ROOTFILES.base` is also included. The official implementation also now supports various file protocols.

[`New shebang`](/Docs/V3/Shebang/)

[`trusted revision count support`](/Docs/V3/Revision-Control/)

[`Single and multi-line comments`](/Docs/V3/Comments/)

[`Shortcut paths`](/Docs/V3/Shortcut-Path/)

[`ROOTFILES.base`](/Docs/V3/ROOTFILES/)

The documents can be viewed separately through the above links. The documentation is also copied below for if you want to keep reading here.

---

## URLL Shebang

Shebangs are a new feature in URLL V2.x and beyond. They are required for certain features, including:

- [x] Anything that isn't a link, which includes
- - [x] Shortcut path
- - [x] Revision count
- - [x] Comments

A version 3 shebang looks like this:

```urll
////urll-version=3;
```

Additionally, you may want to credit the project, you can do so like this:

```urll
////urll-version=3;
//// https://github.com/seanpm2001/URLL-Specification/
```

Or like this:


```urll
////urll-version=3;
//// https://github.com/seanpm2001/URLL/
```

A version 2 shebang looks like this:

```urll
--URLL-version=2;
```

Like other shebangs, it goes at the top of the file. It must be on either line 1 or 2. The version 2 shebang is not compatible with version 3.

## URLL Shortcut path

Shortcut paths are a new feature in URLL V2.x and beyond. They are only available in `.urll` files that have a [shebang](/Docs/V2/Shebang/)

A version 3 shortcut path looks like this:

```urll
////URLL:"///home/<username>/Desktop/MyList1.urll";
```

For repositories, or linking from the root of a directory system, it can be written like this:

```urll
////URLL:"/<FolderName>/MyList1.urll";
```

It is an extra feature.

## URLL Trusted Revision path

Trusted revisions are a new feature in URLL V2.x and beyond. They are only available in `.urll` files that have a [shebang](/Docs/V2/Shebang/)

The term `trusted` is used, as anyone can write any version number they want to it. It is up to the users to decide whether the revision count is correct, and also to show copies of past revisions.

A revision counter looks like this:

```urll
////Revision: 1;
```

The number 0, along with negative numbers are not allowed in the revision counter. However, labeling with letters is fine:

```urll
////Revision: 2A;
```

There can only be 1 revision line per file. It is an extra feature.

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

## ROOTFILES.base

`ROOTFILES.base` is a generated file that contains an index of all of the links to files in the root of a folder. It is an extra vanity feature, and is not required.

---


**Article version:** `1 (2023, Thursday, January 12th at 2:50 pm PST)`

---

<!-- 
()
!-->
