Q: What does `^` represent as a boundary-type assertion in regular expressions?  
A: Matches the beginning of input or immediately after a line break character if the multiline flag is set.  
For example, `/^A/` does not match the "A" in "an A", but does match the first "A" in "An A".  
> **Note:** This character has a different meaning when it appears at the start of a [character class](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_expressions/Character_classes).
<!--ID: 1693833351731-->

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