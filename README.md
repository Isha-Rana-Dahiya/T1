# T1
work flow
received the filled survey form >> submitted forms will be stored in Azure Blob Storage >> use azure logic apps or azure functions to trigger analysis whenever a new form is submitted >> analyze the form with analyze the form >> sum the scores using python script >> send scores via email >> save the extracted so
DocAnalysis1
1. blob storage - storage account
2. need to choose the region- resource should be chosen in the region based on the version we intend to use
3. there is a document page which shows which specific model to choose, based on the documnet typr and the data you need to extract
4. the free version has document size limit and page limit for analysis. if text file exceed 4MB in size or has more than two pages, we will not be able to use the free resource version
5. the pricing of the service is based on the model you use and the number of pages to be processed
6. As we will not be using multiple azure services like, speech, language, vision, we will not use multi-services resource. we will create a dedicated azure document intelligent resource- separate billing and cost
7. deciding wheather to choose Azure Vision with its OCR feature or Azure Document Intelligence, if we want to get just words and text from the image without contextual information. document intelligence provide key-value pairs, tables and contact-specific fields. for huge amount of text, use azure document intelligence and we want meaning from that data
8. we will choose Azure document intelligence studio as it has features like : 1. shows the capabilities of each model available, 2. allows you to test models on sample documents, from your own uploaded documents and URLs. 3. we can experiment with different add-ons settings and preview features to adapt the output to your needs. 4. we can train custom classification models to classify documents 5. it allows to train custom extraction models to extarct fields from custom documents 6. it will rpovide sample JSON outputs and sample code for Python to integrate into your applications 
Azure document intelligence provides you with a SDK and APIs that allow to create apps
need to decide which SDK version is to be used as the functionalities depends on the version we chose
GitHub Free for personal accounts	15 GB-month	120 hrs
Creating a .env file and adding it to .gitignore ensures that sensitive information like the endpoint and key are not shared publicly.
**Azure Document Intelligence can be run in a container, allowing deployment on edge-devices or on-premises.**
Read model - extract printed or written text lines, words, locations, and detected languages
Layout model if we need to extract structural information like tables, selection marks, paragraphs, titles, headings, and subheadings.
Read and Layout model can have 4MB for free tier
2000 pages per file for paid tier, 500 MB for paid tier
   2 pages for free tier - 4MB
   Password pdf cannot be processed
   Layout has all the read model capabilities
   We get the JSON code using document analyser in layout model. We can use this code or API if you want to use this service for our application
   we can use Postman to get the results via API
   (refer to azure document intelligence REST API documentation to get the specifications of the API.
   we have two methods to use document intelligence, POST and GET. postanalyzedocument POST method, and get analyze result method() to get your results
   Step 1: we assign the endpoint, api key and model ID as environment variables in Postman

   
