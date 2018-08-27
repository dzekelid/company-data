swagger: "2.0"
x-collection-name: Intrinio
x-complete: 1
info:
  title: Intrinio
  version: 1.0.0
host: api.intrinio.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /executives:
    get:
      summary: Executive Master
      description: Returns a list of all executives and their unique executive identifier,
        including both U.S. and International executives.
      operationId: executive-master
      x-api-path-slug: executives-get
      parameters:
      - in: query
        name: company
        description: 'the identifier for the specified security or company:'
        type: string
      - in: query
        name: page_number
        description: an integer greater than or equal to 1 for specifying the page
          number for the return values
        type: string
      - in: query
        name: page_size
        description: an integer greater than 1 for specifying the number of results
          on each page
        type: string
      - in: query
        name: query
        description: a string query search of executives name
        type: string
      - in: query
        name: role
        description: the normalized executive and officer role
        type: string
      - in: query
        name: type
        description: 'select whether to show only US or International executives:
          us | non'
        type: string
      responses:
        200:
          description: OK
      tags:
      - Market Data
      - Executives
  /executives/companies:
    get:
      summary: Company Executive Contacts
      description: Returns a list of all information for an executive and their related
        companies.  Information includes the unique Intrinio executive company identifier,
        and detailed contact information for the executive at a specified company.
      operationId: company-executive-contacts
      x-api-path-slug: executivescompanies-get
      parameters:
      - in: query
        name: company
        description: 'the identifier for the specified security or company:'
        type: string
      - in: query
        name: identifier
        description: the Intrinio executive identifier
        type: string
      responses:
        200:
          description: OK
      tags:
      - Market Data
      - Executives
      - companies
  /executives/roles:
    get:
      summary: Company Executive Roles
      description: For a specific executive company identifier, returns a list of
        all roles within the company.  For example, an executive may be the Chief
        Executive Officer, a Director, and the Chairman of the Board of Directors.
      operationId: company-executive-roles
      x-api-path-slug: executivesroles-get
      parameters:
      - in: query
        name: company
        description: 'the identifier for the specified security or company:'
        type: string
      - in: query
        name: identifier
        description: the Intrinio executive identifier
        type: string
      responses:
        200:
          description: OK
      tags:
      - Market Data
      - Executives
      - Executive Roles