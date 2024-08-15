# Cloud Watch

Amazon CloudWatch is an monitor and management service that provides action-oriented data and information for AWS application and infrastructure resources, hybrid and on-premises applications. You can collect and access all performance and operational data in the form of logs and metrics in the same platform ,instead of monitoring in silos (servers, networks, or databases). CloudWatch allows you to monitor end-to-end(applications, infrastructure,services) and leverage alerts, logs ,and event data to take action automatically and reduce average processing time.


You can use CloudWatch Container Insights to monitor, troubleshoot, and alert the applications and microservices containerd in your containers.
CloudWatch collects, aggregates, and summarizes compute usage (such as CPU,memory, disk,and network data) as well as diagnostic information to help Devops engineers Isolate and resolve problems quickly.

## 🚀 Metrics Collection

-  **AWS Service Metrics**: CloudWatch automatically collects and tracks metrics for various AWS services like EC2, RDS, Lambda, DynamoDB, and more. For example, you can monitor CPU utilization, memory usage, and network traffic for your EC2 instances.

- **Custom Metrics**: You can publish custom metrics from your applications or on-premises servers. These metrics can be pushed using AWS SDK, CLI, or Cloud Watch Agent.


## <img src ="./Image/image.png" width="45" height="45"> Alarms

- Cloud Watch Alarms allow you to set thresholds on your metrics. When these thresholds are breached, CloudWatch can trigger actions such as sending notifications through Amazon SNS, executing an Auto Scailing policy, or invoking an AWS Lambda function.
  
- Types of Alarms:
    - **Static Alarms**: Triggered when a metric reaches a specified threshold.
    - **Anomaly Detection Alarms**: Uses machine learning to detect anomalies in your metrics and triggers alarms based on deviations from the normal range.



##  <img src ="./Image/image-1.png" width="45" height="45"> Logs

- **Amazon Cloud Watch Logs**: You can collect, monitor, and store log files from your applications, systems, and AWS services. Logs can be ingested from various sources such as EC2 instances, Lambda functions, VPC Flow Logs, and Route 53 DNS queries.

- **Log Groups & Log Streams**: Logs are organized into log groups (containers for logs), and within each group, logs are divided into log streams (sequence of log events).
  
## 📚 Events 

- **Amazon CloudWatch Events**(also known as Amazon EventBridge): Allows you to monitor events from AWS services and route them to one or more target destinations like Lambda, SQS, or SNS.
  
- **Event Patterns**: You can define patterns to match specific events and trigger actions in response. 


##  <img src ="./Image/image-2.png" width="45" height="45"> Dashboards

- **CloudWatch Dashboards** let you create customized views of the kye metrics and logs taht matter most to your application. You can combine multiple metrics, create visualizations, and set up real-tome monitoring for operational visibility.
  
- **Dashboards** can include widgets for metrics, alarms, logs and even custom text of links.
##  <img src ="./Image/image-3.png" width="45" height="45"> Insights

- **CloudWatch Logs Insights**: A query tool that enables you to search and analyze log data. It supports structured queries, allowing you to extract meaningful information from large volumes of log data.

- **CloudWatch Contributor Insights**: Helps you identify the top contributors impacting your system’s performance. It provides a visual representation of who or what is causing the most impact.