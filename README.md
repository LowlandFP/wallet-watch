# wallet-watch

Watch-only BTC and ETH balance alerts.

## Purpose

wallet-watch is planned as a small, self-hosted monitor for public Bitcoin and Ethereum addresses that the operator is authorized to watch. It will report balances and send alerts to Telegram.

## Security boundary

- It will accept public addresses only.
- It will never generate, collect, store, or test seed phrases.
- It will never request private keys, sign transactions, or move funds.
- Telegram credentials belong in GitHub Actions secrets, never in source files or commits.
- Users are responsible for adding only addresses they own or are authorized to monitor.

## Possible service model

A possible paid service is installation and configuration support for people who want alerts for their own public wallet addresses. This is only a concept; the repository is not currently a paid service and does not promise income. Any future service must be offered with customer permission and without taking custody of funds or secret recovery data.

For work offered in the Netherlands, check the current registration and tax requirements before charging customers. See [KVK guidance](https://www.kvk.nl/starten/moet-ik-mijn-bedrijf-inschrijven-bij-de-kvk/) and the [Belastingdienst guidance on income from other work](https://www.belastingdienst.nl/wps/wcm/connect/fisin/fisin2026/inkomsten_uit_overig_werk).

## Build plan

1. Scaffold — repository, README, and Python ignore rules.
2. Address configuration and input validation.
3. Read-only BTC and ETH balance checks.
4. Telegram notifications and safe secret handling.
5. Scheduled GitHub Actions workflow and operational documentation.
6. Simple status page.

Features will be added in reviewable phases.