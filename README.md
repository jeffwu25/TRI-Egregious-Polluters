# TRI-Egregious-Polluters

My code from an environmental sociology investigation lead by Professor Simone Pulver (UCSB) into whether some facilities in the Toxics Releases Industry database pollute significantly more than others and what common underlying characteristics these facilities may share. 

Authors: Simone Pulver (lead of the project), Jeffrey Wu (quantitative lead), Mary Burke, Dustin Hill (contributors to previous projects)

This project builds on Professor Pulver's work on the topic, see (insert reference). In this project, Professor Pulver wanted to conduct a more rigorous statistical analysis to evaluate the distribution of "egregious polluters" across NAICS code industries and predict egregious polluter status based on facility characteristics, so she sought me out to be the quantitative lead for this project. The analysis is split into the two files included in this repository: 

## TRI-NETS-Merge.qmd

This project involved downloading and wrangling several different datasets: TRI-RSEI data (publicly available), NET/NAICS data (proprietary), and census block group data (proprietary). The TRI-RSEI data contains the emissions and RSEI Hazard data for hundreds of thousands of facilities across tens of thousands of industries from the years 1990-2022. We attach company and industry level information (acquired from Duns and Bradstreet) such as number of employees, sales revenue, and whether the facility has a government contract or not. Finally, we attach some socioeconomic data (acquired from Geolytics) to give us an idea of the socioeconomic status of residents living within a 3 mile radius of each facility. This last step involved using GIS operations to draw a 3 mile buffer around each facility, calculate the areal apportionment of our socioeconomic variables based on which census block groups intersected this buffer, and then calculate an estimate a value for proportion of non-white residents and proportion of residents below the poverty line living near each facility for each facility-year observation. Once the final dataset is put together, we carry it into our quantitative analysis in the next file. 

## TRI-NETS-Analysis.qmd
