# Directus CMS/API Evaluation

Evaluating [Directus](https://directus.io) as a candidate for Headless CMS
and data API projects.

Documentation of R&D efforts: https://arcweb.atlassian.net/wiki/spaces/ET/pages/3017310223/CMS+and+Site+Platform+Research+2022


## Getting Started

This project is intended for local testing of the Directus system, using Docker
containers. Booting a local instance of Directus can be done with Docker Compose
alone:

1. Bring up compose environment: `docker-compose up`
2. Browse to Directus site: http://localhost:8055 (as configured, port forwarding can be changed)
3. Login with admin credentials (as configured: 'admin@example.com' / 'password')
4. Walk through the project confiugration
5. Use Directus

By default, this will create a project database that you can manipulate in the
web-based dashboard. It is also possible to attach Directus to an existing/legacy
database and configure it from there (further exploration TBD).


## Testing the API

Once you have created some Collections and Items in the Directus system, you can
access them via the project API.

API Documentation, incl. Authentication: https://docs.directus.io/reference/introduction/

You can view a starter Postman collection describing a local API Directus with a
"People" collection included in this project.

Basic approach:

1. Authenticate with a POST against /auth/login
2. Retrieve the access token from that response
3. Use Bearer token Header to authenticate additional requests

