# T1
DocAnalysis1
1. blob storage - storage account
2. need to choose the region- resource should be chosen in the region based on the version we intend to use
3. there is a document page which shows which specific model to choose, based on the documnet typr and the data you need to extract
4. the free version has document size limit and page limit for analysis. if text file exceed 4MB in size or has more than two pages, we will not be able to use th efree resource version
5. the pricing of the service is based on the model you use and the number of pages to be processed
6. As we will not be using multiple azure services like, speech, language, vision, we will not use multi-services resource. we will create a dedicated azure document intelligent resource- separate billing and cost
7. deciding wheather to choose Azure Vision with its OCR feature or Azure Document Intelligence, if we want to get just words and text from the image without contextual information. document intelligence provide key-value pairs, tables and contact-specific fields. for huge amount of text, use azure document intelligence and we want meaning from that data
8. we will choose Azure document intelligence studio as it has features like : 1. shows the capabilities of each model available, 2. allows you to test models on sample documents, from your own uploaded documents and URLs. 3. we can experiment with different add-ons settings and preview features to adapt the output to your needs. 4. we can train custom classification models to classify documents 5. it allows to train custom extraction models to extarct fields from custom documents 6. it will rpovide sample JSON outputs and sample code for Python to integrate into your applications 
Azure document intelligence provides you with a SDK and APIs that allow to create apps
need to decide which SDK version is to be used as the functionalities depends on the version we chose
GitHub Free for personal accounts	15 GB-month	120 hrs
