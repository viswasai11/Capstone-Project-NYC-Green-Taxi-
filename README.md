# Capstone-Project-NYC-Green-Taxi-
# TLC Trip Record Data
Yellow and green taxi trip records include fields capturing pick-up and drop-off dates/times, pick-up and drop-off locations, trip distances, itemized fares, rate types, payment types, and driver-reported passenger counts. The data used in the attached datasets were collected and provided to the NYC Taxi and Limousine Commission (TLC) by technology providers authorized under the Taxicab & Livery Passenger Enhancement Programs (TPEP/LPEP). The trip data was not created by the TLC, and TLC makes no representations as to the accuracy of these data.

For-Hire Vehicle (“FHV”) trip records include fields capturing the dispatching base license number and the pick-up date, time, and taxi zone location ID (shape file below). These records are generated from the FHV Trip Record submissions made by bases. Note: The TLC publishes base trip record data as submitted by the bases, and we cannot guarantee or confirm their accuracy or completeness. Therefore, this may not represent the total amount of trips dispatched by all TLC-licensed bases. The TLC performs routine reviews of the records and takes enforcement actions when necessary to ensure, to the extent possible, complete and accurate information.

# Working With Parquet Format
TLC is switching to the Parquet file type for storing raw trip data on our website.
Parquet is the industry standard for working with big data. Using Parquet format
results in reduced file sizes and increased speeds. However, we have been using
the CSV format for a while and the Parquet format might be new to some users.
Below are examples of how to open Parquet files using R and Python:
Python:
import pyarrow.parquet as pq
trips = pq.read_table('trips.parquet')
trips = trips.to_pandas()
Additional documentation: https://arrow.apache.org/docs/python/parquet.html
R:
library(arrow)
trips <- read_parquet('trips.parquet')
Additional documentation: https://arrow.apache.org/docs/r/reference/read_parquet.html
