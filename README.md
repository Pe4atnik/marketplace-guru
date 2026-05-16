# Marketplace Guru

Marketplace Guru helps users choose products on marketplaces by clarifying real purchase intent, delivery constraints, risks, and alternatives before searching.

It is a read-only purchasing advisor: it compares options and gives decision-ready recommendations, but does not buy, add to cart, or change accounts.

## Requirements

- OpenClaw tools for web search/fetch.
- Optional: visible browser support through the `win11-visible-browser` skill for JS-heavy marketplaces and exact price/delivery checks.

## Setup

No API keys are required for the MVP.

For best results with Russian marketplaces, configure the visible Windows browser via `win11-visible-browser` so the agent can inspect pages that require real browser rendering.

## Usage

Examples:

- “Посмотри Samsung 990 Pro 2TB, стоит брать?”
- “Подбери робот-пылесос с влажной уборкой до 40 тысяч.”
- “Найди модную футболку с доставкой к пятнице.”
- “Сравни эти два варианта на Ozon и Яндекс Маркете.”

## Behavior

Marketplace Guru first asks only what matters:

- where delivery is needed;
- whether the user wants a specific model or alternatives are allowed;
- 1–2 key criteria such as budget, deadline, reliability, or size.

Then it searches and returns a short decision-oriented recommendation:

- best overall;
- value option;
- reliable/premium option;
- fastest delivery when relevant;
- avoid/risky options.

## Safety

- No purchases.
- No cart actions.
- No payment handling.
- No account changes.
- Captchas/login walls are reported, not bypassed.

## Install

```bash
clawhub install <author>/marketplace-guru
```
