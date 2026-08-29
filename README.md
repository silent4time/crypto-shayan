# CryptoPay WooCommerce — Security-Hardened Fork

Independent, unofficial fork of [CryptoPay WooCommerce](https://cryptopay-woocommerce.beycanpress.com/) (original publisher: BeycanPress), based on official version **2.4.5**.

This is **not** an official BeycanPress product. It's an independent security review of the free (Lite) version of the plugin. No Full/Pro features have been added.

## Current version

`2.4.5-security.3` — full details in [CHANGELOG.md](./CHANGELOG.md)

## What changed

Summary (see CHANGELOG.md for full details):

- Automatic update checks & one-click "Update now" from this GitHub repo's Releases
- Closed public REST API access (order-ownership check)
- Removed `serialize()`/`unserialize()` in favor of JSON
- Stricter wallet-address validation (regex instead of length check)
- Added simple IP-based rate limiting on public endpoints

## Publishing an update (for the auto-updater)

1. Bump the version in `index.php` and `app/Loader.php`.
2. Commit, tag (`vX.Y.Z-security.N`), and push.
3. Create a GitHub **Release** from that tag and attach the install zip as a release asset.

Sites running this plugin will then see an update notice automatically.

## Installation

Upload `cryptopay-woocommerce-v2.4.5-security.3.zip` directly via WordPress admin (Plugins → Add New → Upload Plugin). Deactivate/remove the official BeycanPress version first if it's installed.

## Before using in production

Test a full checkout flow on staging — both as a logged-in user and as a guest. See "Upgrade notes" in CHANGELOG.md.

## License

GPLv3 (same as the original plugin)

فارسی: [README-fa.md](./README-fa.md)
