## Project: Breakfast at the Frat - Time Series Analysis

### Overview

This project analyses promotional strategies for various breakfast-related products using data from the "Breakfast at the Frat" dataset. The analysis uses the SCAN*PRO econometric model to study how different promotional types impact sales, offering insights to improve marketing tactics for retail businesses.

### Table of Contents

1. [Project Structure](#project-structure)
2. [Data Overview](#data-overview)
3. [Preprocessing and Exploratory Data Analysis (EDA)](#preprocessing-and-exploratory-data-analysis-eda)
4. [Model Implementation - SCAN*PRO](#model-implementation---scanpro)
5. [Results and Analysis](#results-and-analysis)
6. [Future Improvements](#future-improvements)

### Project Structure

| File                               | Description |
|------------------------------------|-------------|
| `Breakfast at the Frat Report.pdf` | Detailed report summarising the analysis and findings, including data exploration, EDA, SCAN*PRO model results, and conclusions. |
| `data.csv`                         | Dataset containing information on unit sales, pricing, promotions, store details, and more. This data is critical for running analyses on promotional impacts. |
| `dunnhumby - Breakfast at the Frat User Guide.pdf` | Documentation provided by dunnhumby outlining the dataset fields, usage guidance, and example questions to explore using the data. |
| `Preprocessing and EDA.html`       | HTML document detailing the steps for data preprocessing and EDA, including data cleaning, trend analysis, and seasonality examination. |
| `Scan pro model.html`              | Implementation of the SCAN*PRO model for assessing how different promotional tactics influence sales. |
| `Scan pro model.ipynb`             | Jupyter Notebook containing the code for SCAN*PRO model implementation and model results. |

### Data Overview

The "Breakfast at the Frat" dataset consists of time-series sales data for five products across four categories: mouthwash, pretzels, frozen pizza, and boxed cereal. Key fields include:

- **Unit Sales**: Number of items sold
- **Promotional Indicators**: Whether products were displayed or featured in circulars and if there was a temporary price reduction
- **Store Attributes**: Characteristics of the stores, such as size and location
- **Product Attributes**: Product identifiers, size, and UPC code

For more details, refer to the *User Guide* (`dunnhumby - Breakfast at the Frat User Guide.pdf`)【17†source】.

### Preprocessing and Exploratory Data Analysis (EDA)

In this stage, the dataset was cleaned and prepared for analysis. Key steps include:

1. **Data Merging and Cleaning**: Combined separate files on transactions, products, and stores into a single dataset. Columns with a high percentage of missing values, such as `PARKING_SPACE_QTY`, were removed. Minor rows with nulls in critical fields like `PRICE` and `BASE_PRICE` were also discarded【16†source】.
2. **Trend and Seasonality Analysis**: Examined sales trends over time to understand the influence of promotions. Seasonal patterns in sales were identified, with peak sales periods noted across different categories【18†source】.

### Model Implementation - SCAN*PRO

The SCAN*PRO model, an econometric tool, was employed to quantify the impact of various promotional types on sales:

- **Promotional Impact Analysis**: Calculated the effect of promotions (FEATURE, DISPLAY, TPR_ONLY) on average units sold, highlighting the importance of visibility-focused strategies like FEATURE and DISPLAY for driving sales.
- **Cross-Elasticities**: Explored cross-elasticities to observe the effect of promotions on similar products within the same category【19†source】.

### Results and Analysis

The model findings show:

- **FEATURE** and **DISPLAY** promotions substantially increase sales across categories, especially in items like boxed cereals and bagged snacks.
- **TPR_ONLY** promotions have a lesser impact compared to FEATURE and DISPLAY, indicating that price reductions alone may not be as effective without the visual and strategic support of in-store displays or advertisements【16†source】.

### Future Improvements

Suggestions for model enhancement include:

1. **Refinement of Promotion Timing**: Adjust timing to align better with seasonal demand peaks.
2. **Additional Variables**: Incorporate more external variables, such as competitor promotions, to capture market dynamics more accurately.
