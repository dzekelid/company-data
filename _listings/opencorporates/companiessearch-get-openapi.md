---
swagger: "2.0"
x-collection-name: OpenCorporates
x-complete: 0
info:
  title: OpenCorporates Companies Search
  description: nThis returns a collection of companies whose name matches the given
    search term (submitted as :q in the query parameters)
  termsOfService: https://opencorporates.com/info/licence
  version: v.04
host: api.opencorporates.com
basePath: v0.4/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /companies/search:
    get:
      summary: Companies Search
      description: nThis returns a collection of companies whose name matches the
        given search term (submitted as :q in the query parameters)
      operationId: companies-search
      x-api-path-slug: companiessearch-get
      parameters:
      - in: query
        name: branch
        description: Filter by branch status (boolean)
      - in: query
        name: company_type
        description: The type of the company, as defined by the company register
      - in: query
        name: country_code
        description: NEWThe companies searched for can be restricted to a given country
          by passing a country_code query parameter
      - in: query
        name: created_since
        description: companies added to OpenCorporates after the given date
      - in: query
        name: current_status
        description: The current status of the company, as defined by the company
          register
      - in: query
        name: dissolution_date
        description: NEWas with all date fields, dissolution_date can be supplied
          either as a specific date or as a span of dates
      - in: query
        name: dissolved_before
        description: DeprecatedRestrict to companies with a dissolution_date before
          the given date
      - in: query
        name: dissolved_since
        description: DeprecatedRestrict to companies with a dissolution_date after
          the given date
      - in: query
        name: exclude_inactive
        description: DeprecatedRestrict to companies that are active/inactive
      - in: query
        name: fields
        description: NEWBy default when searching with a term (e
      - in: query
        name: inactive
        description: Filter by inactive status (boolean)
      - in: query
        name: incorporated_before
        description: DeprecatedRestrict to companies with an incorporation_date before
          the given date
      - in: query
        name: incorporated_since
        description: DeprecatedRestrict to companies with an incorporation_date after
          the given date
      - in: query
        name: incorporation_date
        description: NEWAs with all date fields, incorporation_date can be supplied
          either as a specific date or as a span of dates
      - in: query
        name: industry_codes
        description: NEWOne or more industry codes representing the industries the
          company operates in
      - in: query
        name: jurisdiction_code
        description: The companies searched for can be restricted to a given jurisdiction
          by passing a jurisdiction_code query parameter
      - in: query
        name: nonprofit
        description: NEWFilter by nonprofit company type (boolean)
      - in: query
        name: registered_address
        description: NEWThe companies searched for can be restricted by passing in
          an address or parts of an address
      responses:
        200:
          description: OK
      tags:
      - Businesses
      - Companies
      - Search
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