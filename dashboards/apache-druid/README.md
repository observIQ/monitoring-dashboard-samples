### Dashboards for Apache Druid

#### Notes

- This dashboard is based on Google's [Ops Agent](https://cloud.google.com/stackdriver/docs/solutions/agents/ops-agent).
- The full list of metrics supported by the Ops Agent can be found [here](https://cloud.google.com/stackdriver/docs/solutions/agents/ops-agent/third-party/druid#monitored-metrics).

|Apache Druid Overview|
|:------------------|
|Filename: [apache-druid-gce-overview.json](apache-druid-gce-overview.json)|
|This dashboard has charts displaying `Query Count`, `Successful Query Count`, `Failed Query Count`, `Timed-out Query Count`, `Interrupted Query Count`, `SQL Query Count`, `Average SQL Query Response Bytes`, and `Average SQL Query Response Time` from Apache Druid instances.|