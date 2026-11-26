# Robotics & Automation Directory

One self-contained page: `index.html`. It holds all the data and the chart library inside the file, so it needs no other files and no internet connection.

## Put it on GitHub Pages
1. Replace `index.html` in your repository with the one in this folder (upload it over the old one, same name, same place).
2. Delete the old `d3.min.js`, `data-india.csv` and `data-world.csv` from the repository root if they are still there. The page no longer uses them.
3. In the repository, open Settings, then Pages, and check that the site is built from the branch and folder that contain `index.html`.
4. Wait a minute, then open the site and refresh without cache (Ctrl+Shift+R, or Cmd+Shift+R on Mac). The old version can stay in the browser cache.

## What is in the page
- **Companies:** 1,011 robotics and automation companies (348 India, 663 World). Names link to the website, or LinkedIn if there is no website.
- **Supplier map:** 655 Indian supplier listings (569 companies) and 295 foreign supplier listings (238 companies).
- **Analytics:** charts for both, with Bars / Pie / Numbers toggles.
- **Supply chain:** a visual flow and detailed tables of the 14 layers.
- **README:** how to read the data.

## The `data` folder
CSV copies of the data, for reference and for editing in a spreadsheet. The page does not read them. After you change them, ask for a rebuilt `index.html` to show the changes.

- `data-india.csv`, `data-world.csv`: company lists (20 Nov 2026)
- `suppliers-india.csv`, `suppliers-foreign.csv`: supplier lists (26 Nov 2026)
- `taxonomy.csv`: the 14 layers and 115 components
