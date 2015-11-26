---
id: ubuntu
---

LTTng 2.6 is packaged in Ubuntu 15.10 _Wily Werewolf_. For other
releases of Ubuntu, you need to build and install LTTng 2.6
[from source](#doc-building-from-source). Ubuntu 15.04 _Vivid Vervet_
ships with <a href="/docs/v2.5/" class="ext">LTTng 2.5</a>, whilst
Ubuntu 16.04 _Xenial Xerus_ ships with
<a href="/docs/v2.7/" class="ext">LTTng 2.7</a>.

To install LTTng 2.6 from the official Ubuntu repositories,
simply use `apt-get`:

<pre class="term">
sudo apt-get install lttng-tools
sudo apt-get install lttng-modules-dkms
sudo apt-get install liblttng-ust-dev
</pre>

If you need to trace Java applications, you need to install the
LTTng-UST Java agent also:

<pre class="term">
sudo apt-get install liblttng-ust-agent-java
</pre>
