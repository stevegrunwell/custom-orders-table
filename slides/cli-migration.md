### Migrating data via WP-CLI

<p class="fragment" data-fragment-index="0">Importing orders into the table:</p>

<pre class="fragment-replacement fragment hljs" data-fragment-index="0" style="margin-bottom: 2em;"><code class="fragment fade-out lang-sh" data-fragment-index="1">$ wp wc orders-table migrate</code><code class="fragment fade-in lang-sh" data-fragment-index="1">$ wp wc orders-table migrate --save-post-meta</code></pre>

<p class="fragment" data-fragment-index="2">Moving order data back into <code>wp_postmeta</code></p>

<pre class="fragment hljs" data-fragment-index="2"><code class="lang-sh">$ wp wc orders-table backfill</code></pre>

Note:

Currently, the plugin uses WP-CLI to migrate data.

Migrate command will take all of the post meta, save it into the custom table, then remove the entries from wp_postmeta.

If you don't mind the duplicate data, you can also choose to keep the post meta for existing orders with the `--save-post-meta` flag.

The "backfill" command does the opposite — move everything out of the custom table back into post meta.
