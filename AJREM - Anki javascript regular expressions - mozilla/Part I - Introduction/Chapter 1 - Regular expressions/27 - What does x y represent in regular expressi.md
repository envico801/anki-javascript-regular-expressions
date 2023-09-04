Q: What does `x(?=y)` represent in regular expressions?  
A: Lookahead assertion. Matches "x" only if "x" is followed by "y."  
For example, /`Jack(?=Sprat)/` matches "Jack" only if it is followed by "Sprat".  
`/Jack(?=Sprat|Frost)/` matches "Jack" only if it is followed by "Sprat" or "Frost". However, neither "Sprat" nor "Frost" is part of the match results.  
> **Note:** The `?` character may also be used as a quantifier.
<!--ID: 1693833351450-->

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