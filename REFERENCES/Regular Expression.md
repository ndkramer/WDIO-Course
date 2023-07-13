**Regular Expression Tool:**  https://regex101.com/



**Top 5 best practices for using Regular Expressions:**
1. **Keep it Simple and Understandable**: Regular expressions can become complex very quickly. It's important to keep them as simple as possible and well-documented so that others can understand them.
2. **Avoid Greedy Matches**: By default, regular expressions are greedy, meaning they will match as much as they can. This can lead to unexpected results. Use non-greedy quantifiers where possible.
3. **Use Capturing Groups and Backreferences Appropriately**: Capturing groups (using parentheses) can help extract information from the regex. Backreferences (using \1, \2, etc.) can refer back to these groups.
4. **Be Aware of Special Characters**: Characters like ., *, +, ?, ^, $, (, ), [, ], {, }, |, \ have special meanings in regex. If you want to match these characters literally, you need to escape them using a backslash (\\).
5. **Test Thoroughly**: Regular expressions can be tricky and behave differently across different languages and platforms. Always test your regex thoroughly, and consider using a regex tester tool.



**Basic Regular Expression Reference**

1. **.** - Matches any character except newline
2. **\d** - Matches any digit (equivalent to [0-9])
3. **\D** - Matches any non-digit character
4. **\s** - Matches any whitespace character
5. **\S** - Matches any non-whitespace character
6. **\w** - Matches any word character (equivalent to [a-zA-Z0-9_])
7. **\W** - Matches any non-word character
8. **^** - Matches the start of the string
9. **$** - Matches the end of the string
10. **[abc]** - Matches any of the characters inside the brackets
11. **[^abc]** - Matches any character NOT inside the brackets
12. **(abc|def)** - Matches either the sequence 'abc' or 'def'
13. **a?** - Matches the character 'a' 0 or 1 times
14. **a*** - Matches the character 'a' 0 or more times
15. **a+** - Matches the character 'a' 1 or more times
16. **a{3}** - Matches exactly 3 consecutive 'a' characters
17. **a{3,}** - Matches 3 or more consecutive 'a' characters
18. **a{3,6}** - Matches between 3 and 6 'a' characters
19. **( | )** -  In regular expressions, the vertical bar or pipe symbol "|" is used to denote a logical OR. This means that the pattern will match if either the expression before or after the "|" is present.
For example, in the regular expression "(apple|orange)", the pattern will match either "apple" or "orange".

21.** ? **- In regular expressions, the "?" character has a special meaning. It makes the preceding element optional. This means that the pattern will match whether or not that element is present. For example, the regular expression "colou?r" would match both "color" and "colour".
22.** ?: **- In regular expressions, "?:", when placed at the start of a group, makes that group non-capturing. This means that the group will still match as usual, but it won't capture the matched text for later use. For example, in the regular expression "(?:abc)def", "abc" is part of the matching pattern, but it's not captured for later use.

Remember, regular expressions can be very powerful but also complex, so use them wisely

**Another Reference: ** https://github.com/ndkramer/WDIO-Course/blob/main/CUCUMBER/Cucumber-Regular-Expressions-Cheat-Sheet.pdf

