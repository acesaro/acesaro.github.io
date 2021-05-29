---
title: "Today I Learned (TIL)"
draft: false
---
# 2021-05-29

* [vim] Convert line indention from 2 to 4 spaces

    Convert two space indents to tabs

    ```
    :set ts=2 sts=2 noet
    :retab!
    ```

    Convert two space indents to tabs

    ```
    :set ts=4 sts=4 et
    :retab
    ```

# 2021-03-15

* [python3] Merging two dictionaries in Python 3.x.

    ```
    $ python3
    >>> xs = {"a": 1, "b": 2}
    >>> ys = {"a": 9, "c": 3}
    >>> z = {**xs, **ys}
    >>> z
    {'a': 9, 'b': 2, 'c': 3}
    ```

# 2021-02-21

* [nmap-ncat] Execute a command for any connections established to a listening
  port with the `-e` option for `exec` or `-c` for a command run with `/bin/sh`.

    ```
    ncat -l 1234 -c "date"
    ```

