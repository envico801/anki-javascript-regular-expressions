# AJREM - Anki javascript regular expressions - mozilla

## Questions

### Part I - Introduction

<!-- https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_expressions/Cheatsheet -->
#### Chapter 1 - Regular expressions

Q:: What does `[xyz]` or `[a-c]` represent in regular expressions?  
A:: A character class. Matches any one of the enclosed characters. Can specify a range of characters using a hyphen, but if the hyphen is the first or last character, it is treated as a literal hyphen.  
For example, `[abcd]` is the same as `[a-d]`. They match the "b" in "brisket", and the "a" or the "c" in "arch", but not the "-" (hyphen) in "non-profit".

Q:: What does `[^xyz]` or `[^a-c]` represent in regular expressions?  
A:: A negated or complemented character class. Matches anything that is not enclosed in the brackets.  
For example, `[^abc]` is the same as `[^a-c]`. They initially match "o" in "bacon" and "h" in "chop".  
> **Note:** The ^ character may also indicate the [beginning of input](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_expressions/Assertions).

Q:: What does `.` represent in regular expressions?  
A:: Matches any single character except line terminators (`\n`, `\r`, `\u2028`, `\u2029`).  
For example, `/.y/` matches "my" and "ay", but not "yes", in "yes make my day".  
> **Note:** The `s` "dotAll" flag allows the dot to also match line terminators.

Q:: What does `\d` represent in regular expressions?  
A:: Matches any digit (Arabic numeral), equivalent to `[0-9]`.  
For example, `/\d/` or `/[0-9]/` matches "2" in "B2 is the suite number".

Q:: What does `\D` represent in regular expressions?  
A:: Matches any character that is not a digit (Arabic numeral), equivalent to `[^0-9]`.  
For example, `/\D/` or `/[^0-9]/` matches "B" in "B2 is the suite number".

Q:: What does `\w` represent in regular expressions?  
A:: Matches any alphanumeric character from the basic Latin alphabet, including the underscore, equivalent to `[A-Za-z0-9_]`.  
For example, `/\w/` matches "a" in "apple", "5" in "$5.28", and "3" in "3D".

Q:: What does `\W` represent in regular expressions?  
A:: Matches any character that is not a word character from the basic Latin alphabet, equivalent to `[^A-Za-z0-9_]`.  
For example, `/\W/` or `/[^A-Za-z0-9_]/` matches "%" in "50%".

Q:: What does `\s` represent in regular expressions?  
A:: Matches a single white space character, including various space-related characters and Unicode spaces.  
For example, `/\s\w*/` matches " bar" in "foo bar".

Q:: What does `\S` represent in regular expressions?  
A:: Matches a single character other than white space, excluding space-related characters and Unicode spaces.
For example, `/\S\w*/` matches "foo" in "foo bar".

Q:: What does `\t` represent in regular expressions?  
A:: Matches a horizontal tab.

Q:: What does `\r` represent in regular expressions?  
A:: Matches a carriage return.

Q:: What does `\n` represent in regular expressions?  
A:: Matches a linefeed.

Q:: What does `\v` represent in regular expressions?  
A:: Matches a vertical tab.

Q:: What does `\f` represent in regular expressions?  
A:: Matches a form-feed.

Q:: What does `[\b]` represent in regular expressions?  
A:: Matches a backspace. Not to be confused with the word-boundary character `\b`.

Q:: What does `\0` represent in regular expressions?  
A:: Matches a NUL character.

Q:: What does `\cX` represent in regular expressions?  
A:: Matches a control character using caret notation, where "X" is a letter from A–Z.  
For example, `/\cM/` matches "\\r" in "\\r\\n".

Q:: What does `\xhh` represent in regular expressions?  
A:: Matches the character with the code `hh` (two hexadecimal digits).

Q:: What does `\uhhhh` or `\u{hhhh}` represent in regular expressions?  
A:: (Only when the `u` flag is set.) Matches the character with the Unicode value `U+hhhh` or `U+hhhhh` (hexadecimal digits).

Q:: What does ` \ ` indicate in regular expressions?  
A:: Indicates that the following character should be treated specially or "escaped."  
For example, `/b/` matches the character "b". By placing a backslash in front of "b", that is by using `/\b/`, the character becomes special to mean match a word boundary.
> **Note:** To match this character literally, escape it with itself. In other words to search for ` \ ` use `/\\/`.

Q:: What is the purpose of a disjunction `|` in regular expressions?  
A:: Matches either of the provided alternatives. Each component, separated by a pipe (`|`), is called an alternative.  
For example, `/green|red/` matches "green" in "green apple" and "red" in "red apple".  
> **Note:** A disjunction is another way to specify "a set of choices", but it's not a character class. Disjunctions are not atoms — you need to use a [group](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_expressions/Groups_and_backreferences) to make it part of a bigger pattern. `[abc]` is functionally equivalent to `(?:a|b|c)`.

Q:: What are assertions in regular expressions?  
A:: Patterns indicating in some way that a match is possible, including boundaries and look-ahead/look-behind expressions.

Q:: What does `^` represent as a boundary-type assertion in regular expressions?  
A:: Matches the beginning of input or immediately after a line break character if the multiline flag is set.  
For example, `/^A/` does not match the "A" in "an A", but does match the first "A" in "An A".  
> **Note:** This character has a different meaning when it appears at the start of a [character class](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_expressions/Character_classes).

Q:: What does `$` represent as a boundary-type assertion in regular expressions?  
A:: Matches the end of input or immediately before a line break character if the multiline flag is set.  
For example, `/t$/` does not match the "t" in "eater", but does match it in "eat".

Q:: What does `\b` represent as a boundary-type assertion in regular expressions?  
A:: Matches a word boundary position where a word character is not followed or preceded by another word character.  
**Examples:**

-   `/\bm/` matches the "m" in "moon".
-   `/oo\b/` does not match the "oo" in "moon", because "oo" is followed by "n" which is a word character.
-   `/oon\b/` matches the "oon" in "moon", because "oon" is the end of the string, thus not followed by a word character.
-   `/\w\b\w/` will never match anything, because a word character can never be followed by both a non-word and a word character.

Q:: What does `\B` represent as a boundary-type assertion in regular expressions?  
A:: Matches a non-word boundary position where the previous and next characters are of the same type (both words or both non-words).  
For example, `/\Bon/` matches "on" in "at noon", and `/ye\B/` matches "ye" in "possibly yesterday".

Q:: What does `x(?=y)` represent in regular expressions?  
A:: Lookahead assertion. Matches "x" only if "x" is followed by "y."  
For example, /`Jack(?=Sprat)/` matches "Jack" only if it is followed by "Sprat".  
`/Jack(?=Sprat|Frost)/` matches "Jack" only if it is followed by "Sprat" or "Frost". However, neither "Sprat" nor "Frost" is part of the match results.
> **Note:** The `?` character may also be used as a quantifier.

Q:: What does `x(?!y)` represent in regular expressions?  
A:: Negative lookahead assertion. Matches "x" only if "x" is not followed by "y."  
For example, `/\d+(?!\.)/` matches a number only if it is not followed by a decimal point. `/\d+(?!\.)/.exec('3.141')` matches "141" but not "3".

Q:: What does `(?<=y)x` represent in regular expressions?  
A:: Lookbehind assertion. Matches "x" only if "x" is preceded by "y."  
For example, `/(?<=Jack)Sprat/` matches "Sprat" only if it is preceded by "Jack". `/(?<=Jack|Tom)Sprat/` matches "Sprat" only if it is preceded by "Jack" or "Tom". However, neither "Jack" nor "Tom" is part of the match results.

Q:: What does `(?<!y)x` represent in regular expressions?  
A:: Negative lookbehind assertion. Matches "x" only if "x" is not preceded by "y."  
For example, `/(?<!-)\d+/` matches a number only if it is not preceded by a minus sign. `/(?<!-)\d+/.exec('3')` matches "3". `/(?<!-)\d+/.exec('-3')` match is not found because the number is preceded by the minus sign.

Q:: What does `(x)` represent in regular expressions?  
A:: Capturing group. Matches `x` and remembers the match.  
For example, `/(foo)/` matches and remembers "foo" in "foo bar".

Q:: What does `(?<Name>x)` represent in regular expressions?  
A:: Named capturing group. Matches "x" and stores it under the specified name `<Name>`.  
For example, to extract the United States area code from a phone number, we could use `/\((?<area>\d\d\d)\)/`. The resulting number would appear under `matches.groups.area`.

Q:: What does `(?:x)` represent in regular expressions?  
A:: Non-capturing group. Matches "x" but does not remember the match.

Q:: What does `\n` represent in regular expressions?  
A:: Where "n" is a positive integer. Back reference to the last substring matching the n parenthetical in the regular expression.  
For example, `/apple(,)\sorange\1/` matches "apple, orange," in "apple, orange, cherry, peach".

Q:: What does `\k<Name>` represent in regular expressions?  
A:: Back reference to the last substring matching the Named capture group specified by `<Name>`.  
For example, `/(?<title>\w+), yes \k<title>/` matches "Sir, yes Sir" in "Do you copy? Sir, yes Sir!".  
> **Note:** `\k` is used literally here to indicate the beginning of a back reference to a Named capture group.

Q:: What do Quantifiers indicate in regular expressions?  
A:: Quantifiers indicate numbers of characters or expressions to match.

Q:: What does `x*` match in a regular expression pattern?  
A:: `x*` matches the preceding item "x" 0 or more times.  
For example, `/bo*/` matches "boooo" in "A ghost booooed" and "b" in "A bird warbled", but nothing in "A goat grunted".

Q:: What does `x+` match in a regular expression pattern?  
A:: `x+` matches the preceding item "x" 1 or more times. It is equivalent to `{1,}`.  
For example, `/a+/` matches the "a" in "candy" and all the "a"'s in "caaaaaaandy".

Q:: What does `x?` match in a regular expression pattern?  
A:: `x?` matches the preceding item "x" 0 or 1 times.  
For example, `/e?le?/` matches the "el" in "angel" and the "le" in "angle."

Q:: What does `x{n}` match in a regular expression pattern?  
A:: `x{n}` matches exactly "n" occurrences of the preceding item "x."  
For example, `/a{2}/` doesn't match the "a" in "candy", but it matches all of the "a"'s in "caandy", and the first two "a"'s in "caaandy".

Q:: What does `x{n,}` match in a regular expression pattern?  
A:: `x{n,}` matches at least "n" occurrences of the preceding item "x."  
For example, `/a{2,}/` doesn't match the "a" in "candy", but matches all of the a's in "caandy" and in "caaaaaaandy".

Q:: What does `x{n,m}` match in a regular expression pattern?  
A:: `x{n,m}` matches at least "n" and at most "m" occurrences of the preceding item "x."  
For example, `/a{1,3}/` matches nothing in "cndy", the "a" in "candy", the two "a"'s in "caandy", and the first three "a"'s in "caaaaaaandy". Notice that when matching "caaaaaaandy", the match is "aaa", even though the original string had more "a"s in it.

Q:: What happens when `?` is used immediately after certain quantifiers?  
A:: When used immediately after quantifiers like `*`, `+`, `?`, or `{}`, it makes the quantifier non-greedy, matching the minimum number of times instead of the default greedy behavior.  
For example, given a string like "some <foo> <bar> new </bar> </foo> thing":

-   `/<.*>/` will match "`<foo> <bar> new </bar> </foo>`"
-   `/<.*?>/` will match "`<foo>`"

Q:: What does `/<.*>/` match in regular expressions?  
A:: It matches everything between the first `<` and the last `>` in a string.

---

DECK INFO

TARGET DECK: Javascript::Regular expressions::AJREM - Anki javascript regular expressions - mozilla

FILE TAGS: #Javascript #Regular-expressions

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

