---
swagger: "2.0"
info:
  title: Akamai API Add a Device
  description: Add a Device
  version: 1.0.0
host: developer.akamai.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /galaxy/v1/devices/{deviceId}:
    post:
      summary: Add a Device
      description: Add a Device
      operationId: galaxyv1devicesdeviceid
      parameters:
      - in: query
        name: deviceId
        description: Identifies the device, maximum 50 characters
        type: string
      responses:
        200:
          description: OK
      tags:
      - galaxy
      - devices
      - device
definitions: []
x-collection-name: Akamai
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