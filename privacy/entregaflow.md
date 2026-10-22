# Privacy policy — EntregaFlow


**Last updated:** 2026-10-22
**Who we are:** Brisolo, the maker of EntregaFlow. Contact: brisolo.support@gmail.com · support: https://github.com/brisolo/support/issues

## 1. What this product does

EntregaFlow is a WooCommerce plugin that asks the Correios (Brazilian postal service) API for SEDEX and PAC prices for a cart, using the shop owner's own Correios contract credentials.

## 2. Data we process

The plugin runs on the shop's own WordPress site. We (the plugin's maker) receive nothing from it: the plugin sends no data to us.

| Data | Why | Where it is processed | Kept for |
|---|---|---|---|
| Correios user, access code, postage card number and, when set, contract number and DR number (shop owner) | To authenticate with Correios and to quote with the shop's contract | The shop's database (WordPress option `entregaflow_settings`), unencrypted like other WooCommerce settings | Until the plugin is deleted (uninstall removes it) |
| A short-lived Correios access token | To avoid re-authenticating on every quote | The shop's database (a transient) | Up to its Correios expiry (about a day), or until the plugin is deleted |
| The last quote error per service (a message such as "Correios refused the credentials"), no personal data | To show the shop manager an admin notice until quotes work again | The shop's database (option `entregaflow_last_error`) | Until a quote works again or the plugin is deleted |
| Origin and destination postcodes, package weight, size and, when the shop turns it on, declared value | To get a price | Sent to Correios (section 5) | Not stored by us; the shop keeps it only in the chosen rate's package summary on the order (next row) and, for failed quotes, in its WooCommerce log (last row) |
| Correios product code and package summary (items, weight, size, declared value) of the chosen rate | So the shop's ERP or label tool can tell SEDEX from PAC | The shop's own order records | As long as the shop keeps the order |
| Failed-quote details: HTTP status, the Correios message and the request address — which contains both postcodes, the package figures and, when set, the contract and DR number, never the user, access code, card or token | So the shop manager can diagnose errors | The shop's WooCommerce log (WooCommerce > Status > Logs, source "entregaflow") | WooCommerce's log retention |

If you contact us, we process what you send in order to answer: email is handled by Google (Gmail) on our behalf, and GitHub issues are public and handled by GitHub. We keep support messages while the issue is open and delete email threads on request.

We do not collect telemetry, usage statistics or analytics, including "anonymous" ones.

## 3. Our role

We are not a controller or processor of the shop's data or of its customers' data: the plugin runs on the shop's own server and we have no access to it. The shop is the controller of its customers' data and decides on its use of Correios. For support messages you send us, we are the controller.

## 4. Legal basis

For the plugin's processing: not applicable to us; the shop sets its own basis for sending its customers' postcodes to Correios (normally the performance of the sales contract). For support messages: our legitimate interest in answering the request you sent.

## 5. Where data goes — outbound connections

The product connects only to these hosts. This list is identical to `NETWORK.json`.

| Host | Operated by | Purpose | Data sent |
|---|---|---|---|
| api.correios.com.br | Empresa Brasileira de Correios e Telégrafos (Correios) | Authenticate and get SEDEX/PAC prices | Shop owner's Correios user, access code and postage card (authentication); contract number and DR when set; postcodes, weight, size and, when turned on, declared value of the quoted package |

There are no other subprocessors. Correios' own terms and privacy policy: https://www.correios.com.br/atendimento/developers and https://www.correios.com.br/falecomoscorreios/politica-de-privacidade-e-cookies

## 6. Retention and deletion

Deleting the plugin from the Plugins screen removes the stored settings, token and last-error record. Order records and WooCommerce logs stay under the shop's own retention. Correios' own retention is governed by Correios' terms.

## 7. Your rights

Access, rectification, erasure, restriction, portability and objection under the GDPR/LGPD, as far as we process data: we hold only support correspondence you sent us; ask and we delete it. Questions: brisolo.support@gmail.com or the support tracker https://github.com/brisolo/support/issues .

## 8. Changes

Changes are published here with a new date and in the plugin's changelog.

## 9. Contact

Brisolo, brisolo.support@gmail.com.
