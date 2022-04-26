
***

# URLL sublanguage variants

On 2022, April 22nd, I considered further expansions to the URLL language, and on 2022 April 25th, I have updated the documentation. This is part of the language specification from 2022 April.

Since a URLL file recognizes multiple types of links, and since it is being drafted still, there needs to be sub-languages. My only concern is of polluting the language list. All sub-languages will use the main `*.urll` file extension.

> Variants (9)
> * 1. [`URLL empty list`](#URLL-empty-list)
> * 2. [`URLL invalid list`](#URLL-invalid-list)
> * 3. [`URLL single-entry web list`](#URLL-single-entry-web-list)
> * 4. [`URLL multi-entry web list`](#URLL-multi-entry-web-list)
> * 5. [`URLL single-entry local list`](#URLL-single-entry-local-list)
> * 6. [`URLL multi-entry local list`](#URLL-multi-entry-local-list)
> * 7. [`URLL single-entry IP list`](#URLL-single-entry-IP-list)
> * 8. [`URLL multi-entry IP list`](#URLL-multi-entry-IP-list)
> * 9. [`URLL mix list`](#URLL-mix-list)

## URLL empty list

Due to the prevalence of comments in URLL V2 and up, empty list files are possible, and can be common. Generally, it can be blank:

```urll

```

It can contain just the shebang

```urll
--URLL-version=2;

```

Or it can be just comments:

```urll
--URLL-version=2;
-- Empty list
-- A link will go here

-- Another link will go here

-- End of list
```

## URLL invalid list

If a URLL file is improperly configured, it will be known as URLL invalid. Examples of this include

```urll
-- Comments can't come before the shebang
```

```urll
--URLL-version=2;
<?php
echo ("My invalid URLL file");
?>
```

```urll
--URLL-version=2;
Invalid URLL file. Text must be commented
Although here is a link:
https://www.example.com
Still invalid though
```

and so on.

## URLL single-entry web list

The URLL single entry web list is a variant of the URLL format for list files that contain only 1 link (unless a link is commented, in which that does not count) with links to websites.

Here is an example:

```urll
https://www.example.com
```

## URLL multi-entry web list

Standard URLL files contain 2 or more links, and are known as multi-entry web lists. THey are web lists, only if they contain website links. For mixtures of links, see below.

```urll
--URLL-version=2;
-- My basic multi-entry list
https://www.example.com
https://safe.duckduckgo.com
```

## URLL single-entry local list

URLL files that contain links to local files/unrecognized URI schemes, with 1 link are known as single entry local list files. They can look like this:

```urll
file:///
```

## URLL multi-entry local list

URLL files that contain links to multiple local files/unrecognized URI schemes, with 2 or more links are known as single entry local list files. They can look like this:

```urll
file:///
file:///bin
file:///boot
file:///cdrom
file:///dev
file:///etc
file:///home
file:///lib
file:///lib32
file:///lib64
file:///libx32
file:///lost+found
file:///media
file:///mnt
file:///opt
file:///proc
file:///root
file:///run
file:///sbin
file:///srv
file:///sys
file:///tmp
file:///usr
file:///var
file:///swapfile
```

This is an example of the UNIX file structure, as it counts as a local list.

## URLL single-entry IP list

URLL single-entry IP lists are lists that contain a single IP address link. They are similar to local lists. They can look like this:

```
127.0.0.1
```

Note that URLL encourages the adoption of IPv6, and mixes all IP versions into one format, to prevent severe fragmentation/

## URLL multi-entry IP list

URLL multi-entry IP lists are lists that contain 2 or more IP address links. They are similar to local lists. They can look like this:

```
127.0.0.1
255.255.255.0
```

Note that URLL encourages the adoption of IPv6, and mixes all IP versions into one format, to prevent severe fragmentation/

## URLL mix list

URLL files that contain multiple types of links are known as mix list files. They can look like this:

```urll
https://www.example.com
file:///home/
127.0.01
```

***

**File version:** `1 (2022, Monday, April 25th at 7:15 pm PST)`

***
