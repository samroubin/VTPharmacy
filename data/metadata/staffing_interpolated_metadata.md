- `Title`: Staffing Interpolated (staffing_interpolated.csv)
- `Abstract`: This dataset is primary data that was collected through surveying all VT pharmacies about their staffing levels and hours of operations. It contains information on each VT pharmacy's (117) location, hours of operations on weekdays, Saturdays, and Sundays, and the number of pharmacists and pharmacy technicians that typically work on a given day. It also includes data on the hours of operations of the 75 pharmacies within 10 miles of the VT border (NY, MA, NH). Staffing data was not collected for pharmacies outside of Vermont. Instead, staffing data was interpolated for all out-of-state pharmacies and pharmacies in Vermont for which data could not be collected. There were 192 pharmacies included in our study area in total.
- `Spatial Coverage`: Vermont and ten miles within in Vermont state border, encompassing parts of New York, Massachusetts, and New Hampshire. Canada was excluded.
- `Spatial Resolution`: This data specifies the specific coordinates of the pharmacy locations of interest. Resolution is not relevant.
- `Spatial Reference System`: EPSG 6589 in order to match the results maps.
- `Temporal Coverage`: Data was collected over the course of a couple of months, but it theoretically represents an average or typical week in the fall or early winter of 2023.
- `Temporal Resolution`: A week. Differential data was collected for weekdays, Saturdays, and Sundays of a typical week.
- `Lineage`: Staffing data extracted from pharmacies_raw.csv. This dataset was created using the 00_pharmacy_cleaning.Rmd, which ultimately interpolated missing staffing data and extracted a dataframe with just the staffing levels. 
- `Distribution`: This staffing data will not be made public due to the proprietary nature of this information; however, the staffing data may be available upon request.
- `Constraints`: We have agreed not to publicly release staffing levels of the pharmacy locations due to the proprietary nature of this data for some of the larger pharmacy chains.
- `Data Quality`: Staffing data was interpolated for fifteen of 117 pharmacies in VT. Staffing data was interpolated for all 75 out-of-state pharmacies. 
- `Variables`:

| Label | Definition | Type |
| :--: | :--: | :--: |
| pharmid | unique pharmacy identifier | Text|
| week_open | opening time on weekdays | Integer |
| week_close | closing time on weekdays | Integer |
| sat_open| opening time on Saturdays | Integer |
| sat_close| closing time operations on Saturdays | Integer |
| sun_hours| opening time on Sundays | Integer |
| sun_hours| closing time on Sundays | Integer |
| week_pharm| Typical # pharmacists on weekday | Integer |
| week_tech| Typical # pharm. techs on weekdays  | Integer |
| sat_pharm| Typical # pharmacists on Saturday | Integer|
| sat_tech| Typical # pharm. techs on Saturdays  | Integer|
| sun_pharm| Typical # pharmacists on Sundays | Integer |
| sun_tech| Typical # pharm. techs on Sundays| Integer|


  - `Accuracy`: We are confident in the accuracy of the pharmacy list in Vermont. Our confidence in the out-of-state retail pharmacy locations is slightly diminished since these pharmacy locations are not based on a recent dataset from the respective states. We have confidence in the quality of the data on pharmacy staffing and hours of operations for VT pharmacies since we collected the data by surveying all pharmacies. Hours of operations for non-VT pharmacies were pulled from online. The spatial accuracy of the dataset is further confirmed as we ensured that the point coordinates for the pharmacies were within the building footprint polygon on the OSM map layer in QGIS.
  - `Domain`:  The expected range of all of the pharmacy operational hours is from roughly 7 am to 10 pm. The expected range of pharmacists and technicians is from one to ten for weekdays, Saturdays, and Sundays.
  - `Missing Data Value(s)`: For any missing data on the number of pharmacists and pharmacy technicians at a given pharmacy location, the values are interpolated based on collected data for pharmacies of the same type. There is no missing data for hours of operations, as operational hours for non-surveyed out-of-state pharmacies were pulled from online.
  - `Missing Data Frequency`: We were able to collect staffing data for 102 of 117 pharmacies in Vermont.
