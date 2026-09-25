# Multi-Horizon-Demand-Risk-Forecasting-with-a-Temporal-Fusion-Transformer-TFT-
Uses Google's Temporal Fusion Transformer architecture to forecast a time-dependent quantity (e.g., electricity demand, retail sales, or rainfall/flood-risk levels) multiple steps into the future, meanwhile it  explaining which inputs mattered most for each prediction — something plain LSTMs/transformers don't give you.
Build the road-network graph from OSM (nodes = intersections, edges = road segments with distance/speed-limit attributes)

Collect or simulate a time-series of congestion/speed values per edge (live API pulls, historical logs, or a physically-reasonable simulation if live data is limited)
Implement a GCN/GAT layer to capture spatial dependencies between adjacent roads + an LSTM/GRU or temporal attention layer to capture time dependencies
Set up a lightweight streaming layer (Kafka or even a simpler polling scheduler via Airflow) to simulate reel-time data arrival and trigger periodic re-inference
Evaluate against a naive baseline (historical average, ARIMA) using MAE/RMSE on held-out time windows

Visualization live predicted congestion on an interactive Folium/Streamlit map : colour-coded by predicted congestion level, similar to your flood risk dashboard style
