# StructaLab — instructions for Claude Code

## Project
StructaLab sells 3 civil-engineering tools: Structa Pro ($25), Structa BBS ($15), Structa Continuous ($19), in USD.
Sold on Shopify (znf6s3-r4.myshopify.com), Gumroad, Payhip. Instagram is the marketing channel.
Owner: civil engineering student, Windows laptop, 8 GB RAM. Keep tools, builds and dependencies light.

## How to answer
- Lead with the answer. Keep it short. No filler praise.
- Tag key claims [Certain], [Likely] or [Guessing].
- If I'm wrong, say "I disagree because..." and give a better option.
- Ask at most one question, and only if it changes the work.
- Confirm the plan before building big files. Then give the whole file once.
- For engineering math, show formulas and assumptions briefly, and flag anything to check against a code or by hand.

## Hard rules (never break)
1. NEVER ship, upload, zip or commit anything in `seller_only_DO_NOT_SHIP/` (private.jwk, content.key, test keys). Check every zip before release.
2. No personal info (my name, email, address) in listings, product files or public pages. Use placeholders like [YOUR FULL LEGAL NAME].
3. Ask me before publishing, unpublishing, changing prices or deleting anything on any store.
4. Never create accounts, accept terms or enter payment details for me.
5. Don't assume my country. North Cyprus (TRNC) unless I say otherwise.

## Release checklist (run for every new build)
1. Build the zip into `dist/`.
2. List its contents and confirm no seller-only files are inside.
3. Record file name + byte size + version in `RELEASES.md`.
4. Upload the SAME file to Shopify, Gumroad and Payhip, then compare byte sizes on each platform with RELEASES.md. Old builds were left on stores before.
5. Test a licence key: keys are bound to the buyer's name and issued by hand by email.

## Shopify gotchas
- A product only shows on the store when it is ACTIVE and published to the Online Store sales channel, and is in the homepage collection.
- Claude can't publish themes it didn't create. I publish themes myself.
- Claude's screenshot tool can't render the theme, so ask me for a screenshot to check visuals.
- Design: product-first, blueprint texture background. Check text contrast on every change (we had navy text on navy).
- The store is password-locked (`structa`) and checkout is blocked until I upgrade from trial.

## Files
- Product pages / tools: `items/` (`Structa.html`, `Structa_Pro.html`, `Structa_BBS.html`, `Structa_Continuous.html`).
- Cover images: `covers/`.
- Licence agreements: `EULA_Structa_Pro.txt`, `EULA_Structa_BBS.txt`, `EULA_Structa_Continuous.txt` (root).
- Not in this folder yet: store policies (7-day refund, named-person licence, no professional advice), legal notice (placeholders to fill), Instagram posts. Create them here when needed, e.g. `store/` and `brand/instagram/`.

## Working style
- Test demand cheaply before building big features (a post, a waitlist, a discount code).
- Work in stages on long tasks, and stop to ask before the next stage.
- At the end of a session, update `RELEASES.md` and a short `STATUS.md` (what's done, what's waiting on me).
