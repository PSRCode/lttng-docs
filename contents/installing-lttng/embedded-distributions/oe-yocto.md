---
id: oe-yocto
---

LTTng 2.6 recipes are available in the
<code><a href="http://layers.openembedded.org/layerindex/branch/master/layer/openembedded-core/" class="ext">openembedded-core</a></code>
layer of OpenEmbedded since February 8th, 2015 under the following
names:

  * `lttng-tools`
  * `lttng-modules`
  * `lttng-ust`

Using BitBake, the simplest way to include LTTng recipes in your
target image is to add them to `IMAGE_INSTALL_append` in
`conf/local.conf`:

~~~ text
IMAGE_INSTALL_append = " lttng-tools lttng-modules lttng-ust"
~~~

If you're using Hob, click _Edit image recipe_ once you have selected
a machine and an image recipe. Then, under the _All recipes_ tab, search
for `lttng` and include the three LTTng recipes.

<div class="tip">
<p>
  <span class="t">Note:</span> If you need to trace
  <a href="#doc-java-application" class="int">Java applications</a> on
  OpenEmbedded/Yocto, you need to build and install LTTng-UST 2.6
  <a href="#doc-building-from-source" class="int">from source</a> and
  use the <code>--enable-java-agent-jul</code>,
  <code>--enable-java-agent-log4j</code>, or
  <code>--enable-java-agent-all</code> options.
</p>
</div>
