# Custom Tables & the Checkout Bottleneck

Each time an order is made on a WooCommerce store, dozens of entries are added to the WordPress post-meta database table. On smaller stores, these [expensive] writes are at most a minor nuisance, but on stores with large volumes of orders, these writes become a critical performance bottleneck.

These post-meta entries are all known values, though: customer data, billing and shipping addresses, payment information, etc. What if there was a way to flatten all of these writes into a single row in a database table designed just for order data? What if our store could go from writing ~40 entries each time an order is made to just writing two?

This session is a case study of [the WooCommerce Custom Orders Table plugin](https://github.com/liquidweb/woocommerce-custom-orders-table/), a collaboration between Liquid Web and Mindsize. We’ll explore what it is, how it works, and the impact it’s already had on both the stores running it and WooCommerce as a platform. Finally, we’ll discuss the future of the plugin, including further enhancements and a possible path towards inclusion in WooCommerce core.

:sparkles: **[View slides](http://stevegrunwell.github.io/custom-orders-table)** :sparkles:

## Presentation History

* [WooSesh 2019](https://woosesh.com) — October 10, 2019
