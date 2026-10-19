# E.Corp Energy Efficiency Program Analysis

**Question:** Are E.Corp's energy efficiency programs (EEPs) reducing residential energy use, and are they worth the cost?

I analyzed 1,200+ records across four datasets (customer info, energy usage, program participation and weather) to measure program participation, energy usage before and after enrollment, and cost-effectiveness, broken down by housing type, income level, zip code and temperature.

**Tools:** MySQL (data validation, cleaning, joins) · Python in JupyterLab (pandas, matplotlib, seaborn) · Power BI (interactive dashboard)

## Key Findings

**1. Most customers joined a program.**
40 of 51 customers enrolled, an adoption rate of **78.4%**.

**2. Energy use went down after customers enrolled.**
Average monthly usage fell from about **790 kWh** before enrollment to about **715 kWh** after, a drop of **9.6%** (about 76 kWh per customer per month). I compared averages rather than totals because the before and after periods cover different numbers of months.

**3. The drop is not just the weather.**
Because temperature affects energy use, I compared before and after usage within each temperature category. Usage dropped in every one:

| Temperature | Avg kWh Before | Avg kWh After | Change |
| --- | --- | --- | --- |
| Cold (<40°F) | 799.6 | 708.6 | -11.4% |
| Mild (40–70°F) | 799.8 | 740.9 | -7.4% |
| Hot (>70°F) | 739.1 | 701.5 | -5.1% |

The biggest savings came in cold months, which suggests the programs work best for heating-related usage.

**4. Cost-effectiveness needs one more number.**
The programs cost about **$6.29 per kWh saved**. To decide whether each program should be improved or eliminated, E.Corp needs its price per kWh, which would let us calculate customer savings and the payback period for each program.

## Recommendations

- Keep the programs rather than eliminating them, since usage declined after enrollment in every temperature range.
- Collect the price per kWh so payback period can be measured for each program.
- Compare results by program to see which ones drive most of the savings.

## Project Structure

| Folder | What's inside |
| --- | --- |
| `MySQL/` | SQL for data validation (duplicates, nulls, date ranges), date cleaning, and joining the four tables into one view |
| `PythonJupLab/Notebooks/` | KPI calculations, weather check and charts |
| `PowerBi/` | Interactive Power BI dashboard (.pbix) |

## How to Run the Notebook

1. Put the dataset in `PythonJupLab/Notebooks/data/ecorp_customer_info_dataset_USE.xlsx`.
2. Open `Ecorp analysis Python.ipynb` in JupyterLab.
3. Run all cells (Run → Run All Cells).

## Screenshots

**Power BI**
<img width="1357" height="761" alt="Power BI dashboard" src="https://github.com/user-attachments/assets/9dc390ef-4349-412f-bdf0-30f155607a8f" />

**MySQL**
<img width="1318" height="604" alt="MySQL queries" src="https://github.com/user-attachments/assets/a5bff9c1-15d0-4ebe-85bf-5dc5c8b1320e" />

**Python**
<img width="1141" height="894" alt="Python notebook" src="https://github.com/user-attachments/assets/48f84393-b0ad-41bf-be12-51dd623eff24" />
