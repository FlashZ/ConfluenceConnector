# Confluence Cloud REST API v2 for Microsoft Custom Connectors

- [Introduction](#introduction)
- [Features](#features)
- [Authentication](#authentication)
- [Getting Started](#gettingstarted)
- [Installation](#installation)
- [Usage](#usage)
- [Pagination](#pagination)
- [Resources](#resources)
- [License](#license)


## Introduction
The Confluence Cloud REST API v2 for Microsoft Custom Connectors is a tailored version of Atlassian's Confluence Cloud REST API, optimized for use within Microsoft PowerApps as a custom connector. This version enhances endpoint definitions and performance, ensuring seamless integration and efficient operations within the Microsoft ecosystem.

This custom connector utilizes Basic Authentication with an Atlassian ID and API token, providing secure access at the user level.

## Features
- Comprehensive API Coverage: Access a wide range of Confluence Cloud functionalities.
- Optimized for PowerApps: Seamlessly integrate with Microsoft PowerApps through custom connectors.
- Secure Authentication: Utilizes Basic Authentication with Atlassian credentials.

## Authentication

This custom connector uses Basic Authentication. You will need your Atlassian ID and an API token to generate the necessary credentials.

### Generating the API Token
1. Navigate to Atlassian API Tokens.
2. Click on Create API token.
3. Enter a label and click Create.
4. Copy the generated token and store it securely.

### Creating the Basic Auth Token

Combine your Atlassian ID and API token in the following format:

```
<Atlassian_ID>:<API_Token>
``` 
Encode this string in Base64. 

This encoded string will be used in the Authorization header of your API requests.

For detailed instructions, refer to [Basic auth for REST APIs.](https://developer.atlassian.com/cloud/confluence/basic-auth-for-rest-apis/) 

## Getting Started
### Prerequisites
**Microsoft PowerApps Account:** Ensure you have access to a Microsoft PowerApps environment and sufficient maker permissions.

**Atlassian Confluence Account:** Access to a Confluence **Cloud** instance with appropriate permissions.

**API Token:** As described in the Authentication section.

## Installation

### Importing the Custom Connector

1. Download the Swagger File.
2. Save the provided Swagger JSON to your local machine as confluence-api-swagger.json.
4. Log in to PowerAutomate.
5. Navigate to Data > Custom connectors.
6. Click on New custom connector and select Import an OpenAPI file.
7. Upload the Swagger File
8. Provide a name for your connector, e.g., ConfluenceCloudAPI.
9. Upload the confluence-api-swagger.json file.
10. Click Continue.
11. Configure Security:

   - In the Security tab, select API key.
   - Set the Parameter label to Authorization.
   - Ensure the Parameter name is Authorization and Location is Header.
   - Click Update connector.

12. Test the Connector:

   - Navigate to the Test tab.
   - Create a new connection by providing your Base64 encoded Authorization header.
   - Test an endpoint to ensure connectivity.

## Usage
Once the custom connector is imported and configured, you can utilize it within your PowerApps applications to interact with your Confluence Cloud instance. This includes operations such as retrieving attachments, managing pages, handling comments, and more.

Example: **<TBC>**

## Pagination
The Confluence REST API v2 employs cursor-based pagination to manage large datasets efficiently. When an endpoint returns multiple objects, use the limit and cursor parameters to control the number of results and navigate through pages.


## Resources
- Atlassian Developer Documentation
- Basic Authentication Guide
- PowerApps Custom Connectors

## License
[MIT](https://choosealicense.com/licenses/mit/)