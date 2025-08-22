Insurance data analysis-Dashboard



## Problem Statement

Insurance companies often deal with large volumes of customer and claims data, making it difficult to identify patterns in premium amounts, claim statuses, and customer demographics. The challenge was to design an interactive Power BI dashboard that provides clear insights into claims, customer profiles, and policy distributions, enabling business users to drill deeper into data for decision-making.


## Key Goals-


1)Build a clean, interactive dashboard in Power BI.

2)Represent key metrics such as claim amounts, premium amounts, coverage, and active/inactive policies.

3)Enable visual exploration across demographics like gender and age groups.

4)Provide advanced features such as drill-through filters and slicers for policy types.

5)Ensure consistent formatting and alignment with business-friendly reporting standards.


## Steps Followed-


- Step 1 : **Importing Data into SQL Server-**
Created a new database InsuranceDB in SQL Server, imported the dataset using the Import Flat File option, adjusted column data types, and verified the data with a SELECT * query to ensure successful loading.

- Step 2 : Connecting SQL Server Data to Power BI
Connected InsuranceDB from SQL Server to Power BI Desktop using Import Mode. Previewed and transformed data in Power Query Editor, reviewed key columns (policy details, customer info, premiums, claims, claim status, etc.), and loaded ~10,000 rows into the data model for analysis.

- Step 3 : Data Profiling & Validation in Power BI

Performed data profiling in Power Query Editor to ensure correct data types and column quality. Enabled column distribution, column profile, and column quality for the entire dataset (~10,000 rows). Verified each column:

1)-Policy Number / Customer ID → Text, unique values (primary key check).

2)-Gender → Text, two distinct values (Male/Female).

3)-Age → Whole number, range 18–87.

4)-Policy Type → Text, max claims from Travel.

5)-Dates (Start, End, Claim Date) → Correctly set as Date type (noted ~44% missing Claim Dates).

6)-Premium & Coverage Amounts → Decimal.

7)-Claim Status → Text, with 3 categories (Settled, Rejected, Pending).

Ensured data integrity, distinct counts, and handling of nulls before proceeding to transformations and reporting.

- Step 4 : In this step, we set up the initial report by applying a dark theme for better visualization, adding slicers for Policy Number, Claim Number, and Customer ID to enable interactive filtering, and inserting the company name Prism Insurance Pvt. Ltd. for branding. The slicers were formatted into dropdown style and neatly arranged on the report page for clarity.


  <img width="290" height="131" alt="image" src="https://github.com/user-attachments/assets/8cd79dea-ddb2-4b4d-bfc2-f4a74e2c03d9" />     <img width="588" height="57" alt="image" src="https://github.com/user-attachments/assets/876c04d5-665e-4626-8485-9cbe1f07e497" />


- Step 5 :n this step, we formatted the slicers by updating their font style for better readability and added new card visuals to display key metrics—Premium Amount, Coverage Amount, and Claim Amount. Each card was customized with rounded rectangles, resized for clarity, and labeled properly. The visuals were made interactive, so selecting any Policy, Claim Number, or Customer ID dynamically filters the cards, showing relevant amounts. This step enhanced both readability and interactivity of the report.

snap of one of the card visual - 

<img width="201" height="76" alt="image" src="https://github.com/user-attachments/assets/29f1cc5b-f364-4556-98b7-13a9b952cc57" />




- Step 6 :In this step, we enhanced the report by adding a Multi-row Card to display the count of male and female customers, making the dashboard more interactive by filtering other visuals (cards, slicers, charts) based on gender selection. Additionally, we introduced a Ribbon Chart to show the distribution of claims by status (Rejected, Settled, Pending). Both visuals were formatted with customized fonts, borders, colors, and titles for improved readability and presentation.

- Step 7 :**Adding Stacked Bar & Line Charts with Age Group Analysis-**
In this step, we enriched the report with additional visuals for deeper insights. A Stacked Bar Chart was added to display the premium amount by policy type, with customized formatting such as font styling, data labels, bar colors, and a refined title. Next, we created an Age Group column in Power Query using conditional logic to categorize customers into Young Adult, Adult, and Elder groups. Using this, we added a Line Chart to show claim amounts across age groups, enhanced with markers, shaded areas, data labels, and a clean formatted title. Both charts were styled for clarity and aligned with the overall dashboard theme, while maintaining interactive filtering across all visuals and slicers on the report page.

 snap of line chart- 

 <img width="295" height="177" alt="image" src="https://github.com/user-attachments/assets/9f6d4947-27a7-427f-b3e0-e039fa6e7d08" />

- Step 8 :**Adding Donut Chart & Matrix Visual-**

In this step, we created an Active/Inactive column in Power Query using conditional logic on policy end dates, enabling us to classify customers accordingly. This field was then used to build a Donut Chart that displayed the count of active vs. inactive policies with customized formatting, colors, labels, and borders for better clarity. Additionally, we added a Matrix Visual to show claim coverage amounts across different policy types and claim statuses. The matrix was formatted with custom fonts, borders, and gridlines to enhance readability, completing a more detailed and structured report page.

- Step 9 :**Drill Through Filters-**

In this step, we explore the Drill Through functionality in Power BI. Drill Through allows us to filter a second page of the report based on a selection made in a visual on the first page. For example, we can create a new page with a full table of data and then, by right-clicking on a policy type in the bar chart, drill through to see only the records for that selected policy type. Power BI also provides a back button automatically, making it easy to navigate between pages.
 
 snap of the new page's table -
 <img width="852" height="453" alt="image" src="https://github.com/user-attachments/assets/cdea3c9b-807f-4d7a-a7e6-2a713c3a23b9" />

# Snapshot of Dashboard (Power BI Service)-

<<img width="1365" height="662" alt="image" src="https://github.com/user-attachments/assets/874df161-6d92-41cc-acf5-841524e1f3f9" />



Report Snapshot (Power BI DESKTOP)-

<img width="937" height="539" alt="image" src="https://github.com/user-attachments/assets/07b94ab2-451e-43c9-bc3a-28b0f5714d43" />

# Final Outcome -


The final dashboard enables insurance stakeholders to:

1)-View key KPIs (coverage, premium, claims) at a glance.

2)-Explore claim statuses and policy types with interactive visuals.

3)-Analyze customer demographics through gender and age segmentation.

4)-Drill through to detailed records for deeper investigation.

This project demonstrates end-to-end Power BI dashboard development, including data modeling, Power Query transformations, advanced visuals, and interactivity features.

