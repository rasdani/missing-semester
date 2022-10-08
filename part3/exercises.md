###exercise 2:

```cat /usr/share/dict/words | tr '[:upper:]' '[:lower:]' | awk "/^(.*a.*){3}([^'][^s])$/" | wc -l```
