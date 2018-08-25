---
swagger: "2.0"
x-collection-name: Intrinio
x-complete: 0
info:
  title: Intrinio API Executive Master
  description: Returns a list of all executives and their unique executive identifier,
    including both U.S. and International executives.
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
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---