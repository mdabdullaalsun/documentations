# Mu SOD 

## Send API
- Maximum Reservation observed per day: 9,739,859
- Maximum Reservation observed per hour: 1,131,119

Throughput (December 2024 SS)
- Maximum Allowed QPS: 1000
- Maximum Observed QPS: 972
- Maximum Observed QPS 2xx: 866
- Per Service Allowed QPS: 350
- Per Service Observed QPS: 356 (due to overlapping of seconds)

Response Time (Last 30days data on 2024-12-05)
- 75th Percentile: 12 ms
- 95th Percentile: 15 ms
- 99th Percentile: 19 ms
- 99.5th Percentile: 26 ms
- 99.995th Percentile: 1,072 ms
- Max Response Time: 5,509 ms

Request Size (Last 2days data on 2024-12-05)
- Maximum Allowed Request Size: 100KB of template
- 75th Percentile: 41.2 KB
- 95th Percentile: 41.3 KB
- 99th Percentile: 93.7 KB
- 99.5th Percentile: 94.9 KB

Load Continues for around 50 minutes (19:55 to 20:45) 

## Check API
Throughput (December 2024 SS)
- Maximum Allowed QPS: 400
- Maximum Observed QPS: 972
- Maximum Observed QPS 2xx: 866
- Per Service Allowed QPS: 200
- Per Service Observed QPS: 356 (due to overlapping of seconds)

Response Time (Last 30days data on 2024-12-05)
- 75th Percentile: 12 ms
- 95th Percentile: 15 ms
- 99th Percentile: 19 ms
- 99.5th Percentile: 26 ms
- 99.995th Percentile: 1,072 ms
- Max Response Time: 5,509 ms

Request Size (Last 2days data on 2024-12-05)
- Maximum Allowed Request Size: 100KB of template
- 75th Percentile: 41.2 KB
- 95th Percentile: 41.3 KB
- 99th Percentile: 93.7 KB
- 99.5th Percentile: 94.9 KB

# Mu LMD
Email Size (Last 2days data on 2024-12-05)
- Maximum Allowed Request Size: ~
- 75th Percentile: 54.3 KB
- 95th Percentile: 87.4 KB
- 99th Percentile: 123.7 KB
- 99.5th Percentile: 154.7 KB
- 99.995th Percentile: 218.1 KB

# Summary

## File Size

| Percentile/Max Size | Overall        | Instant    | Bulk           |
|---------------------|----------------|------------|----------------|
| 75th Percentile     | 1,177          | 963        | 28,942         |
| 95th Percentile     | 22,399         | 7,510      | 12,739,036     |
| 99th Percentile     | 2,154,580      | 81,132     | 435,498,239    |
| 99.5th Percentile   | 28,927,030     | 81,261     | 1,035,543,375  |
| Max Size            | 10,945,630,279 | 26,804,813 | 10,945,630,279 |

## Average Line Size

| Percentile/Max Size | Overall       | Instant       | Bulk           |
|---------------------|---------------|---------------|----------------|
| 75th Percentile     | 121           | 114           | 234            |
| 95th Percentile     | 329           | 329           | 965            |
| 99th Percentile     | 899           | 758           | 5,768          |
| 99.5th Percentile   | 2,040         | 878           | 11,369         |
| Max Size            | 78,574        | 8,680         | 78,574         |

## Requests

| Peak                | Overall       | Instant       | Bulk           |
|---------------------|---------------|---------------|----------------|
| Peak per Second     | 24            | 16            | 16             |
| Peak per Minute     | 693           | 252           | 674            |
| Peak per Hour       | 4,117         | 3,074         | 2,944          |
| Peak per Day        | 48,366        | 43,659        | 6,773          |

## Sending

| Metric              | Overall       | Bulk          |
|---------------------|---------------|---------------|
| Max Possible        | 9,313         | 9,313         |
| Peak per Minute     |               | 318,415       |
| Peak per Hour       |               | 15,299,719    |
| Peak per Day        |               | 145,378,619   |
