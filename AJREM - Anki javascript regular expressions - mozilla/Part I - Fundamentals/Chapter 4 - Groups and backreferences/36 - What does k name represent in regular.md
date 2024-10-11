========== Question ==========  

### What does `\k<Name>` represent in regular expressions?  

========== Answer ==========  

Named backreference. **Refers to a previous named capturing group**.

**Example**: `(?<word>\w+)\s+\k<word>` matches repeated words.

========== Id ==========  
36

---

DECK INFO

TARGET DECK: Javascript::Regular expressions::AJREM - Anki javascript regular expressions - mozilla::Part I - Fundamentals::Chapter 4 - Groups and backreferences

FILE TAGS: #Javascript::#Regular-expressions::#AJREM-Anki-javascript-regular-expressions-mozilla::#Part-I-Fundamentals::#Chapter-4-Groups-and-backreferences::#36-What-does-k-name-represent-in-regular

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```


QUESTION STATUS: Safe to store
