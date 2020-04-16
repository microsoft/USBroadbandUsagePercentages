# United States Broadband Usage Percentages Dataset

Amit Misra, Allen Kim, John Kahan, Juan M. Lavista Ferres

Microsoft Introduction and Purpose
We are publishing this dataset we developed as part of our efforts with Microsoft’s Airband Initiative to help close the rural broadband gap. The data is to be used for the purpose of analyzing, understanding, improving, or addressing problems related to broadband access.  
It consists of data derived from anonymized data Microsoft collects as part of our ongoing work to improve the performance and security of our software and services. The data does not include any PII information including IP Address.  We also suppress any location with less than 20 devices. Other than the aggregated data shared in this data table, no other data is stored during this process.  We estimate broadband usage by combining data from multiple Microsoft services. The data from these services are combined with the number of households per county and zip code[1]. Every time a device receives an update or connects to a Microsoft service, we can estimate the throughput speed of a machine. We know the size of the package sent to the computer, and we know the total time of the download.  We also determine zip-code level location data via reverse IP. Therefore, we can count the number of devices that have connected to the internet at broadband speed per each zip code based on the FCC’s definition of broadband that is 25mbps per download[2]. Using this method, we estimate that ~157 million people in the United States are not using the internet at broadband speeds.

Background
Every day our world becomes a little more digital. But reaping the benefits of this digital world – pursuing new educational opportunities through distance learning, feeding the world through precision agriculture, growing a small business by leveraging the cloud, and accessing better healthcare through telemedicine – is only possible for those with a broadband connection, which is especially apparent now as more people are staying home due to the COVID-19 pandemic. Based on the 2019 Broadband Deployment Report from the Federal Communications Commission (FCC)[3], broadband is not available to at least 21 million people, 16 million of whom live in this country’s rural areas.
Getting these numbers right is vitally important. This data is used by federal, state, and local agencies to decide where to target public funds dedicated to closing this broadband gap. That means millions of Americans already lacking access to broadband have been made invisible, substantially decreasing the likelihood of additional broadband funding or much needed broadband service.  We are publishing this data today to allow others to use it to develop solutions to improving broadband access or addressing problems with broadband access.

![broadbandmap.png](/assets/broadbandmap.png)

 
Suggested data sets that can be used in combination with this data:
•	US county boundaries data set: https://catalog.data.gov/dataset/tiger-line-shapefile-2017-nation-u-s-current-county-and-equivalent-national-shapefile 
Here are links to additional broadband information:
•	Microsoft Rural Broadband link: https://news.microsoft.com/rural-broadband/
•	FCC Broadband link: https://www.fcc.gov/document/broadband-deployment-report-digital-divide-narrowing-substantially-0
•	FCC population estimates: https://www.fcc.gov/reports-research/data/staff-block-estimates

[1]	American Fact Finder https://data.census.gov/ and Office of Policy Development Research https://www.huduser.gov/portal/datasets/usps_crosswalk.html
[2]	“2018 Broadband Deployment Report | Federal Communications Commission.” https://www.fcc.gov/reports-research/reports/broadband-progress-reports/2018-broadband-deployment-report (accessed Apr. 15, 2020).
[3]	“2019 Broadband Deployment Report,” Federal Communications Commission, Jun. 11, 2019. https://www.fcc.gov/reports-research/reports/broadband-progress-reports/2019-broadband-deployment-report (accessed Apr. 15, 2020).



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
