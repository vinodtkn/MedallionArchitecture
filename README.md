# MedallionArchitecture
Medallion architecture is a data design pattern used to logically organize data in a lakehouse, with the goal of incrementally and progressively improving the structure and quality of data as it flows through each layer of the architecture. Medallion architectures are sometimes also referred to as "multi-hop" architectures.
The medallion architecture consists of three distinct layers:

1. **Bronze layer:** The bronze layer contains raw data as it is ingested from source systems. This data is typically unprocessed and unvalidated.
2. **Silver layer:** The silver layer contains processed and validated data. The data in the silver layer is typically structured and ready for analysis.
3. **Gold layer:** The gold layer contains enriched data that is optimized for specific business needs. The data in the gold layer is typically aggregated and denormalized.

![bronze-silver-gold](https://github.com/vinodtkn/MedallionArchitecture/assets/82138543/fb2e7768-7c89-4947-930d-7a5d91afecb7)

Data flows through the medallion architecture in a linear fashion, from bronze to silver to gold. At each layer, the data is processed and transformed to improve its quality and usability.
The bronze layer is the simplest layer in the medallion architecture. It is simply a storage layer for raw data. The data in the bronze layer is typically stored in a data lake, such as Amazon S3 or Google Cloud Storage.

The silver layer is where data processing and validation takes place. The data in the silver layer is typically cleansed, standardized, and transformed into a common format. The silver layer is also where data quality checks are performed to ensure that the data is accurate and complete.

The gold layer is where data is enriched and optimized for specific business needs. The data in the gold layer is typically aggregated and denormalized to make it easier to query and analyze. The gold layer is also where data is modeled to support specific business use cases.

The medallion architecture has a number of benefits, including:
1. Improved data quality: The medallion architecture provides a systematic approach to improving the quality of data as it flows through the system.
2. Increased flexibility: The medallion architecture is flexible and can be adapted to meet the specific needs of different businesses.
3. Reduced costs: The medallion architecture can help to reduce the cost of data storage and analysis by optimizing data for specific business needs.

However, the medallion architecture also has some drawbacks, including:
1. Increased complexity: The medallion architecture can be complex to implement and manage.
2. Increased storage costs: The medallion architecture can require more storage space than other data architectures, since each layer of the architecture contains a copy of the data.
3. Increased processing costs: The medallion architecture can require more processing power than other data architectures, since data must be processed and transformed multiple times as it flows through the system.

Overall, the medallion architecture is a powerful and flexible data architecture that can be used to improve the quality, flexibility, and cost-effectiveness of data storage and analysis. However, it is important to carefully consider the benefits and drawbacks of the medallion architecture before implementing it.

# Sample Project

I have added a sample project here, it has a simple  demonstration of Medallion architecture. The project has 3 jupyter files, 1 for each layer. The programming language used is python. The project is executed in Databricks environment, wherein I have automated the execution of all 3 transformation layers using Databricks Workflows. 

**Project Name:** Heka (ancient Egyptian God associated with health and wellness)

**Summary:** The unrivaled threat of android malware is the root cause of various security problems on the internet. Android malware industry is becoming increasingly disruptive with almost 12,000 new android malware instances every day. Detecting android malware in smartphones is an essential target for cyber community to get rid of menacing malware samples.

Android malware is one of the most serious threats on the internet which has witnessed an unprecedented upsurge in recent years. It is an open challenge for cybersecurity experts. There are many techniques available to identify and classify android malware based on machine learning, but recently, deep learning has emerged as a prominent classification method for such samples.

This research work proposes a new comprehensive and huge android malware dataset, named CCCS-CIC-AndMal-2020. The dataset includes 200K benign and 200K malware samples totalling to 400K android apps with 14 prominent malware categories and 191 eminent malware families.

**Impact:** We are trying to project the statistics on the impact of malware on our mobile phones. Specifically we are going to come up with:

1. The most affecting malware for mobile phone
2. The most affected aspect of the mobile phone (sensitive data collection, media, hardware, actions/activities, internet connection, C&C, antivirus and storage & settings)

PS: I wouldnt have implemented the whole impact scenarios, you are free to improvise the code from where i have left :)

# Dataset

https://www.unb.ca/cic/datasets/andmal2020.html (scroll to the end of the page - check for "Download the dataset" button") 

# References

**Workflow setup in databricks:** https://docs.databricks.com/en/workflows/index.html
