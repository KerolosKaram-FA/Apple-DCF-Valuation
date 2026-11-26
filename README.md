# Apple Inc. – DCF Valuation

An integrated financial model and discounted cash flow (DCF) valuation of Apple Inc. (AAPL), built in Excel. The model links the income statement, cash flow statement and balance sheet, and values the company with two terminal value methods: perpetuity growth and exit multiple.

> Educational project. Not investment advice.

## Results (Base Case)

| Method | Enterprise value | Equity value | Value per share | vs. $340.00 reference price |
|---|---|---|---|---|
| Perpetuity growth (g = 2.5%) | $2,882 bn | $2,916 bn | **$192.90** | (43.3%) |
| Exit multiple (20.0x EBITDA) | $4,370 bn | $4,404 bn | **$291.35** | (14.3%) |

Scenario range per share:

| Scenario | Perpetuity | Multiple |
|---|---|---|
| Best case | $242.53 | $366.81 |
| Base case | $192.90 | $291.35 |
| Worst case | $146.15 | $220.59 |

**Takeaway:** under these assumptions the model values Apple below the $340 reference price. Across the full WACC / growth sensitivity grid the perpetuity method ranges from $136.73 to $335.26 per share, and the exit multiple grid from $255.14 to $333.09, so no grid cell reaches $340. Only the best-case scenario under the multiple method ($366.81) is above it. The valuation is highly sensitive to the discount rate and the terminal value, which makes up 79% of enterprise value in the perpetuity method and 83% in the multiple method.

## Key assumptions

- WACC: 9.4%
- Terminal growth: 2.5% (perpetuity method)
- Terminal multiple: 20.0x EBITDA (multiple method)
- Forecast period: 2026F to 2030F, valuation date 30 June 2026 with a partial-period adjustment for the first year
- Revenue grows from $416.2 bn (2025A) to $714.6 bn (2030F), about 11% a year, driven mainly by Services ($109.2 bn to $283.1 bn)
- Operating (EBIT) margin rises from 32.0% (2025A) to 37.0% (2030F)
- Terminal year is a steady state: every segment grows at the terminal growth rate (2.5%) and margins stay at 2030F levels
- Working capital: receivable days 29, inventory days 9, payable days 100
- Capex forecast per year, with depreciation schedules for existing assets (5 years) and new assets (10 years)
- Net cash of $33.8 bn added to enterprise value; 15,116 million diluted shares
- Reference price: $340.00 (update to the price on your valuation date and note the source)

## Model structure

1. Income statement (by product line, with a Services build)
2. Cash flow statement
3. Balance sheet (balance check = 0 in every period)
4. Working capital schedule
5. Depreciation and PP&E schedules
6. Unlevered free cash flow
7. DCF: perpetuity method and exit multiple method
8. Dashboards: Best / Base / Worst scenario switch and WACC vs. growth (or multiple) sensitivity tables

## Model review log

After a self-review the following issues were corrected:

- Working capital schedule: 2025A net sales pointed at the 2023 column, which distorted historical receivable days (38 to 35).
- Terminal year: segment growth in the terminal column (up to 22.5% for Services) is now tied to the terminal growth rate, and terminal margins are held at 2030F levels. Previously terminal revenue grew 10.9% while the perpetuity growth was 2.5%, and a margin step-down inflated the terminal working capital inflow ($14.8 bn vs. $0.8 bn now).
- Labels: "Less: Net Debt" changed to "Plus: Net Cash" (the model adds net cash), "USD thousands" changed to "USD millions", "Ending Balnce" typo, and forecast years in the PP&E header now show "F" instead of "A".
- Removed a broken link to an external workbook that triggered an "Update links" prompt.

## Files

- `DCF_Apple_3.xlsx`: the full Excel model (set to recalculate when opened)
- `DCF_Apple_s.pdf`: model statements and DCF schedules
- `DCF_Apple_v.pdf`: valuation dashboards and sensitivity tables

## Sources

Historical figures (2023 to 2025) come from Apple Inc.'s annual reports (Form 10-K). Forecasts and valuation assumptions are my own.

## Tools

Excel · Financial modeling · DCF valuation · Sensitivity analysis · Scenario analysis

## Author

Kerolos Karam · [LinkedIn](https://www.linkedin.com/in/kerolos-karam-fmva%C2%AE-fpap%C2%AE-2b52092a1/) · [Portfolio](https://kerolloskaram-fa.github.io/)
