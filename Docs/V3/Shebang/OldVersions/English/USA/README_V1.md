
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
