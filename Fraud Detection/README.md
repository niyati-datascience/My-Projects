
# Client-Seller Transaction Analysis and Fraud Detection

## Overview
This assignment involves analyzing transactions between clients and sellers, as well as detecting potentially fraudulent behavior using graph algorithms in Neo4j. The data includes client information, seller details, and transactional data, which is used to create relationships in a graph database. We use Cypher queries and Neo4j Graph Data Science (GDS) algorithms for various tasks such as transaction analysis, community detection, and fraud detection.

### Sections
1. **Part 1**: Setup and Data Loading
2. **Part 2**: Transaction Analysis and Relationship Queries
3. **Part 3**: Graph Algorithms for Fraud Detection

## Part 1: Setup and Data Loading
In this part, constraints, indexes, and CSV data are loaded into the Neo4j database:

### Constraints:
- Ensured that `Client`, `Seller`, and `Transaction` nodes have unique IDs.

### Indexes:
- Optimized query performance with custom indexes for `Client` names, `Seller` names, and transaction attributes like `time` and `amount`.

### Data Loading:
- Loaded data from CSV files (`clients.csv`, `stores.csv`, `purchase.csv`, `xfer.csv`) into the database.
- Established relationships between `Client`, `Seller`, `Phone`, `Email`, and `TFN`.
- Created `Purchase` and `Transfer` transactions, linking `Clients` to `Sellers` or other `Clients`.

---

## Part 2: Transaction and Relationship Queries
### Problem 1: Transaction Analysis
- **Datetime Conversion**: Converted transaction `time` to a readable `transactionDatetime` field.
- **Query 1**: Retrieved the 10 most recent transactions.
- **Query 2**: Identified the client who spent the most between a specific time range.

### Problem 2: Balance and Spending Analysis
- Calculated the total incoming and outgoing transactions for clients and identified those with a negative balance.
- Returned the top 5 clients with the largest negative balance.

### Problem 3: Seller Interaction and Transfer Analysis
- Calculated the total amount spent by clients on purchases from a specific seller (`Woods`).
- Analyzed the percentage of transactions that involved transferring money from clients to others.
  
### Problem 4: Creating Transaction Sequences
- **NEXT Relationship**: Created relationships between consecutive transactions.
- **FIRST_TX and LAST_TX**: Created relationships for the first and last transactions.
- Visualized transaction paths for a client (`Sebastian Stein`).

---

## Part 3: Graph Algorithms for Fraud Detection

### Part A: Graph Projection and Community Detection
1. **i) Client Shared Info Projection**:
   - Used `gds.graph.project` to create a projection of clients sharing information through email, phone, and TFN.
   - Applied `gds.wcc.stream` to detect connected components (clusters) of clients.

2. **ii) Identifying Larger Groups**:
   - Found groups with more than 5 members and returned the group details (name and size).

3. **iii) Assigning Group IDs**:
   - Assigned a `groupId` to each client based on their connected component and visualized relationships excluding specific transaction types.

### Part B: Fraud Detection
1. **i) Identifying Fraudulent Transactions**:
   - Analyzed transactions involving clients from large fraud groups that interacted with clients outside their groups.

2. **ii) Projecting Subgraph for Fraud Movement**:
   - Projected a subgraph of fraud group members and their interactions with clients outside their groups.
   - Used the Louvain community detection algorithm to find tightly connected subgroups within the projected subgraph.

3. **iii) PageRank for Key Players**:
   - Applied the PageRank algorithm to identify key players in the fraud group by ranking clients based on their network influence.

4. **iv) Visualization**:
   - Visualized the largest fraud group using Neo4j Bloom, with virtual relationships (`PERFORMED_WITH`) indicating the number of transactions between clients.

---

## Requirements
- **Neo4j**: Neo4j 4.x or later is required to run the queries and graph algorithms.
- **Neo4j Graph Data Science (GDS)**: Required for community detection, Louvain, and PageRank algorithms.
- **APOC**: Neo4j APOC library for advanced graph algorithms and virtual relationships.

---

## Conclusion
This assignment focuses on analyzing client and seller interactions using a graph-based approach, optimizing the queries with indexes and constraints, and detecting fraudulent activity using graph algorithms like Louvain and PageRank. The resulting graph provides insights into transaction patterns, client behavior, and potentially suspicious activities. 

