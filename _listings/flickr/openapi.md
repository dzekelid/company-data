swagger: "2.0"
x-collection-name: Flickr
x-complete: 1
info:
  title: Flickr
  description: explore-upload-and-organize-photos-on-flickr
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