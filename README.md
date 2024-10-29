
# 🚗 EV Insights - Multi-Source Data Analytics for the Electric Vehicle Industry

## Overview

EV Insights is a serverless data analytics project that integrates multiple data sources to provide actionable insights for the electric vehicle (EV) industry. This project utilizes AWS Step Functions to build a flexible, long-running ELT pipeline that analyzes market data, social media, search analytics, and internal ERP systems.
Table of Contents

- [Architecture Overview](#architecture-overview)
- [Project Structure](#project-structure)
- [Prerequisites](#prerequisites)
- [Setup Instructions](#setup-instructions)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Architecture Overview

EV Insights integrates the following data sources:

    + Market data: EV sales, pricing, and market trends from sources like EV-Volumes and BloombergNEF
    + Social media: Twitter, Facebook, and Instagram data on EV-related conversations and sentiment analysis
    + Search analytics: Google Trends and keyword analysis for EV-related searches
    + Internal ERP systems: Sales, inventory, and supply chain data from EV manufacturers

The project uses the following AWS services:

   + AWS Step Functions for building the ELT pipeline
   + AWS Glue for data processing and transformation
   + Amazon S3 for data storage
   + Amazon Redshift for data warehousing
   + Amazon QuickSight for data visualization
   + AWS Lambda for serverless computing

## Project Structure

```
ev-insights/
├── data/
│   ├── market_data/
│   ├── social_media/
│   ├── search_analytics/
│   └── erp_data/
├── src/
│   ├── step_functions/
│   │   ├── market_data_etl.py
│   │   ├── social_media_etl.py
│   │   ├── search_analytics_etl.py
│   │   └── erp_etl.py
│   ├── glue_jobs/
│   │   ├── market_data_glue.py
│   │   ├── social_media_glue.py
│   │   ├── search_analytics_glue.py
│   │   └── erp_glue.py
│   ├── lambda_functions/
│   │   ├── market_data_lambda.py
│   │   ├── social_media_lambda.py
│   │   ├── search_analytics_lambda.py
│   │   └── erp_lambda.py
│   └── quicksight/
│       └── dashboard.json
├── tests/
├── docs/
├── config/
├── requirements.txt
├── setup.py
└── README.md
```

## Prerequisites

   + AWS Account with appropriate permissions
   + Python 3.8+
   + AWS CLI configured
   + AWS Step Functions, Glue, S3, Redshift, QuickSight, and Lambda

## Setup Instructions

1. Clone the repository: git clone https://github.com/your-username/ev-insights.git
2. Set up a virtual environment: python -m venv venv and source venv/bin/activate
3. Install dependencies: pip install -r requirements.txt
4. Configure AWS services:
    -    Set up S3 buckets for data storage
    -    Configure Glue for data processing
    -    Set up Redshift for data warehousing
    -    Configure QuickSight for data visualization
    -    Set up Lambda functions
    -    Configure Step Functions
5. Update the config/ directory with your AWS resource configurations.

## Usage

   + Run the Step Functions pipeline to extract, transform, and load data.
   + Analyze data using QuickSight dashboards.
   + Use insights to inform business decisions.

## Contributing

We welcome contributions to improve EV Insights. Please follow these steps:

-  Fork the repository
-  Create a new branch (git checkout -b feature/your-feature)
-  Make your changes
-  Commit your changes (git commit -am 'Add some feature')
-  Push to the branch (git push origin feature/your-feature)
-  Create a new Pull Request

## License

This project is licensed under the Apache 2.0 License - see the [LICENSE](LICENSE) file for details.
