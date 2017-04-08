# clipboard-manager

linux clipboard manager

## Requirements

  * Python 3
  * PyGTK
  * dmenu

## Interaction

The clipboard daemon responds to commands through a named pipe at `$XDG_CACHE_HOME/clipboard-manager/clipboard-manager.sock`. The following commands are supported:

  * `current`
  * `get $uuid`
  * `set $text`
  * `summaries`

To write to the name pipe you can `echo` straight into the file:

```
$ echo "current" > "$XDG_CACHE_HOME"/clipboard-manager/clipboard-manager.sock
```

Then to read the response, `cat` the contents:

```
$ cat "$XDG_CACHE_HOME"/clipboard-manager/clipboard-manager.sock
```
