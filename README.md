# Load Testing Landing Page with JMeter

<img src="Images/landing-page.png" height="200px" width="200px">

This repository contains the necessary files and the results of the load testing performed on the landing page of demoblaze website using JMeter.

## Load Test Result Summary

The load test was conducted on the landing page of the website using the following thread group configuration:

- Number of Threads (Users): 100
- Ramp-up Period: 60 seconds
- Loop Count: 5
- Duration: 300 seconds
- Startup Delay: 10 seconds

### Result Summary

The load test results for the "HTTP Request" sampler and the "TOTAL" are as follows:

| Label        | # Samples | Average | Min | Max  | Std. Dev. | Error % | Throughput | Received KB/sec | Sent KB/sec | Avg. Bytes |
| ------------ | --------- | ------- | --- | ---- | --------- | ------- | ---------- | --------------- | ----------- | ---------- |
| HTTP Request | 500       | 274     | 0   | 1498 | 140.44    | 0.00%   | 8.3/sec    | 161.26          | 0.94        | 19902.7    |
| TOTAL        | 500       | 274     | 0   | 1498 | 140.44    | 0.00%   | 8.3/sec    | 161.26          | 0.94        | 19902.7    |

### Analysis

- The load test was performed with 100 concurrent users (threads) emulating real-world traffic on the landing page.

- The average response time for all the requests was 274 milliseconds, with a minimum of 0 milliseconds and a maximum of 1498 milliseconds. The standard deviation of response times was 140.44 milliseconds.

- The load test ran for a duration of 300 seconds, with a ramp-up period of 60 seconds, and each user performed 5 iterations of the test scenario.

- The error percentage was 0.00%, indicating that all requests were successful during the load test.

- The throughput was measured at 8.3 requests per second, indicating the system's capacity to handle incoming requests.

- The received and sent data rates were measured at 161.26 KB/sec and 0.94 KB/sec, respectively.

- The average data size (payload) of each response was 19902.7 bytes.

### Conclusion

The load test results indicate that the landing page of this website performed well under the simulated load of 100 concurrent users. The average response time of 274 milliseconds suggests that the server responds promptly to user requests.

The error percentage of 0.00% indicates that no errors or failures were encountered during the load test, demonstrating the landing page's stability and reliability.

With a throughput of 8.3 requests per second, the website showcased its capability to handle incoming traffic efficiently.

Overall, the load test results are positive, and the landing page appears to be adequately optimized to handle the expected load.
