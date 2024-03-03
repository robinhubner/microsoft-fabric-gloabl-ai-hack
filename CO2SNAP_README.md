
# CO2SNAP Application README

## Overview

CO2SNAP is an innovative application designed to assess and provide insights into the carbon footprint of grocery shopping. It utilizes a robust architecture integrating various technologies and services to capture, store, process, and analyze images of shopping receipts to estimate the CO2 emissions associated with purchased items.

## Architecture

The application workflow is as follows:

1. **Image Capture**: Users can take pictures of their shopping receipts using the MS PowerApps mobile application.
2. **Data Storage**: The images are then stored securely in DataVerse.
3. **Pipeline Orchestration**: A medallion lakehouse architecture orchestrates the data flow.
4. **Image Analysis**: Images are analyzed using a Vision API.
5. **Data Enrichment**: The results are enriched with CO2 information and stored in a dataframe.
6. **Knowledge Base**: The application crawls and indexes CO2 information and handles queries.
7. **Advanced Analysis**: Pictures are analyzed and data is enriched and streamlined using GPT-4's vision capabilities.
8. **Semantic Modeling**: A semantic model is created for better understanding and interaction.
9. **Reporting**: An interactive report is generated for the user.

## Technologies

- **Microsoft PowerApps**: For capturing images on mobile devices.
- **DataVerse**: For secure storage and management of images and data.

## Fabric Workspace

The application leverages a Fabric Workspace consisting of environments, lakehouses, semantic models, SQL endpoints, notebooks, reports, data pipelines, and warehouses managed and maintained by Robin Huebner.

Details of the workspace components are as follows:

- Environments (`fabric_hackathon_env`) for app development and testing.
- Lakehouse structures (`lh_gold`, `lh_silver`) for data storage and processing at various stages of refinement.
- Semantic models (`sm_groceries_emissions`) for data interpretation and analysis.
- SQL analysis endpoints for running complex queries on the lakehouse data.
- Notebooks (`nb_bronze_to_silver`, `nb_silver_to_gold`) for data transformation and analysis scripts.
- Reports (`pbi_co2snap`) for visualizing insights.
- Data pipelines (`pl_orchestration_new_picture_*`) for automating the data flow from capture to analysis.
- Warehouse (`wh_master_data`) for comprehensive data storage.

## Installation

To set up the CO2SNAP application, follow these steps:

1. Clone the repository to your local machine.
2. Ensure that you have access to Microsoft PowerApps and DataVerse.
3. Set up the required environments and lakehouse structures as per the workspace configuration.
4. Deploy the semantic models and SQL analysis endpoints.
5. Run the notebooks to set up data transformation processes.
6. Schedule the data pipelines for regular data flow.
7. Configure the reporting tool with the `pbi_co2snap` report for visualization.

## Usage

To use the CO2SNAP application:

1. Open the MS PowerApps application on your mobile device.
2. Take a picture of your shopping receipt.
3. Submit the picture, which will then be processed by the application.
4. Access the interactive report to view your personal CO2 footprint based on your grocery shopping.

## Contributing

Contributions to CO2SNAP are welcome. Please read the CONTRIBUTING.md file for details on our code of conduct, and the process for submitting pull requests to us.

## Authors

- Robin Huebner - Initial work and ongoing maintenance.
- Luca Pankratz - Initial work and ongoing maintenance.
- Daniel Obermann - Initial work and ongoing maintenance.

---
