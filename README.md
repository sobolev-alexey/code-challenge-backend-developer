# NodeJS Test

We really appreciate your time and effort working on this home task as part of our interview process. It is meant for you to demonstrate your skills as well as get a taste of what we are looking for and what your job at IOTA foundation will get you in.  

Please do not share this task with anyone or make it public in any way. We encourage you to contact us if you have any questions, by replying to the email.


## Task 1
Messaging acronyms are everywhere now. Do you know all of them?

Build a REST API for the **texting app**.

A sample [JSON data](./acronyms.json) file is provided with a base set of acronym definitions. We expect you to create a NodeJS server
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

#### The Data

Use this data however you like, either as a flat file, or to populate a database.  

[acronyms.json](./acronyms.json)

  

  
  
## Task 2

### Scope
Implement a simple load balancer tool, that checks availability of a service and redirects HTTP(S) requests to a working server

### Ice breaker
Please provide the load balancer software architecture and specification and the required technologies and tools used

### Warm up
Provide a simple working prototype. You can use any service behind the load balancer. You can also consider a service, offered by existing IOTA nodes (IP addresses below), i.e., for accepting transactions.

### Wizard
(extra points) If you feel particularly inspired, provide a prototype for a load balancer connected to one or more IOTA nodes you have installed. This task is optional and you can directly jump to this and skip the warm up task.

### Caveat
 - We would expect you to complete the Ice breaker task; 
 - You can choose between one of the other tasks (Warm up and Wizard). The best is always progress for incremental steps especially if you are not familiar with IOTA nodes.
 - Based on our estimations, the overall assignment completion should not take more than 5 hours (5+ hours if you also include the set up of an IOTA node)
 - Implement a simple yet elegant solution to highlight your skills
 - We are not expecting a fancy implementation, crazy UI etc. Only a simple tool
 - We are looking for something basic that allows us to test the system under the following requirement: two servers are connected to the load balancer, and once the one is down, the other one is selected
 - For the **Ice breaker** part use sequence diagrams, architecture diagrams, etc. You can use the free https://app.diagrams.net/ service and export your system design diagrams in PNG.
 - **Warm up** is the part where you can shows us your development skills
 - **Wizard** is optional unless you want to skip the warm up part. It gives you the opportunity to look into the IOTA network service development which will be one of the topics of your work within IOTA foundation

### Reference
 - IOTA documentation: https://docs.iota.org/
 - IOTA examples: https://client-lib.docs.iota.org/docs/libraries/nodejs/examples
 - IOTA nodes addresses (for testing): https://chrysalis-nodes.iota.org:443
