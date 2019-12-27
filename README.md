# EXAMPLE
This is an example readme for a Mule project.  Make sure to fill out all the sections below.  Add sections as necessary.
**Note** when running in studio make sure the `app.runtime property` in the `pom.xml` matches the one in studio. Also make sure you have the latest settings.xml

> All instructions to filling out sections will be in block quotes just like this **at the beginning** of each section.
> Make sure to remove these when filling this out.  Also replace the example text in each section with the specific text for your API.

**Remove this EXAMPLE section.** 

# shs-servicecontracts-exp-api
*Source Code repo:* [*shs-servicecontracts-exp-api*](https://https://github.com/searshomeservices/shs-servicecontracts-exp-api)

## Builds
*Note: the build status is only available on the Sears home services network.*

| Environment   | Status        | 
| :-------------: |:-------------:| 
| Development   | *not implemented yet* | 

## Description
> Description of the API.  Include all applicable information, including considerations for different regions or on-premise vs cloud.

This service raises notifications on behalf of the requester to the specified targets.

All mule apps should send errors or notifications to a standard service so that the actual details of notification (emails, incident creation, CloudHub business event) are abstracted away from each application.  The Notification Service provides the ability for apps to properly notify the appropriate teams regarding errors.

## Features
> Provide list of high level features; this can include the main resources supported.

- Sends notification as an email message if any errors are encountered.

## Healthcheck
> List the Healthcheck path and what is implemented.

- Healthcheck endpoint is available at the path below.  Only the timestamp feature is implemented.
```/```

------

# Development, Testing, & Operations

## Configuration
> Define specific configuration items that operations can set for the API.  The properties section is defined below, but there may be other configuration items as well.

### API Properties
- `api.id="123456"`:  Set to the api id once deployed and added to API manager.

## Flow descriptions
> List all the flow xml files with brief descriptions.

- error-handling: flows to handle API errors.
- global.xml: container for all configurations for the API.

## Dependencies
> List all external dependencies.  These can be Systems of Record for System APIs, data stores, external libraries, etc.

- System

## Testing
> List all testing information here.  This includes MUnit and Postman collections in the project.  Describe anything needs additional detail.

- MUnit tests available at `src/test/munit`
- Postman Test API collection is available at `src/test/resources/test-postman-collection.json`
