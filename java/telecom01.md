# Test task for Telecom company

This example provides requirements for imaginary Telecom company which provides some order management solutions.

## Order Management System

Main entities used in the following requirements:
- Specification
-- Name
-- Description
- Order
-- Identification
-- CreationDate
-- LastModifiedDate
-- Specification Identification (association with specification)
- Instance
-- Orders (associations with Order entiies)
-- Status (can be Initial, Provisioning or Active)

### Functional requirements

1. As an authenticated user I can Create new `Instance` by sending `POST` request to `server:port/orders` URL with `Order` as request body (JSON or XML)
1. As an authenticated user I can Check `Instance` status by sending `GET` request to `server:port/instances/{instanceId}` URL
1. As an unathenticated user I can Get a list of all `Specifications` by sending `GET` request to `server:port/specifications` URL

### Non-functional requirements

1. User authentication should use OAuth2.0
1. System implemented as a set of distributed services
1. System administrator can scale out or scale in any service via one command in `SSH`
1. System provides monitoring API endpoint with information about memory and CPU consumption
