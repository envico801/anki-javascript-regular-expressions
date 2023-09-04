Q: What does `\b` represent as a boundary-type assertion in regular expressions?  
A: Matches a word boundary position where a word character is not followed or preceded by another word character.  
**Examples:**
-   `/\bm/` matches the "m" in "moon".
-   `/oo\b/` does not match the "oo" in "moon", because "oo" is followed by "n" which is a word character.
-   `/oon\b/` matches the "oon" in "moon", because "oon" is the end of the string, thus not followed by a word character.
-   `/\w\b\w/` will never match anything, because a word character can never be followed by both a non-word and a word character.
<!--ID: 1693833351623-->

---

DECK INFO

TARGET DECK: Javascript::Regular expressions::AJREM - Anki javascript regular expressions - mozilla::Part I - Introduction::Chapter 1 - Regular expressions

FILE TAGS: #Javascript #Regular-expressions

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```



QUESTION STATUS: Safe to store