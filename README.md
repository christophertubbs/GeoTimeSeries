# GeoTimeSeries
A standard for embedding varying time series information within geojson documents with accompanying libraries for serialization and deserialization

## Motivation
GeoJSON is not well suited towards a time series of varying data at individual points. There are several projects attempting to recitfy this, such as [GeoJSON-T](https://github.com/kgeographer/geojson-t), but it generally seems to define property values *away* from the changing time definitions. The goal is to create something akin to a mix between GeoJSON and WaterML.

## Requirements
* Base GeoJSON must be readable by *most* standard GIS applications (such as "QGIS") that can make use of GeoJSON
* Some sort of standard `time series` array within each `properties` definition for each feature
* Standard handling for instantaneous time series values - one or more values at a specific instance in time
* The option to declare date/time formatting (with a default) for each feature
* The option to declare the time zone (with a default) for each feature
* A JSON schema used for validation
* A python serialization and deserialization library
* Extensive examples

## Bonus
* A C++ serialization and deserialization library
* A Java serialization and deserialization library
* A library to plot animated maps for python
* A standard for feature linkage (Feature C comes from Features A and B and leads to features D and E) in order to form a graph
