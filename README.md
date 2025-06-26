# Aigeon AI Google Shopping API

## Project Description

The Aigeon AI Google Shopping API is a Python-based server application designed to facilitate seamless interaction with Google's Shopping API. This application allows users to perform detailed product searches on Google Shopping, leveraging various parameters to refine and tailor search results to specific needs. The server is built using the FastMCP framework, ensuring efficient and robust handling of search requests.

## Features Overview

- **Comprehensive Search Capabilities**: Execute Google Shopping searches with a wide range of customizable parameters.
- **Location and Language Customization**: Specify geographic and linguistic preferences to tailor search results.
- **Device-Specific Results**: Choose the device type for which the search results should be optimized.
- **Advanced Search Options**: Utilize advanced search parameters for more precise results.
- **Asynchronous and Cached Searches**: Support for asynchronous search execution and cache management.
- **Enterprise Features**: Includes enterprise-level options like ZeroTrace mode for enhanced privacy.

## Main Features and Functionality

1. **Flexible Query Parameters**: The API supports a variety of parameters to refine search queries, including location, language, and device type.
2. **Advanced Filtering**: Users can apply advanced search filters and parameters to narrow down results.
3. **Pagination and Result Limits**: Control over pagination and the number of results returned per query.
4. **Direct Product Links**: Option to include direct product links in search results, enhancing user experience.
5. **Asynchronous Execution**: Ability to perform searches asynchronously, improving response times for users.
6. **Enterprise Privacy Options**: ZeroTrace mode ensures no server-side storage, catering to enterprise privacy needs.

## Main Functions Description

### `search_google_shopping`

The core function of this application, `search_google_shopping`, allows users to perform a detailed search on Google Shopping. Below is a breakdown of its parameters and functionality:

- **q**: The primary search query string, required for executing a search.
- **location**: Optional parameter to specify the origin of the search, enhancing location-specific results.
- **uule**: An optional Google-encoded location parameter, mutually exclusive with `location`.
- **google_domain**: Specify the Google domain to use, defaulting to `google.com`.
- **gl**: Optional geographic targeting using a two-letter country code.
- **hl**: Optional language targeting using a two-letter language code.
- **tbs**: Allows for advanced search parameters not available in standard queries.
- **shoprs**: A helper ID for setting search filters, used in conjunction with an updated query parameter.
- **direct_link**: When enabled, attempts to include direct product links in the results.
- **start**: Controls pagination by setting the result offset.
- **num**: Limits the number of results returned, with a default of 60.
- **device**: Specifies the device type for which the results should be optimized.
- **no_cache**: Forces fresh results by ignoring cached versions.
- **aasync**: Enables asynchronous search execution.
- **zero_trace**: An enterprise feature that ensures no server-side storage of search data.

The function constructs a payload with the provided parameters, excluding any that are `None`, and sends a request to the Google Shopping API. The response is then returned in JSON format, providing the search results.

The server is initiated using the `mcp.run(transport="stdio")` command, which starts the FastMCP server to handle incoming search requests.