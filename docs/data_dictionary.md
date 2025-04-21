# Data Dictionary
## lane_data.csv
- LaneID: Unique identifier (e.g., Lane-0001)
- Origin: City, State (e.g., Chicago, IL)
- Destination: City, State
- Distance: Miles
- Freight Type: Dry Van
- Historical Cost: Baseline cost (USD)

## bid_*.csv (in carrier_bids/)
- LaneID: Matches lane_data.csv
- Origin, Destination, Distance, Freight Type: Same as lane_data.csv
- CarrierID: Unique carrier ID (e.g., B001, A001)
- CarrierType: Broker or Asset
- BidPrice: Flat rate bid (USD)