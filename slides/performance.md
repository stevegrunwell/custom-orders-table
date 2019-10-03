## What else can be done?

* <!-- .element: class="fragment" --> Stay current
* <!-- .element: class="fragment" --> Stay lean
* <!-- .element: class="fragment" --> Stay cached
* <!-- .element: class="fragment" --> Stay clean

Note:

Keep WooCommerce, WordPress, and PHP up-to-date.
- PHP 7.0 roughly doubled the speed of PHP 5.6
- Fewer resources needed => get further with less

Trim down the number of scripts being loaded.
- The fastest code is code you don't have to run
- Watch out for plugins that can kill your performance

Cache as much as you can, but be careful
- Cart + checkout pages shouldn't be cached, as that'll cause all kinds of pain
- An area we've spent a lot of time focusing on at Liquid Web

Optimize media
- Strip EXIF data
- Don't upload media larger than you need
- TinyPNG, EWWW Image Optimizer, Photon
