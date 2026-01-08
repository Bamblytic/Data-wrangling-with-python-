# Data-wrangling-with-python-
# Data Wrangling on Automobile Dataset

This project is a Jupyter notebook that demonstrates a complete **data‑wrangling pipeline** on a classic automobile dataset. [file:87]

The notebook walks through importing raw data, cleaning and transforming it, engineering new features, and preparing the final dataset for downstream analysis or machine learning models. [file:87]

---

## Dataset

- Source: Automobile dataset with **205 rows × 26 columns**, each row representing a car model. [file:87]  
- Example columns:  
  - Categorical: `make`, `fuel-type`, `aspiration`, `num-of-doors`, `body-style`, `drive-wheels`, `engine-location`, `fuel-system`. [file:87]  
  - Numeric: `symboling`, `normalized-losses`, `wheel-base`, `length`, `width`, `height`, `curb-weight`, `engine-size`, `bore`, `stroke`, `compression-ratio`, `horsepower`, `peak-rpm`, `city-mpg`, `highway-mpg`, `price`. [file:87]  

---

## Notebook overview

### 1. Load and inspect data

- Load the raw CSV into a pandas DataFrame.  
- Inspect the head/tail, shape, column names, and summary statistics to understand structure and data types. [file:87]  

### 2. Handle missing values

- Detect placeholder missing values encoded as `"?"` and convert them to `NaN`. [file:87]  
- Explore where missing values occur using boolean masks and summary checks, then:  
  - Impute numeric features such as `normalized-losses`, `bore`, `stroke`, `horsepower`, and `peak-rpm` with appropriate statistics (e.g., mean).  
  - Drop rows where critical target variables like `price` are missing. [file:87]  

### 3. Correct data types

- Convert numeric‑like object columns into proper numeric types, including `normalized-losses`, `bore`, `stroke`, `horsepower`, `peak-rpm`, and `price`. [file:87]  
- Ensure the final DataFrame uses consistent numeric dtypes for quantitative analysis and modeling. [file:87]  

### 4. Feature transformation and engineering

- Create a new feature `city-L/100km` by converting `city-mpg` to litres per 100 km using the standard formula \(L/100km = 235 / mpg\). [file:87]  
- Normalize or scale continuous variables (for example, scaling `length` relative to its maximum) to bring them into comparable ranges. [file:87]  
- Explore relationships between features such as engine size, fuel consumption, and price. [file:87]  

### 5. Categorical encoding

- Apply one‑hot encoding to categorical features like `fuel-type`, `aspiration`, `num-of-doors`, `body-style`, `drive-wheels`, and similar columns. [file:87]  
- Concatenate encoded columns back into the main DataFrame, expanding the feature space to 60+ columns suitable for machine‑learning models. [file:87]  

### 6. Final clean dataset

- Produce a clean, model‑ready DataFrame with:  
  - No `"?"` placeholders.  
  - Correct numeric dtypes for all quantitative variables.  
  - One‑hot encoded categorical variables.  
  - Engineered feature `city-L/100km`. [file:87]  
- The final dataset can be used for tasks such as regression to predict car price or fuel consumption. [file:87]  

---

## Technologies used

- Python  
- pandas for data manipulation and cleaning. [file:87]  
- NumPy for numerical operations. [file:87]  
- Jupyter Notebook for interactive analysis. [file:87]  

---

## How to run

1. **Clone the repository**

   ```bash
   git clone https://github.com/<your-username>/<your-repo-name>.git
   cd <your-repo-name>
