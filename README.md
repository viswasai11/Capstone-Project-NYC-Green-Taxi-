# Project-NYC-Green-Taxi-
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

### Technology used:
<div align ='left'>
<img src ='https://technology.amis.nl/wp-content/uploads/2020/11/image_thumb-27.png', height = "50" alt = 'Jupyter'/><img width='12'/> 
<img src = 'https://cdn.dribbble.com/users/6569/screenshots/16471177/media/8bbfe7fd594073dc6271d5d852c7381a.png', height = "50" alt = 'Vs code'/><img width = '12'/>
<img src = 'https://thomasjpfan.github.io/data-umbrella-2020-streamlit-slides/images/streamlit.png', height = "50" alt = 'Streamlit'/><img width = '12'/>
<img src = 'https://github.githubassets.com/images/modules/logos_page/GitHub-Mark.png', height = "50" alt = 'Github'/><img width = '12'/>
<!-- <img src = 'https://img.uxwing.com/wp-content/themes/uxwing/download/brands-social-media/chatgpt-icon.png', height = "50" alt = 'ChatGPT'/><img width = '12'/>-->
</div>

Thank you for visiting this project!

**Author:** viswasai goudampally
**Contact:** viswasai.goudampally@gmail.com
