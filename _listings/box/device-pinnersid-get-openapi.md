---
swagger: "2.0"
x-collection-name: Box
x-complete: 0
info:
  title: Box Get Device Pin
  description: Gets information about an individual device pin.
  version: 1.0.0
host: api.box.com
basePath: /2.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /enterprises/{ENTERPRISE_ID}/device_pinners:
    get:
      summary: Get Enterprise Device Pins
      description: Gets all the device pins within a given enterprise. Must be an
        enterprise admin with the manage enterprise scope to make this call.
      operationId: getEnterpriseDevicePins
      x-api-path-slug: enterprisesenterprise-iddevice-pinners-get
      parameters:
      - in: query
        name: direction
        description: Default is asc
      - in: path
        name: ENTERPRISE_ID
      - in: query
        name: limit
        description: Default value is 100
      - in: query
        name: marker
        description: Needs not be passed or can be empty for first invocation of the
          API
      responses:
        200:
          description: OK
      tags:
      - Documents
      - Enterprises
      - Enterprise
      - ""
      - Device
      - Pinners
  /device_pinners/{ID}:
    get:
      summary: Get Device Pin
      description: Gets information about an individual device pin.
      operationId: getDevicePin
      x-api-path-slug: device-pinnersid-get
      parameters:
      - in: path
        name: ID
      responses:
        200:
          description: OK
      tags:
      - Documents
      - Device
      - Pinners
    delete:
      summary: Delete Device Pin
      description: Delete individual device pin.
      operationId: deleteDevicePin
      x-api-path-slug: device-pinnersid-delete
      parameters:
      - in: path
        name: ID
      responses:
        200:
          description: OK
      tags:
      - Documents
      - Device
      - Pinners
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