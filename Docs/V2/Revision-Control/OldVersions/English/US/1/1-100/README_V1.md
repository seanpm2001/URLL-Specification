
---

# URLL Trusted Revision path

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

---

**Article version:** `1 (2022, Friday, January 21st at 7:21 pm)`

---
