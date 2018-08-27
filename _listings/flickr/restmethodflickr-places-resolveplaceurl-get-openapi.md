---
swagger: "2.0"
x-collection-name: Flickr
x-complete: 0
info:
  title: Flickr Places Resolve Place U R L
  description: Find Flickr Places information by Place URL. This method has been deprecated.
    It won't be removed but you should use flickr.places.getInfo instead.
  version: 1.0.0
host: api.flickr.com
basePath: /services/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /rest/?method=flickr.places.getInfoByUrl:
    get:
      summary: Places Get Info By Url
      description: Lookup information about a place, by its flickr.com/places URL.
      operationId: getRestMethodFlickr.places.getinfobyurl
      x-api-path-slug: restmethodflickr-places-getinfobyurl-get
      parameters:
      - in: query
        name: api_key
        description: Your API application key
      - in: query
        name: format
        description: Response format
      - in: query
        name: url
        description: A flickr
      responses:
        200:
          description: OK
      tags:
      - Places
      - GetInfoByUrl
  /rest/?method=flickr.places.resolvePlaceURL:
    get:
      summary: Places Resolve Place U R L
      description: Find Flickr Places information by Place URL. This method has been
        deprecated. It won't be removed but you should use flickr.places.getInfo instead.
      operationId: getRestMethodFlickr.places.resolveplaceurl
      x-api-path-slug: restmethodflickr-places-resolveplaceurl-get
      parameters:
      - in: query
        name: api_key
        description: Your API application key
      - in: query
        name: format
        description: Response format
      - in: query
        name: url
        description: A Flickr Places URL
      responses:
        200:
          description: OK
      tags:
      - Places
      - ResolvePlaceURL
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