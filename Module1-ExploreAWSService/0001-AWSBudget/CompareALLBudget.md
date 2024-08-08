# AWS Budgets Comparison

## Overview

In this lab, we will explore how AWS Budgets can assist you in cost management within your AWS account. AWS Budgets is a service designed to enable you to establish one-time or recurring budgets. These budgets will send you alerts whenever costs exceed your predetermined budgeted cost or usage amount.

You can create several types of budgets:

- Cost Budget
- Usage Budget
- Reserved Instance (RI) Budget
- Savings Plans Budget

## Budget Types Comparison

### Cost Budget

- **Purpose**: To monitor and control spending.
- **Key Characteristics**:
    -   Monitors the total cost of the entire account or specific services.
    -   Does not require a long-term usage commitment.
    -   Alerts are based on current spending or projected costs exceeding the set budget threshold.
- **Alerts**: Provides alerts when the current or projected spending surpasses the cost threshold set within the budget.
- **Example**: Set a monthly budget of $500. Receive alerts at 50%, 80%, and 100% of the budget.

### Usage Budget

- **Purpose**: To monitor and control resource usage.
- **Alerts**: Sends alerts when the current or projected usage of a chosen service or group of services exceeds the usage budget threshold.
- **Example**: Budget the usage of running hours for EC2 compute services. Set a budget of 1000 hours per month. Receive alerts at 50%, 80%, and 100% of the budget.

### Reserved Instance (RI) Budget

- **Purpose**: To monitor and control the usage or coverage of committed usage, known as a reserved instance.
- **Alerts**: Generates alerts based on your usage or coverage of committed usage.
- **Example**: Monitor the usage of reserved instances. Receive alerts when usage falls below the committed usage level.
- **Note**: A Reserved Instance is a discounted EC2 offering when you commit to a one-year or three-year term.

### Savings Plans Budget

- **Purpose**: To monitor and control the usage or coverage of services specified within savings plans.
- **Key Characteristics**: 
    - Provide cost savings based on long-term commitment (one year or three years) for specific services.
    - Discounts apply to a board range of services, not just EC2, but also Fargate and Lambda.
    - Offer more flexibility than Reversed Instances, allowing changes in the type of service and region without losing savings benefits.
- **Alerts**: Receives alerts based on usage or coverage of services specified within savings plans.
- **Example**: Monitor the usage of savings plans. Receive alerts when usage or coverage falls below the committed level.

