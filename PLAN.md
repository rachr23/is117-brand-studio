# UNFORM — T-shirt Plan (PLAN-001)

**Status:** Planning draft for peer review. **Issue:** [#6](https://github.com/rachr23/is117-brand-studio/issues/6). **Research:** [RESEARCH.md](RESEARCH.md). **Existing brand/spec:** [SPEC.md](SPEC.md).

## Audience and direction

Primary audience hypothesis: Alex, a college-age streetwear enthusiast who wants a distinctive white T-shirt and clear sizing. Secondary audience hypothesis: Jordan, a budget-conscious student who wants straightforward price and product information. These are assumptions, not validated customer research.

| Approach | Design and audience effect | Trade-off |
| --- | --- | --- |
| Modernist streetwear | Restrained grid, simple hierarchy and clear product information make sizing and shopping easy to scan. | May feel too conventional for UNFORM's rebellious identity. |
| Postmodernist streetwear **(chosen)** | Dark background, oversized typography, high contrast, asymmetry and UNFORM wordmark express individuality. | Experimental layouts must not hide sizing, prices or checkout controls. |

**Decision:** Preserve the existing postmodernist design and shared live style guide. Brand promise: **Different by Design**. Voice: bold, minimal, rebellious. Outlaw archetype. Product remains the same white T-shirt; do not assert unverified material, fit, shipping or sustainability claims.

## User stories, essential features and observable checks

| Story | Essential feature | Observable check |
| --- | --- | --- |
| As Alex, I want to see the shirt and its details so I can judge whether it matches my style. | Clear product image, visible sample price and concise description. | On desktop and narrow mobile, product and details remain visible and readable without horizontal scrolling. |
| As Alex, I want to choose a size so I can add the intended variant. | Accessible size selector and helpful validation. | Add without size: helpful message, no item added. Select size: bag shows that exact size. |
| As Jordan, I want to review and change my bag before checkout so I can control my total. | Bag summary with item, selected size, quantity, subtotal and remove/edit action. | Add then remove an item; bag count and total update correctly. |
| As a shopper, I want to complete a **simulated** checkout so I can see a confirmation without paying. | Demo checkout form, server-side validation, SQLite order persistence and confirmation number. | Submit valid sample details, receive a demo confirmation, restart the server and retrieve the saved order from SQLite. Invalid or empty inputs do not create orders. |

## Technical plan and boundary

- **Frontend:** Reuse existing HTML/CSS/JavaScript and the UNFORM styling in `public/`; preserve keyboard focus and mobile usability.
- **Backend:** Extend the existing Node.js server with endpoints for submitting a simulated order and reading its confirmation. Use SQLite as the **server-side persistent database**, not localStorage or sessionStorage as a substitute.
- **SQLite records:** Store an order ID, creation timestamp, demo status, and order line items (product ID, size, quantity, unit price). Validate supported sizes, positive quantities and calculate totals on the server. Use parameterized SQL and database transactions. Avoid saving real payment information or unnecessary personal details.
- **Checkout:** Prominently label **SIMULATED CHECKOUT — no real payment or shipment**. No payment processor, credit card fields, real purchase, accounts, or real fulfillment. Confirmation must refer to an order actually saved in SQLite.
- **Verification:** Start the server, submit a demo order, stop/restart the server, reopen the confirmation/order through its endpoint and confirm it persists. Test missing size, invalid quantity and empty bag. Check narrow/mobile view and keyboard navigation. Record actual commands and outcomes only after running them.
- **Deployment limitation:** A GitHub Pages static site cannot itself run a Node/SQLite backend. A deployed checkout needs a separate running backend with persistent storage, or a clearly documented local demo. Do not call a static browser-only bag a completed SQLite checkout.

## Two honest persuasion elements

1. **Reciprocity:** Offer helpful, no-pressure product information and an outfit-styling suggestion (e.g., pairing a white tee with wide-leg jeans). This gives shoppers useful guidance without inventing product claims.
2. **Commitment and consistency:** After the shopper voluntarily selects a size and adds it to the bag, show the exact selected size in the review screen and let them edit or remove it. The follow-through is transparent and reversible, not pressure to buy.

## Peer review and decision history

**Question to ask a classmate:** Can you explain the simulated-checkout story and show exactly how to verify that an order is saved in SQLite after restarting the server?

- Peer question / issue: **Awaiting actual reviewer feedback.**
- Decision: **Pending review.**
- Change/commit: This planning document is the initial draft; implementation is not complete.
- Verification: **Planned, not yet run for SQLite.**
- Resolution: Leave [issue #6](https://github.com/rachr23/is117-brand-studio/issues/6) open until feedback, changes and reviewer retry are documented.

## AI assistance

AI helped organize the planning draft from the existing UNFORM research and SPEC. The learner chose to preserve the existing postmodernist design. The stories and SQLite approach are proposed planning details, not claims of completed implementation or user testing.
