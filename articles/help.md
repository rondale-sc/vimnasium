# Help

Welcome again to vimnasium!  Today we are going to talk about how we can use Vim
to help us learn new things.  Vim's documentation is quite extensive and can be
utilized to both explore new things or uncover hidden functionality from
commands you've used countless times.

## Usage

When learning about programs documentation the first thing I look for is a way
to list out what is available.  For example, using the `apropos <pattern>`
command to look up man pages.  In Vim, we can utilize the `help` commands' auto
completion.

```
:help tabne<ctrl-d>
```

Above we type `:help g` then press `control-d` this will expand all available
help documentation for commands that start with the letter `tabne`.  In this
case it returned the strings for `tabnew` and others.  To view the help simply
finish the expression to `:help tabnew` and press return.  Using `control-d` to
see these options can be cumbersome at times, especially if you are more
comfortable with tab completion to address this Vim gives us the `wildmenu`
option.

```
:set wildmenu
```

Now when you run `:help tabne` and press `tab` you'll see the same options as
when you previously pressed `control-d`

## Links and Searching

Now that you've opend up the `help` documentation for `tabnew` you'll all the
information that Vim has about it.  You'll see some words are highlighted, these
highlighted words are links.  If you move your cursor to a highlighted word and
press `control-]` you'll be taken to more information about that word.  To
return to your previous cursor position press `control-o`.

If you'd like to search you can use `/` like you would normally in command mode.

```
# while in a help pane

/count
```

This will show you the occurance of the word 'count' closest to your current
cursor position.  To transition to the next search term press `n`.  Press `N` to
search in the reverse direction.

And that's about all there is to it. Thanks for reading!
