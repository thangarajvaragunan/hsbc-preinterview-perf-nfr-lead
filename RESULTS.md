This repo contains a Git Pipeline for executing a Jmeter test. This is a non-gui mode test targeting 3 public APIs, running with 25 concurrent users and 120 sec rampup for 5 mins
1. Get - /posts
2. GET - /posts/{id{
3. POST - /post

**Latest Test Results**

| API Name | p95 Latency | SLA Status |
| --- | --- | --- |
| **T01_GetComments** | **41 ms** | ✔ Passed |
| **T02_CreatePost** | **112 ms** | ✔ Passed |
| **T03_GetPost_By_Id** | **29 ms** | ✔ Passed |

**Key Findings from the last Test**
1. All the API endpoints performed well below the SLA threshold of 800ms.
2. Read operations were highly responsive, consistently under 50ms.
3. No regression issues found and the system remained stable under the configured load.

**Risks**
1. Server resources were not monitored, hence cannot ascertain the server side/backend performance
2. No Throughput/Error rate SLA

**Broader NFT Strategy**
1. Collect the missing NFRs
2. Increase the test coverage (More APIs, End-To-End performance testing)
3. Include more performance test types (Stress, Soak, Spike)
4. Integrate server side monitoring



