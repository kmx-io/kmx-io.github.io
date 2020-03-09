---
title: C, Common Lisp, UNIX
---

## 1 Hosting
[OpenBSD](http://www.openbsd.org) is rock solid.

## 2 Development
Open-source based development, mainly targeting UNIX and
Common Lisp.

### 2.1 C
[C](https://en.wikipedia.org/wiki/C_(programming_language))
is probably the true reason for the success of
[UNIX](https://en.wikipedia.org/wiki/Unix)
as an operating system.

#### 2.1.1 Rtbuf
[Rtbuf](https://rtbuf.kmx.io/)
is BSD licensed ANSI C for realtime signal processing.

It seems that these last years most programming action happens in
high level programming languages which rely on garbage collectors
to free memory. The problem of a GC is that it induces latency because
while the program is stopped collecting free memory it stops other
processing so real-time applications are not possible with most modern
programming languages. Multi-processor safe and real-time garbage
collectors are not open source and very expensive pieces of software.

A possible solution to handle real time computation on a garbage
collected platform is to offload real-time computations to a C server
running rtbuf which has no garbage collector and is highly portable.

Possible applications include audio and video applications, games
and experimental setups.

Current audience is developers. Status : alpha.

See the project page on Github :
[https://github.com/rtbuf/rtbuf](https://github.com/rtbuf/rtbuf)

### 2.2 C++

### 2.3 Common Lisp
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

#### 2.3.1 cffi-posix
[cffi-posix](https://github.com/cffi-posix)
is an open-source project to portably and regularly expose the
[POSIX](http://pubs.opengroup.org/onlinepubs/9699919799/)
API to Common Lisp programs using
[CFFI](https://common-lisp.net/project/cffi/)

#### 2.3.2 cl-stream
[cl-stream](https://github.com/cl-stream)
is an experimental project to replace Common Lisp streams with
streams supporting any type of data and non-blocking semantics,
following principles found in
[SICP](https://github.com/sarabander/sicp-pdf/blob/master/sicp.pdf)

Includes a standard library of stream classes to be re-used
easily.

cl-stream streams are compatible with
[cffi-epoll](https://github.com/cffi-posix/cffi-epoll)
and
[cffi-kqueue](https://github.com/cffi-posix/cffi-kqueue)
. See
[Thot](https://github.com/RailsOnLisp/thot)
for an example usage.

#### 2.3.3 adams
[![(adams)](https://avatars1.githubusercontent.com/u/38501850)
 Adams](https://github.com/cl-adams/adams)
is a UNIX system administrator written in Common Lisp.
It produces commands for the shell (/bin/sh) for local or
remote hosts using
<a href="https://www.openssh.com/" target="_blank">SSH</a>
in order to retrieve and modify a UNIX system status.

Currently it allows automated administration of users, groups and
packages on Linux and OpenBSD without any additional requirement
or installation on the target machines.

#### 2.3.4 RailsOnLisp
[![ROL](https://avatars2.githubusercontent.com/u/11281575)
 RailsOnLisp](https://github.com/RailsOnLisp)
Common Lisp MVC web development framework inspired by
[RubyOnRails](https://rubyonrails.org/).

#### 2.3.5 Thot
[Thot](https://github.com/RailsOnLisp/thot)
Threaded HTTP server supporting epoll and kqueue in Common Lisp.

### 2.4 Ruby
[Ruby](https://www.ruby-lang.org/) is nice.

-----

&copy; 2018-2020 kmx.io
