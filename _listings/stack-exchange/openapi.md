---
swagger: "2.0"
x-collection-name: Stack Exchange
x-complete: 1
info:
  title: Stack Exchange
  description: stack-exchange-is-a-network-of-130-qa-communities-including-stack-overflow-
  version: "2.0"
host: api.stackexchange.com
basePath: /2.2
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /search/advanced:
    get:
      summary: Advanced Search
      description: "Searches a site for any questions which fit the given criteria.\n
        \nSearch criteria are expressed using the following parameters:\n  - q - a
        free form text parameter, will match all question properties based on an undocumented
        algorithm.\n - accepted - true to return only questions with accepted answers,
        false to return only those without. Omit to elide constraint.\n - answers
        - the minimum number of answers returned questions must have.\n - body - text
        which must appear in returned questions' bodies.\n - closed - true to return
        only closed questions, false to return only open ones. Omit to elide constraint.\n
        - migrated - true to return only questions migrated away from a site, false
        to return only those not. Omit to elide constraint.\n - notice - true to return
        only questions with post notices, false to return only those without. Omit
        to elide constraint.\n - nottagged - a semicolon delimited list of tags, none
        of which will be present on returned questions.\n - tagged - a semicolon delimited
        list of tags, of which at least one will be present on all returned questions.\n
        - title - text which must appear in returned questions' titles.\n - user -
        the id of the user who must own the questions returned.\n - url - a url which
        must be contained in a post, may include a wildcard.\n - views - the minimum
        number of views returned questions must have.\n - wiki - true to return only
        community wiki questions, false to return only non-community wiki ones. Omit
        to elide constraint.\n  \nAt least one additional parameter must be set if
        nottagged is set, for performance reasons.\n \nThe sorts accepted by this
        method operate on the follow fields of the question object:\n - activity -
        last_activity_date\n - creation - creation_date\n - votes - score\n - relevance
        - matches the relevance tab on the site itself Does not accept min or max\n
        \ activity is the default sort.\n \n It is possible to create moderately complex
        queries using sort, min, max, fromdate, and todate.\n \nThis method returns
        a list of questions."
      operationId: searches-a-site-for-any-questions-which-fit-the-given-criteria-search-criteria-are-expressed-using-t
      x-api-path-slug: searchadvanced-get
      parameters:
      - in: query
        name: accepted
      - in: query
        name: answers
      - in: query
        name: body
      - in: query
        name: callback
        description: All API responses are JSON, we do support JSONP with the callback
          query parameter
      - in: query
        name: closed
      - in: query
        name: filter
        description: '#DiscussionThe Stack Exchange API allows applications to exclude
          almost every field returned'
      - in: query
        name: fromdate
        description: Unix date
      - in: query
        name: max
        description: sort = activity => datesort = creation => datesort = votes =>
          numbersort = relevance => none
      - in: query
        name: migrated
      - in: query
        name: min
        description: sort = activity => datesort = creation => datesort = votes =>
          numbersort = relevance => none
      - in: query
        name: notice
      - in: query
        name: nottagged
        description: String list (semicolon delimited)
      - in: query
        name: order
      - in: query
        name: page
      - in: query
        name: pagesize
      - in: query
        name: q
      - in: query
        name: site
        description: Each of these methods operates on a single site at a time, identified
          by the site parameter
      - in: query
        name: sort
      - in: query
        name: tagged
        description: String list (semicolon delimited)
      - in: query
        name: title
      - in: query
        name: todate
        description: Unix date
      - in: query
        name: url
      - in: query
        name: user
      - in: query
        name: views
      - in: query
        name: wiki
      responses:
        200:
          description: OK
      tags:
      - Search
---