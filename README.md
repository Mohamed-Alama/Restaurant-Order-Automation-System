# Restaurant Order Automation (n8n)

A fully automated workflow designed using n8n to manage customer orders for a restaurant via Telegram, with automatic data logging into Google Sheets.
Features

    AI Agent: Uses language models (via OpenRouter) to understand customer orders in Egyptian colloquial Arabic.

    Conversation Management: Maintains the order context and avoids repeating greetings.

    System State: Precise tracking of order stages:

        Collecting food items.

        Requesting phone numbers.

        Requesting delivery locations.

        Final order confirmation.

    Google Sheets Integration: Saves customer data and order details directly into a spreadsheet.

    Image Support: Automatically sends the restaurant menu images to customers.

Technical Requirements

To run this workflow, you will need:

    An n8n instance (self-hosted or cloud).

    A Telegram Bot Token (obtained via BotFather).

    Google Sheets API Credentials for data access.

    An API Key for OpenRouter (or your preferred AI service provider).

Workflow Architecture

The project consists of the following nodes:

    Telegram Trigger: Receives messages and locations from customers.

    Telegram Trigger: Receives New Menu from manager.

    AI Agent & Memory: Manages the conversation and remembers order details.

    Structured Output Parser: Ensures data extraction in a precise JSON format.

    Python Code Node: Processes text and extracts the required data.

    Google Sheets Node: Appends data to the final sheet.

Setup Instructions

    Download the JSON file for the workflow.

    Open your n8n application.

    Create a new workflow and select Import from File.

    Configure the credentials for Telegram, Google Sheets, and OpenRouter.

    Ensure you update the Document ID for the Google Sheets node to link it to your own file.

    Activate the workflow and enjoy managing orders.

License

This project is open source under the MIT License.

Do you need help with setting up the specific environment variables or configuring the Telegram Webhook for this workflow?
