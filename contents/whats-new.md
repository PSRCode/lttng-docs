---
id: whats-new
---

The **LTTng 2.5** toolchain introduces many interesting features, some
of them which have been requested by users many times.

It is now possible to
[save and restore tracing sessions](#doc-saving-loading-tracing-session).
Sessions are saved to and loaded from XML files located by default in
a subdirectory of the user's home directory. LTTng daemons
are also configurable by configuration files as of LTTng-tools 2.5.
This version also makes it possible to load user-defined kernel probes
with the new session daemon's `--kmod-probes` option (or using
the `LTTNG_KMOD_PROBES` environment variable).

[`tracef()`](#doc-tracef) is a new instrumentation facility in
LTTng-UST 2.5 which makes it possible to insert `printf()`-like
tracepoints in C/C++ code for quick debugging. LTTng-UST 2.5 also
adds support for perf
<abbr title="Performance Monitoring Unit">PMU</abbr> counters in user
space on the x86 architecture
(see [Adding some context to channels](#doc-adding-context)).

As of LTTng-modules 2.5, a new
[LTTng logger ABI](#doc-proc-lttng-logger-abi)
is made available, making tracing Bash scripts, for example, much more
easier (just `echo` whatever you need to record to `/proc/lttng-logger`
while tracing is active).
On the kernel side, some tracepoints are added: state dumps of block
devices, file descriptors, and file modes, as well as
<a href="http://en.wikipedia.org/wiki/Video4Linux" class="ext">V4L2</a>
events. Linux 3.15 is now officially supported, and system call tracing
is now possible on the MIPS32 architecture.
