---
id: opensuse
---

openSUSE 13.1 and openSUSE 13.2 have LTTng 2.6 packages. To install
LTTng 2.6, you first need to add an entry to your repository
configuration. All LTTng repositories are available
<a href="http://download.opensuse.org/repositories/devel:/tools:/lttng/" class="ext">here</a>.
For example, the following commands adds the LTTng repository for
openSUSE&nbsp;13.1:

<pre class="term">
sudo zypper addrepo http://download.opensuse.org/repositories/devel:/tools:/lttng/openSUSE_13.1/devel:tools:lttng.repo
</pre>

Then, refresh the package database:

<pre class="term">
sudo zypper refresh
</pre>

and install `lttng-tools`, `lttng-modules` and `lttng-ust-devel`:

<pre class="term">
sudo zypper install lttng-tools
sudo zypper install lttng-modules
sudo zypper install lttng-ust-devel
</pre>

<div class="tip">
<p>
  <span class="t">Note:</span> If you need to trace
  <a href="#doc-java-application">Java applications</a> on
  openSUSE, you need to build and install LTTng-UST 2.6
  <a href="#doc-building-from-source">from source</a> and use the
  <code>--enable-java-agent-jul</code>,
  <code>--enable-java-agent-log4j</code>, or
  <code>--enable-java-agent-all</code> options.
</p>
</div>
