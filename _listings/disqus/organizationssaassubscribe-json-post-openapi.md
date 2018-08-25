---
swagger: "2.0"
x-collection-name: Disqus
x-complete: 0
info:
  title: Disqus Organizations Saas Subscribe
  description: Organizations Saas Subscribe
  termsOfService: https://docs.disqus.com/kb/terms-and-policies/
  version: 1.0.0
host: disqus.com
basePath: api/3.0/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /organizations/saas/subscribe.json:
    post:
      summary: Organizations Saas Subscribe
      description: Organizations Saas Subscribe
      operationId: organizations-saas-subscribe
      x-api-path-slug: organizationssaassubscribe-json-post
      parameters:
      - in: query
        name: organization
        description: Looks up an organization by ID You must be an admin on the selected
          organization
        type: string
      - in: query
        name: plan
        description: Looks up a PricingOption by name
        type: string
      - in: query
        name: user
        description: Defaults to null                         Looks up a user by ID
          You may look up a user by username using the &#39;username&#39; query type
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Organizations
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