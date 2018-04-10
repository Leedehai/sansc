# Remove shell control sequences

Add this to your `bashrc` or `zshrc`:

`alias sansc="perl -pe 's/\e([^\[\]]|\[.*?[a-zA-Z]|\].*?\a)//g' | col -b "`

Example: `cat text-mangled > text-unreadable` is

`^[[1;32mprimitive types, e.g. int enum ^[[0;m`

use `cat text-mangled | sansc > text-clean` instead to remove the control sequences:

`primitive types, e.g. int enum`

Credit to [Peter Nore](https://unix.stackexchange.com/users/8635/peter-nore).
