# Load Testing for Landing Page with JMeter

<p align="center"><a href="#" target="_blank"><img src="Images/landing-page.png" height="250px"></a></p>

Welcome to the load testing report for the landing page of the [demoblaze](https://www.demoblaze.com) website. This report presents the results of the load testing conducted using JMeter, a powerful open-source tool for performance testing.

## Purpose of Load Testing

Load testing is a crucial step in assessing the performance and scalability of a web application under various user loads. It helps identify potential bottlenecks and areas for improvement in the system. In this load testing scenario, the aim was to analyze how the landing page of the demoblaze website performs when subjected to a simulated real-world load of 100 concurrent users.

## Load Test Configuration

The load test was executed using the following thread group configuration:

- Number of Threads (Users): 100
- Ramp-up Period: 60 seconds
- Loop Count: 5
- Duration: 300 seconds
- Startup Delay: 10 seconds

In this configuration, 100 virtual users (threads) were created to emulate real users accessing the landing page. The ramp-up period allowed for a gradual increase in user load, ensuring a more realistic simulation of user traffic.

## Load Test Result Summary

The load test results were obtained for the "HTTP Request" sampler, which represents individual requests made to the landing page, and the "TOTAL" metric, which aggregates all the requests.

The summary of the load test results is as follows:

| Label        | # Samples | Average | Min | Max  | Std. Dev. | Error % | Throughput | Received KB/sec | Sent KB/sec | Avg. Bytes |
| ------------ | --------- | ------- | --- | ---- | --------- | ------- | ---------- | --------------- | ----------- | ---------- |
| HTTP Request | 500       | 274     | 0   | 1498 | 140.44    | 0.00%   | 8.3/sec    | 161.26          | 0.94        | 19902.7    |
| TOTAL        | 500       | 274     | 0   | 1498 | 140.44    | 0.00%   | 8.3/sec    | 161.26          | 0.94        | 19902.7    |

## Analysis of Load Test Results

Based on the load test results, the following key observations can be made:

- Response Time: The average response time for all requests was 274 milliseconds, with a minimum of 0 milliseconds and a maximum of 1498 milliseconds. The standard deviation of response times was 140.44 milliseconds. These response times indicate that the server is responding promptly to user requests, providing a smooth user experience.

- Duration and Load: The load test ran for a duration of 300 seconds, during which 100 concurrent users executed 5 iterations of the test scenario. This testing duration helped assess the website's performance under sustained load conditions.

- Error Percentage: The load test reported a 0.00% error rate, indicating that all requests made during the test were successful. This suggests that the landing page is stable and reliable, as no errors or failures were encountered.

- Throughput: The throughput was measured at 8.3 requests per second, which indicates the website's capacity to handle incoming requests efficiently. Higher throughput values imply better performance and scalability.

- Data Rates: The received data rate was measured at 161.26 KB/sec, while the sent data rate was 0.94 KB/sec. These values represent the rate at which data was received from the server and sent to the server, respectively.

- Average Data Size: The average data size (payload) of each response was 19902.7 bytes. This metric provides insights into the amount of data transmitted in each response.

## Conclusion

In conclusion, the load test results demonstrate that the landing page of the demoblaze website performed well under the simulated load of 100 concurrent users. The average response time of 274 milliseconds suggests that the server responded promptly to user requests, contributing to a satisfactory user experience.

The 0.00% error rate indicates that the landing page is stable and reliable, with no reported errors during the load test.

With a throughput of 8.3 requests per second, the website showcased its capability to handle incoming traffic efficiently, further affirming its robustness.

Overall, the load test results are positive, and the landing page appears to be adequately optimized to handle the expected load. Any future optimizations can build upon these results to further enhance the website's performance and scalability.
