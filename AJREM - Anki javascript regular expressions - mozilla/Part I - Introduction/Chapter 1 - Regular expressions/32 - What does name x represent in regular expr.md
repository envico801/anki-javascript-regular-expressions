Q: What does `(?<Name>x)` represent in regular expressions?  
A: Named capturing group. Matches "x" and stores it under the specified name `<Name>`.  
For example, to extract the United States area code from a phone number, we could use `/\((?<area>\d\d\d)\)/`. The resulting number would appear under `matches.groups.area`.
<!--ID: 1693833351138-->

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