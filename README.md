# AJREM - Anki javascript regular expressions - mozilla

## Questions

### Part I - Fundamentals

<!-- https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_expressions/Cheatsheet -->

#### Chapter 1 - Character classes

Q:: What does `[xyz]` represent in regular expressions?
A:: A character class. Matches any single character listed in the brackets.
Example: `[aeiou]` matches any vowel in "hello" (e and o).

Q:: What does `[a-z]` represent in regular expressions?
A:: A character range. Matches any single character in the specified range.
Example: `[a-z]` matches any lowercase letter in "Hello123" (e, l, l, o).

Q:: What does `[^xyz]` represent in regular expressions?
A:: A negated character class. Matches any single character not listed in the brackets.
Example: `[^aeiou]` matches any non-vowel in "hello" (h, l, l).

Q:: What does `.` represent in regular expressions?
A:: Matches any single character except line breaks.
Example: `h.t` matches "hat", "hot", and "hit", but not "heat".

Q:: What does `\d` represent in regular expressions?
A:: Matches any single digit (0-9).
Example: `\d{3}` matches "123" in "abc123xyz".

Q:: What does `\D` represent in regular expressions?
A:: Matches any single non-digit character.
Example: `\D{3}` matches "abc" in "abc123xyz".

Q:: What does `\w` represent in regular expressions?
A:: Matches any word character (letter, digit, or underscore).
Example: `\w+` matches "hello_world123" in "hello_world123!".

Q:: What does `\W` represent in regular expressions?
A:: Matches any non-word character.
Example: `\W+` matches "!@#" in "abc!@#123".

Q:: What does `\s` represent in regular expressions?
A:: Matches any whitespace character (space, tab, newline).
Example: `a\sb` matches "a b" in "a b c".

Q:: What does `\S` represent in regular expressions?
A:: Matches any non-whitespace character.
Example: `\S+` matches "hello" and "world" in "hello world".

Q:: What does `\t` represent in regular expressions?
A:: Matches a horizontal tab character.
Example: `a\tb` matches "a    b" (with a tab between a and b).

Q:: What does `\r` represent in regular expressions?
A:: Matches a carriage return character.
Example: `a\rb` matches "a" and "b" on separate lines in Windows text files.

Q:: What does `\n` represent in regular expressions?
A:: Matches a line feed (new line) character.
Example: `hello\nworld` matches "hello" and "world" on separate lines.

Q:: What does `\v` represent in regular expressions?
A:: Matches a vertical tab character.
Example: `a\vb` matches "a" and "b" separated by a vertical tab.

Q:: What does `\f` represent in regular expressions?
A:: Matches a form feed character.
Example: `page1\fpage2` matches "page1" and "page2" on separate form feed-separated pages.

Q:: What does `[\b]` represent in regular expressions?
A:: Matches a backspace character.
Example: `abc[\b]` matches "ab" in "abc\b" (where \b is a backspace).

Q:: What does `\0` represent in regular expressions?
A:: Matches a NULL character.
Example: `abc\0xyz` matches "abc" followed by a NULL character, then "xyz".

Q:: What does `\cX` represent in regular expressions?
A:: Matches a control character, where X is a letter A-Z.
Example: `\cM` matches a carriage return (Ctrl+M).

Q:: What does `\xhh` represent in regular expressions?
A:: Matches a character with the hex code hh (two hex digits).
Example: `\x41` matches "A" (ASCII code 41 in hex).

Q:: What does `\uhhhh` represent in regular expressions?
A:: Matches a Unicode character with the code point hhhh (four hex digits).
Example: `\u00A9` matches the copyright symbol ©.

Q:: What does `\` (backslash) indicate in regular expressions?
A:: Escapes a special character or introduces a special sequence.
Example: `\.` matches a literal dot, while `.` matches any character.

Q:: What is the purpose of `|` (pipe) in regular expressions?
A:: Creates a disjunction, matching either of the alternatives it separates.
Example: `cat|dog` matches either "cat" or "dog" in a string.

#### Chapter 2 - Assertions

Q:: What are assertions in regular expressions?
A:: Special patterns that match positions rather than characters.
Example: `^` matches the start of a line, `$` matches the end of a line.

Q:: What does `^` represent in regular expressions?
A:: Matches the beginning of the input.
Example: `^Hello` matches "Hello" only at the start of a string.

Q:: What does `$` represent in regular expressions?
A:: Matches the end of the input.
Example: `world$` matches "world" only at the end of a string.

Q:: What does `\b` represent in regular expressions?
A:: Matches a word boundary (position between a word and non-word character).
Example: `\bcat\b` matches "cat" in "The cat sat", but not in "category".

Q:: What does `\B` represent in regular expressions?
A:: Matches a non-word boundary.
Example: `\Bcat\B` matches "cat" in "category", but not in "The cat sat".

#### Chapter 3 - Other assertions

Q:: What does `x(?=y)` represent in regular expressions?
A:: Positive lookahead. Matches 'x' only if it's followed by 'y'.
Example: `Jack(?=Sprat)` matches "Jack" in "JackSprat" but not in "JackFrost".

Q:: What does `x(?!y)` represent in regular expressions?
A:: Negative lookahead. Matches 'x' only if it's not followed by 'y'.
Example: `Jack(?!Sprat)` matches "Jack" in "JackFrost" but not in "JackSprat".

Q:: What does `(?<=y)x` represent in regular expressions?
A:: Positive lookbehind. Matches 'x' only if it's preceded by 'y'.
Example: `(?<=Jack)Sprat` matches "Sprat" in "JackSprat" but not in "TomSprat".

Q:: What does `(?<!y)x` represent in regular expressions?
A:: Negative lookbehind. Matches 'x' only if it's not preceded by 'y'.
Example: `(?<!Jack)Sprat` matches "Sprat" in "TomSprat" but not in "JackSprat".

Q:: What does `(?<!y)x` represent in regular expressions?
A:: Negative lookbehind. Matches 'x' only if it's not preceded by 'y'.
Example: `(?<!-)\d+` matches "123" in "a123" but not in "-123".

#### Chapter 4 - Groups and backreferences

Q:: What does `(x)` represent in regular expressions?
A:: Capturing group. Matches and remembers the matched content.
Example: `(foo)bar\1` matches "foobarfoo".

Q:: What does `(?<Name>x)` represent in regular expressions?
A:: Named capturing group. Matches and stores the content under a specified name.
Example: `(?<year>\d{4})-(?<month>\d{2})-(?<day>\d{2})` captures date parts.

Q:: What does `(?:x)` represent in regular expressions?
A:: Non-capturing group. Groups elements without creating a capture group.
Example: `(?:ab)+` matches one or more repetitions of "ab" without capturing.

Q:: What does `\n` (where n is a number) represent in regular expressions?
A:: Backreference. Refers to a previous capturing group.
Example: `(la)\1` matches "lala" but not "lama".

Q:: What does `\k<Name>` represent in regular expressions?
A:: Named backreference. Refers to a previous named capturing group.
Example: `(?<word>\w+)\s+\k<word>` matches repeated words.

#### Chapter 5 - Quantifiers

Q:: What are quantifiers in regular expressions?
A:: Symbols that specify how many times a pattern should match.
Example: `*`, `+`, `?`, and `{n,m}` are common quantifiers.

Q:: What does `x*` match in a regular expression?
A:: Matches 'x' zero or more times.
Example: `ab*c` matches "ac", "abc", "abbc", "abbbc", etc.

Q:: What does `x+` match in a regular expression?
A:: Matches 'x' one or more times.
Example: `a+` matches "a", "aa", "aaa", etc., but not an empty string.

Q:: What does `x?` match in a regular expression?
A:: Matches 'x' zero or one time.
Example: `colou?r` matches both "color" and "colour".

Q:: What does `x{n}` match in a regular expression?
A:: Matches exactly 'n' occurrences of 'x'.
Example: `a{3}` matches "aaa" in "baaaam", but not "aa" or "aaaa".

Q:: What does `x{n,}` match in a regular expression?
A:: Matches 'n' or more occurrences of 'x'.
Example: `a{2,}` matches "aa", "aaa", "aaaa", etc., but not "a".

Q:: What does `x{n,m}` match in a regular expression?
A:: Matches between 'n' and 'm' occurrences of 'x'.
Example: `a{2,4}` matches "aa", "aaa", and "aaaa", but not "a" or "aaaaa".

Q:: What does adding `?` after a quantifier do in a regular expression?
A:: Makes the quantifier non-greedy, matching as few characters as possible.
Example: `.*?` in `<.*?>` matches "<foo>" in "<foo><bar>", not "<foo><bar>".

Q:: What does `/<.*>/` match in regular expressions?
A:: Greedily matches everything between the first '<' and the last '>' in a string.
Example: `/<.*>/` matches "<foo><bar>" in "start <foo><bar> end".

---

DECK INFO

TARGET DECK: Javascript::Regular expressions::AJREM - Anki javascript regular expressions - mozilla

FILE TAGS: #Javascript::#Regular-expressions

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

