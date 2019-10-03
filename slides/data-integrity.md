### Ensuring data integrity

* <!-- .element: class="fragment" --> Assume data lives in custom table
  * Otherwise, attempt to auto-migrate
* <!-- .element: class="fragment" --> Write all new data to custom table
* <!-- .element: class="fragment" --> Data transformations

Note:

When reading data from the custom table, we want to start with the assumption that the data exists in the custom table
- If it doesn't, try to move the data in there

Staring with the assumption of the table == better performance long-term.

When pulling data out, make sure we're returning the types that WooCommerce and other extensions expect
- Sometimes a boolean TRUE gets cast to "yes" or "on"
