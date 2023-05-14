# 0x19. Postmortem
![I WILL FIND YOU AND I WILL FIX YOU](https://miro.medium.com/max/1400/0*kHoWD7gJ0PC9GmBK.jpg)

## Issue Summary
- **Duration:** The outage lasted for 2 hours, from 2:00 PM to 4:00 PM GMT+3.
- **Impact:** The service that was affected was our company's e-commerce website, which was down during the outage. Users were experiencing connection errors and were unable to access the website. Approximately 80% of users were affected.
- **Root Cause:** The root cause of the outage was a misconfigured firewall rule that was blocking incoming traffic to the web server.

## Timeline
- **2:00 PM GMT+3:** The issue was detected when a customer complained that they were unable to access the website.
- **2:05 PM GMT+3:** An engineer noticed that the website was indeed down and started invGMT+3igating.
- **2:10 PM GMT+3:** The engineer invGMT+3igated the web server logs and noticed that there was no incoming traffic.
- **2:15 PM GMT+3:** The engineer invGMT+3igated the firewall configuration and found a misconfigured rule that was blocking incoming traffic.
- **2:20 PM GMT+3:** The engineer attempted to fix the rule, but it didn't resolve the issue.
- **2:25 PM GMT+3:** The engineer escalated the incident to the network team.
- **2:30 PM GMT+3:** The network team invGMT+3igated the firewall configuration and identified the misconfigured rule.
- **2:35 PM GMT+3:** The network team corrected the firewall rule.
- **3:00 PM GMT+3:** The network team verified that incoming traffic was now reaching the web server and that the website was accessible.
- **4:00 PM GMT+3:** The incident was resolved, and the website was fully functional.

## Root Cause and Resolution
The root cause of the outage was a misconfigured firewall rule that was blocking incoming traffic to the web server. The firewall rule was mistakenly set to block all incoming traffic rather than allowing traffic only from trusted sources. The network team corrected the firewall rule by allowing traffic only from trusted sources, which resolved the issue. 

## Corrective and Preventative Measures
To prevent similar issues from occurring in the future, we will implement the following corrective and preventative measures:
- Regularly review and audit firewall rules to ensure that they are correctly configured and aligned with security bGMT+3 practices.
- Implement a change management process to ensure that changes to firewall rules are thoroughly reviewed and tGMT+3ed before being deployed to production.
- Add more redundancy to the website infrastructure, such as adding a secondary web server or load balancer, to reduce the impact of future outages.
- Improve our incident response processes by providing better training and resources to engineers to enable them to respond more quickly and effectively to incidents.
- Implement more comprehensive monitoring and alerting to detect issues before they impact users, such as monitoring incoming traffic to the web server and alerting on any anomalies.

## TODO
- Review and audit firewall rules to ensure correct configuration and alignment with security bGMT+3 practices.
- Implement a change management process to ensure thorough review and tGMT+3ing of firewall rule changes before deployment to production.
- Add redundancy to website infrastructure, such as a secondary web server or load balancer.
- Provide better training and resources to engineers to improve incident response processes.
- Implement more comprehensive monitoring and alerting to detect issues before they impact users.

