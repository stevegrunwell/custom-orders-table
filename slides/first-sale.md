## Your First Sale

<ul class="collapsing-list">
    <li class="fragment" data-fragment-index="0">
        Billing details
        <ul class="fragment fade-out" data-fragment-index="1">
            <li>First name, last name</li>
            <li>Street address, city, state, postal code, etc.</li>
        </ul>
    </li>
    <li class="fragment" data-fragment-index="1">
        Shipping details
        <ul class="fragment fade-out" data-fragment-index="2">
            <li>First name, last name</li>
            <li>Street address, city, state, postal code, etc.</li>
        </ul>
    </li>
    <li class="fragment" data-fragment-index="2">
        Payment data
        <ul class="fragment fade-out" data-fragment-index="3">
            <li>Payment method</li>
            <li>Currency</li>
            <li>Shipping costs</li>
            <li>Discounts</li>
            <li>Totals</li>
        </ul>
    </li>
    <li class="fragment" data-fragment-index="3">
        Tax data
        <ul class="fragment fade-out" data-fragment-index="4">
            <li>Cart tax, shipping tax, etc.</li>
        </ul>
    </li>
    <li class="fragment" data-fragment-index="4">
        Customer data
        <ul class="fragment fade-out" data-fragment-index="5">
            <li>User-agent, IP address</li>
        </ul>
    </li>
    <li class="fragment" data-fragment-index="5">
        Refunds
        <ul>
            <li>Amount, notes, approvals, etc.</li>
        </ul>
    </li>
</ul>

Note:

You happen to be looking at the database when you make your first sale, and you see a bunch of new entries in the postmeta table.

Billing details. Shipping details. Payment information. Tax data. Around 40 postmeta entries, and that's for *each* order.

Refunds push this number even higher — amounts, who approved it, notes, dates
