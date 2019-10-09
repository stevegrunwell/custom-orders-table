## Database Performance

<div class="row fragment" data-fragment-index="0">
    <div class="col fragment-replacement">
        <h3>Reading</h3>
        <span class="fragment fade-out" data-fragment-index="2"><span class="fragment fade-in fade-in-out giant-emoji" data-fragment-index="0">😄</span></span>
        <span class="fragment fade-out" data-fragment-index="4"><span class="fragment fade-in giant-emoji" data-fragment-index="2">🙂</span></span>
        <span class="fragment fade-in giant-emoji" data-fragment-index="4">😐</span>
    </div>
    <div class="col fragment-replacement">
        <h3>Writing</h3>
        <span class="fragment fade-out giant-emoji" data-fragment-index="1">😄</span>
        <span class="fragment fade-out" data-fragment-index="2"><span class="fragment fade-in giant-emoji" data-fragment-index="1">😅</span></span>
        <span class="fragment fade-out" data-fragment-index="3"><span class="fragment fade-in giant-emoji" data-fragment-index="2">😐</span></span>
        <span class="fragment fade-out" data-fragment-index="4"><span class="fragment fade-in giant-emoji" data-fragment-index="3">😟</span></span>
        <span class="fragment fade-in giant-emoji" data-fragment-index="4">😖</span>
    </div>
</div>

<p class="fragment fragment-replacement" data-fragment-index="0">
    Table size:
    <span class="fragment fade-out" data-fragment-index="1">10</span>
    <span class="fragment fade-out" data-fragment-index="2"><span class="fragment fade-in" data-fragment-index="1">10k</span></span>
    <span class="fragment fade-out" data-fragment-index="3"><span class="fragment fade-in" data-fragment-index="2">1M</span></span>
    <span class="fragment fade-out" data-fragment-index="4"><span class="fragment fade-in" data-fragment-index="3">10M</span></span>
    <span class="fragment fade-in" data-fragment-index="4">10M w/ concurrency</span>
</p>

Note:

Generally speaking, database writes are more expensive than reads.
- Constraints: uniqueness, column length, etc.
- Check and update indexes

On small databases, this is negligible as everything might just be held in memory.

As the size grows, these checks get more expensive. Longer writes + table locking can impact performance.

If you're handling multiple checkouts at the same time, these slow writes start to pile up. Customers start wondering why you're taking so long to take their money, and reading all of this information starts getting more expensive, too. These 40M rows are dragging down your site performance, but that's just how WooCommerce works, right?
