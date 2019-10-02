### Solution: Extend the WooCommerce Test Framework

1. <!-- .element: class="fragment" --> Install WooCommerce as a **dev** dependency
2. <!-- .element: class="fragment" --> Bootstrap WooCommerce's bootstrap
3. <!-- .element: class="fragment" --> Activate the plugin
4. <!-- .element: class="fragment" --> Extend `WC_Unit_Test_Case`

[stevegrunwell.com/blog/writing-woocommerce-extensions](https://stevegrunwell.com/blog/writing-woocommerce-extensions/)<!-- .element: class="fragment" style="font-size: smaller;" -->

Note:

Since WooCommerce already has a canonical test suite, we can use that as the basis for our plugin's test suite.

First, we install the `master` branch of WooCommerce as a dev dependency using Composer
- Need to install from source, as tests are removed from zip/tar archives

Next, we write our PHPUnit bootstrap file to first load WooCommerce's PHPUnit bootstrap file.
- Let WooCommerce handle setting up WooCommerce

Finally, we do anything necessary to inject our plugin into the environment, then let our PHPUnit test classes extend `WC_Unit_Test_Case`.
