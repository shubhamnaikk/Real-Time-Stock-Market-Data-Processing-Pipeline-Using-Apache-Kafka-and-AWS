# Real-Time Stock Market Data Processing Pipeline Using Apache Kafka and AWS

## Project Overview
This project demonstrates the implementation of a real-time stock market data processing pipeline. Leveraging Apache Kafka and AWS services, the pipeline covers data simulation, streaming, distributed storage, and real-time querying capabilities.

## Table of Contents
- [Project Overview](#project-overview)
- [System Architecture](#system-architecture)
- [Project Structure](#project-structure)
- [How to Run](#how-to-run)
- [Results](#results)
- [Future Enhancements](#future-enhancements)
- [Demo Video](#demo-video)

## System Architecture
The architecture consists of the following components:
1. **Data Simulation**: Simulates stock market events using Python.
2. **Apache Kafka**: Manages data streaming between producers and consumers.
3. **Amazon S3**: Stores streamed data in a scalable manner.
4. **AWS Glue**: Crawls the data and catalogs the schema.
5. **Amazon Athena**: Enables querying of data using SQL.

![System Architecture](./Architecture.jpg)

## Project Structure
```
Project-Real-Time-Stock-Market
│
├── Architecture.jpg          # System architecture image
│
├── Data                      # Folder containing datasets
│   └── indexProcessed.csv    # Preprocessed stock market data
│
├── Notebook                  # Folder for Jupyter notebooks
│   ├── KafkaProducer.ipynb   # Notebook for Kafka producer implementation
│   ├── KafkaConsumer.ipynb   # Notebook for Kafka consumer implementation
│
├── Outputs                   # Folder for output files
│   ├── outputs.pdf           # PDF showing results
│   ├── Real time Processing data.mp4 # Video demonstrating real-time processing
│
├── Report                    # Folder for the project report
│   └── reportstockmarket.pdf # Final project report in PDF format
│
└── README.md                 # Project documentation file
```

## How to Run
### Prerequisites
1. Install [Apache Kafka](https://kafka.apache.org/).
2. Configure AWS CLI with access to S3, Glue, and Athena.
3. Install required Python libraries:
   ```bash
   pip install pandas kafka-python s3fs boto3
   ```

### Steps
1. **Run Kafka Producer**:
   - Navigate to the `Notebook` folder.
   - Open `KafkaProducer.ipynb` and execute the notebook.
2. **Run Kafka Consumer**:
   - Open `KafkaConsumer.ipynb` in the same folder and execute it to stream data to S3.
3. **Set up AWS Glue**:
   - Use the Glue crawler to catalog the streamed data.
4. **Query Data in Athena**:
   - Query the cataloged data in Athena using SQL.

## Results
- The pipeline streams real-time stock data, stores it in S3, and makes it queryable via Athena.
- Sample outputs and a video demonstration are available in the `Outputs` folder.

## Future Enhancements
1. Integrate machine learning models for stock price prediction.
2. Add support for other data sources such as IoT sensors.
3. Improve fault tolerance and scalability of the pipeline.

## Demo Video
Below is a demo video of the real-time stock market data processing pipeline:

<video width="640" height="360" controls autoplay loop>
    <source src="./Outputs/Real%20time%20Processing%20data.mp4" type="video/mp4">
    Your browser does not support the video tag.
</video>

---

For more details, refer to the [project report](./Report/reportstockmarket.pdf).
