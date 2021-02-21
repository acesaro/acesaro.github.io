---
title: "Today I Learned (TIL)"
draft: false
---
# 2021-02-21
- nmap-ncat can execute a command for any connections established to a listening port with the `-e` option for `exec` or `-c` for a command run with `/bin/sh`.
    ```
    ncat -l 1234 -c "date"
    ```

