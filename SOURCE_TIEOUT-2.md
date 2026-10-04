# Input tie-out

Every model input checked against its source. Sources: ADT Form 10-K (filed Mar 2, 2026), Form 10-Q (filed Jul 30, 2026),
Q2 2026 earnings release, Form 8-K (filed Aug 31, 2026), and S&P Capital IQ NetAdvantage. $mm unless noted.

| Input | Value in model | Source | Status |
|---|---|---|---|
| FY2025 revenue | 5,129 | 5,128.6 (10-K; Capital IQ) | Verified |
| H1 2026 / H1 2025 revenue | 2,591 / 2,555 | 10-Q; Q2 2026 release | Verified |
| LTM revenue | 5,165 | 5,164.9 (Capital IQ) | Verified |
| FY2025 Adjusted EBITDA | 2,680 | 2,680.4 (10-K MD&A) | Verified |
| H1 2026 / H1 2025 Adjusted EBITDA | 1,345 / 1,335 | 1,344.3 / 1,334.4 (10-Q MD&A) | Verified |
| LTM Adjusted EBITDA | 2,690 | 2,690.2 calculated; Capital IQ standardized EBITDA 2,695.5 | Verified |
| FY2025 capex: dealer accounts / subscriber systems / PP&E | 596 / 396 / 176 | 596.5 / 396.0 / 175.7 (10-K cash flow) | Verified |
| FY2025 deferred subscriber acquisition cost / revenue | 381 / 225 | 380.5 / 224.8 (10-K cash flow) | Verified |
| FY2025 interest expense, net | 459 | 459.3 (10-K); Capital IQ shows 474.7 on its own definition | Verified (10-K basis) |
| FY2025 D&A | 1,367 | 1,367.2 (10-K) | Verified |
| All-in capex / net SAC, % of revenue | 22.0% / 3.5% | LTM actual 20.3% / 3.45%; FY2025 22.8% / 3.0% | Assumption: capex ~1.7 pts above LTM actual |
| Share price | $7.22 | NYSE close, Sep 8, 2026 (Capital IQ) | Verified |
| Basic shares | 730.6mm | 675.8mm common + 54.7mm Class B (10-Q cover, Jul 23, 2026) | Verified |
| Dilutive securities | 28.1mm at offer; 19.7mm at current price | 10-K award table (Dec 31, 2025) + 2026 grants (10-Q), treasury method | Estimate: 10-Q has no award roll-forward |
| Existing gross debt | 7,418 | Term loans 3,609.3 + notes 3,749.9 + finance leases 58.4 (10-Q Note 6, Jun 30, 2026) | Verified |
| Existing cash | 4 | Jun 30, 2026 balance sheet (28 including restricted cash) | Verified |
| Receivables facility | 416 held flat; SOFR + 0.95% (~19/yr) | 10-Q Note 6 | Verified; excluded from EV, interest charged |
| Debt breakage | ~37 (0.5% of existing debt) | 101% change-of-control put on ~3,750 of notes; term loans prepay at par | Assumption |
| Term Loan A increase, Aug 28, 2026 | Not in model | +100 principal; Term Loan A now 520.3 (Form 8-K) | Not modeled: use of proceeds not disclosed |
| SOFR 3.6%; TLB spread 350bp; notes 8.5%; fees 1% / 2.25% | As stated | Fed funds target 3.50-3.75%; remaining terms illustrative | Assumption |

## Reconciliation to Capital IQ debt

Capital IQ reports total debt of 7,784.7. Its principal build is term loans 3,609.4 + notes 3,749.9 + all lease liabilities 155.5 +
receivables facility 416.0 = 7,930.8, less discounts and accounting adjustments. ADT's own net debt of about $7.4bn excludes the receivables
facility, which is why the model's net debt (7,414) is lower.

## Open items

1. Dilution is an estimate; replace it with the Q3 2026 10-Q award table (IRR moves about 0.5 point per 16mm shares).
2. Confirm the receivables facility can stay in place after a change of control.
3. Sec. 163(j): ADT carries a disallowed-interest carryforward (indefinite). The model ignores the existing balance and future carryforwards (conservative); a buyout would also trigger a new Sec. 382 ownership-change limit.
4. ADT flagged 2027 headwinds of $50-100mm each from higher taxes and expiring swaps on the Q2 call; not modeled.
5. Q3 2026 results (early November) will update LTM figures, net debt and share count.
