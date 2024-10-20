# ProjectIQ: Automated Documentation Generation with Azure OpenAI and Microsoft Fabric
## Introduction
Documentation is one of the most important but often tedious and time-consuming tasks. What if we could leverage Generative AI to simplify the process? ProjectIQ is an idea aimed at automating documentation by utilizing metadata from work items, tickets, bugs, and wikis to generate concise and relevant summaries for topics you're interested in. This project was made possible thanks to Microsoft Fabric and Azure OpenAI, which provided the tools to build a proof of concept (PoC).

## Overview
ProjectIQ uses Microsoft Fabric as the backbone for data storage and processing, and Azure OpenAI to analyze metadata and produce intelligent summaries. By integrating various work item types from Azure DevOps, such as tasks, bugs, and documentation, ProjectIQ can generate quick, meaningful summaries in a matter of seconds, saving hours of manual work.

## Key Features
- **Automated Summaries**: The system uses metadata from Azure DevOps and generates documentation based on user queries.
- **Seamless Integration with Microsoft Fabric**: ProjectIQ integrates with Microsoft Fabric's lakehouse to store and process data efficiently.
- **Azure OpenAI Integration**: Utilizes OpenAI’s generative models to understand work items and summarize documentation.
- **Fast and Scalable**: Generate insights in seconds, even for large projects.

## Files in this Project
**00-Libraries.ipynb**

This notebook handles the setup and imports necessary libraries, including configuration of Azure OpenAI and Spark environments in Microsoft Fabric.

**01-ProjectIQ_Application.ipynb**

The main logic of ProjectIQ is implemented here. It handles user queries, sends them to Azure OpenAI, retrieves relevant data from Microsoft Fabric, and generates summaries. The notebook demonstrates how various components work together to generate meaningful insights.

**configuration.ipynb**

This notebook contains the configuration settings for ProjectIQ, such as the connection details for Microsoft Fabric, authentication for Azure OpenAI, and other key parameters.
## How to Run
1. Setup Microsoft Fabric Environment
- Ensure you have access to Microsoft Fabric with the necessary lakehouse and compute resources enabled.
- Import the three notebooks in your workspace.
2. Configure OpenAI and Fabric
- In the configuration.ipynb file, input your OpenAI API keys and Microsoft Fabric credentials.
Run the Application
3. Start with 00-Libraries.ipynb to load the necessary dependencies.
- Proceed with 01-ProjectIQ_Application.ipynb to initiate the main application. This notebook allows you to input questions and receive real-time documentation summaries based on your Azure DevOps data.
4. Customization
- You can modify the queries or keywords based on your specific project needs.
- Adjust the parameters in configuration.ipynb as needed for different Azure DevOps projects or environments.
## Challenges Faced
Building ProjectIQ presented several challenges:

- Data Complexity: Parsing and understanding different work item types from Azure DevOps required a well-structured approach.
- Scalability: Processing large volumes of data quickly within Microsoft Fabric demanded optimization to ensure smooth performance.
- API Rate Limits: Managing Azure OpenAI API rate limits was a key concern, especially for generating high-quality summaries in real-time.

## Future Improvements
- Enhanced AI Models: Explore using more advanced models or fine-tuning to improve the accuracy of generated summaries.
- Real-Time Updates: Implementing real-time sync with Azure DevOps to fetch and summarize the latest work items automatically.
- User Interface: Developing a more user-friendly interface for non-technical users to interact with the system.

## Conclusion
ProjectIQ aims to bridge the gap between extensive metadata and human-readable documentation by leveraging the power of AI and cloud technologies. With this tool, creating comprehensive documentation becomes not only easier but faster, freeing up time for more critical tasks.
