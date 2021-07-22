Even if the file was already saved with new lines at the end:

vim -b file and once in vim:

:set noeol
:wq
done.

alternatively you can open files in vim with :e ++bin file

Yet another alternative:

:set binary
:set noeol
:wq
