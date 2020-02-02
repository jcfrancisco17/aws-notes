# Overview of Amazon Web Services (January 2020)

## Six Advantages of Cloud Computing

 - Trade capital expense for variable expense
 - Benefit from massives economies of scale
 - Stop guessing capacity
 - Increase speed and agility
 - Stop spending money running and maintaining data centers
 - Go global in minutes

 ## Types of Cloud Computing

 - Infrastructure as a Service (IaaS)
   - Basic buiding blocks
     - networking features 
     - computers (virtual or dedicated hardware)
     - data storage space
    - Provides highest level of flexibility and control over IT resources.
 - Platform as a Service (Paas)
   - Removes the need to manage the underlying infrastructure (hardware and OS)
   - Focus on deployment and management of applications
   - No need to worry about resource procurement, capacity planning, software maintenance, patching, etc.
 - Software as a Service (SaaS)
   - A complete product that is run and managed by the service provider.
   - An end-user application.
   - No need to think about how the service is maintained or how the underlying infrastructure is managed.
 
## Cloud Computing Deployment Models

- Cloud
  - Fully deployed in the cloud and all parts of the application run in the cloud.
  - Either created in the cloud or migrated to the cloud.
 - Hybrid
   - Cloud and existing on-premises infrastructure
 - On-premises
   - Same as legacy IT infrastructure but uses virtualization and resource management tools
   - Sought because of its ability to provide dedicated resources.

## Global Infrastructure

 - AWS Cloud Infrastructure
   - Built around AWS Regions and Availabililty Zones (AZ)
   - Currently over 60 AZs over 20 Regions
 - AWS Region
   - A physical location in the world
   - Designed to be completely isolated from other regions.
   - A Region has multiple AZs.
 - Availability Zone
   - Consists of one or more discrete data centers
   - Has redundant power, networking, and connectivity, housed in separate facilities.
   - AZs in a Region are connected through low-latency links.
   - Designed as an independent failure zone.
   - Redundantly connected to multiple tier-1 transit providers

## Security and Compliance

### Security

 - Cloud security at AWS is the higheset priority.
 - Much like on-premise security but without the cost of maintaining facilities and hardware.
 - Uses softwre-based security tools to monitor and protect the flow of information in and out of cloud resources.
 - AWS Cloud enables a shared responsibility model.
   - AWS manages security of the cloud
   - You are responsible for security in the cloud.

#### Benefits of AWS Security

 - Keep your data safe
   - All data is stored in highly secure AWS data centers.
 - Meet compliance requirements
   - Segments of your compliance have already been completed.
 - Save money
   - Maintain highest standard of security without managing your own facility.
 - Scale quickly
   - Security scale with AWS Cloud usage.

### Compliance

 - SOC 1/ISAE 3402, SOC 2, SOC 3
 - FISMA, DIACAP, and FedRAMP
 - PCI DSS Level 1
 - ISO 9001, ISO 27001, ISO 27017, ISO 27018

 ## Amazon Web Services Cloud Platform

 ### Analytics

 - Athena
   - Query and analyze data in S3 using SQL.
   - Serverless, only pay for queries run.
   - Most results are delivered within seconds.
   - No need for ETL jobs
   - Integrated with AWS Glue Data Catalog
     - Create unified metadata repository across various services
     - Crawl data sources to discover schemas and populcate Catalog with new and modified table and patition defintions
     - Maintain schema versioning
     - Transform or convert data into columnar format to optimize cost and improve performance.

  - EMR
    - Managed Hadoop framework
    - Easy, fast, and cost-effective service to process vast amounts of data across dynamically scalable EC2 instances
    - Also availbale in Spark, HBase, Presto, and Flink
    - Interact with AWS data stores such as S3 and DynamoDB
    - EMR Notebooks, based on Jupyter Notebook, provide dev and collaboration environment for ad hoc querying and exploratory analysis.
    - Handles big data use cases
      - log analysis
      - web indexing
      - ETL
      - machine learning
      - financial analysis
      - scientific simulation
      - bioinformatics

  - CloudSearch
    - Set up, manage, and scale a search solution for your website or app
    - Supports 34 languages, higlighting, autocomplete, and geospatial search

  - Elasticsearch
    - Log analytics, full-text search, application monitoring, and clickstream analytics
    - Integrates with Logstash and Kibana for data ingestion and visualization
    - Integrates with AWS services:
      - VPC
      - KMS
      - Kinesis Data Firehose
      - Lambda
      - IAM
      - Cognito
      - CloudWatch

  - Kinesis
    - Collect, process, and analyze real-time, streaming data
    - Process and analyze data as it arrives and respond instantly
    - Ingest video, audio, application logs, website clickstreams, and IoT telemetry data for machine learning, analytics, etc
    - Currenlty offers four services:
      - Kinesis Data Firehose
      - Kinesis Data Analytics
      - Kinesis Data Streams
      - Kinesis Video Streams

   - Kinesis Data Firehose
     - Easiest way to reliaby load streaming data into data stores and analytics tools.
     - Capture, transform, and load streaming data into
       - S3
       - Reshift
       - Elasticsearch
       - Splunk
     - Fully managed. Scales to match throughput of data
     - Can batch, compress, transform, and encrypt data before loading it at the destination.
     - Can configure delivery stream to convert incoming data to columnar formats like Apached Parquet and Apacher ORC before data is delivered to S3.

   - Kinesis Data Analytics
     - Easiest way to analyze streaming data, gain actionable insights, and respond to business and customer needs in real time.
     - Reduces complexity of building, managing, and integrating streaming applications with other AWS services.
     - Easily query streaming data using SQL or build entire streaming applications using templates and an interactive SQL editor
     - Has open source Java libraries
     - Scales automatically to match volume and throughput rate of incoming data

   - Kinesis Data Streams
     - Massively scalable real-time data streaming service.
     - Continuously caputre gigabytes of data per second from hundreds of thousands sources.
     - Data is availalable in milliseconds to enable real-time analytics.

   - Kinesis Video Streams
     - Securely stream video from connected devices to AWS for analytics, ML, playback, etc.
     - Automatically provisions and elastically scales all infrastructure.
     - Durably stores, encrypts, and indexes video data in streams.
     - Allows access to data through APIs.
     - Allows playback video for live and on-demand viewing
     - Integrates with Amazon Recognition Video for computer vision and video analytics.
     - Has libraries for ML like Apache MxNet, TensorFlow, and OpenCV.

