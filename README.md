# Load Testing for Landing Page with JMeter

<p align="center"><a href="#" target="_blank"><img src="Images/landing-page.png" height="250px"></a></p>

Welcome to the load testing report for the landing page of the [demoblaze](https://www.demoblaze.com) website. This report presents the results of the load testing of this website conducted using JMeter, an open-source tool for analyzing and measuring the performance of a variety of services, with a focus on web applications. Demoblaze is a mock ecommerce system and the purpose of conducting this performance testing was to gain familiarity with the JMeter tool and assess how the landing page of this website handles different levels of user load.

## Purpose of Load Testing

Load testing is a crucial step in assessing the performance and scalability of a web application under various user loads. It helps identify potential bottlenecks and areas for improvement in the system. In this load testing scenario, the aim was to analyze how the landing page of the demoblaze website performs when subjected to a simulated real-world load of 1000 concurrent users.

## Load Test Configuration

The load test was executed using the following thread group configuration:

- <b>Number of Threads (Users): 1000</b>: This configuration simulates a significant number of concurrent users (1000) accessing the landing page simultaneously.
- <b>Ramp-up Period: 60 seconds</b>: The ramp-up period of 60 seconds means that the load was gradually increased over this time frame. This helps in mimicking real-world scenarios where user traffic doesn't surge instantly.
- <b>Loop Count: 5</b>: Each virtual user went through the landing page 5 times during the test. This can be useful to observe how the application performs over repeated interactions.
- <b>Duration: 300 seconds</b>: The load test ran for 5 minutes, allowing you to observe the application's performance under sustained load over an extended period.
- <b>Startup Delay: 10 seconds</b>: A startup delay of 10 seconds was set before starting the load test. This can help the application stabilize before the full load is applied.

## Load Test Result Summary

The load test results were obtained for the "HTTP Request" sampler, which represents individual requests made to the landing page, and the "TOTAL" metric, which aggregates all the requests.

The summary of the load test results is as follows:

| Label        | # Samples | Average | Min | Max  | Std. Dev. | Error % | Throughput | Received KB/sec | Sent KB/sec | Avg. Bytes |
| ------------ | --------- | ------- | --- | ---- | --------- | ------- | ---------- | --------------- | ----------- | ---------- |
| HTTP Request | 5000      | 239     | 0   | 1304 | 83.17     | 0.00%   | 82.3/sec   | 1366.41         | 9.32        | 17707.8    |
| TOTAL        | 5000      | 239     | 0   | 1304 | 83.17     | 0.00%   | 82.3/sec   | 1366.41         | 9.32        | 17007.8    |

## Analysis of Load Test Results

Based on the load test results, the following key observations can be made:

- Response Time: The average response time for all requests was 239 milliseconds, with a minimum of 0 milliseconds and a maximum of 1304 milliseconds. The standard deviation of response times was 83.17 milliseconds. These response times indicate that the server is responding promptly to user requests, providing a smooth user experience.

- Duration and Load: The load test ran for a duration of 300 seconds, during which 1000 concurrent users executed 5 iterations of the test scenario. This testing duration helped assess the website's performance under sustained load conditions.

- Error Percentage: The load test reported a 0.00% error rate, indicating that all requests made during the test were successful. This suggests that the landing page is stable and reliable, as no errors or failures were encountered.

- Throughput: The throughput was measured at 82.3 requests per second, which indicates the website's capacity to handle incoming requests efficiently. Higher throughput values imply better performance and scalability.

- Data Rates: The received data rate was measured at 1366.41 KB/sec, while the sent data rate was 9.32 KB/sec. These values represent the rate at which data was received from the server and sent to the server, respectively.

- Average Data Size: The average data size (payload) of each response was 17007.8 bytes. This metric provides insights into the amount of data transmitted in each response.

## Conclusion

In conclusion, the load test results demonstrate that the landing page of the demoblaze website performed well under the simulated load of 1000 concurrent users. The average response time of 239 milliseconds suggests that the server responded promptly to user requests, contributing to a satisfactory user experience.

The 0.00% error rate indicates that the landing page is stable and reliable, with no reported errors during the load test.

With a throughput of 82.3 requests per second, the website showcased its capability to handle incoming traffic efficiently, further affirming its robustness.

Overall, the load test results are positive, and the landing page appears to be adequately optimized to handle the expected load. Any future optimizations can build upon these results to further enhance the website's performance and scalability.
