## NodeJS Test

Messaging acronyms are everywhere now. Do you know all of them?

Build a REST API for the **World Texting Foundation**, also known as **WTF**.

A sample JSON data file will be provided with a base set of acronym definitions. We expect you to create a NodeJS server
using modern best practices for API development and testing.
You can use docker & docker-compose if needed.

These endpoints should be created:

- **`GET /acronym?from=50&limit=10&search=:search`**
  - ▶ returns a list of acronyms, paginated using query parameters
  - ▶ response headers indicate if there are more results
  - ▶ returns all acronyms that fuzzy match against `:search`
- **`GET /acronym/:acronym`**
  - ▶ returns the acronym and definition matching `:acronym`
- **`GET /random/:count?`**
  - ▶ returns `:count` random acronyms
  - ▶ the acronyms returned should not be adjacent rows from the data
- **`POST /acronym`**
  - ▶ receives an acronym and definition strings
  - ▶ adds the acronym definition to the db
- **`PUT /acronym/:acronym`**
  - ▶ receives an acronym and definition strings
  - ▶ uses an authorization header to ensure acronyms are protected
  - ▶ updates the acronym definition to the db for `:acronym`
- **`DELETE /acronym/:acronym`**
  - ▶ deletes `:acronym`
  - ▶ uses an authorization header to ensure acronyms are protected

## The Data

Use this data however you like, either as a flat file, or to populate a database.  

[acronyms.json](./acronyms.json)
