# Chicago Food Inspection Data Analysis

## Project Overview
This project analyzes restaurant and food establishment inspection data for the City of Chicago. The goal is to create an end-to-end data pipeline that ingests inspection data, transforms it into a structured data model, and generates insights through interactive BI dashboards. The project aims to support Chicago health officials in monitoring compliance, identifying high-risk establishments, and improving food safety across the city.

## Data Source
The dataset for this analysis is sourced from the *Chicago Open Data Portal, focusing on **Restaurant and Food Establishment Inspections* data from October 2016 to the present. The dataset includes inspection dates, scores, types and numbers of violations, and establishment details.

### Data Links
- [Chicago Open Data API](https://data.cityofchicago.org/resource/4ijn-s7e5.csv)


## Tools and Technologies

 ![Alteryx](https://img.shields.io/badge/Alteryx-0066CC?style=for-the-badge&logo=alteryx&logoColor=white)  
 ![SQL](https://img.shields.io/badge/SQL-4479A1?style=for-the-badge&logo=MySQL&logoColor=white)  
 ![Azure SQL Database](https://img.shields.io/badge/Azure_SQL-0089D6?style=for-the-badge&logo=Microsoft-Azure&logoColor=white)  
 ![ER/Studio](https://img.shields.io/badge/ER%2FStudio-0056D2?style=for-the-badge&logo=data-modeling&logoColor=white)  
 ![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=for-the-badge&logo=power-bi&logoColor=black)
 ![Tableau](https://img.shields.io/badge/Tableau-E97627?style=for-the-badge&logo=tableau&logoColor=white)  


## Project Phases and Deliverables

### Part 1: Data Extraction and Staging
- *Data Loading*: Extract data from the Chicago Open Data portal and load it into a staging area in Azure SQL.
  
  ![counts](https://github.com/RutujaMore1706/Chicago-Food-Inspection-Data-Analysis/blob/main/Data%20staging/Chicaago%20-%20Part3/Screenshots/No.Of%20Records.png)
  
  ![Facts Model Loading](https://github.com/RutujaMore1706/Chicago-Food-Inspection-Data-Analysis/blob/main/Data%20staging/Chicaago%20-%20Part3/Screenshots/Load_Chicago_Fact.png)

- *Data Profiling*: Perform data profiling to validate structure, data types, and completeness futhuremore staging data.

  ![Image](https://github.com/RutujaMore1706/Chicago-Food-Inspection-Data-Analysis/blob/main/Data%20staging/Chicaago%20-%20Part3/Screenshots/scd_chicago.png)

### Part 2: Dimensional Modeling
- *Identify Dimensions and Facts*: Establish core entities such as Restaurants, Inspections, and Violation.
- *Create Dimensional Model*: Design a star schema with a central fact table for inspection results and dimension tables for supporting details.
- *Database Schema Creation*: Implement the model in Azure SQL using DDL scripts.

### Phase 3: Data Integration and Transformation
- *ETL Workflow Development*: Design Alteryx workflows to transform and load data from staging tables into the dimensional model.
- 
   ![Image](https://github.com/RutujaMore1706/Chicago-Food-Inspection-Data-Analysis/blob/main/Data%20staging/Chicaago%20-%20Part3/Screenshots/scd_chicago.png)
  
- *Data Transformation*:
  - Generate surrogate keys for each dimension.
  - Standardize date formats, ensure referential integrity, and aggregate metrics as needed.
- *Load Integration Tables*: Populate fact and dimension tables with transformed data.

### Phase 4: Business Intelligence and Dashboarding

- *Power BI Dashboards*:
  - *Inspection Trends Over Time*: Visualize frequency of inspections and identify trends.
  - *Pass/Fail Analysis*: Overview of passing vs. failing scores.
  - *Top Violations*: Most common types of violations by establishment.
  - *Top and Bottom Establishments*: Analysis of most and least compliant establishments.
  - 
    ![Image](https://github.com/RutujaMore1706/Chicago-Food-Inspection-Data-Analysis/blob/main/Data%20Visualization/Screenshot%202024-11-08%20at%208.27.59%E2%80%AFAM.png)
    
    ![Image](https://github.com/RutujaMore1706/Chicago-Food-Inspection-Data-Analysis/blob/main/Data%20Visualization/Screenshot%202024-11-08%20at%208.28.07%E2%80%AFAM.png)

    ![Image](https://github.com/RutujaMore1706/Chicago-Food-Inspection-Data-Analysis/blob/main/Data%20Visualization/Screenshot%202024-11-08%20at%208.28.30%E2%80%AFAM.png)
    
    ![Image](https://github.com/RutujaMore1706/Chicago-Food-Inspection-Data-Analysis/blob/main/Data%20Visualization/Screenshot%202024-11-08%20at%208.28.22%E2%80%AFAM.png)

    
- *Tableau Dashboards*:
  - *Map of Inspection Results*: Geospatial representation of inspection outcomes.
  - *Performance by Neighborhood*: Neighborhood-wise breakdown of scores and violation severity.
  - Interactive filters for custom insights by score range, violation type, or establishment type.
 
  ![Image](https://raw.githubusercontent.com/RutujaMore1706/Chicago-Food-Inspection-Data-Analysis/main/Data%20Visualization/Screenshot%202024-11-07%20at%2011.01.33%E2%80%AFPM.png)

## Key Insights and Business Value
- *Inspection Score Trends*: Identified trends in inspection scores, highlighting potential areas for increased oversight.
- *Violation Patterns*: Most common violations and the establishments with repeated non-compliance.
- *High-risk Establishments*: Insights to prioritize follow-up inspections and focus on high-risk areas.
- *Geospatial Analysis*: Enabled visualization of inspection patterns by neighborhood, guiding resource allocation.
To format your "Tools and Technologies" section with badges, here’s an example of how it could look for each tool and technology:

---

## Conclusion
The Chicago Food Inspections Analysis Project transformed raw inspection data into a structured and accessible format, enabling city officials to make data-driven decisions to improve food safety standards. By integrating Azure SQL, Alteryx, Power BI, and Tableau, this project provided a full pipeline from data ingestion to BI visualization, showcasing a robust approach to public health monitoring and compliance enforcement.
