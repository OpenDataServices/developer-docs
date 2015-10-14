# The Terminal

## Tips

The readline shortcuts at 
https://wiki.archlinux.org/index.php/Keyboard_shortcuts#Readline 
are very useful.

In particular, Ctrl+A and Ctrl+E are useful for jumping to the start/end of a line and Ctrl+R for searching through command history.

There's also a vi style mode availible by adding `set editing-mode vi` to .inputrc

Note that readline is used by other shells, such as the Python shell, so you can use these same keyboard shortcuts there too.

### autojump

```
*~$* j bar

*~/some/dir/foobar/$* j bar

*~/other/barcamp/$* j bar
```

