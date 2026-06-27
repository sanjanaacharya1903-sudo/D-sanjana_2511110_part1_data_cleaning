Cleaning Log

Project

Retail Order Data Cleaning and Validation

 Objective

The objective of this project was to transform the raw retail order dataset into a clean, validated, and analysis-ready dataset by applying data cleaning techniques, business validation rules, and generating summary reports for business analysis.

---

Issues Found

 Text Issues

* Leading and trailing spaces in text fields.
* Inconsistent capitalization.
* Different spellings for similar values.
* Blank values in Region and Ship Mode.

 Date Issues

* Missing Order Dates.
* Missing Ship Dates.
* Invalid date values.
* Ship Dates earlier than Order Dates.

 Duplicate Issues

* Exact duplicate records.
* Duplicate Order IDs with conflicting information.

 Missing Values

* Region
* Ship Mode
* Discount

Discount Issues

* Blank discount values.
* Negative discount values.
* Discounts greater than the allowed range.

 Business Logic Issues

* Cancelled Orders
* Failed Payments
* Refunded Orders
* Sales calculation inconsistencies
* Profit calculation inconsistencies

---

 Cleaning Actions Performed

 Text Cleaning

Applied:

* TRIM
* Proper Case
* Find & Replace
* Standardization of category names
* Removed unnecessary spaces

Standardized columns:

* customer_name
* segment
* region
* state
* city
* category
* sub_category
* ship_mode
* payment_status
* order_status

---

 Missing Value Handling

Region

* Missing values replaced with **Unknown**.

Ship Mode

* Missing values replaced with **Unknown**.

Discount

* Missing values replaced with **0** only when other sales fields were valid.

---

 Date Cleaning

* Converted all dates into a consistent Excel Date format.
* Flagged missing dates.
* Flagged invalid dates.
* Flagged Ship Date earlier than Order Date.
* Calculated Shipping Delay.

---

 Duplicate Handling

Performed:

* Exact duplicate detection.
* Duplicate Order ID detection.
* Conflicting record identification.

Exact duplicate rows were removed.

Conflicting duplicate Order IDs were retained and flagged for manual review.

---

Calculated Columns Added

* cleaned_discount
* calculated_sales
* calculated_profit
* profit_margin
* shipping_delay_days
* order_month
* order_year
* data_quality_flag

---

 Business Rules Applied

| Rule                        | Action                                |
| --------------------------- | ------------------------------------- |
| Missing Region              | Filled with Unknown                   |
| Missing Ship Mode           | Filled with Unknown                   |
| Missing Discount            | Filled with 0 when valid              |
| Negative Discount           | Flagged Invalid                       |
| Discount > Allowed Range    | Flagged Invalid                       |
| Cancelled Orders            | Excluded from completed sales summary |
| Failed Payments             | Excluded from completed sales summary |
| Refunded Orders             | Reported separately                   |
| Ship Date before Order Date | Flagged Invalid                       |

---

Assumptions

* Discount is expressed as a decimal percentage.
* Blank discounts indicate no discount when sales information is complete.
* Unknown Region and Ship Mode are acceptable replacement values.
* Cancelled and Failed Payment orders are excluded only from business summaries and not removed from the dataset.

---

 Records Removed

* Exact duplicate records only.

---

 Records Flagged

* Invalid discounts
* Invalid dates
* Shipping issues
* Duplicate Order IDs
* Missing mandatory values
* Sales calculation mismatches

---

Limitations

* Business rules were applied based on the provided specification.
* Customer master data was unavailable for further validation.
* Product master validation was not possible.
* Geographic validation of City and State was outside the project scope.

---

 Outcome

The final dataset is standardized, validated, analysis-ready, and suitable for business reporting, dashboard creation, and further analytical processing.
