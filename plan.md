# GraphLens Project Plan

## Goal
Compare graph-based recommendation analytics across three graph database paradigms
(Neo4j, TigerGraph, JanusGraph) using the MovieLens 25M dataset.

## Steps

1. **Real-time / Streaming Simulation**
   - Stream batches from `ratings.csv` and compute online mean rating.

2. **Ingestion & Preprocessing**
   - Clean ratings and movies.
   - Parse timestamps, extract year from titles, handle missing genres.

3. **Exploratory Data Analysis (EDA)**
   - Rating distribution.
   - Top genres.
   - Ratings per month.
   - User/item degree distributions (log-log).
   - Item–item Jaccard heatmap for top-20 items.

4. **Graph Construction (Simulated DBs)**
   - Build three NetworkX graphs:
     - `Neo4j` (smaller sample),
     - `TigerGraph` (medium),
     - `JanusGraph` (largest).
   - Bipartite user–item structure; store ratings & timestamps on edges.

5. **Queries (per graph)**
   - 5 simple queries:
     - Count users / items / ratings.
     - Top items by number of ratings.
     - Top items by average rating with minimum support.
   - 5 complex queries:
     - 2-hop recommendations for user 1.
     - Item–item Jaccard similarity (top pairs on popular items).
     - High-quality peers (users who rate the same items ≥ 4★).
     - Trending items in last 365 days.
     - Similar users by co-rated overlap.

6. **Visualizations**
   - Bar charts for top items and peers.
   - Three small graph structure plots (one per DB).
   - Comparison of entity/edge counts across the three graphs.

7. **Discussion**
   - Tradeoffs between sample size, query cost, and memory.
   - How each simulated graph mirrors real Neo4j/TigerGraph/JanusGraph workloads.
