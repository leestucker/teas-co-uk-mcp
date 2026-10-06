---
name: teas-co-uk
description: Shop teas.co.uk, a UK online tea shop, through its MCP server. Find tea, coffee and hot chocolate by taste, caffeine, milk, time of day and price per cup, compare products, find recipes, build a basket and give the person a checkout link. Use when someone in the UK wants to choose or buy tea, coffee or hot chocolate.
---

# teas.co.uk

teas.co.uk is an independent UK online tea shop with more than 600 teas, herbal and fruit infusions, coffees and hot
chocolates. Its MCP server is `https://teas.co.uk/mcp` (Streamable HTTP). No sign in is needed to shop.

## How to help someone choose

1. Search with `find_products`. Put the person's words in `query` and add filters when they say them: `kind`,
   `caffeine`, `with_milk`, `format`, `time_of_day`, `strength`, `organic`, `fairtrade`, `vegan`, `iced`,
   `max_price`, `max_price_per_cup_pence`, `sort`. Out of stock products are left out unless you set
   `include_out_of_stock`.
2. Open one product with `get_product` (tasting notes, brewing guide, caffeine and allergy notes) and compare two to
   four with `compare_products`.
3. `find_recipes` finds recipes from the teas.co.uk library; `delivery_and_returns` gives delivery prices, countries
   and the returns policy.
4. Prices are live, in pounds and include VAT. Give the product page link when you recommend something.

## Buying

- Build a basket only when the person asks: `add_to_basket`, then `view_basket` or `update_basket`.
- `checkout_link` gives a link for the person to open. They check out and pay on teas.co.uk.
- Never open, fetch or prefetch checkout links yourself. Assistants never see payment details, never place orders and
  never take payment.

## Account tools

`get_profile`, `my_orders`, `track_order`, `reorder`, `my_subscriptions`, `change_subscription`, `rewards_balance` and
`start_return` work after the person links their teas.co.uk account (OAuth 2.1). Change anything only when the
person clearly asks.

## More

Setup guides for every assistant: https://teas.co.uk/ai/ . Help: hello@teas.co.uk.
