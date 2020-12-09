# awesome-tsdb

A **time series database (TSDB)** is a software system that is optimized for storing and serving time series through associated pairs of time(s) and value(s). In some fields, time series may be called profiles, curves, traces or trends. Several early time series databases are associated with industrial applications which could efficiently store measured values from sensory equipment (also referred to as data historians), but now are used in support of a much wider range of applications.

In many cases, the repositories of time-series data will utilize compression algorithms to manage the data efficiently. Although it is possible to store time-series data in many different database types, the design of these systems with time as a key index is distinctly different from relational databases which reduce discrete relationships through referential models.

## 1. Overview

### 1.1 Time Series

A **time series** is a series of data points indexed (or listed or graphed) in time order. Most commonly, a time series is a sequence taken at successive equally spaced points in time. Thus it is a sequence of discrete-time data. Time Series analysis can be useful to see how a given asset, security or economic variable changes over time. Examples of time series are heights of ocean tides, counts of sunspots, and the daily closing value of the Dow Jones Industrial Average.

Time series are very frequently plotted via run charts (a temporal line chart). Time series are used in statistics, signal processing, pattern recognition, econometrics, mathematical finance, weather forecasting, earthquake prediction, electroencephalography, control engineering, astronomy, communications engineering, and largely in any domain of applied science and engineering which involves temporal measurements.

### 1.2 TSDB

A time series database typically separates the set of fixed, discrete characteristics from its dynamic, continuous values into sets of points or 'tags.' An example is the storage of CPU utilization for performance monitoring: the fixed characteristics would include the name 'CPU Utilization' the units of measure '%' and a range '0 to 1'; and the dynamic values would store the utilization percentage and a timestamp. The separation is intended to efficiently store and index data for application purposes which can search through the set of points differently than the time-indexed values.

The databases vary significantly in their features, but most will enable features to create, read, update and delete the time-value pairs as well as the points to which they are associated. Additional features for calculations, interpolation, filtering, and analysis are commonly found, but are not commonly equivalent.

### 1.3 TSDB Scenarios

Now let’s consider a few examples of time-series workloads:

-   **DevOps/server/container monitoring**. The system typically collects metrics about different servers or containers: CPU usage, free/used memory, network tx/rx, disk IOPS, etc. Each set of metrics is associated with a timestamp, unique server name/ID, and a set of tags that describe an attribute of what is being collected.

-   **IoT sensor data**. Each IoT device may report multiple sensor readings for each time period. As an example, for environmental and air quality monitoring this could include: temperature, humidity, barometric pressure, sound levels, measurements of nitrogen dioxide, carbon monoxide, particulate matter, etc. Each set of readings is associated with a timestamp and unique device ID, and may contain other metadata.

-   **Financial data**. Financial tick data may include streams with a timestamp, the name of the security, and its current price and/or price change. Another type of financial data is payment transactions, which would include a unique account ID, timestamp, transaction amount, as well as any other metadata. (Note that this data is different than the OLTP example above: here we are recording every transaction, while the OLTP system was just reflecting the current state of the system.)

-   **Fleet/asset management**. Data may include a vehicle/asset ID, timestamp, GPS coordinates at that timestamp, and any metadata.

## 2. List of Time Series Database

### 2.1 [InfluxDB](https://github.com/influxdata/influxdb)

![](./assets/Influxdb_logo.png)

InfluxDB is an open source time series platform. This includes APIs for storing and querying data, processing it in the background for ETL or monitoring and alerting purposes, user dashboards, and visualizing and exploring the data and more. The master branch on this repo now represents the latest InfluxDB, which now includes functionality for Kapacitor (background processing) and Chronograf (the UI) all in a single binary.

More information at [here](./influxdb/README.md)

### 2.2 [VictoriaMetrics](https://github.com/VictoriaMetrics/VictoriaMetrics)

VictoriaMetrics is fast, cost-effective and scalable monitoring solution and time series database.

### 2.3 [Prometheus](https://github.com/prometheus/prometheus)

Prometheus, a Cloud Native Computing Foundation project, is a systems and service monitoring system. It collects metrics from configured targets at given intervals, evaluates rule expressions, displays the results, and can trigger alerts when specified conditions are observed.

### 2.4 [Amazon Timestream](https://aws.amazon.com/timestream/)

Amazon Timestream is a fast, scalable, and serverless time series database service for IoT and operational applications that makes it easy to store and analyze trillions of events per day up to 1,000 times faster and at as little as 1/10th the cost of relational databases. Amazon Timestream saves you time and cost in managing the lifecycle of time series data by keeping recent data in memory and moving historical data to a cost optimized storage tier based upon user defined policies. Amazon Timestream’s purpose-built query engine lets you access and analyze recent and historical data together, without needing to specify explicitly in the query whether the data resides in the in-memory or cost-optimized tier. Amazon Timestream has built-in time series analytics functions, helping you identify trends and patterns in your data in near real-time. Amazon Timestream is serverless and automatically scales up or down to adjust capacity and performance, so you don’t need to manage the underlying infrastructure, freeing you to focus on building your applications.


