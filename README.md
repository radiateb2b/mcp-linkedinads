# mcp-linkedinads
Analyse your LinkedIn Ads performance. Compare to benchmarks and get optimisation recommendations.


# Overview
A Model Context Protocol (MCP) server implementation that provides integration with LinkedIn Ads. This server enables AI models to interact with your LinkedIn Ads data to:

- Campaign Analysis
- Creative Analysis 
- Analyse Companies engaging with your campaigns 
- Benchmark 
- Request recommendations for improving your campaigns. 

For more information about the Model Context Protocol and how it works, see Anthropic's [MCP documentation](https://www.anthropic.com/news/model-context-protocol).

# Example Prompts
- How do my LinkedIn Ad campaigns compare to benchmarks for the past 90 days?
- Which LinkedIn Ad campaigns are performing best?
- How do my LinkedIn Ad campaigns compare this week compared to last week?
- Can you analyse the performance of my LinkedIn Ad campaigns for the past 3 quarters and make recommendations.

# Setup
## Prerequisites
### Install node and npm.
Download Node and NPM [here](https://nodejs.org/en/download).

You'll need a Radiate B2B private access token for each LinkedIn Ads account. You can get started and also obtain your private access token by completing the form [here](https://radiateb2b.com/linkedin-ads-mcp-server/).  

Note: Keep your access token secure and never commit it to version control.

# Using the MCP Server
## Claude Desktop
Download Claude Desktop [here](https://claude.ai/download).
Make sure it’s on the latest version by clicking on the Claude menu on your computer and selecting “Check for Updates…”

To set up Claude Desktop, complete the following instructions:
- Open the Claude menu on your computer and select “Settings…”. Please note that these are not the Claude Account Settings found in the app window itself.
- Click on “Developer” in the left-hand bar of the Settings pane, and then click on “Edit Config”
- This will create a configuration file if you don’t already have one at:

`macOS: ~/Library/Application Support/Claude/claude_desktop_config.json`  
`Windows: %APPDATA%\Claude\claude_desktop_config.json`

- Open up the configuration file in any text editor. Replace the file contents with this:
```
{
    "mcpServers": {
      "RadiateB2B LinkedIn Advertising": {
        "command": "npx",
        "args": [
          "mcp-remote",
          "https://mcp.radiateb2b.com/sse",
          "--header",
          "Authorization: Bearer <your private access token>"
        ]
      }
    }
}
```

- Restart Claude Desktop
- Visit [this page](https://radiate-b2b.gitbook.io/docs/integrations/claude-desktop-and-mcp-server-for-linkedin-ads) for more information and troubleshooting.

# Terms and Conditions
The Radiate B2B LinkedIn Ads MCP Server is in beta and subject to our [terms](https://radiateb2b.com/terms).

# Links
Official Website: https://radiateb2b.com



