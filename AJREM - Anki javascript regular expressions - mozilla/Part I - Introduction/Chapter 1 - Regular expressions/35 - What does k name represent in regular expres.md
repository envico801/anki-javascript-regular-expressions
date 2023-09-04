Q: What does `\k<Name>` represent in regular expressions?  
A: Back reference to the last substring matching the Named capture group specified by `<Name>`.  
For example, `/(?<title>\w+), yes \k<title>/` matches "Sir, yes Sir" in "Do you copy? Sir, yes Sir!".  
> **Note:** `\k` is used literally here to indicate the beginning of a back reference to a Named capture group.
<!--ID: 1693833351001-->

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