from:
https://stackoverflow.com/questions/1497958/how-do-i-use-vim-registers/1498026#1498026

At first this looks like you accidentally opened a binary file in notepad, but upon second glance, it's the exact sequence of characters in our macro!

You are a curious person, so let's do something interesting and edit this line of text to insert a ! instead of boring old %.

```
EEa!<ESC>j0
```

Then let's yank this into the n register by typing B"nyE. Then, just for kicks, let's run the n macro on a line of our data using @n....

OMG, IT ADDED A !

Essentially, running a macro is like pressing the exact sequence of keys in that macro's register. If that isn't a cool register trick, I'll eat my hat.

This is totally key. I haven't noticed until now that registers are the same as macro buffers. This means you can just store all your macros in text, yank them, and run them. Pretty cool, and a little bit weird. Very Vim.
