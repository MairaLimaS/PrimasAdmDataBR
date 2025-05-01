
# This document provides methodological guidance for the inspection and validation of Brazilian administrative data.

## 1. Understanding Data Validation

- **Definition**: Data validation is an activity that checks whether a combination of values is a member of a set of acceptable combinations. This set may consist of possible values for a single field or valid combinations for a record, column, or a larger dataset.    
- **Objective**: The main objective of data validation is to ensure a certain level of quality in the final data. Validation seeks to achieve a minimum level of data consistency, resulting in "plausible" data. In the context of Administrative Data Curation, data inspection is an essential process carried out using statistical techniques and standardized procedures to verify the structural and documentary compliance of received datasets.
- **Validation vs. Editing**: It is important to distinguish data validation from data editing. Validation detects potential errors, indicating whether an error might be present, while editing involves the actual correction of the data.    
- **Relationship with Quality**: Data validation focuses on quality dimensions related to the "structure of data," namely accuracy, comparability, and consistency. It does not directly address process-related quality aspects. Additionally, it addresses the collection and comparative-based analysis of schema-versioning for each database: 
	- **Historicity**: Evaluating an approach based on information historical presence notation to track changing properties on the databases throughout the time.
	- **Maturity Assessment at the Domain-Steward Level**: Based on the domain-specificity of each administrative data model, considering information utility and reliability. It evaluates factors ranging from the social, political, and regulatory context of data collection to technical documentation and the potential for open data. 
    
## 2. How to Perform Data Validation: Levels and Rules

Data validation is performed by applying validation rules at different levels of validation.

- **A. Technical Integrity of the File**: Consistency with expected IT structural requirements, such as data corruptions.  
- **B. Logical and Statistical Consistency of the Data**: Divided into subcategories that involve increasing levels of information:

  **Level 0**: Ensures compliance with expected structural requirements, such as file format, delimiters, number of columns, and data formats. **Level 1**: Consistency within the dataset (values within expected limits, consistency between columns, valid dictionary codes, consistency with data sender documentation, plausibility based on prior information, micro and macro consistency of variables). **Level 2**: Consistency with other data within the same administrative information system, based on the same data source (revision detection, comparison with previous versions).

- **B1. Historicity**: Subcategories that track the presence of the same set of variables within the same data information system over time during updates.
  **Level 3**: The presence and consistency of a variable across different data updates (plausibility or mirror checks between variables from different time periods).

- **B2. Information domain presence**: Subcategories that track the presence of the same set of variables across different data information systems.
  **Level 4**: Consistency of a variable across different data information systems within the same or different data providers (plausibility or consistency checks across various data information systems).
  
- **Products**:         
    - **Data description**: The purpose is to collect, organize, classify, and represent data based on the main characteristics of the dataset. Its main goal is to convey accurate information so that the researcher can extract the maximum knowledge from the data and avoid incorrect inferences later.       
    - **Data Report**:  Document that systematizes the process and results of the initial analysis of one or more datasets. The main objective of this report is to provide a clear understanding of the structure, content, quality, and potential issues within the data, serving as a foundation for subsequent steps in data curation, analysis, and utilization.
        
## 3. Validation Rules

The data validation rules applied encompass various checks to ensure data quality and reliability. The main validation categories include:  

- **Format and Structure Verification**: The initial inspection involves checking the initial data structure and the database format (CSV, DBF, XLSX, Parquet, DTA). The dataset size and the number of variables are also analyzed.
- **Integrity**: The verification of potential database corruption is essential to ensure data integrity.  
- **Structural Quality**: This category verifies data compliance with metadata and documentation standards. It involves column schema verification and compliance with the data dictionary, ensuring that the variables in the dataset match the documentation. Additionally, it checks for the field separator identification in files and data encoding (such as UTF-8 or Latin-1); The absence of record displacement is also verified. The inspection can also involve viewing the random rows of the dataset and identifying values per variable.
- **Data Schema**:  Infer or extract the underlying data model/pattern to guide deeper inspections.
- **Data Type Validation**: The classification of variable data types (text, numeric, date, categorical, boolean, array) and the identification of potential misclassifications are performed.  
- **Missing Data and Completeness Analysis**: A crucial part of validation involves assessing the absence of data per variable. This includes counting missing values (counts and missings per variable) and calculating the percentage of variable completeness.  
- **Consistency with Previous Versions**: For databases with versions or previous years, the presence of new variables, record counts and the compatibility of new versions with previous ones is verified. 
- **Minimal Data Quality Assurance**: Refers to the establishment of clear criteria that define the minimum acceptable quality standards for a dataset to be considered usable. It involves setting threshold values and essential conditions—such as completeness, accuracy, consistency, and timeliness—that data must meet to support reliable analysis and informed decision-making.
- **Provenance Check**: Retrieves the history and legacy of the dataset within the catalog. Methodologically, it includes information from both the Data Inventory and the Data Documentation.

- ## 4. Data Validation as a Process

Data validation is performed at different stages of the data curation process:

- **Design Phase**: Defines the technical and statistical processing methodology, including specifying validation routines and creating a validation plan.
- **Collection Phase**: Basic validation of the structure and integrity of received information (file formats, expected fields) may occur, but not content validation.  
- **Processing Phase**: Dedicated to data validation to identify potential issues, errors, and discrepancies by applying predefined edit rules. Data may be flagged for manual or automatic inspection.    
- **Analysis Phase**: In this phase, it  validate the quality of the produced outputs by comparing statistics with previous cycles, other relevant data (same information system, internal or external*), investigating inconsistencies, and performing macro-editing.    

## 5. Lifecycle of the Data Validation Process: A Maturity Analysis

To improve performance and optimize data validation, considering its lifecycle is beneficial:

- **Design**: Study datasets, variables, and their relationships; assess quality requirements; determine a satisfactory set of validation rules.
    
- **Implementation**: Formalize validation rules in a common syntax; define metrics; test and evaluate results; refine rules.
    
- **Execution**: Verify data against validation rules; measure results.
    
- **Review**: Analyze stakeholder feedback; assess execution results; identify and prioritize issues for design improvements.
    
This cycle is iterative, with review results being used to refine validation rules and processes.

## 6. Metrics for Data Validation

Indicators will provide quantitative information that helps design, maintain, and monitor a data validation procedure. Metrics can refer to a single rule or the entire validation procedure.

## 7. Evaluation of Validation Rules

Evaluating validation rules involves analyzing their properties and performance when applied to data.

- **Completeness**: The extent to which prior knowledge about a dataset is expressed in validation rules. It can be assessed through peer review or formal methods that verify the coverage of variables by the rules.
    
- **Redundancy**: The presence of rules that always produce the same result as other rules when satisfied. Removing redundancies can simplify the rule set but may reduce readability.
    
- **Coherence**: Whether a set of rules can be simultaneously satisfied. 
    
- **Complexity**: Can refer to the variety of information needed to evaluate a rule, computational complexity, or the cohesion of a rule set (interconnection through shared variables). A graphical representation of dependencies between rules and variables can provide insights into cohesion.
    

## Conclusion
Applying a data validation methodology requires a systematic and iterative approach, involving continuous evaluation and refinement of rules. It is important to clearly define validation objectives, understand the different levels and types of rules, and integrate validation into the data curation, analysis, engineering and statistical production processes.

