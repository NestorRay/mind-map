<template>
  <div>
    <h1>Formula 插件</h1>
<blockquote>
<p>v0.7.2+</p>
</blockquote>
<blockquote>
<p>该插件仅在富文本模式下支持，所以需要在注册了RichText插件的前提下使用</p>
</blockquote>
<p>该插件用于支持给节点插入公式。</p>
<h2>注册</h2>
<pre class="hljs"><code><span class="hljs-keyword">import</span> MindMap <span class="hljs-keyword">from</span> <span class="hljs-string">&#x27;simple-mind-map&#x27;</span>
<span class="hljs-keyword">import</span> Formula <span class="hljs-keyword">from</span> <span class="hljs-string">&#x27;simple-mind-map/src/plugins/Formula.js&#x27;</span>

MindMap.usePlugin(Formula)
</code></pre>
<p>注册完且实例化<code>MindMap</code>后可通过<code>mindMap.formula</code>获取到该实例。</p>
<h2>使用</h2>
<p>注册了该插件后，可以使用命令<code>INSERT_FORMULA</code>来给节点插入指定公式：</p>
<pre class="hljs"><code>mindMap.execCommand(<span class="hljs-string">&#x27;INSERT_FORMULA&#x27;</span>, <span class="hljs-string">&#x27;a^2&#x27;</span>)
</code></pre>
<p>上述命令会给当前激活的节点插入<code>a^2</code>公式。</p>
<p>如果要指定给某个或某些节点插入公式，可以传递第二个参数：</p>
<pre class="hljs"><code>mindMap.execCommand(<span class="hljs-string">&#x27;INSERT_FORMULA&#x27;</span>, <span class="hljs-string">&#x27;a^2&#x27;</span>, [Node])
</code></pre>
<p>通过第二个参数传入指定的节点实例即可。</p>

  </div>
</template>

<script>
export default {

}
</script>

<style>

</style>