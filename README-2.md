# ADT Inc. (NYSE: ADT) - Illustrative Take-Private LBO Model

A leveraged-buyout analysis of ADT Inc., built from the company's own SEC filings and market data as of
September 8, 2026. It asks one question: **does a 35% take-private of ADT earn a sponsor-style return on
guidance-level fundamentals?** The answer on the base case is no (4.7% net IRR), and the model shows why.

**`ADT_LBO_Model.xlsx`** is the model, with live formulas throughout. Tabs: Summary, Assumptions, Dilution,
Sources & Uses, Operating Model, Debt Schedule, Returns Analysis, Sensitivities, Calibration.
`ADT_LBO_Summary.pdf` is a one-page print of the Summary tab.

## Base-case result

| | |
|---|---|
| LTM (Jun-2026) revenue / Adj. EBITDA | $5,165mm / $2,690mm (52.1% margin) |
| Operating case | ~2% revenue growth (2026 guidance), flat EBITDA margin, capex 22% + net subscriber acquisition cost 3.5% of revenue |
| Offer | $9.75 per share (35% premium to the $7.22 close on Sep 8, 2026); 759mm diluted shares |
| Entry EV / Adj. EBITDA | 5.51x (10.8x on EBITDA less capex and net subscriber costs); ADT traded at 4.77x |
| Financing | 4.0x leverage: $8,070mm Term Loan B (SOFR + 350) and $2,690mm senior notes (8.5%); $416mm receivables facility left in place |
| Sponsor equity | $4,577mm (29.8% of sources) |
| Exit (year 5, at the unaffected 4.77x) | EV $14.2bn; net debt / EBITDA 2.8x |
| **Sponsor net IRR / MOIC** | **4.7% / 1.26x** (after an 8% management option pool) |

| Scenario | Growth | Margin / yr | Exit multiple | Net IRR | MOIC |
|---|---|---|---|---|---|
| Base (2026 guidance) | 2% | flat | 4.77x (unaffected) | 4.7% | 1.26x |
| Downside | 0% | -20bp | 4.27x | -13.5% | 0.48x |
| Upside | 5% | +40bp | 5.77x | 22.5% | 2.75x |
| Management case | 3% | +20bp | 5.51x (entry) | 14.7% | 1.99x |

## What the model shows

1. **The exit multiple decides the outcome.** A 35% premium puts entry at 5.5x against a 4.8x trading multiple. Selling at the
   unaffected multiple gives up about $2.2bn of value; if the premium were retained, the base operating case returns 11.2%.
2. **Operating assumptions matter, but less.** Moving from 2% to 3% growth adds about three points of IRR; adding 20bp of annual margin expansion adds about 1.3.
3. **Debt service is tight.** EBITDA less capex and net subscriber costs covers net interest only 1.7x at the weakest point (EBITDA alone covers it 3.4x), because ADT reinvests roughly a quarter of revenue in capex and customer acquisition.
4. **The downside is severe by design** (0% growth, margin erosion, higher capex, lower exit multiple): it loses most of the equity and is a stress case, not a forecast.

## Method

- **LTM build:** FY2025 + H1 2026 - H1 2025, as live formulas (Assumptions tab).
- **Cash flow:** EBITDA less all-in capex (dealer accounts, subscriber systems, PP&E), net subscriber acquisition cost, working capital, cash interest and tax. The `Calibration` tab runs the same method on ADT's own FY2025 and LTM figures: it lands about 14% below reported FY2025 adjusted free cash flow (27% below LTM), mainly because the model charges full book tax. At a 10% cash tax rate the base case would return about 7.1%.
- **Debt:** interest on beginning balances (no circularity); mandatory amortization plus a cash sweep to the Term Loan B; unswept cash accumulates and is credited at exit; Sec. 163(j) interest-deduction cap at 30% of EBITDA.
- **Dilution:** treasury method at the offer price on the 10-K award table plus 2026 grants (`Dilution` tab).
- **Returns:** sponsor MOIC and IRR net of a management option pool, with a value-creation bridge (EBITDA growth, multiple change, debt paydown, fees, option pool).
- **Sensitivities:** Excel data tables on growth, exit multiple, capex, leverage and premium, plus a scenario table; all follow the active scenario and hold period.
- **Checks:** sources = uses, value bridge foots, minimum cash held, no negative debt balances, data-table input cells blank.

## Sources

ADT Form 10-K (filed Mar 2, 2026); Form 10-Q (filed Jul 30, 2026) including Note 6 (debt) and the cover page (shares); Q2 2026 earnings release; Form 8-K (filed Aug 31, 2026); S&P Capital IQ NetAdvantage (Sep 8, 2026 closing price; cross-checks). `SOURCE_TIEOUT.md` lists every input against its source.

## How to use

Set the scenario in `Assumptions!B55` (1-4) and the hold period in the Exit section (3-5 years); every tab updates.
Blue cells are inputs, black are formulas, green are links to other tabs. Leave the yellow input cells on the
Sensitivities tab blank: the data tables write to them.

## Limitations

- **Illustrative, not a proposed transaction.** Financing terms (spreads, coupon, fees, premium) are assumptions, not market quotes.
- **Dilution is an estimate.** The 10-Q has no full equity-award roll-forward; counts are from the 10-K (Dec 31, 2025) plus 2026 grants, with unvested awards assumed to accelerate.
- **Taxes are conservative:** 26% book rate with no NOLs or cash-tax deferral; disallowed interest is not carried forward.
- **Not modeled:** the $100mm Term Loan A added on Aug 28, 2026 (use of proceeds not disclosed), ADT's 2027 tax and swap headwinds, management rollover, a revolver draw, bolt-on M&A, and whether the receivables facility survives a change of control.
- **Adjusted EBITDA** excludes capitalized subscriber costs; the cash-earnings multiple is shown alongside it.
- **Leverage:** 4.0x Adj. EBITDA is about 73% of entry value (4.15x including the receivables facility); financeability is not tested.

---
*Hypothetical transaction for illustration only.*
