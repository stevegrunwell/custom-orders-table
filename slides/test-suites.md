### A Tale of Two Test Suites

Repository has two test suites:

1. Plugin tests
2. WooCommerce w/ plugin enabled

Note:

With our tests based on the WooCommerce test framework, I decided to define two test suites:
- Tests just for our plugin
- Run through all of WooCommerce's tests with our plugin active

The **goal** is to see no difference. Remember: we want to be invisible.

Bonus: if something not yet released is going to break the plugin, we'll know about it!
