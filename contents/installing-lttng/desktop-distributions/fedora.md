---
id: fedora
---

Fedora 22 and Fedora 23 ship with official LTTng-tools 2.6 and
LTTng-UST 2.6 packages. Simply use `yum`:

<pre class="term">
sudo yum install lttng-tools
sudo yum install lttng-ust
sudo yum install lttng-ust-devel
</pre>

LTTng-modules 2.6 still needs to be built and installed from source. For
that,  make sure that the `kernel-devel` package is already installed
beforehand:

<pre class="term">
sudo yum install kernel-devel
</pre>

Proceed on to fetch
[LTTng-modules 2.6's source](#doc-building-from-source). Build and
install it as follows:

<pre class="term">
KERNELDIR=/usr/src/kernels/$(uname -r) make
sudo make modules_install
</pre>
