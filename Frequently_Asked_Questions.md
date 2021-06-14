# Broadband Usage Percentages Dataset Frequently Asked Questions

- Why did Microsoft make this data available?
    -  We are publishing datasets we developed as part of our efforts with Microsoft’s Airband Initiative to help close the rural broadband gap. The data can be used for the purpose of analyzing, understanding, improving, or addressing problems related to broadband access.

- Where does the usage data come from?
    - The datasets consist of data derived from anonymized data Microsoft collects as part of our ongoing work to improve the performance and security of our software and services.
    - The data does not include any PII information including IP Address.
    - We also suppress any location with less than 20 devices. Other than the aggregated data shared in the data table, no other data is stored during this process. 

- How is usage calculated?
    - We estimate broadband usage by combining data from multiple Microsoft services.
    - Every time a device receives an update or connects to a Microsoft service, we can estimate the throughput speed of a machine. We know the size of the package sent to the computer, and we know the total time of the download.
    - The data from these services are combined with the number of households per county and zip code.
    - We also determine zip code level location data via reverse IP. Therefore, we can count the number of devices that have connected to the internet at broadband speed per each zip code based on the FCC’s definition of broadband that is 25mbps per download.

- How do we ensure privacy in the data shared?
    - Given the zip code-level dataset provides a more granular view of broadband usage percentages by households, we took the additional step to ensure data privacy guarantees by utilizing differential privacy, a technique that adds noise to the data aggregations, preventing leakage about the presence of specific individuals in the dataset.
    - We implemented differential privacy through the SmartNoise platform, a first-of-its-kind open source platform for differential privacy co-developed by Microsoft and the OpenDP initiative led by Harvard. 
    - As Differential Privacy adds noise to protect privacy, the noise added to zip codes with a small number of households can impact utility. To ensure transparency into how zip codes with different population magnitudes are affected, we have included error range data.

