# Lab: Create System Monitoring with Grafana and AWS Cloud Watch


In this lab, we will use Grafana to monitor your resources on AWS. `Grafana` is open source visualization and analytics software. It allows you to pull up metrics that make sense of the massive amount of data & to monitor our apps, beside of capability to query, visualize, alert on, and explore your metrics no matter where they are stored.

## Introduction to Grafana 


- Grafana is able to connect with nearly every possible data source, such as Graphite, Prometheus, Influx DB, Elastic Search, MySql, PostgreSQL, etc. It helps us track the user behaviour, application behaviour,frequency of errors popping up in production or a pre-prod environment, type of erros popping up & the contextual scenarios by providing relavtive data.Besides the core open source solution there are other two services offerd by the Grafana team for bussinees known as the Grafana Cloud & the Enterprise.

## Grafana Features

Grafana has some features as following:

-   Visualize: Fast and flexible visualizations with a multitude of options allow you to visualize your data any way you want.
  
-   Dynamic Dashboards: Create dynamic & reusable dashboards with template variables that appear as dropdowns at the top of the dashboard.
   
-   Explore Metrics: Explore your data through ad-hoc queries and dynamic drilldown. Split view and compare different time ranges, queries and data sources side by side.
   
-   Explore Logs: Experience the magic of switching from metrics to logs with preserved label filters. Quickly search through all your logs or streaming them live. Works best with our Loki data source but support for more are coming very soon.
  
-   Alerting: Visually define alert rules for your most important metrics. Grafana will continuously evaluate and send notifications to systems like Slack, PagerDuty, VictorOps, OpsGenie.
  
-   Mixed Data Sources: Mix different data sources in the same graph! You can specify a data source on a per-query basis. This works for even custom datasources.
  
-   Annotations: Annotate graphs with rich events from different data sources. Hover over events shows you the full event metadata and tags.
Ad-hoc Filters: Ad-hoc filters allow you to create new key/value filters on the fly, which are automatically applied to all queries that use that data source