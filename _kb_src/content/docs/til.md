---
title: "Today I Learned (TIL)"
draft: false
---
# 2022-02-08

* [vim] Updating an environment variable in a currently running vim session.

    ```
    # In the original shell after SSHing in
    $ env |grep SSH | sed 's/^/export /g'
    export SSH_AUTH_SOCK=/tmp/ssh-abcdefg/agent.2268696
    
    # In the existing vim session running in a tmux session
    :let $SSH_AUTH_SOCK = '/tmp/ssh-abcdefg/agent.2268696'
    ```

# 2021-12-13

* [k8s] Deleting "stuck" resources that reference finalizers.  After applying this
  you should be able to delete the objects, or those that depend on this one.
  
    ```
    $ kubectl patch {kind}/{name} -p '{"metadata":{"finalizers":[]}}' --type=merge
    ```

# 2021-12-02

* [shell] Using `envsubst` to template files in shell with GNU gettext utils.

    Create a template file with variables using the similar shell syntax:
    ```
    $ vi tmp.tmpl
    my_config_key_1="${MY_CONFIG_KEY_1}"
    my_config_key_2="${MY_CONFIG_KEY_2}"
    ```

    Render the template with `envsubst`:
    ```
    $ export MY_CONFIG_KEY_1=tony MY_CONFIG_KEY_2=cesaro
    $ envsubst < tmp.tmpl
    my_config_key_1="tony"
    my_config_key_2="cesaro"
    ```

# 2021-05-29

* [vim] Convert line indention from 2 to 4 spaces

    Convert two-space indents to tabs:

    ```
    :set ts=2 sts=2 noet
    :retab!
    ```

    Convert tabs to four-space indents:

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

