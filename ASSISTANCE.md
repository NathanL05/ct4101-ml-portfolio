# Assistance Declaration

This file records all outside help used in this project, as required by the CT4101 brief (generative AI, coding assistants, external code and collaboration). It is updated as the work progresses.

## How I used AI

I used Claude (Anthropic) as a tutor and coding assistant. It explained concepts, suggested approaches, and provided code and draft text for some sections; each entry below states which. For everything it provided, I ran the code myself, checked outputs against the data and the CT4101 lecture slides, and edited explanations so they match my own results. I made the final decisions about the dataset, features, evaluation design and conclusions, and I have tried to make sure I can explain every line of code and every decision in this repository.

## Generative AI / coding assistants

Date - Area - What Claude provided - My own work and verification

25/09/2026 - Choosing a dataset - A list of candidate UCI datasets - Chose AI4I 2020 myself and checked its licence, size and documentation on the UCI page

25/09/2026 - Project plan - A step-by-step project plan (kept outside this repository) - Followed it as a guide for the order of work; I reviewed and justified each step myself

25/09/2026 - Reference solution - A reference solution to the project, kept outside this repository and not submitted - Used for reference only. No code, text or files from it were copied into this repository, and each section of my work was run and checked against my own data.

25/09/2026 - Proposal (Milestone 1) - An example proposal, explanation of the brief's requirements, and a review of my draft - Wrote and formatted the submitted proposal myself

26/09/2026 - Environment setup - Explained a pip "externally-managed-environment" error and how to create a virtual environment - Set up the venv and requirements.txt myself and checked it with the Week 2 commands

26/09/2026 - README files - Templates for README.md and data/README.md - Edited and simplified them, and added the dataset details from the UCI page

26/09/2026 - JupyterLab setup - Explained how to create a notebook, add and run cells, and the relative path to the data - Created and ran 01_data_audit.ipynb myself

29/09/2026 - Audit 1: first look - Draft observation bullets for df.head() and df.info(); explained a NameError caused by restarting the kernel - Checked each bullet against my output and reworded them; fixed the error by running the cells in order

29/09/2026 - Audit 2: data dictionary - How to make a markdown table, the table contents, and the leakage explanation - Checked every row against the UCI variables table and the df.info() output

29/09/2026 - Audit 3: missing values and duplicates - Code for the missing-value, duplicate and ID checks, and the point that df.duplicated() cannot find duplicates while UDI is unique - Ran the checks, added the check without ID columns, and wrote conclusions that match the outputs

29/09/2026 - Audit 4: target distribution - Code for the class counts and bar chart, and an outline of the conclusions - Checked the counts (339 failures, 3.4%) and how they affect metric choice

29/09/2026 - Audit 5: failure-mode check - Code for the failure-type counts and the label consistency check - Ran it, found that all 18 inconsistent rows are RNF, and recorded this as label noise

29/09/2026 - Audit 6: outliers - Code for the summary statistics, box plots (with plt.tight_layout()), the IQR rule and the failure rate with and without outliers; an outline of the decision - Interpreted the results (418 speed and 69 torque outliers, 15.7% vs 2.8% failure rate) and decided to keep the outliers

30/09/2026 - Audit 7: product type - The groupby code and draft conclusions - Checked the counts and failure rates for L, M and H against my output

30/09/2026 - Audit 8: leakage register - A list of leakage risks and the table - Checked each risk against my data and the Week 3 lecture

30/09/2026 - Audit 9: engineered features - The power formula (rpm to rad/s), the temperature difference idea, the code and the table - Checked the formula and units, and compared both features between failures and non-failures

30/09/2026 - Audit 10: summary - A draft summary of the audit findings - Checked every number against the earlier sections

02/10/2026 - Notebook 02, Section 1 - Code for loading the data, dropping ID and failure-type columns, and separating X and y - Checked X has 6 columns and no ID, failure-type or target columns

02/10/2026 - Week 4 review and evaluation protocol (02, Sections 2–3) - A comparison of my plan with the Week 4 lecture, a recommendation of F2 as the primary metric, the protocol table and the configuration cell - Identified the Week 4 changes needed myself, then checked the protocol against slides 18, 23, 26, 44 and 45 and confirmed the versions match requirements.txt. I accepted F2 after checking it against the lecture and my 3.4% class imbalance.

02/10/2026 - Time-order check (01, Section 8) - Found that the rows are in time order, the code to measure it, and the rewritten leakage risk 5 - Ran the code, checked the numbers, and used them to justify the split in notebook 02

02/10/2026 - Train/test split (02, Section 4) - Code for the stratified split and the explanation of the design - Checked the 8,000/2,000 split and the 3.4% failure rate in both sets

02/10/2026 - Notebook 02, Section 5 (preprocessing) - Code for the ColumnTransformer and the design explanation - Checked the output has 8 columns with the expected names, and checked the choices against Week 3 slides

13/10/2026 - Notebook 02, Section 7 (baseline diagnostics) - Explained cross_val_predict, predict_proba and how to read the confusion matrix - Ran it, checked the confusion matrix counts add up to the 8,000 training rows (271 failures) and that the medians (0.007 and 0.211) match my output

13/10/2026 - Notebook 02, Section 8 (coefficient interpretation and stability) - Explained odds ratios, per-standard-deviation interpretation and correlated features - Checked the coefficients, odds ratios and standard deviations against my output and the interpretation against Week 5 slides

05/11/2026 - Notebook 03, Section 1 (setup) - Showed me how to structure the shared setup and evaluate() function, with code, and explained each part (stratified split, preprocessing pipeline, cross-validation, scoring metrics) - Ran the code and checked that the split and baseline scores match notebook 02

05/11/2026 - Notebook 03, Section 2 (kNN) - Explained how grid search and the kNN parameters work and how to interpret the results. I wrote the grid search and evaluation code myself. - Ran it, checked the results against my output, and can explain why k = 1 was selected and its limitations

05/11/2026 - Notebook 03, Section 3 (Decision Tree) - Code for the grid search and evaluation, and an explanation of the tuned settings - Ran it, checked the results against my output, and can explain the tuned settings and why the scores are close across the top settings

05/11/2026 - Notebook 03, Section 4 (Random Forest) - Code for the grid search and evaluation, and draft findings - Ran it, checked the results against my output, edited the findings, and can explain how a forest differs from a single tree and why the F2 gain is modest

05/11/2026 - Notebook 03, Section 5 (visualisations) - Code for the out-of-fold precision-recall curves and the confusion matrix, and draft findings - Ran it, checked that the confusion matrix sums to the 8,000 training rows and matches my output, and can explain why precision-recall curves suit a 3.4% positive class

05/11/2026 - Notebook 03, Section 6 (error analysis) - Code for labelling errors, the failure mode table and the feature comparison, and draft findings - Ran it, checked that the outcome counts match the confusion matrix and my output, and can explain why tool wear failures are missed

05/11/2026 - Notebook 03, Section 7 (model settings and draft conclusion) - Help building the settings table, and a draft conclusion - Checked each claim against my results tables, edited the wording, and can explain the limitations and next steps

17/11/2026 - Notebook 04, Sections 1–2 (setup and threshold comparison) - Code for the setup and the out-of-fold threshold comparison, and draft findings - Ran it, checked the results against my own output, and edited the findings to match. I can explain why the threshold is chosen on training data (out-of-fold predictions, so the test set is not used for tuning) and why 0.5 was kept.

17/11/2026 - Notebook 04, Section 3 (engineered features) - Code for the feature comparison and the threshold re-check, a check of the power and heat dissipation rules in the data, and draft findings - Ran it, checked the results against my own output, and edited the findings to match. I can explain why the engineered features improve the model and why that is also a limitation: they encode the rules that define the failure labels, so part of the gain comes from the labels themselves rather than from new information.

17/11/2026 - Notebook 04, Section 4 (time-ordered split check) - Code for the time-ordered validation and the failure modes by period, an investigation into why fold 2 scores lower, and draft findings - Ran it, checked the results against my own output, and edited the findings to match. I can explain why time-ordered validation scores lower than shuffled cross-validation and what this means for real use.

17/11/2026 - Findings wording (notebooks 01-04) - Suggested shorter wording for the findings sections - I checked every figure against my output, removed claims I could not verify, and edited the text so it is in my own words.

## External code

No code copied from external sources. Methods follow the CT4101 lecture slides and the scikit-learn and pandas documentation.

## Collaboration

None.