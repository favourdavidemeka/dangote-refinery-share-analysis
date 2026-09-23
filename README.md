# I Bought a Refinery for ₦5,250

### What the Dangote Petroleum Refinery IPO actually sells you — measured in millilitres, teaspoons, and dollars

**Author:** Favour (Chukwuemeka) David — Chemical Engineering student & data analyst

**Data source:** Dangote Petroleum Refinery & Petrochemicals FZE — IPO Prospectus, 7 September 2026 (SEC-registered)

**Tools:** Google Sheets (no code required)

**Date:** September 2026

---

## The hook

The minimum subscription for the Dangote Refinery IPO is **10 shares at ₦525 each — ₦5,250**. Everyone is joking about becoming "co-owners" of the refinery. As a chemical engineering student, I wanted to answer a more literal question:

> **If I pay ₦5,250, how much of an actual oil refinery do I own — in physical units?**

Everyone is debating whether the IPO is a good buy. Nobody I could find translated the share price into refinery units. This project does that, using only figures from the official prospectus.

---

## The math

### Step 1 — How many shares exist after the offer?

| Item | Shares | Source |
|---|---|---|
| Shares in issue pre-offer | 120,128,915,901 | Prospectus p.33 & p.62 |
| IPO base offer | 4,100,000,000 | Prospectus p.34 |
| **Post-offer total (base)** | **124,228,915,901** | Calculated |
| Post-offer if 30% greenshoe exercised | 125,458,915,901 | Prospectus p.37, p.62 |

### Step 2 — One share's share of the refinery

The refinery's rerated nameplate capacity is **700,000 barrels per day** (p.16, p.108 — rerated from the original 650,000 bpd design after performance tests in June 2026).

```
Barrels per share per day  = 700,000 ÷ 124,228,915,901
                           = 0.0000056 bpd

Litres per share per day   = 0.0000056 × 158.987 L/bbl
                           = 0.90 mL
```

**One share = 0.90 mL of crude oil processed per day.**

The minimum lot (10 shares = ₦5,250):

```
8.96 mL/day ≈ 1.8 teaspoons of crude per day
Ownership of the entire plant: 0.000008%
```

### Step 3 — Your 9 mL, split into real products

Using the refinery's **actual 12-month product yields to 30 June 2026** (p.111) — not industry estimates:

| Product | Actual yield | Your mL/day (10 shares) | Your litres/year |
|---|---|---|---|
| PMS (petrol) | 39.9% | 3.58 | **1.31** |
| AGO (diesel) | 21.4% | 1.92 | 0.70 |
| ATF (jet fuel) | 20.6% | 1.85 | 0.67 |
| RCO + CBFS | 16.6% | 1.49 | 0.54 |
| LPG | 1.3% | 0.12 | 0.04 |
| Polypropylene | 0.2% | 0.02 | 0.01 |

**Your yearly petrol dividend, measured in petrol: ~1.3 litres — about two small bottled-water bottles.**

### Step 4 — The money layer (H1 2026, audited, p.76)

| Metric | Value |
|---|---|
| H1 2026 revenue | $13.91bn |
| H1 2026 profit after tax | $1.82bn |
| Annualized revenue per 10-share lot | **~$2.26/yr** |
| Annualized profit per 10-share lot | **~$0.30/yr (≈ ₦407)** |
| Simple payback at 100% payout | ~12.9 years |

Dividends, when declared, are paid in **US dollars** (prospectus dividend policy, pp.129–133) — which means a naira-earning investor's dividend holds its value against naira depreciation.

### Step 5 — The sanity check nobody else is running

```
Indicative market cap at listing:  ₦65.22tn (p.35)  ≈ $47.4bn
Annualized PAT:                    $1.82bn × 2       =  $3.64bn

Implied P/E ≈ 13x
```

Whether the IPO is a good buy depends on refining margins holding (Issuer estimates ~$24.2/bbl GRM for 2026, p.80) and the expansion delivering — but the entry price itself is not absurd on these numbers.

### Step 6 — The engineer's lens

| Build | Capex | Capacity | Capex per bpd |
|---|---|---|---|
| Original refinery | ~$19bn (p.100) | 650,000 bpd (design) | **$29,231/bpd** |
| Expansion (target 2029) | ~$14.3bn (p.34) | +700,000 bpd | **$20,429/bpd** |

The expansion is ~30% cheaper per unit of capacity — the brownfield learning curve, visible in the company's own numbers. (For context: the refinery's Nelson Complexity Index of 11.5 vs 8.9 for the average emerging-market refinery, p.80 — it's built to squeeze more valuable products out of every barrel.)

---

## Data & sources

Every number traces to the prospectus:

| Figure | Value | Page |
|---|---|---|
| Shares pre-offer | 120,128,915,901 | p.33, p.62 |
| Base offer | 4,100,000,000 @ ₦525 | p.34 |
| Greenshoe cap | 30% (SEC approval required) | p.37 item 24 |
| Minimum lot | 10 shares | p.37 item 22 |
| Market cap at listing (indicative) | ₦65.22tn | p.35 |
| Capacity | 700,000 bpd (rerated) | p.16, p.108 |
| H1 2026 revenue / PAT | $13.91bn / $1.82bn | p.76 |
| Product yields | PMS 39.9%, AGO 21.4%, ATF 20.6%... | p.111 |
| GRM estimate 2026 | ~$24.2/bbl | p.80 |
| Debt | ~$5.67bn (30 Jun 2026), all secured | p.38 |
| Expansion | +700,000 bpd by 2029, ~$14.3bn | p.34 |
| FX (H1 2026 closing) | ₦1,377/$ | p.17 |

**Verification notes (because data integrity matters more than a hot take):**
- Media widely reported H1 revenue as **$14.4bn**. The audited prospectus says **$13.91bn**. This project uses the audited figure.
- The document contains a minor internal discrepancy: the KPMG extract (p.70) shows ₦19,153,842m revenue vs ₦19,134,942m on p.76 (~0.1% gap; Naira PAT differs similarly). USD figures agree on both pages — so all outputs here are presented in USD, the company's functional currency.

---

## Limitations

1. Per-share throughput assumes steady-state at the rerated 700,000 bpd nameplate. Actual throughput varies with maintenance, crude mix, and market conditions.
2. The greenshoe (up to 30% more shares, p.37) dilutes per-share figures by ~1% if fully exercised. Base-offer numbers are used; full-exercise numbers are in the calculator.
3. Annualizing H1 2026 (×2) is an arithmetic exercise, **not a forecast**. Refining is cyclical.
4. Product yields are actual 12-month figures to 30 June 2026, but yields shift with crude slate and operating mode.
5. The $24.2/bbl GRM is the Issuer's own estimate, not an audited actual.
6. Market cap is the indicative listing valuation, not a market-tested price.
7. Dividend payment in USD is per the dividend policy; payout ratio and timing are not assumed here.
8. This is an educational analysis of public documents. **It is not investment advice.**

---

## Reproduce it yourself

📊 **[Download the Google Sheets calculator](sandbox:///mnt/agents/output/dangote_refinery_share_calculator.xlsx)** — upload to Google Drive, open with Google Sheets. Four tabs: verified source data (with page refs), the ownership calculator, the financial layer, and the limitations. Change any input on the Source tab and every result recalculates.

Or from scratch:
1. Shares post-offer = 120,128,915,901 + 4,100,000,000
2. bpd per share = 700,000 ÷ result
3. mL per share = result × 158.987 × 1,000
4. Multiply by actual yields from p.111
5. Finance layer = H1 figures from p.76 ÷ 181 days ÷ shares × 365

---

## What I'm watching next

- The **expansion to ~1.4 million bpd by 2029** ($14.3bn programme, p.34) — where the next tranche of this story lives.
- Whether realized GRM tracks the ~$24.2/bbl estimate.
- The **Cement Price Tracker** — my next project: ~8 years of Nigerian cement prices, explained through the process-industry lens (energy, clinker chemistry, logistics).

---

*Built by a final-year Chemical Engineering student learning data analytics in public. If this made you see the IPO differently, share it — and follow the next build.*

