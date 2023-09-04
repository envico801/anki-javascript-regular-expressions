Q: What is the purpose of a disjunction `|` in regular expressions?  
A: Matches either of the provided alternatives. Each component, separated by a pipe (`|`), is called an alternative.  
For example, `/green|red/` matches "green" in "green apple" and "red" in "red apple".  
> **Note:** A disjunction is another way to specify "a set of choices", but it's not a character class. Disjunctions are not atoms — you need to use a [group](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_expressions/Groups_and_backreferences) to make it part of a bigger pattern. `[abc]` is functionally equivalent to `(?:a|b|c)`.
<!--ID: 1693833351839-->

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