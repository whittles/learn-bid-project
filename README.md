# Bid Analysis Project

## Summary
You are tasked with analyzing a bid for your company (**Bob's Widgets**), from the point of view of the shipper. Using the provided data, figure out how to ingest the data, process it, and deliver the results.

## Learning Goals
- **Develop proficiency in data ingestion and processing:** Learn to read, manipulate, and combine multiple data files (e.g., lane data and carrier bid CSVs) using Python and pandas, ensuring data integrity and consistency for analysis.
- **Master data modeling and relationships:** Build a functional data model in PowerBI that connects lane and bid tables, understanding how to structure relationships for effective querying and reporting.
- **Enhance analytical skills through bid evaluation:** Apply quantitative methods to compare carrier bids against historical baselines, calculate cost impacts, and determine optimal lane awards based on price and business rules.
- **Gain expertise in automated reporting:** Create Python scripts to generate structured Excel outputs with multiple tabs (lane awards and bidder summaries), automating data summarization and formatting processes.
- **Improve data visualization techniques:** Design an insightful PowerBI report with custom visuals, slicers, and a map, adhering to data storytelling principles to communicate findings effectively to stakeholders.
- **Understand logistics and bid analysis concepts:** Explore key freight transportation concepts, such as historical cost baselines, and the impact of business rules on bid awards.
- **Implement complex business logic:** Develop algorithms to enforce constraints, such as limiting broker awards per origin or applying incumbent pricing advantages, to optimize outcomes while meeting strategic goals.
- **Practice version control and collaboration:** Utilize Git for version control, including cloning repositories, creating branches, and pushing changes, to simulate professional software development workflows.
- **Cultivate problem-solving and critical thinking:** Tackle real-world logistics challenges by interpreting data, addressing bonus objectives (e.g., shadow pricing), and making data-driven decisions under constraints.
- **Apply professional communication standards:** Produce clear, well-documented deliverables (Python scripts, Excel files, and PowerBI reports) that meet business requirements and are suitable for stakeholder review.

## Instructions
1. Clone the main repository and create your own branch.
2. Do the work.
    - Use the provided file structure. 
        - Python work into the **src** folder.
        - PowerBI file in the **reports** folder.
3. Push progress and files to your branch on Git.
    - You don't need to wait until you have the final product. Push frequently as you make progress.

## Basic Requirements / Deliverables
- Python script that produces an output excel file showing:
    - The lane detail and the winning carrier. Each lane should only be represented in a single row.
    - Summary tab with just a summary of the bidders
        - Volume won by carrier
        - Spend by carrier
        - Impact vs historical baseline
    - **The Excel file with both tabs must be created as part of the python script, not copy/paste.**
- A PowerBI Report
    - Data Engineering (ask and take notes on file structure if need be)
        - Imports the lane data
        - Scrapes a data folder to retrieve the bids from the carriers
            - In the import process, the final step should return all bids as a single table (hint: concat)
        - Working data model that connects the Lane table to the Bids
    - Data Analysis
        - Summary of Bidders
            - Volume won by carrier
            - Spend by carrier
            - Impact vs historical baseline
            - Map
        - Two slicers that make sense given the data
        - Single page report, don’t use the default styling. Recommend looking at the “Storytelling with Data” book.
        - Logo provided in the **img** folder, include it on the report.
        - Theme JSON file provided in the **reports** folder.

## Bonus Objectives
### Difficulty: Moderate
1. In either analysis (Python might be easier here), implement a rule that only allows 1 Broker to win at any specific origin city to prevent multiple brokers from calling on the same trucks that artificially inflates the cost.
2. In either analysis, implement a rule that favors incumbents by 5% to mitigate carrier churn. Hint: “shadow” pricing (ask me and take notes).

### Difficulty: Hard
3. Implement the rules as separate scenarios from the main low-cost result.
    - Have a summary that compares the results of these scenarios.

