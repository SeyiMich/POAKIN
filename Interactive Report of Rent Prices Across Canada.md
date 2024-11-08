# Interactive Report of Rent Prices Across Canadian Cities

One-paged report showing available rental properties for accommodation across Canada.


### Problem Statement
The escalating housing crisis, marked by soaring rental prices and increasing homelessness, demands innovative solutions. Afrinest, a pioneering startup, is addressing this challenge by promoting shared accommodations.

To support their mission, I conducted a comprehensive geospatial analysis, visualized in a concise two-page report. By mapping rental properties across various provinces and cities, I identified regions with high potential for shared living arrangements. 


### Data Processing Steps 

- Step 1 : Assessed Kaggle for relevant dataset and found one by 
https://www.kaggle.com/datasets/sergiygavrylov/25000-canadian-rental-housing-market-june-2024

- Step 2 : Data was extracted into Power Query for further transformation. 

- Step 3 : After changing the status bar option to "column profiling based on entire dataset" and assessing the column profile option, I discovered the data had over 25000 entries but with lots of empty cells in the rows. 

- Step 5 : After removing duplicate data, I moved on to handling empty and null rows to ensure data integrity and accuracy. Key attributes like price, beds, baths, availability date were checked for empty/null values and any of such found were deleted completely. Same for the pets columns.

- Step 6 : The smoking column had two entries that were synonymous; "Non-smoking" and "Smoke free building". Every "Smoke free building" entry was renamed to "Non-smoking".
![1](https://github.com/user-attachments/assets/fa25da71-0462-49a0-bfcf-792ea6c04083)

Empty values in this column were renamed into "Not Specified", leaving us with only 4 occurences, ensuring we deal with only concise amount of extra data points on its related visuals.  
![2](https://github.com/user-attachments/assets/1cad75f4-201f-4c2b-9046-93f888887e1c)


- Step 7 : Choose Column option was selected, to leave out unnecessary columns and consequently reduce model size. All the columns were finally checked to ensure there was no empty cells and that the right data type were selected.

- Step 8 : All transformation changes made were saved and then data loaded to the model. 

- Step 9 : For ease of representation, the Availability column entries; which had the 12 months of the year as it entries, were grouped into a group of 5 for ease of analysis and representation.

![gr and Ung](https://github.com/user-attachments/assets/6233f742-d773-42ae-acac-521c4010b01f)

        Availability Column (Ungrouped)                        Availability_Column_grouped 


        
- Step 10 : For the visual type an ArcGIS was chosen and poplulated with the necessary Long. and Lat. data, while setting rent price to the color field. The visual was formatted for easy dentification of data points.



### Summary Page 

![final](https://github.com/user-attachments/assets/97058740-5efd-4fb5-ab75-92178d84838c)

        Different slicers were made for increased interactivity with the report. An 'Apply all slicers' button 
        and 'Clear all slicers' button was also added to apply and deselect all selected slicers at the click of a buttton. 
        This is very important to increase visual refresh time and optimize report performance especially during presentations. 



### Conclusion
 This data-driven approach enables Afrinest to:
 #### [1] Target strategic areas: Pinpoint locations where shared living could significantly reduce housing costs.  
 ####  [2] Optimize property selection: Assist tenants and co-tenants in finding suitable shared accommodations.  
 #### [3] Inform marketing strategies: Develop targeted campaigns to promote shared living in specific regions.
