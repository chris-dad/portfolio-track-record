# Portfolio Track Record

A self-directed personal investment portfolio record, published monthly and version-tracked with Git and SHA-256 report fingerprints.

## What this is

- A self-directed personal portfolio with ~RMB 1,000,000 principal (six-figure USD scale).
- Monthly reports benchmarked against the Hang Seng Index and the S&P 500.
- Every published report version is fingerprinted with a SHA-256 hash in audit_log.json, so the record is version-tracked: anyone who keeps a fingerprint can check a report against it. Corrections are logged as new entries in the audit log.
- The trading log starts in February 2026; hash-tracked monthly reports run from August 2026 onward.

## Current standing (snapshot from the 2026-10-24 report)

The report shows the result on two bases.

- *RMB basis:* principal RMB 1,000,000 -> portfolio value ~RMB 803,826 (about US$120,246), -19.62%.
- *Fixed-reference USD comparison:* the report holds a USD reference cost of $140,845 (RMB 1,000,000 at 7.1 USD/CNY, set on 2026-08-18). Against it, $120,246 is -14.63%.
- *Gap between the two:* 19.62 - 14.63 = about 4.99 percentage points. This is consistent with the move in the reference rate (7.1 -> 6.6849) translating USD values into fewer RMB, but it is an arithmetic comparison, not a proven causal split. Actual cash-flow dates and FX rates are not reconstructed here, so the USD figure is a reference comparison, not a definitive currency-adjusted return.

Many holdings are priced in USD and the reports are computed in USD, but not all: Consun Pharmaceutical is HK$-denominated. The reports show KAP (LSE IOB) down ~30% on cost and Consun ~20.6%, among other positions. No quantified attribution of the total is claimed here.

Figures are a mid-month snapshot.

## How the portfolio is organised

This is a self-directed portfolio, not an effort to generate management-fee income. It has two parts with different purposes:

- *Long-term value holdings (KAP, Consun Pharmaceutical):* held as long-term value positions with a longer investment horizon, so I do not trade them frequently and accept interim drawdowns. This is intent, not a claim that they will recover; their current losses are shown in the reports.
- *Crypto trading sleeve:* BTC dual-momentum signals executed on OKX (entries and exits logged against exchange order IDs and fill prices), BTC covered calls (options ledger settled and reported in BTC terms), and OKX stablecoin yield products for cash between signals. My intended options approach is wheel-style; the repo records covered calls only. This sleeve is for liquidity and active trading. It carries its own market and counterparty risk and is not a risk-free reserve.
- Background: in crypto since 2014; I previously ran my own mining hardware.

## Losses are part of the record

On 2026-08-21 a covered-call position (short BTC 68000 calls expiring 2026-08-28) was force-liquidated. The realized loss of -0.043289 BTC (about US$2,857 at the time) is logged in the August report and in audit_log.json. The reports also log losing months and data corrections.

## Files in this repo

- index.html - the current monthly report (written in Chinese; the figures, benchmark comparisons, and hashes are language-neutral).
- audit_log.json - the version history: date, report fingerprint (SHA-256), and a note on what changed in each published version.

## What the hashes do and do not prove

Each entry in audit_log.json ties a published report version to a SHA-256 fingerprint, and git history versions every file. Anyone who keeps a fingerprint can check whether a report still matches it.

The fingerprints make the record version-tracked. They do not by themselves verify trading performance: the underlying figures rest on the exchange and broker records quoted inside each report.

## Why this is public

The point of the repo is that the record speaks for itself: benchmark discipline, loss reporting, and a version-tracked history.
