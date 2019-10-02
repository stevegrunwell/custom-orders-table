## C.R.U.D.

<p class="fragment" data-fragment-index="0" style="margin-bottom: 1em;">Create, Read, Update, &amp; Delete</p>

<pre class="fragment fragment-replacement hljs" data-fragment-index="1"><code class="fragment fade-out lang-php" data-fragment-index="2"># Older versions of WooCommerce
get_post_meta( $order_id, '_billing_first_name', true );</code><code class="fragment fade-in lang-php" data-fragment-index="2"># WooCommerce 3.0 and newer
$order->get_billing_first_name();</code></pre>

Note:

Plugin uses the CRUD API, introduced in WooCommerce 3.0
- Instead of explicitly calling get_post_meta(), we call getter methods

This abstraction lets us store the data in a custom table that's tailor-made for WooCommerce order data.
- Columns for billing_first_name, billing_last_name, etc.

Instead of writing 40 post meta entries, we can write one entry per order.
- Can also use proper column types instead of cramming everything into LONGTEXT
    - Bring down data size and let us get smarter with indexes
