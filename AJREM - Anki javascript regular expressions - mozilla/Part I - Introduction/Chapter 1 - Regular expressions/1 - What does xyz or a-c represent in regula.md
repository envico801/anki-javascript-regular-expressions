Q: What does `[xyz]` or `[a-c]` represent in regular expressions?  
A: A character class. Matches any one of the enclosed characters. Can specify a range of characters using a hyphen, but if the hyphen is the first or last character, it is treated as a literal hyphen.  
For example, `[abcd]` is the same as `[a-d]`. They match the "b" in "brisket", and the "a" or the "c" in "arch", but not the "-" (hyphen) in "non-profit".
<!--ID: 1693833352513-->

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