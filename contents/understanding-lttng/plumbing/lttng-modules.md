---
id: lttng-modules
---

The LTTng Linux kernel modules provide everything needed to trace the
Linux kernel: various probes, a ring buffer implementation for a
consumer daemon to read trace data and the tracer itself.

Only in exceptional circumstances should you ever need to load the
LTTng kernel modules manually: it is normally the responsability of
`root`'s session daemon to do so. If you were to develop your own LTTng
probe module, however&mdash;for tracing a custom kernel or some kernel
module (this topic is covered in the
[Linux kernel](#doc-instrumenting-linux-kernel) instrumenting guide of
the [Using LTTng](#doc-using-lttng) chapter)&mdash;you should either
load it manually, or use the `--kmod-probes` option of the session
daemon to load a specific list of kernel probes (beware, however,
that the `--kmod-probes` option specifies an _absolute_ list, which
means you also have to specify the default probes you need). The
session and consumer daemons of regular users do not interact with the
LTTng kernel modules at all.

LTTng kernel modules are installed, by default, in
<code>/usr/lib/modules/<em>release</em>/extra</code>, where
<code><em>release</em></code> is the kernel release
(see `uname --kernel-release`).
