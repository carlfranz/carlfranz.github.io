---
title: Useful daily bask command: find duplicates files
---

# Useful daily bask command: find duplicates files

As you may know, having files with same name in a project is not usually good. Sometime is necessary, sometime not. In java have two file with same name in the same project can lead to:

1. debug error: opens the other file in your IDE
2. logger misunderstanding: expecially if both have similar package

A solution is to change one class filename. To spot those files, I've found (see [source](http://stackoverflow.com)) the command below.

```bash
find /some/path -type f -printf '%f\n' | sort | uniq -c
```

What you got is a list of files with occurence in a path.

As example:

```
   
   1 MainApp.java
   1 AuthorizationClass.java
   2 JwsParser.java

```

Keep your project files _not_ clean _but_ sane.
