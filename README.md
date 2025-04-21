# Bid Analysis Project

## Summary
You are tasked with analyzing a bid for your company, from the point of view of the shipper. Using the provided data, figure out how to ingest the data, process it, and deliver the results.

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
        - Single page report, don’t use the default styling. Recommend looking at the “Storytelling with Data” book. Bonus: Look into PBI Theme Generator that gives you a theme JSON file.

## Bonus Objectives
1. In either analysis (Python might be easier here), implement a rule that only allows 1 Broker to win at any specific origin city to prevent multiple brokers from calling on the same trucks that artificially inflates the cost.
2. In either analysis, implement a rule that favors incumbents by 5% to mitigate carrier churn. Hint: “shadow” pricing (ask me and take notes).
