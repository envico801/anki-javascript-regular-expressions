Q: What does `.` represent in regular expressions?  
A: Matches any single character except line terminators (`\n`, `\r`, `\u2028`, `\u2029`).  
For example, `/.y/` matches "my" and "ay", but not "yes", in "yes make my day".  
> **Note:** The `s` "dotAll" flag allows the dot to also match line terminators.
<!--ID: 1693833351276-->

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