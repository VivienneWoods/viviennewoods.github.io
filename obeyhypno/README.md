# Obey Hypno — starter site
A self-contained static site under `/obeyhypno/`, staged in the existing GitHub Pages repo without altering its original homepage.

## Files
- `index.html`: landing page / 18+ notice
- `approved/index.html`: informational approval-return page; does NOT assert payment confirmation
- `denied/index.html`: informational denial-return page

## Production deployment
For a separate Cloudflare Pages project, import this GitHub repository and set the **build output directory** to `obeyhypno` with no build command, then attach `obeyhypno.com` as a custom domain. Check this setup against the actual Pages import UI before going live. Do NOT point the domain at the existing repository-level GitHub Pages homepage: that belongs to a different site.

If hosted from the domain root, the proposed redirect paths are:
- `https://obeyhypno.com/approved/`
- `https://obeyhypno.com/denied/`

## Important: payments NOT yet integrated
The static site cannot safely process server-to-server payment notifications. A provider-specific, authenticated backend webhook handler is required; never register a guessed URL as operational. Do NOT enable checkout or automatic content access until provider identification, webhook authentication, a test successful payment, a failed payment, cancellation and refund behavior are verified. The prior WooCommerce-specific `?wc-api=...` URLs must NOT be used for this new site.

## Before accepting purchases
Provide complete merchant contact, legal terms, privacy notice, digital fulfillment and refund policies, approved content catalog and prices, age restrictions and provider-required disclosures. These must reflect actual business practices.
