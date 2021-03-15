---
title: "Today I Learned (TIL)"
draft: false
---
# 2021-03-15
- Merging two dictionaries in Python 3.x.
    ```
    $ python3
    >>> xs = {"a": 1, "b": 2}
    >>> ys = {"a": 9, "c": 3}
    >>> z = {**xs, **ys}
    >>> z
    {'a': 9, 'b': 2, 'c': 3}
    ```

# 2021-02-21
- nmap-ncat can execute a command for any connections established to a listening port with the `-e` option for `exec` or `-c` for a command run with `/bin/sh`.
    ```
    ncat -l 1234 -c "date"
    ```

