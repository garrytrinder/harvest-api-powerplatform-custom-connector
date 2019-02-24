# Harvest API PowerPlatform Custom Connector

A PowerPlatform Custom Connector that securely connects to Harvest API using OAuth authentication.

## Actions

- List time entries

## Installation

#### Import JSON file to create Custom connector

- Sign-in to Microsoft Flow
- Expand the Data menu and go to Custom connectors
- Click Create custom connector and choose Import an OpenAPI from URL
- Enter the below into the prompt
  - Name: Harvest API
  - URL: https://raw.githubusercontent.com/garrytrinder/harvest-api-powerplatform-custom-connector/master/Harvest-API.swagger.json
- Click Import and then Continue
- From the General screen, move to the Security screen 

#### Create OAuth2 Application in Harvest

- Open a new tab and sign-in to Harvest
- Go to https://id.getharvest.com/developers
- Click Create New OAuth2 Application button
- Enter the below into the form
  - Name: Harvest API Custom Connector
  - Redirect URL: https://localhost (we will change this later)
- Click Create Application
- Take note the Client ID and Client Secret on the next screen

#### Update Custom Connector Security details

- Go back to the Security screen for the Custom Connector
- Enter the Client ID and Client Secret values from the Harvest OAuth 2 application
- Copy the value from the Token URL field into the Refresh URL field
- Click Create Connector to generate the Redirect URL in the Security section

#### Update Harvest OAuth2 application Redirect URL

- Copy the Redirect URL and go back to the Harvest OAuth2 application screen
- Enter the generated Redirect URL, replacing https://localhost in the Application Setting screen
- Click Update Application to update the setting

#### Test OAuth2 Connection

- Go back to the Custom connector and move to the Test section
- Click New Connection
- Click Authorize App button to create a connection

#### Obtain Harvest Account ID

- Go to https://id.getharvest.com/developers
- Click Create New Personal Access Token i.e. TEST
- Enter a name for the Token and click Create Personal Access Token
- Take note of the Harvest Account ID on the following screen
- Click Revoke Token as it it not required

## Flow Usage

![Flow](/HarvestAPIPowerPlatformCustomConnector.png)
