## Hosting
[OpenBSD](http://www.openbsd.org) is rock solid.

## Development
Open-source based development, mainly targeting UNIX and
Common Lisp.

### C
[C](https://en.wikipedia.org/wiki/C_(programming_language))
is probably the true reason for the success of
[UNIX](https://en.wikipedia.org/wiki/Unix)
as an operating system.

### C++

### Common Lisp
[Common Lisp](https://cliki.net/)
is one of the few programming languages still in use after
20 years of existence.

It has the best object model around (CLOS), compiles to native
code and supports multiple paradigms thanks to macros which make
the compiler itself programmable.

Its weights are an archaic namespace, lack of non-blocking semantics
for streams, and loads of misconceptions forwarded by non-lispers.
However the standard is stable and there are many compilers so the
notion of bitrot has almost disappeared.

The open-source (and free) native compilers are quite young and the
open source community is on the rise. The party is just starting now.

#### cffi-posix
Open-source project to portably and regularly expose the
[POSIX](http://pubs.opengroup.org/onlinepubs/9699919799/)
API to Common Lisp programs using
[CFFI](https://common-lisp.net/project/cffi/)

#### cl-stream
Experimental project to replace Common Lisp streams with
streams supporting any type of data and non-blocking semantics,
following principles found in
[SICP](https://github.com/sarabander/sicp-pdf/blob/master/sicp.pdf)

Includes a standard library of stream classes to be re-used
easily.

#### adams
Adams is a UNIX system administrator written in Common Lisp.
It produces commands for the shell (/bin/sh) for local or
remote hosts using
<a href="https://www.openssh.com/" target="_blank">SSH</a>
in order to retrieve and modify a UNIX system status.

Currently it allows automated administration of users, groups and
packages on Linux and OpenBSD without any additional requirement
or installation on the target machines.

&copy; 2018-2020 kmx.io
