# SampleDMV


#### **Q1. Visualisation Design [20 marks]**

**Question:**  
Given the following brief to create a data visualisation for a client, answer all the questions below. You do not need to create the visualisation.  
“DCU wants to understand the current situation regarding student accommodation. The information summarised in the table below has been collected for currently enrolled students. You are asked to create a single presentation summarising the main finding that 60% of students live within 10 km of the Glasnevin campus and showing the geographical distribution. This will be presented to senior university management.”  
Distance from DCU (km)	Number of students	Percentage of enrolled students	Median monthly rent
0-5	5,600	35	€700
6-10	4,000	25	€850
11-20	3,200	20	€800
21-50	2,400	15	€750
50+	800	5	€700
![image](https://github.com/user-attachments/assets/a37a5177-0fb1-46b6-851c-472020f5b9dd)


1. **Is this an exploratory or explanatory visualisation task?**  
   **Answer:** This is an explanatory visualisation task because it aims to communicate specific insights (e.g., 60% of students live within 10 km of Glasnevin campus) to a targeted audience, in this case, senior university management.

2. **Who is the intended audience for the data visualisation?**  
   **Answer:** The intended audience is senior university management at DCU.

3. **What title might you give to the data visualisation and why? Make assumptions about any conclusion.**  
   **Answer:** A suitable title could be *"Student Accommodation Proximity: Insights on Housing Around Glasnevin Campus"*. This title highlights the focus on proximity and provides context for decision-making.

4. **What specific chart type would you use? Justify your choice referring to the principles discussed in class relating to data types and the message.**  
   **Answer:** A choropleth map or a bubble map could be used to show geographical distribution effectively. These chart types are ideal for spatial data and help visualize how many students live within specific distances from Glasnevin campus.

5. **For your data visualisation, what marks and attributes will you use to encode the data? Be specific about the values of the attributes.**  
   **Answer:** 
   - Marks: Points or areas (e.g., circles or shaded regions on a map).  
   - Attributes: Size (to represent student density), color intensity (to show proximity bands such as <10 km, 10–20 km, etc.), and position (to reflect actual locations on a map).

6. **Considering the purpose and intended audience, comment on how you would use colour or layout principles for this data visualisation.**  
   **Answer:** Use a clear and professional color scheme (e.g., shades of blue) with increasing intensity for closer distances to emphasize proximity. Layout principles should ensure simplicity, with key insights highlighted prominently for quick comprehension by senior management.

---

#### **Q2. Data Cleaning [20 marks]**

**Question:**  
Download the dataset provided in loop and use it to answer the questions below. The dataset contains statistics for the Road Safety Authority Ireland on injuries and deaths for road users (cyclists, pedestrians, passengers, and drivers) grouped by age.

1. **Using the data provided, identify three (3) different possible errors or artefacts in the dataset. These errors or artefacts should each likely come from a different cause. Give the column name and cell reference if appropriate.**  
   **Answer:**  
   - Missing values in “Age Group” column (e.g., Row 15).  
   - Outliers in “Injuries” column where values exceed realistic thresholds (e.g., Row 25 shows 10,000 injuries).  
   - Inconsistent date formats in “Date” column (e.g., DD/MM/YYYY in some rows and MM-DD-YYYY in others).

2. **Briefly describe your approach to finding these errors or artefacts including any tools you used.**  
   **Answer:** I used Excel filters and conditional formatting to identify missing values and outliers. For inconsistent date formats, I applied Excel’s text-to-columns feature and Python’s pandas library for further validation.

3. **Suggest how each error or artefact was most likely introduced and give the phase from the generic data analytics pipeline.**  
   **Answer:**  
   - Missing values: Likely introduced during data collection due to incomplete surveys (Data Collection phase).  
   - Outliers: Possible manual entry errors during data entry (Data Entry phase).  
   - Inconsistent formats: Result of merging datasets from different sources without standardization (Data Integration phase).

4. **Pick one of the errors or artefacts you identified. What data quality methods could be used to avoid or reduce the probability of this specific error/artefact occurring?**  
   **Answer:** For missing values, implementing mandatory fields during survey design or using imputation techniques during preprocessing can help address this issue.

---

#### **Q3. Data Project Analysis (Storage) [20 marks]**

**Question:**  
“At the request of the Irish Government, you are preparing a report on the impact of COVID-19 restrictions on working and commuting behaviour in Ireland during 2020 comparing it to surveys and records from 2019 and 2009. You have data available from data.gov.ie showing pedestrian footfall in the central shopping area, records from the traffic monitoring cameras on the main arterial routes (vehicle count), survey data on working from home practises as well as weather and standard economic (business growth, median wage, import/export figures, etc.) information. You have permission to conduct further consumer surveys as required. The data from the report will need to be accessed and queried on an ongoing basis by many government departments to monitor the impact of policy decisions.”![image](https://github.com/user-attachments/assets/943d9743-e82e-42b2-9588-01af5cd5033c)
 

1. **List three (3) important questions you would ask your client.**  
   **Answer:**  
   - What specific insights are required from this analysis?  
   - How frequently will this data need to be updated or accessed?  
   - Are there any constraints regarding storage budget or infrastructure?

2. **Describe the data sources and/or specific file formats that you are likely to use in collecting and storing the data for this project.**  
   **Answer:** Likely data sources include CSV files from traffic monitoring systems, JSON files from API endpoints like weather services, SQL databases for structured survey responses, and Excel sheets for economic statistics.

3. **Suggest a type of database storage approach to use for this project, giving a reason for your choice and stating any assumptions you make.**  
   **Answer:** A hybrid approach using a relational database like PostgreSQL for structured data (e.g., surveys) combined with NoSQL storage like MongoDB for unstructured data (e.g., JSON weather logs). This ensures flexibility while maintaining query efficiency.

4. **For this project, can you identify any possible risks in terms of data privacy or GDPR requirements? What data items cause this risk?**  
   **Answer:** Risks include processing personal identifiable information (PII) like home addresses or survey responses tied to individuals without proper anonymization measures, violating GDPR regulations.

---

#### **Q4. Data Visualisation Critique [20 marks]**
<img width="452" alt="image" src="https://github.com/user-attachments/assets/1965c5d0-5cc7-405e-8914-f15052b24f22">


**Question:** For the visualisation above, identify the data encoding methods (marks and attributes) and critique the visualisation design according to principles discussed in CA682 – consider how colour, layout, Gestalt etc., have been applied.

1. **Identify the data encoding methods (marks and attributes).**  
   **Answer:** Marks include bars/points; attributes include length/size (quantitative values), color intensity (categorical groupings), and spatial position (geographical location).

2. **Critique of visualisation design according to principles discussed in CA682:**  
   - Color: Overuse of bright colors may distract viewers; better use of muted tones is recommended.
   - Layout: Crowded elements make it hard to focus; grouping related elements using Gestalt principles like proximity can improve readability.
   - Gestalt: Lack of clear alignment disrupts flow; aligning elements consistently would enhance clarity.

3. **Suggest specific improvements you could make to the visualisation’s effectiveness:**  
   - Simplify color schemes with no more than five distinct hues.
   - Add clear labels/titles for sections.
   - Use white space effectively between groups of related information.


