# Options

## Owned node ( High effort )
- Create a copy of the blockchain on own/cloud hardware
- Analyse directly as the blockchain is updated
- Advantages:
  - Full control over operations
  - Live data
  - Access to entire history since the beginning of the blockchain
- Disadvantages:
  - High effort in writing code for all the data engineering that happens
    - Inflow of large amounts of data
    - Persistance
    - Logging
    - Need to pay per blockchain
  - Maintenance effort in keeping it running
  - Parsing entire blockchain with custom code
- Hardware:
  - 20TB of disk
  - 32GB RAM
  - 4 core proc
- Cost: Approx $150 per month
- Example providers: Any cloud provider should be okay, or buy a server

## Node Provider (Medium Effort)
- Use a node managed by a provider
- Analyse directly as blockchain is updated
- Advantages:
  - No need to manage the infra and data engineering yourself
  - Live data
  - Access to entire history since the entire node is still available
- Disadvantages:
  - Parsing streamed events or logs with your own code
  - Heavy historical scans may apply asymmetrical costs
  - Need to pay per blockchain
- Hardware: Only whatever is needed for analysis: personal laptop should be okay, if not, cloud
- Cost: Free tier + pay as you go
- Example providers: Alchemy, Infura, QuickNode

## Indexer API
- Subscribe to feeds from a data provider
- Query the API and analyse data that is returned
- Advantages:
  - Fastest/easiest way to look at price trends
  - Low Cost
  - Low effort (write SQL or API wrappers to get data)
  - Single provider provides access to many blockchains
- Disadvantages
  - No control over speed/latency
- Hardware: Only whatever is needed for analysis: personal laptop should be okay, if not, cloud
- Cost: Free + Pay as you go
- Example providers: Dune, Covalent, Flipside

# Notes
- Whale Alert is good for large trades only as the name suggests, cannot stream events of small transactions
  - Free tier has 10 requests per minute for early experiments
