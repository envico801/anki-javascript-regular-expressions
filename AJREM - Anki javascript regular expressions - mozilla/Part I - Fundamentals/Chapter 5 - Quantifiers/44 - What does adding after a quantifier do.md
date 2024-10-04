========== Question ==========  

### What does adding `?` after a quantifier do in a regular expression?  

========== Answer ==========  

Makes the quantifier non-greedy, matching as few characters as possible.

**Example**: `a.*?b` matches "ab" in "abcb", not "abcb".

========== Id ==========  
44

---

DECK INFO

TARGET DECK: Javascript::Regular expressions::AJREM - Anki javascript regular expressions - mozilla::Part I - Fundamentals::Chapter 5 - Quantifiers

FILE TAGS: #Javascript::#Regular-expressions::#AJREM-Anki-javascript-regular-expressions-mozilla::#Part-I-Fundamentals::#Chapter-5-Quantifiers::#44-What-does-adding-after-a-quantifier-do

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```


QUESTION STATUS: Safe to store
