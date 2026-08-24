FestiveCart-Sales-Analytics: Exploratory Data Analysis (EDA)

📌 Business Problem
During major festive shopping periods like Diwali, retail platforms experience high transaction volumes across various demographics and product verticals. The primary objectives of this project are:
1. Improve Customer Experience: Understand customer preferences and spending behavioUrs through sales data analysis.
2. Increase Business Revenue: Identify key revenue-generating demographics, locations, and high-demand product categories to optimize inventory, targeted advertising, and stock allocation.

Environment Setup & Tools Used
* Python Environment: Configured via PowerShell (`pip install Jupyter Notebook`) and launched using `python -m notebook`.
* Libraries Installed & Imported:
  * Pandas: Data manipulation, cleaning, and aggregation (`pd.read_csv()`, `df.dropna()`, `df.describe()`).
  * NumPy: Numeric operations and array processing.
  * Matplotlib (`%matplotlib inline`): Static data visualization rendering directly inside the notebook.
  * Seaborn (`sns`): Enhanced statistical data visualisations (bar plots, count plots).

Data
* Dataset Size: 11,252 recorded transactions.
* Attributes: Includes demographic indicators (Gender, Age Group, Marital Status, State, Occupation) and transaction details (Product Category, Product ID, Order Count, Amount).

Data Cleaning
To ensure high data quality prior to analysis, various Pandas functions were applied to clean the dataset:
* Handling Missing Values: Executed `df.dropna(inplace=True)` to remove blank/null rows in memory.
* Data Type Conversion: Converted floating-point numeric columns (such as `Amount`) into integer formats (`df['Amount'].astype('int')`) for clean mathematical aggregation.
* Column Renaming & Cleanup: Renamed ambiguous columns and dropped unnecessary uninformative columns to streamline processing.
  
Data Transformation
* Aggregated raw transactional records using `df.groupby()` to compute total sales (`Amount`) and total volume (`Orders`).
* Created key demographic groupings based on `Age` brackets and `Marital_Status` indicators to isolate high-value consumer target segments.

Analysis
Exploratory Data Analysis was performed across 7 key parameters:
1. Gender: Comparing total orders and purchasing power between male and female shopping.
2. Age Group: Identifying top-contributing age brackets to overall retail revenue.
3. State: Mapping geographic revenue distributions across various Indian states.
4. Marital Status: Assessing spending patterns between single vs. married consumers.
5. Occupation: Evaluating buying trends across different employment sectors (IT, Healthcare, Aviation, etc.).
6. Product Category: Evaluating top-performing verticals (Food, Clothing, Electronics, etc.).
7. Product ID: Identifying individual high-volume SKUs.

Visualization
Data patterns were visualised using `Matplotlib` and `Seaborn`:
* Count plots (`sns.countplot`) for demographic distributions (Gender, Marital Status, Age Groups).
* Grouped bar charts (`sns.barplot`) for state-wise revenue and occupation-based spending comparisons.
* Category-wise sales distribution charts to highlight dominant product verticals.

Insights
* Primary Target Demographic: Married women in the 26–35 years age group generate the highest sales volume.
* Geographic Hotspots: The top states contributing to total sales are Uttar Pradesh (UP), Maharashtra, and Karnataka.
* High-Value Occupations: Buyers working in IT, Healthcare, and Aviation sectors demonstrate the highest purchasing capacity.
* Dominant Product Categories: The majority of expenditure is concentrated in Food, Clothing & Apparel, and Electronics.

Recommendations
1. Targeted Ad Campaigns: Allocate festive marketing budgets toward digital ads targeted at married women aged 26–35 in UP, Maharashtra, and Karnataka.
2. Inventory Optimization: Maintain higher inventory stock for high-demand verticals (Food, Clothing, Electronics) prior to peak festive surges.
3. Sector-Specific Promotions: Launch targeted promotional packages or corporate offers tailored for professionals in IT, Healthcare, and Aviation.

Impact
* Enables data-driven inventory management, preventing stockouts in high-demand categories during festive surges.
* Optimizes marketing spend by targeting hyper-specific buyer personas, resulting in higher ROI and customer retention.
