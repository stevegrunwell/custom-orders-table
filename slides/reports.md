## Reporting

<div class="fragment-replacement">
    <img src="resources/loading.svg" alt="Loading animation" class="seamless fragment fade-out" data-fragment-index="0" />
    <span class="fragment fade-in giant-emoji" data-fragment-index="0" style="margin-top: 3rem;">😱</span>
</div>

Note:

You log into WordPress and load up the WooCommerce reports. And you wait. And wait. And eventually you might get the numbers, but you're noticing that your site is slow. You think back to that first order and those 40-ish postmeta rows, then you start doing the math.

One million orders times 40 is 40 million rows in that postmeta table. If you're querying that data, MySQL is attempting to process all of that order data *plus* anything else in post meta — all of your custom fields for posts, pages, products, and more. That's a lot of data being stuffed into what amounts to a simple key:value store.
