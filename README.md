GraphLens is a graph-analytics project built on the MovieLens 25M dataset.  
It simulates three graph database paradigms — Neo4j (property graph),
TigerGraph (real-time analytics), and JanusGraph (big-data ETL) — using Python
and NetworkX, so no external DB credentials are required.

The pipeline includes:
- real-time style streaming ingestion from ratings.csv,
- data cleaning and preprocessing,
- exploratory data analysis with statistical summaries and plots,
- construction of three bipartite user–item graphs at different scales,
- 5 simple + 5 complex recommendation queries per graph
  (top items, 2-hop recommendations, item–item Jaccard, high-quality peers,
   trending items, similar users),
- and visualizations of graph structures and query results.
