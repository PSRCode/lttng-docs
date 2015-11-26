---
id: buildroot
---

LTTng 2.6 packages in Buildroot 2015.05 are named `lttng-tools`,
`lttng-modules`, and `lttng-libust`.

To enable them, start the Buildroot configuration menu as usual:

<pre class="term">
make menuconfig
</pre>

In:

  * _Kernel_: make sure _Linux kernel_ is enabled
  * _Toolchain_: make sure the following options are enabled:
    * _Enable large file (files > 2GB) support_
    * _Enable WCHAR support_

In _Target packages_/_Debugging, profiling and benchmark_, enable
_lttng-modules_ and _lttng-tools_. In
_Target packages_/_Libraries_/_Other_, enable _lttng-libust_.

<div class="tip">
<p>
  <span class="t">Note:</span> If you need to trace
  <a href="#doc-java-application">Java applications</a> on
  Buildroot, you need to build and install LTTng-UST 2.6
  <a href="#doc-building-from-source">from source</a> and use the
  <code>--enable-java-agent-jul</code>,
  <code>--enable-java-agent-log4j</code>, or
  <code>--enable-java-agent-all</code> options.
</p>
</div>
