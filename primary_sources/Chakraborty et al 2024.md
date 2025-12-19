---
DOI: 10.18520/CS/V127/I5/572-580
Date: 19 Dec 2025
Rating: /5
Title: Framework for eForest fire management in the shifting cultivation-dominated landscape of Meghalaya, North East India, using remote sensing and GIS
ShortSummary: Maps fire counts from 2003-203 with MODIS, generated forest fire vulnerability map.  Maps jhum and land use
---
#burning #data

Kasturi Chakraborty, Dhruval Bhavsar, Suraj Kumar Swain, Siddharth Bhuyan, Harish Chaudhary, Jakesh Mohapatra, Praveen Kumar, Balajied Lyngdoh, Joydeep Dey, Brandon Rynjah, Nilay Nishant
and K. K. Sarma
# [[Chakraborty_etal_2024.pdf|Framework for eForest fire management in the shifting cultivation-dominated landscape of Meghalaya, North East India, using remote sensing and GIS]]

> [!tldr] Summary 4/5
> Maps fire, fire vulnerability and land-use (?).  Delivers Meghalaya Forest Fire Information System dashboard. 

> [!quote] Quotable
>The purpose of MeFFIS is to involve Government decision-makers and local communities in effective fire suppression and management. Shifting cultivation (jhum) is a predominant land-use category and a major cause of forest fires in Meghalaya. Therefore the forest fire assessment
has been carried out in jhum and non-jhum areas for planning effective fire management strategies by forest fire managers in the jhum- and the non-jhum-prone areas.

> [!quote] Quotable
> For efficient and effective forest fire management, an attempt has been made in this study to distinguish forest fires as jhum and non-jhum. Jhum fires are limited to jhum cultivation areas. Such forest fires can be controlled only by controlling jhum cultivation.


### Aim of Paper
Used MODIS data to map fire occurrences from 20023-2023 and data from the Indian Space Research Organization (ISRO) to map forest cover and land-use classes.   Information on jhum management was obtained from LULC maps 'available from the North Eastern Space Applications Center.'  Presents a dashboard.
### Insights
- Paints fire as a very negative force 
	- "damaging the growing stock  and making the area vulnerable to erosion (Satendra and Kaushik, 2014; citation 6)"
	- "Forest fire studies in Meghalaya have raised concerns over their frequent occurrence due to shifting cultivation and other human activities, and the need for scientific forest fire management strategies (Mukherjee, S. and Raj, K.,;Dhar, T., Bhatta, B. and Aravindan, S., and Chakraborty, K., Mondal, P. P., Chabukdhara, M. and Sudhakar, S.,  citations 12–14)."
- ==Note: Dhar et al. maps fire prone areas. Dhar, T., Bhatta, B. and Aravindan, S., Forest fire occurrence, distribution and risk mapping using geoinformation technology: a case study in the sub-tropical forest of the Meghalaya, India. Remote Sensing Appl.: Soc. Environ., 2023, 29, 100883.==
- ==Note: see Champion and Seth (1968) classification. Champion, H. G. and Seth, S. K., A Revised Classification of the Forest Types in India, Manager Publications, GoI, New Delhi, 1968, pp. 105–115.==
- Data inputs:
	- Forest cover %: India State of Forest Report. Forest Survey of India, India State of Forest Report, Forest Survey of India, Ministry of Environment and Forests, Government of India, Dehradun, 2021
	- Forest Fire Data: MODIS
	- Forest-type maps for fuel characteristics: Forest Survey of India (https://fsi-forestfire.gov.in)
	- Forest Cover: ISRO created satellite imagery
	- LULC: ISRO created satellite imagery
	- Elevation, slope and aspect: Carto DEM
	- Jhum areas: land-use/land-cover (LULC) maps of 2005–06, 2011–2012, 2015–2016, 2017–2018 and 2021 (available from the North Eastern Space Applications Centre data repository)
- Vulnerability
	- Used expert driven Analytic Hierarchy Process to determine the weights of:
		- forest type
		- forest density
		- settlement
		- slope
		- road
		- aspect
		- elevation
	- They basically compared factors in pairs (e.g., is forest type more important than slope?), then built a matrix of the comparisons.  Normalized the matrix then averaged the rows to get weights:
				Vulnerability = Forest type × 0.29 + forest density
				× 0.21 + settlement × 0.19 + slope × 0.15 + road
				× 0.06 + aspect × 0.05 + elevation × 0.05
	* This is less robust than using fire occurrences coupled with machine learning, stats or even a AHP/ML hybrid approach, but is structured, transparent and flexible.  Good for when data is scarce.
	* There was field verification and checking with fire occurrence data.  Not clear how that was done.  Maybe Table 2 is the source?
	* With the App/dashboard:
		* forest fire managers can report fires with causes and area estimation and to upload data
		* data can be saved in app for uploading later when internet is available
		* dashboard has near real time data.  
		* The dashboard has a jhum/not jhum dataset that can be used to classify fires
	* With results
		* ~45k fires during the time period
		* no fire size reported
	* Prevalence of jhum lead to situations with high prone-ness, moderate vulnerability.
	* #recommendation  are around:
		* dealing with litter
		* real time warning system and collection of fire data
		* better mapping of jhum


![[Pasted image 20251219122906.png]]







