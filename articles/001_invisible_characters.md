# 001 Invisible Characters & List Character Mode

Welcome to the first edition of Vimnasium.  Here we'll take (mostly) weekly
journeys into the depths of the editor formerly known as Vi.  The topics
discussed within Vimnasium will hopefully have something for everyone from
beginner to experts.  With all that said, let's dive in!

## Invisible Characters

The whitespace, tab, and newline characters can be exceedingly difficult to deal
with.  In languages like Python and Coffeescript their precense is integral to
the parsing process.  So you can imagine just how frustrating it is to have
these characters come out and bite you unseen.

I've had this happen.  Learning about how Python handles mixed whitespace/tab
indentation is not always a fun experience.  Incidentally, you should always
test your code before pushing to production, :).  Vim has you covered, it can
easily handle showing you these invisible characters and let you better
see/understand your code.

## Let's talk about list mode

Vim displays invisible characters in list mode.  By default it will display
unprintable characters as `^` and `$` for end of line characters.  These
defaults can be overridden by using the `listchars` setting.

It allows you to set the representation for the following non-printable
characters:

- `eol` - End of line characters
- `tab`
- `trail` - Character to show trailing spaces
- `extends` - Character to show in last column
- `precedes` - Character to show in first column
- `conceal` - Character to show in place of concealed text
- `nbsp` - Character to show for non-breakable space

This is the format needed to set the above non-printables:

```
:set listchars=tab:>_,eol:$
```

In the above command tabs are represented by `>` and end of line characters are
represented by `$`

The command requires that `listchars=` be followed by a command separated set of
value pairs.  The value pairs should be the name of the non-printable (listed
above) followed by the character (or characters) that you'd like to to be the
representation.  The value pair is separated by a colon.  The representation can
be almost anything that vim will draw, however the colon is reserved.

And that's about all there is to it. Thanks for reading!
