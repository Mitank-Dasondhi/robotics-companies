# Robotics & Automation Directory

A searchable directory of 859 robotics and automation companies: 330 in India and 529 in the rest of the world. One static page, no build step.

## Files

| File | What it is |
|---|---|
| `index.html` | The whole page (layout, styles, scripts). |
| `d3.min.js` | The chart library (d3, ISC licence), included so the page needs nothing from the internet. |
| `data-india.csv` | The India list (330 companies). |
| `data-world.csv` | The World list (529 companies). |

## Put it on GitHub Pages

1. Create a repository and upload all five files to the root.
2. Go to **Settings → Pages**, choose the `main` branch and the root folder, then save.
3. Open the link GitHub gives you.

## Run it on your computer

Browsers block a page from reading files when you open it straight from a folder, so serve it:

```
python3 -m http.server
```

Then open http://localhost:8000.

## If the page is blank or shows dashes

- Open the page from GitHub Pages or `python3 -m http.server`, never by double-clicking `index.html`. Browsers block the data files in that case, and a yellow note appears at the top.
- Make sure all five files are in the same folder (the repo root), with these exact names.
- GitHub Pages can take a minute or two after the first save. Refresh with Ctrl+Shift+R.
- Open the browser console (F12, then Console) and read any red message. That is what to send if you need help.

## Update the data

Replace the two CSV files. Keep the header row exactly as it is:

- `data-india.csv`: `S.No, Segment, Company, Website, LinkedIn, Category, HQ City, India Presence, Headcount, What they do`
- `data-world.csv`: `S.No, Segment, Company, Website, LinkedIn, Category, HQ City, Country, Headcount, What they do`

Headcount values the page recognises: `1`, `2-10`, `11-50`, `51-200`, `201-500`, `501-1,000`, `1,001-5,000`, `5,001-10,000`, `10,001+`. An empty value shows as "Not listed". Any new category appears automatically.

## How the list is ordered

Each list starts with the **Robotics** companies. Below them, with serial numbers running straight on: **Suppliers (Tier 2-3)**, then **Aerospace & Space**, **Drones & UAVs** and **AV & Adjacent** at the very end. The list is shown in `S.No` order, with a divider row at the start of each segment. To change the order, change the `S.No` values in the CSV (and the segment order in `SEG_ORDER` in `index.html`).

Suppliers, aerospace, drones and AV & adjacent companies are in the India list when their country is India, and in the World list otherwise. In the `Category` column, Robotics rows hold the sub-category and Suppliers rows hold the tier.

Segments: `Robotics`, `Suppliers (Tier 2-3)`, `Aerospace & Space`, `Drones & UAVs`, `AV & Adjacent`. Each has a fixed colour (blue, orange, green, yellow, purple).

## What the page has

- **Companies:** search, clickable segment tiles, filters (segment, sub-category, city or country, headcount, and India presence on the India list), sortable columns, 50 rows per page, click a row for the description and links.
- **Analytics:** for each list, share by segment, top sub-categories, top cities (India) or countries (World), headcount, and segment by company size. Click a bar to open those companies.
- **README tab:** column guide and a table of data gaps.

## Design rules

White page, one font, light pastel highlights, dark shades for charts. Segments keep the same colour everywhere, on both lists and in every chart. The selected market button is light blue.

## Notes

- "India presence" in the sheet is free text. The filter groups it into "HQ in India" (exactly `HQ`) and "Office or R&D in India" (everything else).
- The data is a copy of the "Robotics & Automation Directory – MASTER" Google Sheet taken on 19 November 2026 (segmented version).
