# Portfolio Track Record

A self-directed personal investment portfolio, reported monthly in two editions, with every published version fingerprinted (SHA-256) and logged in a public chain file.

## What this is

- A self-directed personal portfolio with **RMB 1,000,000 principal** (six-figure USD scale), reported in USD and in RMB.
- **Two editions of every monthly report**: the Chinese edition (`index.html`, RMB basis) and the English edition (`index-en.html`, USD).
- Every published version carries a **content fingerprint** — a hash of the report's content only, not of when it was generated — so a fingerprint kept today can be re-checked against the file years later.
- Monthly reports are benchmarked against the **Hang Seng Index** and the **S&P 500** from the first valuation date.
- **The performance record starts on 18 Aug 2026** (first valuation date). Trades before that date are in the execution history but are not part of the record.

## Current standing — as at 30 Oct 2026 close (October 2026 report)

| Measure | Value |
|---|---|
| Net assets, investment portfolio | **USD 123,523** · RMB 824,021 |
| Month, 30 Sep → 30 Oct 2026 | **−3.63%** |
| Since inception, 18 Aug → 30 Oct 2026 | **+0.57%** (from USD 122,821) |
| RMB basis, vs RMB 1,000,000 principal | **−17.60%** |
| USD basis, vs fixed reference cost USD 140,845 | **−12.30%** |
| Cash & equivalents | 54.8% · USD 67,659 |
| Maximum drawdown, month-end valuations (4 points) | **−6.55%** |

### The two bases, and why they differ

The RMB 1,000,000 principal was committed when USD/CNY was **7.1**, so the USD reference cost is held fixed at **USD 140,845** and is never re-translated. At 30 Oct 2026 the rate was **6.6710**.

The gap splits exactly: **−12.30% investment P&L** (measured at the fixed 7.1) plus **−5.30pp of currency translation**, and the two add back to **−17.60%** with a residual under RMB 1. This is an arithmetic identity on a USD-denominated book — it is *not* a decision-level attribution of why the portfolio moved. Actual cash-flow dates are not reconstructed here.

### Returns by period

| Period | Portfolio (USD) | Hang Seng Index | S&P 500 |
|---|---|---|---|
| Aug 2026 — partial, from 18 Aug | +7.62% | +0.38% | −0.07% |
| Sep 2026 | −3.03% | −3.73% | −0.45% |
| Oct 2026 | −3.63% | −5.36% | −0.93% |
| **Since inception** | **+0.57%** | −8.55% | −1.45% |

The first period is partial — the record begins on the first valuation date — so it is **not a full-month return and is not annualised**. Portfolio figures are month-end valuations derived from the execution ledger and month-end closing prices: **derived, not broker statements**. The monthly figures chain-link to the since-inception figure above; they are the same measure stated two ways.

## Corrections are part of the record

- **2026-08-21 — forced liquidation.** A short BTC 68,000 call (expiring 2026-08-28) was force-liquidated: **−0.043289 BTC**, about USD 2,857 at the time. Logged in the August report and in the audit chain.
- **Interest basis — cash to accrual.** IBKR cash interest is now accrued daily on the official rate schedule (3.13% to 16 Sep 2026, 3.38% from 17 Sep 2026, ACT/360, on the USD 19,547 of portfolio cash) instead of being booked only when received. This **restated two published valuations**: 31 Aug 2026 **+USD 22.09** and 30 Sep 2026 **+USD 74.98**. Accrued interest is carried as its own asset line.
- **Position size.** The Consun Pharmaceutical (1681.HK) holding was corrected to **5,000 shares** (7,000 bought less 2,000 sold) against the broker statement, replacing an earlier 4,000-share figure.
- **2026-11-02 — wording, not numbers.** The Chinese edition's descriptions of cash, interest and inception were aligned with the English edition. **No figure changed**: net assets, the monthly return and the cumulative return are identical in both editions, and both fingerprints are logged together.

## How the portfolio is organised

This is a self-directed portfolio, not an effort to generate management-fee income. It has two parts with different purposes:

- **Long-term value holdings** (KAP on LSE IOB, Consun Pharmaceutical 1681.HK): held with a longer horizon, traded infrequently, interim drawdowns accepted. That is stated intent, not a claim that they will recover — their current losses are shown in the reports.
- **Crypto trading sleeve**: BTC dual-momentum signals executed on OKX (entries and exits logged against order IDs and fill prices), BTC covered calls (options ledger settled in BTC terms), and OKX stablecoin yield for cash between signals. This sleeve is for liquidity and active trading; it carries its own market and counterparty risk and is not a risk-free reserve. **It has been flat since 24 Oct 2026**, when the dual-momentum signal went flat and the BTC position was sold in full (0.54438727 BTC at USD 80,614.63).
- Background: in crypto since 2014; previously ran my own mining hardware.

## Files in this repo

| Path | What it is |
|---|---|
| `index.html` | Chinese edition of the current monthly report — RMB basis |
| `index-en.html` | English edition of the same report — USD |
| `audit_log.json` | Version history: date, content fingerprint of both editions, and what changed in each published version (**23 entries**) |
| `reports/` | Monthly review write-ups |
| `research/` | Single-name research behind holding decisions (e.g. the October 2026 KAP review, in Chinese and English) |

## What the hashes prove, and what they do not

Each entry in `audit_log.json` ties one published version to a SHA-256 fingerprint of the report's content, and git versions every file alongside it. Anyone who keeps a fingerprint can check whether a report still matches it, and can see from the log what each revision changed and which version it replaced.

The fingerprints make the record **version-tracked**. They do not by themselves verify performance: the underlying figures rest on the exchange and broker records quoted inside each report.

## Reporting standards and limits

- **No annualised return and no risk statistics are presented for the portfolio.** GIPS 2020 requires 36 monthly observations before risk statistics and a full 12 months before annualisation: first eligible annualised figure **August 2027**, first eligible risk statistics **August 2029**.
- The Chinese edition does show an **account-level** Sharpe/Sortino/Calmar block, flagged on the page as account-level: it includes cash that is not part of the portfolio, and only 4 monthly points exist. It is not portfolio performance and is not a basis for external comparison.
- Valuations are derived from the execution ledger and month-end closing prices, **not from broker statements**; where a price rests on a single venue, the report says so.
- One-person record, published as-is: no independent auditor, administrator or custodian verification of the valuations, and no guarantee against error. Errors found after publication are logged as new entries rather than quietly edited.

## Why this is public

The point of the repo is that the record speaks for itself: benchmark discipline, losses reported at the same resolution as gains, corrections disclosed instead of overwritten, and a version-tracked history anyone can check.

## Disclosure

Personal investment record, not investment advice, not an offer or solicitation, and not a fund. The author holds the positions shown. Past performance is not indicative of future results.
