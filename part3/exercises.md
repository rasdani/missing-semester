2. Find the number of words (in `/usr/share/dict/words`) that contain at
   least three `a`s and don't have a `'s` ending. What are the three
   most common last two letters of those words? `sed`'s `y` command, or
   the `tr` program, may help you with case insensitivity. How many
   of those two-letter combinations are there? And for a challenge:
   which combinations do not occur?

```cat /usr/share/dict/words | tr '[:upper:]' '[:lower:]' | awk "/^(.*a.*){3}([^'][^s])$/" | wc -l```
