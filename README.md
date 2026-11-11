# sytals store starter

This is a static, black-and-white storefront preview. It does not take payments or issue licenses yet.

## Preview
Open `index.html` in a browser.

## Free hosting
1. Create a public GitHub repository named `sytals-store`.
2. Upload `index.html` to the repository root.
3. In Settings > Pages, choose Deploy from a branch, `main`, `/ (root)`.
4. Visit `https://YOUR-USERNAME.github.io/sytals-store/` after deployment.

## Production checkout and licensing architecture
1. Set prices and determine an eligible merchant account owner. Confirm the payment processor permits this type of software.
2. Create four hosted checkout products/prices (1 day, 7 days, 30 days, lifetime).
3. Add a server-side checkout session endpoint. Never put payment secret keys in the static site.
4. Verify signed payment webhooks and payment completion server-side, then create an idempotent license record with purchase ID, product, expiry, activation status, and purchaser contact.
5. Deliver the key by an approved transactional email provider or secure receipt page.
6. Have the desktop app call a TLS-protected activation API. On first activation bind the license to a hashed device identifier; validate expiration on the server. Provide reset and refund/revocation handling.
7. Publish a signed, scanned installer from a trusted release location and add the download link.
8. Add terms, privacy notice, refund policy, support contact, and appropriate security/rate limits.

No live checkout is included because merchant credentials, pricing, backend hosting, and existing licensing API details have not been provided.
