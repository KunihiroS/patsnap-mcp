# PatSnap MCP Server

This MCP server is designed to collect patent-related information from PatSnap's API for trend analysis and reporting. It is not intended for individual patent investigations. The server is based on the stdio protocol and can be integrated with other MCP tools.

## Features

- **get_patent_trends**: Analyze annual application and issued trends for patents using PatSnap's Application and Issued Trend API. Supports filtering by keywords, IPC classification, application/publication dates, and patent authority.
- Additional tools for patent technology trend investigation are planned, focusing on features classified under Technology Key Report.

## Setup

1. Clone the repository.
2. Install dependencies using `npm install`.
3. Run the server using `npm start`.

## Usage

- Use the provided tools to interact with PatSnap's API.
- Ensure you have valid API credentials for authentication.

## Configuration for MCP Host

To integrate this MCP server with your MCP Host, add the following configuration to your Host configuration file:

```json
{
  "mcpServers": {
    "patsnap-mcp": {
      "command": "npx",
      "args": ["-y", "patsnap-mcp"],
      "env": {
        "PATSNAP_CLIENT_ID": "your_patsnap_client_id_here",
        "PATSNAP_CLIENT_SECRET": "your_patsnap_client_secret_here"
      },
      "disabled": false,
      "autoApprove": []
    }
  }
}
```

Ensure you replace `your_patsnap_client_id_here` and `your_patsnap_client_secret_here` with your actual PatSnap API credentials. This configuration will enable the PatSnap MCP Server to run with the necessary credentials using `npx` for invocation.

## License

This project is licensed under the MIT License.
