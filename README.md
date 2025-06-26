```markdown
# Aigeon AI Google Shopping API

## Project Description

The Aigeon AI Google Shopping API is a Python-based server application designed to facilitate seamless interaction with Google Shopping search results. This project leverages the capabilities of the SERP API to perform detailed product searches on Google Shopping, providing users with a robust tool for retrieving shopping data programmatically.

## Features Overview

- **Google Shopping Search**: Perform detailed searches on Google Shopping using a variety of customizable parameters.
- **Flexible Query Options**: Includes support for location-based searches, language and country targeting, and device-specific results.
- **Advanced Search Parameters**: Utilize advanced search options such as direct product links and pagination.
- **Asynchronous Search Capabilities**: Option to execute searches asynchronously for improved performance.
- **Enterprise Features**: Includes enterprise-specific options like ZeroTrace mode for enhanced privacy.

## Main Features and Functionality

The core functionality of this application is encapsulated in the `search_google_shopping` function. This function allows users to perform comprehensive searches on Google Shopping by specifying a wide range of parameters. The application is built on top of the FastMCP framework, which facilitates efficient server management and execution.

### Key Functionalities:

- **Query Customization**: Users can define search queries (`q`) and specify the origin of the search (`location` or `uule`).
- **Domain and Language Targeting**: Customize the Google domain (`google_domain`) and language (`hl`) for search results.
- **Result Filtering and Pagination**: Control the number of results (`num`) and pagination (`start`) for detailed data retrieval.
- **Device-Specific Searches**: Specify the type of device (`device`) to tailor the search results accordingly.
- **Cache Management**: Options to bypass cached results (`no_cache`) for fresh data retrieval.
- **Asynchronous Execution**: Enable asynchronous search execution (`aasync`) for non-blocking operations.
- **Enterprise Privacy**: Activate ZeroTrace mode (`zero_trace`) for searches without server-side data storage.

## API Endpoints or Main Functions Description

### `search_google_shopping`

This is the primary function of the application, designed to search Google Shopping for product listings and shopping results. It accepts a variety of parameters to customize the search:

- **q**: *(Required)* The search query string.
- **location**: *(Optional)* The geographical location for the search.
- **uule**: *(Optional)* Google encoded location.
- **google_domain**: *(Optional)* The Google domain to use.
- **gl**: *(Optional)* Country code for geographic targeting.
- **hl**: *(Optional)* Language code for search results.
- **tbs**: *(Optional)* Advanced search parameters.
- **shoprs**: *(Optional)* Helper ID for search filters.
- **direct_link**: *(Optional)* Include direct product links.
- **start**: *(Optional)* Result offset for pagination.
- **num**: *(Optional)* Maximum number of results.
- **device**: *(Optional)* Device type for results.
- **no_cache**: *(Optional)* Force fresh results.
- **aasync**: *(Optional)* Asynchronous search execution.
- **zero_trace**: *(Optional)* ZeroTrace mode for privacy.

The function constructs a payload with the specified parameters and makes a GET request to the SERP API. It processes the response and returns the search results in JSON format.

## Conclusion

The Aigeon AI Google Shopping API provides a comprehensive and flexible solution for accessing Google Shopping data programmatically. With its wide range of customizable search parameters and advanced features, it is an invaluable tool for developers and businesses looking to integrate Google Shopping data into their applications.
```