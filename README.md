# awesome-tsdb

A **time series database (TSDB)** is a software system that is optimized for storing and serving time series through associated pairs of time(s) and value(s). In some fields, time series may be called profiles, curves, traces or trends. Several early time series databases are associated with industrial applications which could efficiently store measured values from sensory equipment (also referred to as data historians), but now are used in support of a much wider range of applications.

In many cases, the repositories of time-series data will utilize compression algorithms to manage the data efficiently. Although it is possible to store time-series data in many different database types, the design of these systems with time as a key index is distinctly different from relational databases which reduce discrete relationships through referential models.

## Overview

A time series database typically separates the set of fixed, discrete characteristics from its dynamic, continuous values into sets of points or 'tags.' An example is the storage of CPU utilization for performance monitoring: the fixed characteristics would include the name 'CPU Utilization' the units of measure '%' and a range '0 to 1'; and the dynamic values would store the utilization percentage and a timestamp. The separation is intended to efficiently store and index data for application purposes which can search through the set of points differently than the time-indexed values.

The databases vary significantly in their features, but most will enable features to create, read, update and delete the time-value pairs as well as the points to which they are associated. Additional features for calculations, interpolation, filtering, and analysis are commonly found, but are not commonly equivalent.

## List of Time Series Database

### InfluxDB

### [VictoriaMetrics](https://github.com/VictoriaMetrics/VictoriaMetrics)

