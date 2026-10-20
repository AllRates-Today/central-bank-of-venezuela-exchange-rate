# Central Bank of Venezuela Exchange Rates API — central-bank-of-venezuela-exchange-rate

[![npm version](https://img.shields.io/npm/v/central-bank-of-venezuela-exchange-rate.svg)](https://www.npmjs.com/package/central-bank-of-venezuela-exchange-rate)
[![license](https://img.shields.io/npm/l/central-bank-of-venezuela-exchange-rate.svg)](https://github.com/AllRates-Today/central-bank-of-venezuela-exchange-rate/blob/main/LICENSE)
[![zero dependencies](https://img.shields.io/badge/dependencies-0-brightgreen.svg)](https://www.npmjs.com/package/central-bank-of-venezuela-exchange-rate)
[![TypeScript](https://img.shields.io/badge/TypeScript-types%20included-3178C6.svg)](https://www.typescriptlang.org/)
[![USD/VES today](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fallratestoday.com%2Fapi%2Fopen%2Fcentral-bank%2Fbcv%3Fsource%3DUSD%26target%3DVES&query=%24.rate&label=USD%2FVES%20published%20by%20Central%20Bank%20of%20Venezuela&color=0A7E8C&cacheSeconds=3600)](https://allratestoday.com/central-bank-rates-api/bcv/)
[![rate date](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fallratestoday.com%2Fapi%2Fopen%2Fcentral-bank%2Fbcv%3Fsource%3DUSD%26target%3DVES&query=%24.rate_date&label=rate%20date&color=555&cacheSeconds=3600)](https://allratestoday.com/central-bank-rates-api/bcv/)

**Official Central Bank of Venezuela (Venezuela) daily exchange rates for Node.js and TypeScript. The published central bank rates behind tax filings, customs valuations, audits, and compliant invoicing — not market estimates, but the numbers Central Bank of Venezuela itself prints, every business day.**

## 🚀 Why this client?

- 🏛️ **Official published rates** — Central Bank of Venezuela's own table, with the publisher's own `rate_date` on every response
- 📅 **History back to 2016** — point-in-time tables and daily series for any past date
- 🔀 **Published vs derived, always flagged** — computed inverse/cross pairs carry `derived: true`, never mixed with official prints
- ⚡ **Zero dependencies** — pure ESM + CJS over global `fetch`; Node 18+, Bun, Deno, and edge runtimes
- 🔷 **Type-safe** — full TypeScript definitions shipped with the package
- 🧾 **Compliance-grade metadata** — `rate_type`, publication date, and source disclaimer on every response

> **Official rate, not mid-market:** every value here is a number Central Bank of Venezuela itself published, fixed once printed and carrying the central bank's own `rate_date` — what filings and audits require. Need the live mid-market rate for pricing or display instead? Use the [mid-market API](https://allratestoday.com/docs/) or [`@allratestoday/sdk`](https://www.npmjs.com/package/@allratestoday/sdk). The two can diverge by several percent.

## ⚡ Try it without a key

The latest Central Bank of Venezuela table is also served keyless, CORS-open and edge-cached, for evaluation, embeds and AI agents:

```bash
curl "https://allratestoday.com/api/open/central-bank/bcv?source=USD&target=VES"
```

```js
const r = await fetch('https://allratestoday.com/api/open/central-bank/bcv').then((x) => x.json());
console.log(r.rate_date, r.rates.length); // the central bank's latest published table, no key
```

The open endpoint serves the *latest* table only (JSON by default; add `?format=csv`, `xml` or `xlsx` for a file) and asks for a visible attribution link. The client below uses the keyed API, which adds point-in-time tables and history.

## 📈 Latest published table

[![Latest Central Bank of Venezuela table](https://allratestoday.com/api/open/central-bank/bcv/table.svg)](https://allratestoday.com/central-bank-rates-api/bcv/)

The image is rendered live from the keyless endpoint above, so it follows the central bank's publications on npm and on GitHub alike without a new release. The same table as text is folded below for search and copy-paste: on GitHub [a daily Action](.github/workflows/daily-table.yml) refreshes it whenever the central bank publishes a new table; on npm it is as of the package's publish date.

<!-- daily-table:start -->
<details>
<summary>Table as text: published 2026-10-20 by Central Bank of Venezuela — 42 rates. Updated 2026-10-20.</summary>

| Base | Quote | Type | Rate |
| --- | --- | --- | ---: |
| ANG | VES | buy | 504.37028137 |
| ANG | VES | sell | 505.63436729 |
| ARS | VES | buy | 0.57778141 |
| ARS | VES | sell | 0.57922949 |
| BOB | VES | buy | 75.7032881 |
| BOB | VES | sell | 75.89302065 |
| BRL | VES | buy | 173.82421557 |
| BRL | VES | sell | 174.25986523 |
| CAD | VES | buy | 624.11559504 |
| CAD | VES | sell | 625.67979453 |
| CLP | VES | buy | 0.89750564 |
| CLP | VES | sell | 0.89975503 |
| CNY | VES | buy | 131.68548491 |
| CNY | VES | sell | 132.01552371 |
| COP | VES | buy | 0.27917239 |
| COP | VES | sell | 0.27987207 |
| CUC | VES | buy | 879.67220775 |
| CUC | VES | sell | 881.8769 |
| DOP | VES | buy | 14.33624849 |
| DOP | VES | sell | 14.37217894 |
| EUR | VES | buy | 986.49960065 |
| EUR | VES | sell | 988.97203073 |
| INR | VES | buy | 9.26799987 |
| INR | VES | sell | 9.29122794 |
| JPY | VES | buy | 5.55204907 |
| JPY | VES | sell | 5.56596398 |
| MXN | VES | buy | 47.70404918 |
| MXN | VES | sell | 47.8236082 |
| NIO | VES | buy | 24.69525668 |
| NIO | VES | sell | 24.75714955 |
| PEN | VES | buy | 255.62206368 |
| PEN | VES | sell | 256.26272048 |
| RUB | VES | buy | 10.62598547 |
| RUB | VES | sell | 10.65261701 |
| TRY | VES | buy | 17.75361729 |
| TRY | VES | sell | 17.79811257 |
| TTD | VES | buy | 130.68579268 |
| TTD | VES | sell | 131.013326 |
| USD | VES | buy | 879.67220775 |
| USD | VES | sell | 881.8769 |
| UYU | VES | buy | 21.93860407 |
| UYU | VES | sell | 21.99358804 |

</details>

Source: [Official rates published by BCV, served by AllRatesToday](https://allratestoday.com/central-bank-rates-api/bcv/). Rates are as printed by the central bank; AllRatesToday is not affiliated with it.
<!-- daily-table:end -->

## 🔑 Get your API key

Get a free API key at [allratestoday.com/register](https://allratestoday.com/register) — no credit card required. Latest rates are on every plan, including free.

## 📦 Installation

```bash
npm install central-bank-of-venezuela-exchange-rate
```

```bash
yarn add central-bank-of-venezuela-exchange-rate
```

```bash
pnpm add central-bank-of-venezuela-exchange-rate
```

Requires Node 18+ (global `fetch`); also runs on Bun, Deno and edge runtimes. Also published under the org scope as [`@allratestoday/central-bank-of-venezuela-exchange-rate`](https://www.npmjs.com/package/@allratestoday/central-bank-of-venezuela-exchange-rate) — same code, same versions.

## 🏁 Quick start

```js
import { getRate } from 'central-bank-of-venezuela-exchange-rate';

const pair = await getRate('USD', 'VES', { apiKey: 'art_live_...' });
console.log(pair.rate, pair.rate_date); // the official Central Bank of Venezuela rate, on the central bank's own date
```

## 📚 API reference

- [Latest pair rate](#latest-pair-rate) — one pair from the latest published table
- [Full published table](#full-published-table) — everything the central bank printed, in one call
- [Table for a date](#table-for-a-date) — the official table for an invoice or filing date
- [Daily time series](#daily-time-series) — one pair across a date range

---

### Latest pair rate

Free plan and up. Pairs the central bank does not print directly are resolved from its table and flagged (see *Published vs derived rates* below).

```js
const pair = await getRate('USD', 'VES', { apiKey: 'art_live_...' });
```

**Response:**

```javascript
{
  bank: 'bcv',
  name: 'Central Bank of Venezuela',
  rate_date: '2026-10-14',   // Central Bank of Venezuela's own publication date
  source: 'USD',
  target: 'VES',
  rate: 877.9023,
  rate_type: 'sell',
  derived: false,
  method: 'published',
  disclaimer: 'Official rates as published by the named central bank. On weekends/holidays the most recent published rate_date is returned.'
}
```

### Full published table

Free plan and up. The complete table for the latest publication date.

```js
import { getLatestRates } from 'central-bank-of-venezuela-exchange-rate';

const table = await getLatestRates({ apiKey: 'art_live_...' });
console.log(table.rate_date, table.rates.length);
```

**Response:**

```javascript
{
  bank: 'bcv',
  name: 'Central Bank of Venezuela',
  rate_date: '2026-10-14',
  rates: [
    { "base": "USD", "quote": "VES", "type": "sell", "value": 877.9023 },
    { "base": "USD", "quote": "VES", "type": "buy", "value": 875.70754 },
    // … the rest of the published table (21 currencies vs VES)
  ],
  disclaimer: '…'
}
```

### Table for a date

Paid plans. The official table for any date since 2016 — weekends and holidays return the most recent published date, flagged via `published_on_requested_date`, which is exactly the in-force rate a filing needs.

```js
import { getRatesForDate } from 'central-bank-of-venezuela-exchange-rate';

const day = await getRatesForDate('2026-06-30', { apiKey: 'art_live_...' });
// Optionally narrow to one pair:
const one = await getRatesForDate('2026-06-30', { apiKey: 'art_live_...', source: 'USD', target: 'VES' });
```

**Response:**

```javascript
{
  bank: 'bcv',
  requested_date: '2026-06-30',
  rate_date: '2026-06-30',                // the date actually published
  published_on_requested_date: true,      // false when a weekend/holiday fell back
  rates: [ /* the full table for that date */ ],
  disclaimer: '…'
}
```

### Daily time series

Paid plans. One resolved rate per publication date — ready for charting, revaluation runs, or audit workpapers.

```js
import { getHistory } from 'central-bank-of-venezuela-exchange-rate';

const series = await getHistory(
  { source: 'USD', target: 'VES', from: '2026-01-01', to: '2026-10-14' },
  { apiKey: 'art_live_...' }
);
```

**Response:**

```javascript
{
  bank: 'bcv',
  source: 'USD',
  target: 'VES',
  from: '2026-01-01',
  to: '2026-10-14',
  count: 152,
  rates: [
    // one entry per publication date
    { date: '2026-10-14', rate: 877.9023, rate_type: 'sell', derived: false, method: 'published' },
    // …
  ],
  disclaimer: '…'
}
```

Pass `{ symbol: 'USD' }` instead of `source`/`target` to get the raw published rows for one currency (all rate types, no pair resolution).

---

## 🗺️ Currencies covered

Central Bank of Venezuela currently publishes rates covering **21 currencies** against the VES (as of the latest table):

`ANG` · 🇦🇷 `ARS` · 🇧🇴 `BOB` · 🇧🇷 `BRL` · 🇨🇦 `CAD` · 🇨🇱 `CLP` · 🇨🇳 `CNY` · 🇨🇴 `COP` · 🇨🇺 `CUC` · 🇩🇴 `DOP` · 🇪🇺 `EUR` · 🇮🇳 `INR` · 🇯🇵 `JPY` · 🇲🇽 `MXN` · 🇳🇮 `NIO` · 🇵🇪 `PEN` · 🇷🇺 `RUB` · 🇹🇷 `TRY` · 🇹🇹 `TTD` · 🇺🇸 `USD` · 🇺🇾 `UYU`

## 🏛️ Source

The Central Bank of Venezuela publishes the official reference exchange rate — around 21 currencies with buying and selling sides in bolivars, dated by the Fecha Valor on which each rate legally applies. Venezuelan accounting and tax practice are required to use the BCV rate, which has often stood far from parallel-market quotes; the official print is precisely what filings must cite.

- Publisher's own page: [Tipo de cambio de referencia](https://www.bcv.org.ve/estadisticas/tipo-de-cambio-de-referencia-0) · [www.bcv.org.ve](https://www.bcv.org.ve)
- Publication: every business day; the exact schedule, freshness status and any current delay are on the [Central Bank of Venezuela rates page](https://allratestoday.com/central-bank-rates-api/bcv/)
- Values are stored unmodified, with the publisher's own `rate_date` on every row — see the [methodology](https://allratestoday.com/official-rates-methodology/)

## 🧭 Reading the numbers

- `value` is always **quote currency per 1 unit of base currency** (`base: "EUR", quote: "USD", value: 1.15` means 1 EUR = 1.15 USD).
- Central Bank of Venezuela quotes **VES per 1 unit of foreign currency** (e.g. `base: "USD", quote: "VES"` means VES per one US dollar).
- Need the other way round? Ask `getRate(target, source)` and the API inverts or crosses for you, flagged `derived: true` — never divide a published rate yourself in a compliance workflow.
- `rate_type` tells you which of the central bank's series a row belongs to (`sell` here); some publishers print buy/sell or several fixings for the same pair.

## 🧩 ERP & accounting systems

Loading the official Central Bank of Venezuela rate into an accounting system is a supported workflow, not a hack. Step-by-step guides with the direction each system expects:

- [Dynamics 365 Business Central](https://allratestoday.com/docs/integrations/business-central/) — built-in Currency Exchange Rate Service, no code
- [Xero](https://allratestoday.com/docs/integrations/xero/) · [QuickBooks Online](https://allratestoday.com/docs/integrations/quickbooks/) · [SAP S/4HANA and ECC](https://allratestoday.com/docs/integrations/sap/) · [Odoo](https://allratestoday.com/docs/integrations/odoo/)

The same keyed endpoints return `?format=csv`, `?format=xml` and `?format=xlsx`, and accept the key as `?api_key=` on the URL for importers that cannot send headers:

```bash
curl "https://allratestoday.com/api/v1/central-bank/bcv/latest?format=xml&api_key=art_live_..."
```

## 🤖 AI agents

- MCP server: `npx -y @allratestoday/central-bank-mcp` (stdio) or the hosted endpoint `https://allratestoday.com/api/mcp` — tools for official rates, history, cross-bank comparison and publication calendars
- Already using the general SDK or MCP server? Since 2026-10-01 [`@allratestoday/sdk`](https://www.npmjs.com/package/@allratestoday/sdk) 1.4+ has `officialRates('bcv')` and [`@allratestoday/mcp-server`](https://www.npmjs.com/package/@allratestoday/mcp-server) 0.6+ has a `get_official_rates` tool — both return this source's latest table with no key, so you can add it without a second dependency
- Claude Code plugin (no key): `/plugin marketplace add AllRates-Today/claude-code-plugin` then `/plugin install allratestoday@allratestoday` — bundles both MCP servers plus an `/official-rate bcv ...` command
- Evaluating? Agents can self-issue a trial key with no signup: `POST https://allratestoday.com/api/agent/keys` (send `Content-Type: application/json`) returns a 100-call key valid 7 days that covers the free-plan methods (latest table, pairs); dated tables and history need a [paid plan](https://allratestoday.com/pricing/). The MCP servers expose it as `request_trial_key`
- Machine-readable site guide: [llms.txt](https://allratestoday.com/llms.txt) · [for-ai-agents](https://allratestoday.com/for-ai-agents/)

## ⚖️ Published vs derived rates

If Central Bank of Venezuela does not print a pair directly, the API resolves it from the central bank's own table and says so — official and computed values are never confused:

| `method` | `derived` | Meaning |
| --- | --- | --- |
| `published` | `false` | The central bank printed this pair directly |
| `inverse` | `true` | Computed as 1 ÷ the published opposite direction |
| `cross` | `true` | Computed via VES from two published rates |

## 🛡️ Error handling

Errors are thrown as `Error` with `status` (HTTP code) and `body` (the API's JSON error) attached:

```js
try {
  const pair = await getRate('USD', 'XXX', { apiKey: 'art_live_...' });
} catch (err) {
  console.log(err.message); // human-readable reason
  console.log(err.status);  // e.g. 404
}
```

| Status | Meaning |
| ------ | ------- |
| — | Missing `apiKey` (thrown before any request) |
| `400` | Malformed date or parameters |
| `401` | Invalid API key |
| `403` | Endpoint needs a [paid plan](https://allratestoday.com/pricing/) (historical dates & series) |
| `404` | Pair or date range not covered by Central Bank of Venezuela |
| `429` | Monthly quota exceeded |

## 🔷 TypeScript

Full definitions ship with the package — no `@types` install:

```ts
import type { LatestRates, PairRate, DatedRates, RateEntry, HistoryQuery, RequestOptions } from 'central-bank-of-venezuela-exchange-rate';
```

## 📦 CommonJS

```javascript
const { getRate } = require('central-bank-of-venezuela-exchange-rate');

getRate('USD', 'VES', { apiKey: 'art_live_...' }).then((pair) => console.log(pair.rate));
```

## 💡 Quota tips

- Rates change once per business day — cache the published table locally and a small monthly quota goes a long way.
- Every request counts toward your AllRatesToday quota, shared across all AllRatesToday endpoints on your key.

## 📖 Methods reference

| Method | Plan | Description |
| ------ | ---- | ----------- |
| `getRate(source, target, { apiKey })` | Free | Latest rate for one pair, resolved from the published table |
| `getLatestRates({ apiKey })` | Free | The central bank's full latest published table |
| `getRatesForDate(date, { apiKey, source?, target? })` | Paid | The official table (or one pair) for a YYYY-MM-DD date |
| `getHistory({ symbol \| source+target, from?, to? }, { apiKey })` | Paid | Daily series since 2016 |

## 📥 Bulk data (no key)

Need the whole archive rather than an API call? The same published tables are mirrored daily as open data:

- Hugging Face: [AllRatesToday/central-bank-exchange-rates](https://huggingface.co/datasets/AllRatesToday/central-bank-exchange-rates) — one CSV per institution (`rates/bcv.csv`)
- Kaggle: [allratestoday/central-bank-exchange-rates](https://www.kaggle.com/datasets/allratestoday/central-bank-exchange-rates)
- Raw JSON on GitHub: `https://raw.githubusercontent.com/AllRates-Today/central-bank-exchange-rates/main/data/bcv/latest.json`

## 🔗 Links

- [Central Bank of Venezuela rates page](https://allratestoday.com/central-bank-rates-api/bcv/) — live table, publication cadence, FAQ
- [All central bank sources](https://allratestoday.com/central-bank-rates-api/)
- [Package docs on the site](https://allratestoday.com/docs/sdk/central-bank-of-venezuela-exchange-rate/) · [ERP integration guides](https://allratestoday.com/docs/integrations/)
- [API documentation](https://allratestoday.com/docs/#central-bank) · [Interactive reference](https://allratestoday.com/api-reference/) · [Methodology](https://allratestoday.com/official-rates-methodology/)
- [Register (Free)](https://allratestoday.com/register) · [Dashboard](https://allratestoday.com/profile) · [Pricing](https://allratestoday.com/pricing/)
- [Status](https://allratestoday.com/status)
- [GitHub](https://github.com/AllRates-Today/central-bank-of-venezuela-exchange-rate)

## 📜 License

MIT
