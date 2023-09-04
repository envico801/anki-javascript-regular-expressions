Q: What happens when `?` is used immediately after certain quantifiers?  
A: When used immediately after quantifiers like `*`, `+`, `?`, or `{}`, it makes the quantifier non-greedy, matching the minimum number of times instead of the default greedy behavior.  
For example, given a string like "some <foo> <bar> new </bar> </foo> thing":
-   `/<.*>/` will match "`<foo> <bar> new </bar> </foo>`"
-   `/<.*?>/` will match "`<foo>`"
<!--ID: 1693833350591-->

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