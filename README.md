# RMS vs. ROE – Polish apparel market 2025

An interactive bubble chart that plots **Return on Equity** against **relative market share (RMS)** for the main clothing, footwear and accessories retailers in Poland. It also includes a builder for testing M&A scenarios.

**[▶ Open the interactive chart](./index.html)**

---

## What the chart shows

| Element | Meaning |
|---|---|
| **X axis** | Relative market share = own sales in scope ÷ sales of the largest competitor (for the leader: ÷ #2). Log scale. |
| **Y axis** | ROE = net income ÷ average equity, latest fiscal year. |
| **Bubble area** | Sales in scope 2025 (PLN m). See the legend in the upper-left corner. |
| **White corridor** | Normative band: log trend of ROE on RMS across 13 companies (Decathlon excluded as an outlier), ± 1 standard deviation of the residuals (≈ 15.7 pp). |
| **Hatched bubbles** | Pro forma merger scenarios. |

The trend is **ROE ≈ 32.5% + 8.7 pp × ln(RMS)**. The fit is weak (R² ≈ 0.26), so treat the corridor as a guide, not a precise benchmark.

## How to use it

### Controls (bar above the chart)

- **Scenarios on chart**: show or hide each scenario. Click **×** to delete one.
- **Band ±**: widen or narrow the corridor. **1σ** resets it to one standard deviation.
- **Format**: set the chart's shape.
  - **16:9 wide** (1100 × 620) and **4:3 standard** (827 × 620) match the shape of a whole slide.
  - **Width / Height** sliders set any other shape. Text and bubbles stay the same size; only the plot area stretches.
- **Labels**: show or hide the company names. Modivo, LPP and Inditex always stay labelled.

Hover a bubble, or move to it with Tab, for its full figures and its distance from the trend. The data table below the chart can be sorted by clicking a column header.

### Build an M&A scenario

1. Choose an **acquirer** and tick one or more companies to **merge with**.
2. Optionally add a **company not on the chart** (name, sales, net income, average equity in PLN m).
3. Optionally enter **adjustments**:
   - *Net income synergies*: PLN m per year.
   - *Sales lost to overlap*: % of combined sales.
   - *Equity added / paid*: positive for new equity issued, negative for cash paid out of equity.
4. Check the live preview, then click **Add to chart**.

Pro forma = sum of the companies' sales, net income and average equity, plus your adjustments. RMS is measured against the largest competitor left after the merger.

Scenarios and the chart format are saved in your browser (`localStorage`). They are not shared with other visitors. **Restore workbook scenarios** brings back the three scenarios from the original workbook.

## Putting the chart on a slide

Size the chart to the space it will fill, not to the whole slide, because the title and source line take up part of the height.

| Where it goes | Space for the chart | Ratio | Width × Height |
|---|---|---|---|
| 16:9 slide, full width under a title | ~12.3 × 5.6 in | ~2.2 : 1 | **1240 × 570** |
| 4:3 slide, full width under a title | ~9.2 × 5.6 in | ~1.65 : 1 | **1000 × 605** |
| 16:9 slide, chart on the left ⅔ with text on the right | ~8.3 × 5.6 in | ~1.5 : 1 | **920 × 615** |
| Whole slide, no title (e.g. appendix) | full slide | 16:9 or 4:3 | use the preset buttons |

At 1240 × 570, scaled to 12.3 in wide, the chart text comes out at about 9 pt, the smallest that is still easy to read on a projector. Avoid going much wider than about 1300.

## Merger scenarios: what stands out

Modivo combined with each company, as plain sums with **no synergies**:

| Modivo + … | Sales PLN m | Market share | RMS | ROE | vs. trend |
|---|---:|---:|---:|---:|---:|
| **Pepco** | 9,467 | 13.3% | 1.04 | **15.6%** | −17 pp |
| **Inditex** | 10,635 | 15.0% | **1.17** | **15.0%** | −19 pp |
| H&M + Deichmann | 10,559 | 14.9% | 1.16 | 9.4% | −24 pp |
| Decathlon | 7,753 | 10.9% | 0.85 | 6.9% | −24 pp |
| H&M | 9,507 | 13.4% | 1.05 | 6.5% | −26 pp |
| Deichmann | 7,404 | 10.4% | 0.81 | 5.0% | −26 pp |
| Zalando | 9,155 | 12.9% | 1.01 | 2.0% | −31 pp |
| Answear | 6,768 | 9.5% | 0.74 | 1.4% | −29 pp |
| *Modivo standalone* | 6,352 | 9.0% | 0.70 | 1.1% | −28 pp |

1. **Size alone does not fix ROE.** Modivo's issue is PLN 1.95bn of equity earning PLN 22m. Partners with little profit (Zalando, Answear, KiK, VRG) add sales but leave ROE at 1–2%. Modivo + Zalando overtakes LPP on RMS (1.01) and is still at 2% ROE: a market-position story, not a returns story.
2. **Pepco and Inditex are the only partners that change the picture.** Both bring high profit on little equity. Each lifts ROE to about 15% and makes Modivo #1 in the market (RMS > 1). Modivo + Pepco needs only about **PLN 50m of net income synergies** to reach the corridor; Modivo + Zalando would need about **PLN 330m**.
3. **Deichmann fits the business but not the numbers.** Footwear overlaps with CCC, so some sales would likely be lost. It is a good case for testing *Sales lost to overlap*.
4. **Decathlon is misleading on the chart.** Its 83% ROE comes from a very small equity base (PLN 149m), so the combined result (6.9%) is far below what its bubble suggests.

### Caveats

- These are illustrative sums of the companies' figures. They take no view on whether a deal is possible. Inditex, H&M and Pepco are Polish units of large groups.
- They ignore purchase price and goodwill, which would add to equity and lower ROE. Use *Equity added / paid* to model this.
- Several large combinations (e.g. with Deichmann or Zalando) would likely face competition-authority review.

## Data and sources

- Polish entities from eKRS where available (Inditex = sum of Polish subsidiaries, Zara Home excluded; Zalando = Zalando OpCo Polska).
- Modivo and LPP from company reports. VRG = VRG SA standalone, jewellery (W.Kruk) removed. Shein allocated from group figures (HK prospectus).
- Shein and Zalando revenue are estimates in the market model (Euromonitor e-commerce share).
- C&A fiscal year Mar–Feb, treated as 2025. Pepco excludes Dealz.
- Total market in scope: PLN 70.9bn.
- RMS is based on sales value, not units.
- Source: Modivo market model, sheet "RMS vs. ROE" (24 Nov 2025).

## Hosting on GitHub Pages

1. Put `index.html` and this `README.md` in the root of a repository.
2. In the repository, go to **Settings → Pages**, choose **Deploy from a branch**, select `main` and `/ (root)`, and save.
3. After a minute the chart is live at `https://<your-username>.github.io/<repository-name>/`.

The page is a single self-contained HTML file. It only loads the IBM Plex fonts from Google Fonts and falls back to system fonts if they are unavailable.

> **Note:** A public GitHub Pages site can be seen by anyone, even if the repository is private (on paid plans). Check that the figures are cleared for sharing before publishing.
