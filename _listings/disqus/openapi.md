swagger: "2.0"
x-collection-name: Disqus
x-complete: 1
info:
  title: Disqus
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
  /organizations/saas/unsubscribe.json:
    post:
      summary: Organizations Saas Unsubscribe
      description: Organizations Saas Unsubscribe
      operationId: organizations-saas-unsubscribe
      x-api-path-slug: organizationssaasunsubscribe-json-post
      parameters:
      - in: query
        name: immediately
        description: Defaults to false
        type: string
      - in: query
        name: organization
        description: Looks up an organization by ID You must be an admin on the selected
          organization
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
      - Organizations