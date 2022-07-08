# Ticketmaster Event System API
This repository contains a system API for unlocking Ticketmaster event data. The Ticketmaster Event System API is a reusable asset that enables developers to access Ticketmaster event data without any need to learn the underlying systems. In other words, it provides a means of insulating developers from the complexity of integrating with Ticketmaster.

## Table of Contents
- [Technology Stack Overview](#technology-stack-overview)
- [Implementation Overview](#implementation-overview)
- [Instructions](#instructions)
- [Reporting Issues](#reporting-issues)
- [Additional Resources](#additional-resources)

## Technology Stack Overview
We implemented this system API using the following technology stack:
- MuleSoft Anypoint Studio 7.11
- Mule Server 4.3.0
- Ticketmaster Discovery API v2

Although not formally tested, you could easily use older or newer versions of the MuleSoft Anypoint Studio, Mule Server, or both.

## Implementation Overview
As of this writing, the Ticketmaster Event System API implements a single operation for retrieving Ticketmaster events. In addition, the get operation accepts four optional query parameters for filtering the results: `venueId`, `city`, `startDateTime`, and `endDateTime`. You can call the get operation without any query parameter, which will return the first 200 events. Additionally, you can specify any combination of the four query parameters.

As it is common practice at MuleSoft, we leverage RAML to specify our API. Primarily for convenience and to make sharing the Anypoint Studio project easier, we included the RAML file in the project (`src/main/resources/api`) rather than having a dependency to its published specification in Anypoint Exchange.

## Instructions
1. Download this repo or clone it to your Anypoint Studio workspace.
    ```sh
    git clone https://github.com/abelisle-mulesoft/ticketmaster-event-sapi.git
    ```

2. Edit `src/main/resources/mule-properties.yaml` and configure the following property:
   - `ticketmaster.apikey`, which is your Ticketmaster API key (i.e., the consumer key of your Ticketmaster client application).

3. Compile and run the project in Anypoint Studio as a smoke test. Optionally, test the Ticketmaster Event System API using the API Console in Anypoint Studio or your preferred API testing tool (e.g., Postman).

## Reporting Issues
You can report new issues at this link https://github.com/abelisle-mulesoft/ticketmaster-event-sapi/issues

## Additional Resources
Following are references and additional resources:
- Getting Started with the Ticketmaster API: https://developer.ticketmaster.com/products-and-docs/apis/getting-started
- Ticketmaster Discovery API: https://developer.ticketmaster.com/products-and-docs/apis/discovery-api/v2

