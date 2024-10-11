========== Question ==========  

### What does `(?<!y)x` represent in regular expressions?  

========== Answer ==========  

Negative lookbehind. **Matches '_x_' only if it's not preceded by '_y_'**.

**Example**: `(?<!Jack)Sprat` matches "_Sprat_" in "_TomSprat_" but not in "_JackSprat_".

========== Id ==========  
31

---

DECK INFO

TARGET DECK: Javascript::Regular expressions::AJREM - Anki javascript regular expressions - mozilla::Part I - Fundamentals::Chapter 3 - Other assertions

FILE TAGS: #Javascript::#Regular-expressions::#AJREM-Anki-javascript-regular-expressions-mozilla::#Part-I-Fundamentals::#Chapter-3-Other-assertions::#31-What-does-y-x-represent-in-regular-e

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```


QUESTION STATUS: Safe to store
