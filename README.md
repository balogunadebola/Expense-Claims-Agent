# Expense Agent

A Python-based expense processing application that uses Azure AI and Semantic Kernel to automate expense claim submissions.

## Description

This application provides an AI-powered interface for processing expense claims. It reads expense data from a file and uses an Azure AI agent to analyze and process the data, automatically sending formatted expense claim emails.

## Features

- Reads expense data from a text file
- Uses Azure AI for intelligent expense processing
- Automatically formats and sends expense claim emails
- Built with Semantic Kernel for AI agent orchestration

## Prerequisites

- Python 3.x
- Azure subscription with appropriate permissions
- Azure AI services configured

## Required Packages

```
python-dotenv
azure-identity
semantic-kernel
```

## Setup

1. Clone this repository
2. Create a `.env` file in the root directory with your Azure configuration:
   ```
   AZURE_OPENAI_DEPLOYMENT_NAME=your_deployment_name
   AZURE_OPENAI_ENDPOINT=your_endpoint
   AZURE_OPENAI_API_KEY=your_api_key
   ```
3. Install the required packages:
   ```
   pip install python-dotenv azure-identity semantic-kernel
   ```

## Usage

1. Place your expense data in `data.txt`
2. Run the application:
   ```
   python semantic-kernel.py
   ```
3. Follow the prompts to process your expense data
4. The application will generate and send an expense claim email automatically

## Project Structure

- `semantic-kernel.py`: Main application file containing the AI agent and email processing logic
- `data.txt`: Input file for expense data
- `.env`: Configuration file for Azure credentials (not included in repository)

## How It Works

1. The application loads expense data from `data.txt`
2. It creates an Azure AI agent with specific instructions for handling expense claims
3. The agent processes the data and generates a formatted expense report
4. The EmailPlugin simulates sending the expense claim via email
5. All resources are properly cleaned up after processing

## Security Notes

- Azure credentials are handled securely using environment variables
- The application uses Azure DefaultAzureCredential for authentication
- Sensitive data should be properly secured in the `.env` file