I have been spending most of my careers on system and framework related works:

1. Build and scale systems. Often, the critical part is to identify the right bottleneck and address it. Selected examples includes:

   (a) Scale up graph processing system in multicore [1] and distributed MapReduce-like envirinoment [2]. We found communication cost is often the bottleneck and proposed different methods to overcome it from shceduling and algorithmic perspective.

   (b) Scale up Distributed Analystics SQL Systems. Traditional in-memory RPC shuffle often becomes the bottleneck for scaling up such systems. Disaggregated shuffle is the proven approach to scale it up. 

2. Develop framework with elegant and useful abstractions.

   (a) Introduce SQL-native lambda functions to flexibly support nested data processing and a common family of aggregation functions. With SQL-builtin language extension, data engineers can usually express new analytic requirement without leaving SQL. 

   (b) Unify feature engineering and model authoring. Traditional ML has relatively fixed model archtecture and spent most of the effort in feature engineering; the new emerging deep learning mostly focus on model archtecture instead and has simple or no feature engineering work. However, we found there are critical use cases requires co-optimizations in both feature engineering and model authoring. We developed TorchArrow to leverage `nn.Module` as the unified programming interface and Arrow layout for standard data exchange format. This work also requires spent significant system side work to make all the components orchestration in the right way.




[1] Fast Iterative Graph Computation with Block Updates. Proceedings of the VLDB Endowment 6(14) 2014-2025.

[2] Joins and aggregations on massive graphs using large-scale graph processing. US Patent 10,191,948 B2 \hfill  Jan. 2019

