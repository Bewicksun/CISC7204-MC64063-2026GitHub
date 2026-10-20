# CISC7204 — Assignment 02 (2026)

**Student:** SUN JIAWEI · **Student ID used for this repository:** MC64063  
**Git commit email:** mc64063@um.edu.mo  
**Course:** Data Science and Data Visualization, University of Macau

Assignment artifacts are organized under [`cisc7204-Assgn02-2026-MC64063`](cisc7204-Assgn02-2026-MC64063), following the optional GitHub repository instructions. Original assignment filenames containing MC640633 have been retained; the repository identifier follows the UM email and Moodle identifier.

| Folder | Work included |
|---|---|
| [Module01](cisc7204-Assgn02-2026-MC64063/Module01) | Dataset exploration, preprocessing, Matplotlib and line plots |
| [Module02](cisc7204-Assgn02-2026-MC64063/Module02) | Area, histogram, bar, pie, box, scatter and bubble plots |
| [Module03](cisc7204-Assgn02-2026-MC64063/Module03) | Waffle charts, word clouds, regression and geospatial visualization |
| [Module04](cisc7204-Assgn02-2026-MC64063/Module04) | Plotly basics and Dash applications (Labs 01–04) |
| [Module05-Practice](cisc7204-Assgn02-2026-MC64063/Module05-Practice) | Australian wildfire analysis and dashboard |
| [Module05-Final](cisc7204-Assgn02-2026-MC64063/Module05-Final) | Automobile sales analysis and interactive dashboard |
| [proposal](cisc7204-Assgn02-2026-MC64063/proposal) | Revised pair project proposal and Macao recovery analysis |

## How to review

Browse each module for notebooks, dashboard Python scripts, screenshots and the existing project-space ZIPs. Open notebooks using Jupyter; launch Dash scripts from their own directory after installing the imports used by that lab. Several labs download course datasets from URLs in their code, so an internet connection is needed. Course lab instructions and source credits remain in the notebooks.

## Verification scope and known issue

This repository preserves the supplied coursework artifacts and saved outputs. It does **not** claim that all labs have been rerun or graded. Module01 Lab01 contains a saved `TypeError` at `df_can['Total'] = df_can.sum(axis=1)`, where text and numeric columns are mixed. This output is retained transparently and needs review before treating the notebook as a clean run. Some code cells in other notebooks also have no saved execution count.

The separately documented [Macao recovery project](https://github.com/Bewicksun/data-science-project) was successfully rerun during portfolio preparation. [Live portfolio](https://bewicksun.github.io/data-science-portfolio/).

## Attribution and AI assistance

Course-provided notebook instructions, educational datasets and third-party materials retain their original ownership and terms; this repository does not grant a new licence over them. Dataset sources are recorded in the notebooks. Macao source links and usage notes are in `proposal/SOURCES.md`. Local IDE settings and source website archives are excluded.

OpenAI Codex assisted with organizing existing files, preparing this repository documentation, configuring GitHub and posting the repository links. This statement describes this repository setup; refer to the original work for any separate AI declarations.
