# Proposal: stock and trend tracker for small retail shops

## The idea I'll build

A stock and sales tracker for small retail shops that takes almost no effort to use. It shows the owner when a trending item is slowing down, how much to reorder, and when to put slow stock on a clearance offer before it goes dead.

**First user:** My father's shop in Agra, which sells artificial jewellery, cosmetics and small girls' items (hairbands, claw clips, rubber bands). He's a guaranteed first user, and I can test with him every day.

**Later users:** Similar small retail shops in Agra. The free apps (Vyapar, Khatabook) handle billing, not what's going out of fashion.

## Why this idea

I combined ideas #1 and #2 (a stock tracker and a shared trend feed). Of my three ideas, this one is the strongest:
- It's the strongest problem I've found, backed by two rounds of interviews (see [feedback.md](feedback.md)).
- I have a guaranteed first user and can test daily.
- The money lost is real: about ₹1.5–2 lakh of stock is sitting in the godown.

The other two ideas are still options: the clinic token system and cafe QR ordering near GNDEC (see [ideas.md](ideas.md)).

## The problem

1. Something becomes popular, so he buys it in bulk. The quantity is a guess, and the wholesaler pushes him to buy more.
2. Only part of it sells before the trend ends. Trends can slow down within about a week (e.g. 5 dozen claw clips).
3. He notices the slowdown by eye, days late, because the register only records totals, not items.
4. Wholesalers don't take stock back, so the rest becomes dead stock: sold at half rate or stored in the godown, some of it 3–4 years old.
5. The next trend comes and the cycle repeats. Only 1 in 3–4 bulk deals works out.

He's stuck between two fears: **dead stock** if he buys too much, and **running out** if he buys too little (he tried buying less, and he ran out).

## What I learned that changed the idea

- **A shared trend platform is weaker than I thought.** He trusts the WhatsApp group only about half the time. Wholesalers post their own stock there, and local taste differs from Delhi.
- **The real need is spotting slowdowns early and buying the right quantity**, using his own shop's sales data.
- **Data entry has to be almost zero effort**, like one tap or a photo. A billing app already failed because entering 300 designs during rush hours took too long.
- **A multi-shop platform needs many shops before it's useful.** So it starts as a single-shop tool that's useful on its own.

## What I'll build

### Version 1 (my father's shop only)
- **Quick sales logging:** One tap per sale, or a photo, during rush hours. No typing out 300 designs upfront.
- **Item-level sales tracking:** How fast each item sells and how much is left. This is the data the register doesn't capture.
- **Slowdown alert:** Flags an item when its sales start dropping, so he stops reordering in days, not weeks.
- **Reorder suggestion:** How much to buy next time, based on how fast similar items sold before.
- **Clearance suggestion:** Which slow items to put on offer now, while they can still sell at a decent price.

### Later (once 10–20 shops are using it)
- **Shared trend feed:** Shop owners in the same city post what's trending and what customers are asking for, alongside each shop's own sales data.

### Not building now
- Full billing or accounting (Vyapar and Khatabook already do this)
- The shared trend feed, until enough shops are using the tracker

## Risks and open questions

- **Retailer, wholesaler or both?** I told my partner he "sells to retailers," but the interviews describe a shop selling to customers. This changes who uses the product and what the right buying quantities are.
- **Will he actually log sales?** Data entry killed the last app, so this is the biggest risk.
- **Will he pay?** I haven't asked yet whether he'd pay or what he pays for anything today.
- **Better demand signal:** His customers (college girls and housewives) may tell him what they want before he stocks it, which could be more reliable than the WhatsApp group.
- **Market size:** I need to check how many similar shops are actually in his market in Agra.

## How I'll test it

1. Count one godown shelf with him to turn "a godown full" into a real number.
2. Track a few fast-moving items by hand (paper or a simple sheet) for 1–2 weeks to see whether slowdowns can be spotted early.
3. Build the simplest one-tap logging and test it with him during rush hours.
4. Interview the two shop owners he referred me to, to see whether the problem is common.
5. Ask directly whether he'd pay, and how much.
