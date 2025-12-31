# Distributed Load Testing – Sample Result

## Test Overview
- Test Type: Distributed Load Test
- Tool Used: k6
- Environment: AWS EC2
- Load Generation: Distributed across multiple EC2 instances

---

## Test Configuration
- Number of EC2 instances: 3
- Virtual Users per EC2: 50
- Total Distributed Users: 150
- Test Duration: 1 minute
- Target Application: https://test.k6.io

---

## Test Results Summary
- Total Requests Sent: 9,000
- Successful Requests: 9,000
- Failed Requests: 0
- Error Rate: 0%
- Average Response Time: 180 ms
- 95th Percentile Response Time (p95): 300 ms
- Throughput: 150 requests/second

---

## Resource Utilization (Observed in CloudWatch)
- Average CPU Utilization: 55%
- Peak CPU Utilization: 72%
- Network Traffic: Stable during test execution
- No instance crashes observed

---

## Observations
- Application handled distributed load without errors
- Response times remained within acceptable limits
- System scaled well under concurrent distributed traffic
- No performance degradation was observed

---

## Conclusion
The Distributed Load Test was successful. The application demonstrated stability and scalability under distributed user load generated from multiple AWS EC2 instances.

