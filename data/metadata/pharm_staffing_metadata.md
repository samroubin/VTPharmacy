- `Title`: Pharmacy staffing (pharm_staffing)
- `Abstract`: This contains the staffing data for each pharmacy for which staffing levels were collected via survey by a unique pharmacy ID. We attempted to survey all pharmacies in VT for staffing. 
- `Spatial Coverage`: Vermont and ten miles within in Vermont state border, encompassing parts of New York, Massachusetts, and New Hampshire. Canada was excluded.
- `Temporal Coverage`: Data was collected over the course of a couple of months, but it theoretically represents a an average or typical week in the fall or early winter of 2023.
- `Temporal Resolution`: A week. Differential data was collected for weekdays, Saturdays, and Sundays of a typical week.
- `Lineage`: This data was collected by surveying each pharmacy location in Vermont. Hannaford staffing levels were collected and derived in bulk from the regional pharmacy manager providing 
- `Distribution`: This data will not be made public due to the proprietary nature of this information; however, the staffing data may be available upon request.
- `Constraints`: We have agreed not to publicly release staffing levels of the pharmacy locations due to the proprietary nature of this data for some of the larger pharmacy chains.
- `Data Quality`: The staffing levels were reported directly from pharmacy staff at each individual pharmacy location (besides Hannaford data). Therefore, the quality is unknown but is presumed to be high. 
- `Variables`: 

| Label | Alias | Definition | Type | Accuracy | Domain | Missing Data Value(s) | Missing Data Frequency |
| :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: |
| pharmid | Pharmacy ID | A unique identifier given to each pharm. in study area | text | NA | VT, NY, MA, NH 1 - 117 | NA | NA |
| week_pharm | Weekday pharmacists | Typical # pharmacists on weekday | integer | ... | 0 - 10 | NULL | Could not collect data for 15/117 pharmacies in VT. No staffing data collected for out of state pharmacies. |
| week_tech | Weekday techs | Typical # techs on weekday | integer | ... | 0 - 10 | NULL | Could not collect data for 15/117 pharmacies in VT. No staffing data collected for out of state pharmacies. |
| sat_pharm | Saturday pharmacists | Typical # pharmacists on Sat | integer | ... | 0 - 10 | NULL | Could not collect data for 15/117 pharmacies in VT. No staffing data collected for out of state pharmacies. |
| sat_tech | Saturday techs | Typical # techs on Sat | integer | ... | 0 - 10 | NULL | Could not collect data for 15/117 pharmacies in VT. No staffing data collected for out of state pharmacies. |
| sun_pharm | Sunday pharmacists | Typical # pharmacists on Sun | integer | ... | 0 - 10| NULL | Could not collect data for 15/ 117 pharmacies in VT. No staffing data collected for out of state pharmacies. |
| sun_tech | Sunday techs | Typical # techs on Sun | integer | ... | 0 - 10| NULL | Could not collect data for 15/ 117 pharmacies in VT. No staffing data collected for out of state pharmacies. |
