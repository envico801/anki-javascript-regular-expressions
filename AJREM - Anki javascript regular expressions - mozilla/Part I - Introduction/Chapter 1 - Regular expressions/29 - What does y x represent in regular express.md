Q: What does `(?<=y)x` represent in regular expressions?  
A: Lookbehind assertion. Matches "x" only if "x" is preceded by "y."  
For example, `/(?<=Jack)Sprat/` matches "Sprat" only if it is preceded by "Jack". `/(?<=Jack|Tom)Sprat/` matches "Sprat" only if it is preceded by "Jack" or "Tom". However, neither "Jack" nor "Tom" is part of the match results.
<!--ID: 1693833351321-->

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