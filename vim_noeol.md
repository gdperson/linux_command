Even if the file was already saved with new lines at the end:

vim -b file and once in vim:

:set noeol

:wq

done.

Yet another alternative:

:set binary

:set noeol

:wq
