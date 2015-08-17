# Notes

there have been a few patches to suppress such popups when running a script...

now, what's the best way to make the programmer or the user that a warning / error has been issued?

the easy way is to simply have a warning output in the terminal.
the "correct" way might be to introduce exceptions.

another way would to have a custom method "get_last_error()" that you can check after running a command that might raise an error.

all in all, most scripts run in a controlled environment and just ignoring the warnings is not the worst idea.
