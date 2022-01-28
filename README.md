# United States Broadband Usage Percentages Dataset
John Kahan - Vice President, Chief Data Analytics Officer |
Juan Lavista Ferres - Chief Scientist, Microsoft AI for Good Research Lab

Please contact bb_data@microsoft.com for questions.

Microsoft Introduction and Purpose
We are publishing datasets we developed as part of our efforts with Microsoft’s Airband Initiative to help close the rural broadband gap. The data can be used for the purpose of analyzing, understanding, improving, or addressing problems related to broadband access.

The datasets consist of data derived from anonymized data Microsoft collects as part of our ongoing work to improve the performance and security of our software and services. The data does not include any PII information including IP Address. We also suppress any location with less than 20 devices. Other than the aggregated data shared in this data table, no other data is stored during this process. We estimate broadband usage by combining data from multiple Microsoft services. The data from these services are combined with the number of households per county and zip code[1]. Every time a device receives an update or connects to a Microsoft service, we can estimate the throughput speed of a machine. We know the size of the package sent to the computer, and we know the total time of the download. We also determine zip code level location data via reverse IP. Therefore, we can count the number of devices that have connected to the internet at broadband speed per each zip code based on the FCC’s definition of broadband that is 25mbps per download[2]. Using this method, we estimate that ~120.4 million people in the United States are not using the internet at broadband speeds.

Background
Every day our world becomes a little more digital. But reaping the benefits of this digital world – pursuing new educational opportunities through distance learning, feeding the world through precision agriculture, growing a small business by leveraging the cloud, and accessing better healthcare through telemedicine – is only possible for those with a broadband connection, which is especially apparent now as more people are staying home due to the COVID-19 pandemic. Based on the Fourteenth Broadband Deployment Report from the Federal Communications Commission (FCC)[4], broadband is not available to at least 14.5 million people, 11.3 million of whom live in this country’s rural areas. Getting these numbers right is vitally important. This data is used by federal, state, and local agencies to decide where to target public funds dedicated to closing this broadband gap. That means millions of Americans already lacking access to broadband have been made invisible, substantially decreasing the likelihood of additional broadband funding or much needed broadband service. We are publishing this data today to allow others to use it to develop solutions to improving broadband access or addressing problems with broadband access.

![broadbandmap.png](/assets/broadbandmap.png)
Figure 1: Map of the United States by county with indicators of broadband availability and broadband usage
 
# Broadband Usage Percentages Zip Code Dataset: A Differentially Private Data Release
The initial dataset released in April 2020 provided broadband usage percentages at a US county-level.  In December 2020, we are adding a zip code-level view of this same information. The data is to be used for the purpose of analyzing, understanding, improving, or addressing problems related to broadband access.
As mentioned in the April 2020 release, the Broadband Usage Percentages Dataset is derived from aggregated and anonymized data Microsoft collects as part of our ongoing work to improve software and service performance and security. Given the zip code-level dataset provides a more granular view of broadband usage percentages by households, we took the additional step to ensure data privacy guarantees by utilizing differential privacy, a technique that adds noise to the data aggregations, preventing leakage about the presence of specific individuals in the dataset. We implemented differential privacy through the SmartNoise platform, a first-of-its-kind open source platform for differential privacy co-developed by Microsoft and the OpenDP initiative led by Harvard.  We estimate broadband usage by combining privatized data from multiple Microsoft services.
As Differential Privacy adds noise to protect privacy, the noise added to zip codes with a small number of households can impact utility. To ensure transparency into how zip codes with different population magnitudes are affected, we have included error range data. To read more about how differential privacy has been applied to this data, read the [Broadband usage differential privacy paper](./assets/Broadband_usage_differential_privacy_paper.pdf)

![broadbandusagezipcode.png](/assets/broadbandusagezipcode.png)
Figure 2: Map of the United States by zip codes with indicators of broadband usage

# Data table
Data contained in the  data table includes counties in the United States
- ST: is the 2 letter abbreviation of states in the United States https://www.iso.org/obp/ui/#iso:code:3166:US
- COUNTY ID: 4 to 5 digit code used to represent the county (last 3 digits) and the state (first digit or first 2 digits) https://www.census.gov/geographies/reference-files.html
- BROADBAND AVAILABILITY PER FCC: percent of people per county with access to fixed terrestrial broadband at speeds of 25 Mbps/3 Mbps as of the end of 2019 https://www.fcc.gov/reports-research/reports/broadband-progress-reports/fourteenth-broadband-deployment-report
- BROADBAND USAGE: percent of people per county that use the internet at broadband speeds based on the methodology explained above. Data is from October 2020.

Data contained in the zip code data table includes the following fields:
- ST: is the 2 letter abbreviation of states in the United States https://www.iso.org/obp/ui/#iso:code:3166:US
- COUNTY ID: 4 to 5 digit code used to represent the county (last 3 digits) and the state (first digit or first 2 digits) https://www.census.gov/geographies/reference-files.html
- ZIP CODE: 5 digit code used to represent geographic area used by the United State Postal Service
- BROADBAND USAGE: percent of people per county that use the internet at broadband speeds based on the methodology explained above. Data is from October 2020.
- ERROR RANGE (MAE)(+/-) : mean absolute error (MAE). The non-private broadband coverage estimate will be, on average, within the mean absolute error (MAE) error range.
- ERROR RANGE (95%)(+/-) : 95th percentile error range. For 95% of the time, the non-private broadband coverage estimate for zip codes with a similar number of households will be within 95th percentile error range.
- MSD: We also provide the mean signed deviation (MSD). The mean signed deviation offers an estimate of bias introduced by the process.
- For a detailed explanation of the differential privacy methodology, please refer to https://arxiv.org/pdf/2103.14035.pdf



Suggested datasets that can be used in combination with the county level data:
- US county boundaries data set: https://catalog.data.gov/dataset/tiger-line-shapefile-2017-nation-u-s-current-county-and-equivalent-national-shapefile 

Here are links to additional broadband information:
- Microsoft Rural Broadband link: https://news.microsoft.com/rural-broadband/
- FCC Broadband link: https://www.fcc.gov/document/broadband-deployment-report-digital-divide-narrowing-substantially-0
- FCC population estimates: https://www.fcc.gov/reports-research/data/staff-block-estimates

1. American Fact Finder https://data.census.gov/ and Office of Policy Development Research https://www.huduser.gov/portal/datasets/usps_crosswalk.html
2. “2018 Broadband Deployment Report | Federal Communications Commission.” https://www.fcc.gov/reports-research/reports/broadband-progress-reports/2018-broadband-deployment-report (accessed Apr. 15, 2020).
3. “2019 Broadband Deployment Report,” Federal Communications Commission, Jun. 11, 2019. https://www.fcc.gov/reports-research/reports/broadband-progress-reports/2019-broadband-deployment-report (accessed Apr. 15, 2020).
4. “Fourteenth Broadband Deployment Report," Federal Communications Commission, Jan 19, 2021. https://www.fcc.gov/reports-research/reports/broadband-progress-reports/fourteenth-broadband-deployment-report

Here are links to differential privacy information:
- SmartNoise: https://smartnoise.org, https://github.com/opendifferentialprivacy/smartnoise-core-python, https://github.com/opendifferentialprivacy/smartnoise-sdk 
- OpenDP: https://projects.iq.harvard.edu/opendp and https://github.com/opendifferentialprivacy
- OpenDP.Accuracy: Pitfalls and edge cases. https://github.com/opendifferentialprivacy/smartnoise-samples/blob/master/analysis/accuracy_pitfalls.ipynb
- OpenDP.Privacy preserving statistical release. https://github.com/opendifferentialprivacy/smartnoise-samples/blob/master/analysis/tutorial_mental_health_in_tech_survey.ipynb 


# Contributing

This project welcomes contributions and suggestions.  Most contributions require you to agree to a
Contributor License Agreement (CLA) declaring that you have the right to, and actually do, grant us
the rights to use your contribution. For details, visit https://cla.opensource.microsoft.com.

When you submit a pull request, a CLA bot will automatically determine whether you need to provide
a CLA and decorate the PR appropriately (e.g., status check, comment). Simply follow the instructions
provided by the bot. You will only need to do this once across all repos using our CLA.

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or
contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.

The data in the broadband_data.csv file is licensed under the Open Use of Data Agreement v1.0. Data sources include Microsoft’s Rural Broadband initiative and the Federal Communications Commission’s 2019 Broadband Deployment Report.