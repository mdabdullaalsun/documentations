# Mu SOD

## Send API

### Maximum Reservation Observed
| Metric                          | Value       |
|---------------------------------|-------------|
| Maximum Reservation per Day     | 9,739,859   |
| Maximum Reservation per Hour    | 1,131,119   |

### Throughput (December 2024 SS)
| Metric                   | Value                               |
|--------------------------|-------------------------------------|
| Maximum Allowed QPS      | 1,000                               |
| Maximum Observed QPS     | 972                                 |
| Maximum Observed QPS 2xx | 866                                 |
| Per Service Allowed QPS  | 350                                 |
| Per Service Observed QPS | 356 (due to overlapping of seconds) |

### Response Time (Last 30 days data on 2024-12-05)
| Percentile/Max Response Time    | Time (ms)   |
|---------------------------------|-------------|
| 75th Percentile                 | 12          |
| 95th Percentile                 | 15          |
| 99th Percentile                 | 19          |
| 99.5th Percentile               | 26          |
| 99.995th Percentile             | 1,072       |
| Max Response Time               | 5,509       |

### Request Size (Last 2 days data on 2024-12-05)
| Percentile/Max Request Size  | Size (KB)      |
|------------------------------|----------------|
| Maximum Allowed Request Size | 100 (template) |
| 75th Percentile              | 41.2           |
| 95th Percentile              | 41.3           |
| 99th Percentile              | 93.7           |
| 99.5th Percentile            | 94.9           |

**Load Continues for around 50 minutes (19:55 to 20:45)**

## Check API

### Throughput (December 2024 SS)
| Metric                          | Value       |
|---------------------------------|-------------|
| Maximum Allowed QPS             | 400         |
| Maximum Observed QPS            | 255         |
| Maximum Observed QPS 2xx        | 255         |
| Per Service Allowed QPS         | 200         |
| Per Service Observed QPS        | 127         |

### Response Time (Last 30 days data on 2025-01-15)
| Percentile/Max Response Time    | Time (ms)   |
|---------------------------------|-------------|
| 75th Percentile                 | 4           |
| 95th Percentile                 | 6           |
| 99th Percentile                 | 56          |
| 99.5th Percentile               | 505         |
| 99.995th Percentile             | 1,228       |
| Max Response Time               | 2,985       |


# Mu LMD

## API Performance 
| Percentile/Max Response Time | Time (ms) |
|------------------------------|-----------|
| 75th Percentile              | 67        |
| 95th Percentile              | 130       |
| 99th Percentile              | 237       |
| 99.5th Percentile            | 262       |
| 99.995th Percentile          | 2,804     |
| Max Response Time            | 15,155    |

## Email Size (Last 2 days data on 2024-12-05)
| Percentile/Max Size          | Size     |
|------------------------------|----------|
| Maximum Allowed Request Size | ~        |
| 75th Percentile              | 54.3 KB  |
| 95th Percentile              | 87.4 KB  |
| 99th Percentile              | 123.7 KB |
| 99.5th Percentile            | 154.7 KB |
| 99.995th Percentile          | 218.1 KB |


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
