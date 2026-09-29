# Assistance Declaration

This file lists all the outside help I used in this project e.g AI tools. I will update it as I go.

## Generative AI / coding assistants

Date - What for - Tool - What it did - What I did / how I checked it

25/09/2026 - Choosing a dataset - Claude - Suggested a list of possible UCI datasets - Picked AI4I myself and checked the licence and details on the UCI page

26/09/2026 - JupyterLab / notebook setup - Claude - Explained how to create the notebook, add and run cells (code and markdown) and the relative file path for loading the data - Wrote and ran all cells in 01_data_audit.ipynb myself

29/09/2026 - Fixing a NameError in 01_data_audit.ipynb - Claude - Explained that "name 'df' is not defined" happened because I reopened JupyterLab and ran df.head() without first running the import and load cells, so the kernel had no df in memory. Suggested running the cells in order or using Restart Kernel and Run All Cells - Ran the cells above in order myself and confirmed df.head() and df.info() worked

29/09/2026 - Section 2 of the audit (data dictionary) - Claude - Explained how to make a table in a markdown cell, and gave me the full table (types, units, roles, availability at prediction time) - Checked the values against the UCI variables table and the df.info() output, and rendered and saved the cells myself

29/09/2026 - Section 3 of the audit (missing values and duplicates) - Claude - Taught me how to find the missing-value, duplicate and ID checks, and pointed out that df.duplicated() can't find duplicates because UDI is unique, suggesting I also check with the ID columns dropped - Wrote the code and ran the cells myself, checked the outputs, and updated my conclusions to match the results