# Capstone Project
Capstone project for SSDS program. Low Code, No Code 

Topics Covered: 
- Delta Lake
- Medallion Architecture
- Bamboolib
  - EDA
  - ETL
  - Feature Engineering
- AutoML
- MlFlow
- Dashboards

Personas Covered:
- Citizen Data Scientist, who is a business SME, getting into insights from raw data with low code no code solution

## Problem Statement
In this exercise, you will use Databricks Lakehouse platform to go through the whole data science pipeline to solve a business problem and predict engine faliure using synthetically generated telematics data. Dataset used in this excercise except weather data is generated using databricks datagen library https://databrickslabs.github.io/dbldatagen/public_docs/APIDOCS.html.

When you have completed this excercise, you will understand how to:

* Use platform to load, visualize, and analyze data
* Use bamboolib UI to perform EDA, ETL and feature engineering
* Use AutoML to quick build and test machine learning algorithm
* Deploy a selected machine learning model to production using UI

## Data Dictionary
Dataset consistes for 400 engines build and sold between January 2022 and September 2022, their telemetry data and faliure data

### Engine Data

<pre> * engine_serial_number:               Unique identifier for an engine
 * build_date:                         Date the engine was built
 * ship_date:                          Date the engine was shipped to OEM / Customer
 * inservice_date:                     Date the vehicle went into service / sold to end customer
 * engine_config:                      Differentiating engines based on options or configs like HP
 * user_application:                   Vehicle type where the engine is intalled </pre>

### Engine Events

 <pre> * engine_serial_number                Unique identifier for an engine	
 * event_timestamp                     Timestamp when the engine event was generated
 * altitude                            Altitude at which the vehicle is being driven
 * altitude_uom	                       Unit of measure for Altitude
 * location                            City in which the truct is at the time	
 * rpm	                               Engine rpm	
 * oil_temperature                     Engine oil temperature in farenhite	
 * exhaust_temperature	               Engine exhaust temperature in farenhite
 * intake_temperature	               Engine intake air temperature in farenhite
 * fault_code	                       Falut Code generated by engine	
 * event_type                          Type of event received HB - Heart Beat of FC - Fault Code </pre>
 
### Engine Faliure Data

<pre> * engine_serial_number                Unique identifier for an engine
 * event_timestamp                      Date engine had a faliure	
 * failed                               Flag indicating engine had a faliure </pre>

### UOM Conversion Data

 <pre> * uom                                 Unit of measure
 * conversion_rate_feet                UOM comversion rate to feet </pre>
