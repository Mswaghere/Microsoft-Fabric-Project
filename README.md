# Microsoft-Fabric-Project (Bing API - Azure Data Factory - Microsoft Fabric)

## Flow Of A Project
![Microsoft Fabric Flow](https://github.com/user-attachments/assets/bf9496de-32ba-420f-b9be-44ea1e190cee)

## Step-By-Step Process

### Step 1: Set Up Azure Resources 
Created Azure Resources: Setting up an Azure resource group. Created a Bing Search v7 resource to access the Bing API.
Setting Up Microsoft Fabric account: Accessed Microsoft Fabric, which includes Data Factory, OneLake, and Synapse services.

### Step 2: Ingest Data from Bing API
Created a Data Factory Pipeline: In Microsoft Fabric, navigate to Azure Data Factory. Created a new pipeline for data ingestion.
Configure the Bing API Connector: Used the HTTP connector in Azure Data Factory to connect to the Bing Search v7 API. Set up the necessary authentication to access the API.
Define the Data Flow: Used the Copy Data activity to retrieve data from the Bing API and store it as a JSON file in OneLake.
![Data Ingestion (Microsoft Fabric)](https://github.com/user-attachments/assets/509f7055-3ff3-4829-81e4-68a735c15b09)


### Step 3: Transform JSON Data Using Synapse Data Engineering
Open Azure Synapse Analytics: Navigate to Synapse workspace within Microsoft Fabric.
Create a Data Flow: Used Synapse Data Engineering to create a new data flow that reads the JSON data from OneLake.
Transform the Data: PySpark was used to convert the JSON data into a structured format (e.g., DataFrame). Wrote transformations to clean and structure the data as needed.

### Step 4: Perform Sentiment Analysis
Use Synapse Data Science: In Synapse workspace, navigate to the Data Science section.
Create a New Notebook: Setting up a new notebook to perform sentiment analysis on the structured data.
Implement Sentiment Analysis: Used various libraries within the notebook to analyze the sentiment of the textual data.
![Data Pipeline (Microsoft Fabric)](https://github.com/user-attachments/assets/6d4a4391-a7fc-4277-95e8-f8047f84f089)

## Summary of Project Flow

1. Data Ingestion: Bing API → Azure Data Factory → OneLake (as JSON)
2. Data Transformation: OneLake (JSON) → Synapse Data Engineering (structured format)
3. Sentiment Analysis: Structured Data → Synapse Data Science (sentiment analysis)
