# Postmortem Report

## Web Application Service Degradation due to Load Balancer Misconfiguration


### Incident report for [Web Application Service Degradation due to Load Balancer Misconfiguration](https://github.com/yassminee00/alx-system_engineering-devops/tree/master/0x12-web_stack_debugging_2)

#### Issue Summary

- **Duration:** - February 12, 2024, 5:00 AM - February 13, 2024, 6:00 PM (UTC)
- **Impact:** - The web application experienced intermittent downtime, resulting in a slowdown and occasional unavailability. Approximately 30% of users were affected by degraded performance and connectivity issues.
- **Root Cause:** - A misconfiguration in the load balancer settings led to uneven distribution of traffic, causing server overload and subsequent service degradation.

#### Timeline

- **February 12, 2024, 5:00 AM (UTC):** - The issue was detected when monitoring alerts indicated a spike in server response times.
- **Actions Taken:** - Engineers investigated backend services, database performance, and network connectivity, assuming a potential server overload due to increased traffic.
- **Misleading Investigation Paths:** - Initially, engineers suspected a database bottleneck and conducted thorough database queries optimization. Additionally, they inspected server logs for any signs of malicious activity or abnormal requests.
- **Escalation:** - After initial investigation, the incident was escalated to the DevOps team to analyze load balancer configurations.
- **February 12, 2024, 11:00 PM (UTC):** - The root cause was identified as a misconfigured load balancer, causing unequal distribution of traffic to backend servers.
- **February 13, 2024, 6:00 PM (UTC):** - The incident was resolved by reconfiguring the load balancer to evenly distribute incoming traffic across all backend servers.


#### Root Cause and Resolution

- **Root Cause Explanation:** - The misconfiguration in the load balancer settings led to an imbalance in traffic distribution. Some backend servers were overwhelmed with requests, while others remained underutilized.
- **Resolution:** - Engineers adjusted the load balancer settings to evenly distribute incoming traffic among all backend servers. Additionally, they implemented automated checks to monitor load balancer configurations for any discrepancies.

#### Corrective and Preventive Measures

- **Improvements/Fixes:**
- Implement regular audits of load balancer configurations to prevent misconfigurations.
- Enhance monitoring systems to promptly detect and alert on traffic imbalances or unusual patterns.
- Conduct regular load testing to ensure the infrastructure can handle peak traffic loads without degradation.

- **Tasks to Address the Issue:**
- Update load balancer configuration scripts to enforce consistent settings across all environments.
- Document load balancer configuration best practices and share them with the engineering team to prevent future misconfigurations.
- Schedule regular reviews of critical infrastructure components to identify and address potential vulnerabilities or misconfigurations proactively.

By addressing the misconfigured load balancer and implementing preventative measures, we aim to minimize the likelihood of similar incidents occurring in the future. We appreciate the patience and understanding of our users during this period of service disruption.
